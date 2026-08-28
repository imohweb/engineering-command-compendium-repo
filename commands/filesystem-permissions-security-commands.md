# Filesystem Permissions and Security

> **Section:** 18  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `chmod 755 file.txt` | Set rwx for owner and rx for group/others. | Source |  |
| `chown user:group file.txt` | Change file owner and group. | Source |  |
| `chgrp group file.txt` | Change group ownership. | Source |  |
| `umask 022` | Set a default mask commonly resulting in 755 directories and 644 files. | Source |  |
| `setfacl` | Set filesystem ACLs. | Source |  |
| `getfacl` | Read filesystem ACLs. | Source |  |
| `chmod 600 PRIVATE_KEY` | Allow only the owner to read/write a private key. | Added |  |
| `chmod 700 DIRECTORY` | Allow only the owner full access to a directory. | Added |  |
| `chmod -R g+rX PATH` | Recursively grant group read and directory/search permissions without blindly making every file executable. | Added |  |
| `chmod 1777 DIRECTORY` | Apply world-writable permissions plus sticky bit, like /tmp. | Added |  |
| `chmod 2775 DIRECTORY` | Apply setgid so new entries inherit the directory group. | Added |  |
| `namei -l /path/to/file` | Show permissions for every component of a path. | Added |  |
| `setfacl -m g:GROUP:rx PATH` | Grant a group read/execute ACL permissions. | Added |  |
| `setfacl -d -m g:GROUP:rwx DIRECTORY` | Set a default ACL inherited by newly created entries. | Added |  |
| `getfacl -p PATH` | Display ACLs with absolute path information. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
