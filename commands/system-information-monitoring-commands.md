# System Information and Monitoring

> **Section:** 7  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `uname` | Print system information. | Source |  |
| `hostname` | Show or set the system's hostname. | Source |  |
| `uptime` | Show uptime and load averages. | Source |  |
| `dmesg` | Display kernel ring-buffer messages. | Source |  |
| `free` | Display memory usage. | Source |  |
| `top` | Display Linux tasks. | Source |  |
| `vmstat` | Report virtual-memory statistics. | Source |  |
| `lscpu` | Display CPU architecture information. | Source |  |
| `lsusb` | List USB devices. | Source |  |
| `lspci` | List PCI devices. | Source |  |
| `lshw` | List hardware configuration. | Source |  |
| `uname -a` | Show kernel, hostname, architecture and other system details. | Added |  |
| `cat /etc/os-release` | Show Linux distribution and version information. | Added |  |
| `hostnamectl` | Show host, kernel and OS information on systemd systems. | Added |  |
| `free -h` | Show memory and swap usage in human-readable units. | Added |  |
| `vmstat 1` | Sample CPU, memory, process and I/O statistics every second. | Added |  |
| `iostat -xz 1` | Show extended CPU and device I/O statistics every second (sysstat package). | Added |  |
| `sar -u 1 5` | Sample CPU statistics using sysstat. | Added |  |
| `sensors` | Display hardware temperature and sensor readings (lm-sensors). | Added |  |
| `lsmem` | List memory ranges and memory-block state. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
