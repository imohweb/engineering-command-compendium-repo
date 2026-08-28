# System Diagnostics and Troubleshooting

> **Section:** 13  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `dmesg` | Print kernel ring-buffer messages. | Source |  |
| `journalctl` | Query and view systemd's journal. | Source |  |
| `strace COMMAND` | Trace a command's system calls and signals. | Source |  |
| `lsof` | List open files. | Source |  |
| `lsof FILE` | Show processes using a specific file. | Source |  |
| `vmstat` | Report virtual-memory statistics. | Source |  |
| `iostat` | Report CPU and I/O statistics. | Source |  |
| `mpstat` | Report CPU usage statistics. | Source |  |
| `pidstat` | Report statistics by process. | Source |  |
| `free` | Display memory usage. | Source |  |
| `uptime` | Show uptime and load averages. | Source |  |
| `watch -n 1 free` | Watch memory usage every second. | Source |  |
| `lshw` | List hardware configuration. | Source |  |
| `htop` | Interactive process viewer. | Source |  |
| `netstat` | Display network statistics. | Source | Legacy; prefer ss. |
| `ss` | Display socket statistics. | Source |  |
| `journalctl -xe` | Show recent journal messages with explanatory context. | Added |  |
| `journalctl -u SERVICE --since "1 hour ago"` | Show recent logs for a service. | Added |  |
| `dmesg -T &#124; tail -100` | Show recent kernel messages with human-readable timestamps. | Added |  |
| `systemctl --failed` | List failed systemd units. | Added |  |
| `lsof -i :PORT` | Show processes using a network port. | Added |  |
| `fuser -v PATH` | Show processes using a file, mount point or socket. | Added |  |
| `strace -f -p PID` | Attach to a process and follow system calls across child processes. | Added |  |
| `pidstat -p PID 1` | Sample resource usage for a specific process every second. | Added |  |
| `iostat -xz 1` | Inspect extended disk latency, queue and utilization metrics. | Added |  |
| `vmstat 1` | Inspect CPU run queue, memory, swap and I/O in real time. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
