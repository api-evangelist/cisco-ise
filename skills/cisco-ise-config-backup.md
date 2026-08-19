---
name: Take and verify a Cisco ISE configuration backup
description: Register a repository, trigger a configuration backup, poll it to completion, and confirm the last-backup status — the safe operational flow to run before any change window.
api: openapi/_original/cisco-ise-open-api-backuprestore.yaml
operations: [getRepositories, createRepository, getRepositoryFiles, configBackup, getLastConfigBackupStatus, cancelBackup, createScheduledConfigBackup, getAllTaskStatus, getTaskStatus]
---

# Take and verify a Cisco ISE configuration backup

The backup is the rollback plan. Run this before touching policy.

## Before you start

- HTTP Basic against the customer's own ISE appliance; the account needs **ERS Admin** (this flow
  writes). Backup and restore operate against the **primary PAN** — in a distributed deployment
  writes are only accepted there.
- Two APIs are involved: Backup and Restore (`/api/v1/backup-restore/...`) and Repository
  (`/api/v1/repository/...`). A backup has nowhere to go without a repository.

## Steps

1. **Confirm a destination exists.** `getRepositories` (`GET /api/v1/repository`). If the target
   repository is missing, `createRepository` (`POST /api/v1/repository`) — this is a real write,
   so confirm the intent with a human first.

2. **Check what is already there.** `getRepositoryFiles`
   (`GET /api/v1/repository/{repositoryName}/files`) so you do not overwrite or misread an existing
   backup set.

3. **Check the current state before starting.** `getLastConfigBackupStatus`
   (`GET /api/v1/backup-restore/config/last-backup-status`). If a backup is already running, stop —
   do not start a second one.

4. **Trigger the backup.** `configBackup` (`POST /api/v1/backup-restore/config/backup`), naming the
   repository and the backup encryption key. **Send this exactly once.** There is no idempotency
   key; if the call times out, poll status rather than resending.

5. **Poll to completion.** `getLastConfigBackupStatus` on an interval, or `getAllTaskStatus`
   (`GET /api/v1/task`) / `getTaskStatus` (`GET /api/v1/task/{taskId}`) if you were handed a task id.
   Back off between polls — the 100 TPS ceiling is deployment-wide and you are sharing it.

6. **If you must stop it**, `cancelBackup` (`POST /api/v1/backup-restore/config/cancel-backup`).

7. **To make it recurring instead**, `createScheduledConfigBackup`
   (`POST /api/v1/backup-restore/config/schedule-config-backup`) or
   `updateScheduledConfigBackup` (`PUT` on the same path).

## Rules

- **Do not call `restoreConfigBackup`** (`POST /api/v1/backup-restore/config/restore`) from an
  automated flow. Restoring configuration to a policy server is a destructive, service-affecting
  action; it needs an explicit human decision and a change window.
- A `500` carrying `INTERNAL_EXCEPTION`, `CONVERSION_EXCEPTION` or `CRUD_OPERATION_EXCEPTION` means
  the same thing — an unexpected server-side failure. Poll status to find out whether the backup
  actually started before doing anything else.
