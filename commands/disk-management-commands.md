# Disk Management

> **Section:** 4  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `df` | Report filesystem disk-space usage. | Source |  |
| `du` | Estimate file or directory space usage. | Source |  |
| `fdisk` | Manipulate MBR/GPT partition tables on Linux. | Source |  |
| `lsblk` | List information about block devices. | Source |  |
| `mount` | Mount a filesystem. | Source |  |
| `umount` | Unmount a filesystem. | Source |  |
| `parted` | Create and manipulate disk partitions. | Source |  |
| `mkfs` | Create a filesystem. | Source |  |
| `fsck` | Check and repair a filesystem. | Source |  |
| `blkid` | Locate or print block-device attributes. | Source |  |
| `df -hT` | Show filesystem usage in human-readable form with filesystem type. | Added |  |
| `du -sh PATH` | Show total size of a path. | Added |  |
| `du -h --max-depth=1 PATH &#124; sort -h` | Show first-level directory sizes, sorted. | Added |  |
| `lsblk -f` | Show block devices, filesystem types, labels and UUIDs. | Added |  |
| `fdisk -l` | List partition tables. | Added |  |
| `parted -l` | List disks and partitions known to parted. | Added |  |
| `findmnt` | List mounted filesystems in a structured tree. | Added |  |
| `swapon --show` | Show active swap devices/files. | Added |  |
| `sync` | Flush pending filesystem writes to storage. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
