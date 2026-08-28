# User and Group Management

> **Section:** 6  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `useradd USER` | Add a user account. | Source |  |
| `usermod` | Modify a user account. | Source |  |
| `userdel USER` | Delete a user account. | Source |  |
| `groupadd GROUP` | Add a group. | Source |  |
| `groupdel GROUP` | Delete a group. | Source |  |
| `passwd USER` | Change a user password. | Source |  |
| `chage` | Change password expiry information. | Source |  |
| `whoami` | Print the current effective username. | Source |  |
| `who` | Show logged-in users. | Source |  |
| `w` | Show logged-in users and what they are doing. | Source |  |
| `id` | Display user and group IDs. | Source |  |
| `groups USER` | Show a user's groups. | Source |  |
| `useradd -m -s /bin/bash USER` | Create a user with a home directory and Bash shell. | Added |  |
| `usermod -aG GROUP USER` | Add a user to an additional group without replacing existing memberships. | Added |  |
| `groupmod -n NEW OLD` | Rename a group. | Added |  |
| `getent passwd USER` | Query the configured account databases for a user. | Added |  |
| `getent group GROUP` | Query group information. | Added |  |
| `last` | Show login history. | Added |  |
| `lastlog` | Show most recent login for users. | Added |  |
| `su - USER` | Switch to another user with a login shell. | Added |  |
| `sudo -u USER COMMAND` | Run a command as another user. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
