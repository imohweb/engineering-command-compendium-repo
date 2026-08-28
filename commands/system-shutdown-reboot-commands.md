# System Shutdown and Reboot

> **Section:** 16  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `shutdown -h now` | Shut down immediately. | Source |  |
| `shutdown -r now` | Reboot immediately. | Source |  |
| `shutdown -h +10` | Schedule shutdown in ten minutes. | Source |  |
| `reboot` | Reboot the system. | Source |  |
| `halt` | Halt the system. | Source |  |
| `poweroff` | Power off the system. | Source |  |
| `init 0` | Shutdown using legacy SysV init runlevel. | Source | Legacy on modern systemd distributions. |
| `init 6` | Reboot using legacy SysV init runlevel. | Source | Legacy on modern systemd distributions. |
| `shutdown -c` | Cancel a scheduled shutdown. | Added |  |
| `systemctl reboot` | Reboot a systemd host. | Added |  |
| `systemctl poweroff` | Power off a systemd host. | Added |  |
| `systemctl suspend` | Suspend a systemd host when supported. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
