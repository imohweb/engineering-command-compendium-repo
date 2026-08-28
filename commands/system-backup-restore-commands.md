# System Backup and Restore

> **Section:** 12  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `rsync -avz SOURCE/ DESTINATION/` | Synchronize files/directories with archive mode and compression. | Source |  |
| `rsync -avz -e ssh SOURCE/ USER@HOST:/DEST/` | Synchronize files over SSH. | Source |  |
| `cpio` | Copy files to and from cpio archives. | Source |  |
| `dd` | Low-level block/file copying. | Source |  |
| `dd if=/dev/sda of=/path/to/backup.img` | Create a raw image backup of a disk/partition. | Source | High-risk; verify source and destination carefully. |
| `dd if=/path/to/backup.img of=/dev/sda` | Restore a raw image to a disk/partition. | Source | Destructive; overwrites the destination. |
| `rsync -aHAX --delete SOURCE/ DEST/` | Mirror a Linux tree while preserving hard links, ACLs and xattrs. | Added | --delete removes destination files absent from source; test first. |
| `rsync -avn --delete SOURCE/ DEST/` | Dry-run a mirror operation before using --delete. | Added |  |
| `dd if=SOURCE of=DEST bs=64K status=progress conv=fsync` | Copy blocks with progress and flush data. | Added |  |
| `sha256sum BACKUP_FILE` | Generate an integrity checksum for a backup. | Added |  |
| `sha256sum -c checksums.sha256` | Verify checksums. | Added |  |
| `tar -czf backup.tar.gz PATH` | Create a compressed file-level backup. | Added |  |
| `cp -a SOURCE DEST` | Create a local copy preserving metadata. | Added |  |
| `sync` | Flush pending writes before detaching storage. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
