# Text Processing Utilities

> **Section:** 15  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `grep 'pattern' file.txt` | Search a file for a pattern. | Source |  |
| `grep -r 'pattern' /dir/` | Recursively search files for a pattern. | Source |  |
| `sed 's/old/new/g' file.txt` | Replace all matches of old with new in output. | Source |  |
| `awk '{print $1}' file.txt` | Print the first whitespace-delimited field from each line. | Source |  |
| `cut -d ':' -f 1 /etc/passwd` | Print the first colon-delimited field of each line. | Source |  |
| `sort file.txt` | Sort lines in ascending order. | Source |  |
| `sort file.txt &#124; uniq` | Sort and remove adjacent duplicate lines. | Source |  |
| `tee` | Write standard input to standard output and files. | Source |  |
| `echo "text" &#124; tee file.txt` | Write text to a file while displaying it. | Source |  |
| `echo 'hello' &#124; tr 'a-z' 'A-Z'` | Translate lowercase letters to uppercase. | Source |  |
| `paste file1.txt file2.txt` | Merge corresponding lines side by side. | Source |  |
| `wc -l file.txt` | Count lines. | Source |  |
| `wc -w file.txt` | Count words. | Source |  |
| `grep -nEi "ERROR&#124;WARN" FILE` | Search case-insensitively with line numbers and extended regex. | Added |  |
| `grep -v PATTERN FILE` | Exclude matching lines. | Added |  |
| `rg PATTERN PATH` | Fast recursive search with ripgrep (when installed). | Added |  |
| `sed -n '10,20p' FILE` | Print only lines 10 through 20. | Added |  |
| `awk -F, '{print $1,$3}' file.csv` | Print selected comma-separated fields. | Added |  |
| `sort FILE &#124; uniq -c &#124; sort -nr` | Count repeated lines and sort by frequency. | Added |  |
| `comm -12 <(sort A) <(sort B)` | Print lines common to two sorted inputs in Bash. | Added |  |
| `join FILE1 FILE2` | Join sorted text files on a common field. | Added |  |
| `xargs -n1 COMMAND < input.txt` | Build command invocations from standard input. | Added |  |
| `split -l 1000 FILE chunk-` | Split a file into chunks of 1,000 lines. | Added |  |
| `column -t FILE` | Align whitespace-separated data into columns. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
