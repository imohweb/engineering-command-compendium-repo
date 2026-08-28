# GitHub CLI

> **Section:** 29  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `gh auth login` | Authenticate GitHub CLI. | Added |  |
| `gh auth status` | Show authentication status. | Added |  |
| `gh repo clone OWNER/REPO` | Clone a GitHub repository. | Added |  |
| `gh repo view --web` | Open the current repository in a browser. | Added |  |
| `gh repo create` | Create a GitHub repository interactively or with flags. | Added |  |
| `gh issue list` | List issues. | Added |  |
| `gh issue create` | Create an issue. | Added |  |
| `gh pr list` | List pull requests. | Added |  |
| `gh pr checkout NUMBER` | Check out a pull request locally. | Added |  |
| `gh pr create` | Create a pull request. | Added |  |
| `gh pr checks NUMBER` | Show pull-request checks. | Added |  |
| `gh pr merge NUMBER` | Merge a pull request subject to repository policy. | Added |  |
| `gh workflow list` | List workflows. | Added |  |
| `gh workflow run WORKFLOW` | Dispatch a workflow. | Added |  |
| `gh run list` | List workflow runs. | Added |  |
| `gh run watch RUN_ID` | Watch a workflow run. | Added |  |
| `gh run view RUN_ID --log` | View workflow-run logs. | Added |  |
| `gh release list` | List releases. | Added |  |
| `gh release create TAG FILES...` | Create a GitHub release and upload assets. | Added |  |
| `gh api repos/{owner}/{repo}` | Call the GitHub API with authentication. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
