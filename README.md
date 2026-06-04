# Cloud-Based Data Backup & Disaster Recovery

## Overview
A cloud-based backup and disaster recovery system built on Google Cloud Platform (GCP).
Files are automatically backed up to Google Cloud Storage and can be restored instantly
in case of data loss.

## Tools Used
- Google Cloud Storage (GCS)
- gcloud CLI
- Bash Scripting
- Cron (Task Scheduler)
- Ubuntu (WSL)

## Scripts
- backup.sh → Backs up local files to GCS with error handling and logging
- restore.sh → Restores files from GCS back to local in case of disaster

## How It Works
1. backup.sh creates a timestamped backup file and uploads it to GCS
2. Verifies upload success and logs the result
3. Runs automatically every day via cron scheduler
4. If data is lost, restore.sh downloads all files back from GCS instantly

## How to Run
### Manual Backup
bash backup.sh

### Restore After Disaster
bash restore.sh

### Check Backup Logs
cat ~/backup.log

### View Files in Cloud
gcloud storage ls gs://vaishu-backup-project-2026/backups/

## Project
RISE 5.0 Internship — Cloud Computing Project 2
