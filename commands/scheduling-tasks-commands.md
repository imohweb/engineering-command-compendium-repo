# Scheduling Tasks

> **Section:** 10  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `crontab -e` | Edit the current user's cron jobs. | Source |  |
| `crontab -l` | List the current user's cron jobs. | Source |  |
| `crontab -r` | Remove the current user's cron jobs. | Source | Destructive; removes the current crontab. |
| `at 09:00` | Schedule commands to run at 09:00. | Source |  |
| `batch` | Run queued commands when system load is low. | Source |  |
| `sleep 5s` | Delay for five seconds. | Source |  |
| `crontab -u USER -l` | List another user's crontab (requires appropriate privileges). | Added |  |
| `atq` | List pending at jobs. | Added |  |
| `atrm JOB_ID` | Remove a pending at job. | Added |  |
| `systemctl list-timers --all` | List systemd timers and their next/last run times. | Added |  |
| `systemd-run --on-active=10m COMMAND` | Create a transient systemd timer that runs once after ten minutes. | Added |  |
| `watch -n 5 COMMAND` | Run a command repeatedly every five seconds in an interactive terminal. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
