# Node.js and npm

> **Section:** 31  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `node --version` | Show the Node.js version. | Added |  |
| `npm --version` | Show the npm version. | Added |  |
| `npm init -y` | Create a default package.json. | Added |  |
| `npm install` | Install dependencies from package.json. | Added |  |
| `npm install PACKAGE` | Add a package dependency. | Added |  |
| `npm install -D PACKAGE` | Add a development dependency. | Added |  |
| `npm ci` | Install dependencies exactly from package-lock.json; useful in CI. | Added |  |
| `npm run SCRIPT` | Run a package.json script. | Added |  |
| `npm test` | Run the configured test script. | Added |  |
| `npm outdated` | Show outdated packages. | Added |  |
| `npm audit` | Check dependencies against npm security advisories. | Added |  |
| `npm audit fix` | Apply compatible dependency updates for known vulnerabilities. | Added | Review resulting dependency changes and retest. |
| `npx COMMAND` | Run a package-provided command without a permanent global install in common workflows. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
