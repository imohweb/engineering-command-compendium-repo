# File and Directory Management

> **Section:** 1  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `ls` | List directory contents. | Source |  |
| `cd` | Change the current directory. | Source |  |
| `pwd` | Print the current working directory. | Source |  |
| `cp` | Copy files and directories. | Source |  |
| `mv` | Move or rename files and directories. | Source |  |
| `rm` | Remove files or directories. | Source | Destructive; verify paths before using recursive/force options. |
| `mkdir` | Create directories. | Source |  |
| `rmdir` | Remove empty directories. | Source |  |
| `touch` | Create an empty file or update file timestamps. | Source |  |
| `find` | Search files and directories in a hierarchy. | Source |  |
| `locate` | Find files by name using an indexed database. | Source |  |
| `tree` | Display directories in a tree-like format. | Source |  |
| `chmod` | Change file permissions. | Source |  |
| `chown` | Change file owner and group. | Source |  |
| `chgrp` | Change group ownership. | Source |  |
| `stat` | Display file or filesystem status. | Source |  |
| `ls -lah` | List all files with human-readable sizes and details. | Added |  |
| `cp -a SOURCE DEST` | Archive-style copy preserving permissions, timestamps and symlinks. | Added |  |
| `mkdir -p path/to/dir` | Create nested directories without failing when parents already exist. | Added |  |
| `rm -rf PATH` | Recursively and forcibly remove a path. | Added | High-risk destructive command. |
| `find . -type f -name "*.log"` | Find .log files below the current directory. | Added |  |
| `find . -type f -mtime +30` | Find files modified more than 30 days ago. | Added |  |
| `ln -s TARGET LINK` | Create a symbolic link. | Added |  |
| `readlink -f PATH` | Resolve a path or symbolic link to its canonical path. | Added |  |
| `realpath PATH` | Print an absolute normalized path. | Added |  |
| `basename PATH` | Return the filename portion of a path. | Added |  |
| `dirname PATH` | Return the directory portion of a path. | Added |  |
| `file PATH` | Identify a file type from its contents. | Added |  |
| `mktemp` | Create a secure temporary file or directory. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
