# System Services and Daemon Management

> **Section:** 9A  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `systemctl start SERVICE` | Start a systemd service. | Source |  |
| `systemctl stop SERVICE` | Stop a systemd service. | Source |  |
| `systemctl restart SERVICE` | Restart a systemd service. | Source |  |
| `systemctl enable SERVICE` | Enable a service at boot. | Source |  |
| `systemctl disable SERVICE` | Disable a service at boot. | Source |  |
| `systemctl status SERVICE` | Check service status. | Source |  |
| `service SERVICE start` | Start a service on SysV/init-compatible systems. | Source |  |
| `service SERVICE stop` | Stop a service on SysV/init-compatible systems. | Source |  |
| `service SERVICE restart` | Restart a service on SysV/init-compatible systems. | Source |  |
| `service SERVICE status` | Check legacy service status. | Source |  |
| `systemctl enable --now SERVICE` | Enable a service at boot and start it immediately. | Added |  |
| `systemctl disable --now SERVICE` | Disable a service and stop it immediately. | Added |  |
| `systemctl reload SERVICE` | Reload service configuration without a full restart when supported. | Added |  |
| `systemctl list-units --type=service --state=running` | List running services. | Added |  |
| `systemctl --failed` | List failed systemd units. | Added |  |
| `systemctl cat SERVICE` | Show the effective unit file and drop-ins. | Added |  |
| `systemctl edit SERVICE` | Create or edit a systemd override drop-in. | Added |  |
| `systemctl daemon-reload` | Reload systemd manager configuration after unit-file changes. | Added |  |
| `journalctl -u SERVICE -f` | Follow logs for a systemd service. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
