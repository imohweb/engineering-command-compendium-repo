# File Viewing and Editing

> **Section:** 2  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `cat` | Concatenate and display file content. | Source |  |
| `tac` | Display file content in reverse line order. | Source |  |
| `more` | View file content page by page. | Source |  |
| `less` | View file content interactively with scrolling and search. | Source |  |
| `head` | Output the first part of a file. | Source |  |
| `tail` | Output the last part of a file. | Source |  |
| `nano` | Terminal-based text editor. | Source |  |
| `vim / vi` | Advanced terminal text editors. | Source |  |
| `emacs` | Text editor. | Source |  |
| `grep` | Search text using patterns. | Source |  |
| `sed` | Stream editor for filtering and transforming text. | Source |  |
| `awk` | Pattern scanning and text-processing language. | Source |  |
| `cut` | Remove or select sections from each line. | Source |  |
| `sort` | Sort lines of text files. | Source |  |
| `uniq` | Report or omit repeated adjacent lines. | Source |  |
| `tail -f FILE` | Follow a file as new lines are appended, useful for logs. | Added |  |
| `head -n 20 FILE` | Show the first 20 lines. | Added |  |
| `less +F FILE` | Open a file and follow appended output interactively. | Added |  |
| `nl -ba FILE` | Display a file with line numbers, including blank lines. | Added |  |
| `strings BINARY` | Extract printable strings from a binary file. | Added |  |
| `diff -u OLD NEW` | Show a unified diff between two files. | Added |  |
| `cmp FILE1 FILE2` | Compare two files byte by byte. | Added |  |
| `patch -p1 < change.patch` | Apply a patch file. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
