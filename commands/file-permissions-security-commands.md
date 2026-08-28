# File Permissions and Security

> **Section:** 11  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `chmod` | Change file permissions. | Source |  |
| `chown` | Change file owner and group. | Source |  |
| `chgrp` | Change group ownership of a file. | Source |  |
| `umask` | Set default permission mask for newly created files. | Source |  |
| `setfacl` | Set POSIX access-control lists (ACLs). | Source |  |
| `getfacl` | Read POSIX access-control lists. | Source |  |
| `sudo` | Execute a command as another user, usually root. | Source |  |
| `visudo` | Edit the sudoers policy safely. | Source |  |
| `passwd` | Change a user's password. | Source |  |
| `/etc/sudoers` | Sudo policy configuration file. | Source | The screenshot labels “sudoers” as a command; it is a configuration file. Edit with visudo. |
| `gpasswd` | Administer group membership/passwords. | Source |  |
| `ss` | Display socket statistics. | Source | The screenshot places ss in this section; it is primarily a networking diagnostic tool. |
| `chmod 640 FILE` | Set owner read/write, group read, others none. | Added |  |
| `chmod u+x SCRIPT` | Add execute permission for the owner. | Added |  |
| `chown -R USER:GROUP PATH` | Recursively change ownership. | Added |  |
| `umask 027` | Default to permissions that deny access to others. | Added |  |
| `setfacl -m u:USER:rw FILE` | Grant a named user read/write ACL permissions. | Added |  |
| `getfacl FILE` | Display ACL entries. | Added |  |
| `sudo -l` | Show commands the current user may run with sudo. | Added |  |
| `visudo -c` | Validate sudoers syntax. | Added |  |
| `lsattr FILE` | List extended filesystem attributes. | Added |  |
| `chattr +i FILE` | Mark a supported filesystem file immutable. | Added | Requires care; remove with chattr -i before modification. |
| `getcap -r / 2>/dev/null` | List file capabilities recursively. | Added |  |
| `setcap cap_net_bind_service=+ep BINARY` | Grant a binary permission to bind low-numbered ports without full root privileges. | Added | Use least privilege and review security implications. |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
