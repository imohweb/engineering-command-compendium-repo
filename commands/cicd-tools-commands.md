# CI/CD Tools and Commands

> **Section:** 21  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `java -jar jenkins.war` | Start Jenkins from a WAR file. | Source |  |
| `http://localhost:8080` | Default local Jenkins web endpoint in many standalone setups. | Source | URL, not a shell command. |
| `.gitlab-ci.yml` | GitLab CI/CD pipeline configuration file. | Source | Configuration file, not a shell command. |
| `gitlab-runner register` | Register a GitLab Runner. | Source |  |
| `gitlab-runner run` | Run GitLab Runner to process jobs. | Source |  |
| `actions/checkout@v2` | Source screenshot example of the GitHub checkout action. | Source | Older major shown in the source; use a currently maintained action version in real workflows. |
| `actions/setup-node@v2` | Source screenshot example of the Node setup action. | Source | Older major shown in the source. |
| `docker/setup-buildx-action@v1` | Source screenshot example for Docker Buildx setup. | Source | Older major shown in the source. |
| `gitlab-runner list` | List configured GitLab runners. | Added |  |
| `gitlab-runner verify` | Verify registered runners can connect to GitLab. | Added |  |
| `gitlab-runner status` | Show GitLab Runner service status where supported. | Added |  |
| `gh workflow list` | List GitHub Actions workflows using GitHub CLI. | Added |  |
| `gh workflow run WORKFLOW` | Manually dispatch a GitHub Actions workflow. | Added |  |
| `gh run list` | List recent GitHub Actions runs. | Added |  |
| `gh run view RUN_ID --log` | View logs for a GitHub Actions run. | Added |  |
| `gh run rerun RUN_ID --failed` | Rerun failed jobs in a workflow run. | Added |  |
| `curl -fsS http://localhost:8080/login` | Quickly test whether a local Jenkins HTTP endpoint is responding. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
