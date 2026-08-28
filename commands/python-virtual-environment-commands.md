# Python and Virtual Environments

> **Section:** 30  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `python3 --version` | Show the Python 3 version. | Added |  |
| `python3 -m venv .venv` | Create a virtual environment. | Added |  |
| `source .venv/bin/activate` | Activate a virtual environment on POSIX shells. | Added |  |
| `deactivate` | Leave the active Python virtual environment. | Added |  |
| `python -m pip install PACKAGE` | Install a Python package using the interpreter-associated pip. | Added |  |
| `python -m pip install -r requirements.txt` | Install requirements from a file. | Added |  |
| `python -m pip list` | List installed packages. | Added |  |
| `python -m pip freeze > requirements.txt` | Write exact installed package versions to a requirements file. | Added |  |
| `python -m pip check` | Check installed package dependency consistency. | Added |  |
| `python -m pytest` | Run tests with pytest when installed. | Added |  |
| `python -m http.server 8000` | Start a simple local HTTP file server. | Added |  |
| `python -m json.tool file.json` | Pretty-print/validate JSON. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
