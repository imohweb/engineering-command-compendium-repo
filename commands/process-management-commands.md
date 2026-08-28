# Process Management

> **Section:** 3  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `ps` | Report a snapshot of current processes. | Source |  |
| `top` | Display and monitor Linux tasks. | Source |  |
| `htop` | Interactive process viewer (when installed). | Source |  |
| `kill PID` | Send a signal to a process, commonly to request termination. | Source |  |
| `killall NAME` | Send a signal to processes by name. | Source |  |
| `bg` | Resume a suspended job in the background. | Source |  |
| `fg` | Bring a job to the foreground. | Source |  |
| `jobs` | List active jobs in the current shell. | Source |  |
| `nice -n 10 COMMAND` | Run a program with a modified scheduling priority. | Source |  |
| `renice 10 -p PID` | Alter the priority of a running process. | Source |  |
| `uptime` | Show system uptime and load averages. | Source |  |
| `time COMMAND` | Measure command runtime and resource use. | Source |  |
| `ps aux --sort=-%mem &#124; head` | Show the top memory-consuming processes. | Added |  |
| `ps aux --sort=-%cpu &#124; head` | Show the top CPU-consuming processes. | Added |  |
| `pgrep -af PATTERN` | Find processes by pattern and print full command lines. | Added |  |
| `pkill -TERM PATTERN` | Send a signal to matching processes. | Added |  |
| `pstree -p` | Display processes as a tree with PIDs. | Added |  |
| `nohup COMMAND >app.log 2>&1 &` | Run a command so it can continue after logout. | Added |  |
| `disown %JOB` | Detach a shell job from the current shell. | Added |  |
| `timeout 30s COMMAND` | Stop a command if it runs longer than the specified duration. | Added |  |
| `kill -STOP PID` | Suspend a process. | Added |  |
| `kill -CONT PID` | Resume a suspended process. | Added |  |
| `kill -9 PID` | Force-kill a process. | Added | Use only when graceful termination fails. |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
