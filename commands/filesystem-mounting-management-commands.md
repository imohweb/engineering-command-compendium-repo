# File System Mounting and Management

> **Section:** 17  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `mount /dev/sda1 /mnt` | Mount a partition at /mnt. | Source |  |
| `umount /mnt` | Unmount the filesystem mounted at /mnt. | Source |  |
| `/etc/fstab` | Persistent filesystem mount configuration file. | Source | The screenshot labels “fstab” as a command; it is a configuration file. |
| `blkid` | Display block-device attributes. | Source |  |
| `fsck /dev/sda1` | Check and repair /dev/sda1. | Source | Do not run on a mounted writable filesystem unless the filesystem documentation explicitly permits it. |
| `findmnt` | Show the current mount tree. | Added |  |
| `findmnt /mnt` | Show details for a specific mount point. | Added |  |
| `mount -a` | Mount filesystems configured in /etc/fstab that are eligible for automatic mounting. | Added |  |
| `mount -o remount,rw MOUNTPOINT` | Remount a filesystem read-write. | Added |  |
| `mount -o ro DEVICE MOUNTPOINT` | Mount a filesystem read-only. | Added |  |
| `lsblk -f` | Show filesystems, labels, UUIDs and mount points. | Added |  |
| `blkid DEVICE` | Show UUID/type metadata for a device. | Added |  |
| `tune2fs -l DEVICE` | Display ext-family filesystem parameters. | Added |  |
| `xfs_info MOUNTPOINT` | Display XFS filesystem geometry when applicable. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
