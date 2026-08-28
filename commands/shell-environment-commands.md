# Shell and Environment

> **Section:** 25  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `echo "$VAR"` | Print a shell variable. | Added |  |
| `env` | Print the process environment. | Added |  |
| `printenv VAR` | Print one environment variable. | Added |  |
| `export VAR=value` | Set and export an environment variable to child processes. | Added |  |
| `unset VAR` | Remove a shell variable/environment variable. | Added |  |
| `source FILE` | Execute shell code from a file in the current shell. | Added |  |
| `. FILE` | POSIX shorthand for source. | Added |  |
| `which COMMAND` | Locate an executable via PATH (implementation varies). | Added |  |
| `command -v COMMAND` | Portable way to determine how a command resolves. | Added |  |
| `type COMMAND` | Show whether a name is an alias, builtin, function or executable. | Added |  |
| `alias ll='ls -lah'` | Create a shell alias. | Added |  |
| `unalias NAME` | Remove an alias. | Added |  |
| `history` | Show shell command history. | Added |  |
| `history &#124; grep PATTERN` | Search shell history. | Added |  |
| `COMMAND > file.log 2>&1` | Redirect standard output and error to a file. | Added |  |
| `COMMAND 2> errors.log` | Redirect standard error only. | Added |  |
| `COMMAND1 &#124; COMMAND2` | Pipe one command output into another. | Added |  |
| `COMMAND1 && COMMAND2` | Run the second command only if the first succeeds. | Added |  |
| `COMMAND1 &#124;&#124; COMMAND2` | Run the second command only if the first fails. | Added |  |
| `set -euo pipefail` | Common Bash strict-mode settings for scripts. | Added | Understand each option before adopting it in existing scripts. |
| `trap "COMMAND" EXIT` | Run cleanup logic when a shell script exits. | Added |  |
| `read -r VAR` | Read a line from standard input without backslash interpretation. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
