# Engineering Command Compendium

A practical, editable command reference for developers, cloud architects, DevOps engineers, SREs, platform engineers and other technical practitioners.

The baseline commands were transcribed from the screenshots in the supplied Word document. The repository then expands those sections with commonly needed commands for modern Linux administration, networking, troubleshooting, containers, Kubernetes, automation, CI/CD, cloud CLIs, observability, Git, GitHub CLI, Anthropic Claude / Claude Code and developer tooling.

## How to use this repository

- Browse by command category in the `commands/` directory.
- Use repository search to find a command, binary, flag or workflow.
- Treat examples as templates: replace placeholders such as `HOST`, `USER`, `FILE`, `RG`, `CLUSTER` and `PACKAGE`.
- Prefer documented, non-destructive inspection commands before write/delete operations.
- Some source commands are intentionally retained as **legacy** references (`ifconfig`, `netstat`, `init`, `docker-compose`, etc.); modern alternatives are noted beside them.

## Command categories

| # | Category | File |
|---:|---|---|
| 1 | File and Directory Management | [`commands/file-directory-management-commands.md`](commands/file-directory-management-commands.md) |
| 2 | File Viewing and Editing | [`commands/file-viewing-editing-commands.md`](commands/file-viewing-editing-commands.md) |
| 3 | Process Management | [`commands/process-management-commands.md`](commands/process-management-commands.md) |
| 4 | Disk Management | [`commands/disk-management-commands.md`](commands/disk-management-commands.md) |
| 5 | Networking | [`commands/networking-commands.md`](commands/networking-commands.md) |
| 6 | User and Group Management | [`commands/user-group-management-commands.md`](commands/user-group-management-commands.md) |
| 7 | System Information and Monitoring | [`commands/system-information-monitoring-commands.md`](commands/system-information-monitoring-commands.md) |
| 8 | Archiving and Compression | [`commands/archiving-compression-commands.md`](commands/archiving-compression-commands.md) |
| 9 | Package Management (Depends on Distribution) | [`commands/package-management-commands.md`](commands/package-management-commands.md) |
| 9A | System Services and Daemon Management | [`commands/system-services-daemon-management-commands.md`](commands/system-services-daemon-management-commands.md) |
| 10 | Scheduling Tasks | [`commands/scheduling-tasks-commands.md`](commands/scheduling-tasks-commands.md) |
| 11 | File Permissions and Security | [`commands/file-permissions-security-commands.md`](commands/file-permissions-security-commands.md) |
| 12 | System Backup and Restore | [`commands/system-backup-restore-commands.md`](commands/system-backup-restore-commands.md) |
| 13 | System Diagnostics and Troubleshooting | [`commands/system-diagnostics-troubleshooting-commands.md`](commands/system-diagnostics-troubleshooting-commands.md) |
| 14 | Networking & Remote Management | [`commands/networking-remote-management-commands.md`](commands/networking-remote-management-commands.md) |
| 15 | Text Processing Utilities | [`commands/text-processing-utilities-commands.md`](commands/text-processing-utilities-commands.md) |
| 16 | System Shutdown and Reboot | [`commands/system-shutdown-reboot-commands.md`](commands/system-shutdown-reboot-commands.md) |
| 17 | File System Mounting and Management | [`commands/filesystem-mounting-management-commands.md`](commands/filesystem-mounting-management-commands.md) |
| 18 | Filesystem Permissions and Security | [`commands/filesystem-permissions-security-commands.md`](commands/filesystem-permissions-security-commands.md) |
| 19 | Containerization and Orchestration | [`commands/containerization-orchestration-commands.md`](commands/containerization-orchestration-commands.md) |
| 20 | Automation and Configuration Management | [`commands/automation-configuration-management-commands.md`](commands/automation-configuration-management-commands.md) |
| 21 | CI/CD Tools and Commands | [`commands/cicd-tools-commands.md`](commands/cicd-tools-commands.md) |
| 22 | Cloud Services | [`commands/cloud-services-cli-commands.md`](commands/cloud-services-cli-commands.md) |
| 23 | Logging and Monitoring | [`commands/logging-monitoring-commands.md`](commands/logging-monitoring-commands.md) |
| 24 | Git Version Control | [`commands/git-version-control-commands.md`](commands/git-version-control-commands.md) |
| 25 | Shell and Environment | [`commands/shell-environment-commands.md`](commands/shell-environment-commands.md) |
| 26 | JSON, YAML and Structured Data | [`commands/json-yaml-structured-data-commands.md`](commands/json-yaml-structured-data-commands.md) |
| 27 | Security, Cryptography and Certificates | [`commands/security-crypto-certificates-commands.md`](commands/security-crypto-certificates-commands.md) |
| 28 | Database CLI | [`commands/database-cli-commands.md`](commands/database-cli-commands.md) |
| 29 | GitHub CLI | [`commands/github-cli-commands.md`](commands/github-cli-commands.md) |
| 30 | Python and Virtual Environments | [`commands/python-virtual-environment-commands.md`](commands/python-virtual-environment-commands.md) |
| 31 | Node.js and npm | [`commands/nodejs-npm-commands.md`](commands/nodejs-npm-commands.md) |
| 32 | Anthropic Claude / Claude Code | [`commands/anthropic-claude-commands.md`](commands/anthropic-claude-commands.md) |

## Safety conventions

- The repository combines commands transcribed from the supplied screenshot-based document with carefully selected additions for practical engineering use.
- Commands that can delete data, overwrite disks, change firewall rules, destroy infrastructure, or alter permissions include caution notes.
- Do not paste secrets, access tokens, passwords, private keys or production credentials directly into shell history.
- For cloud and Kubernetes commands, confirm the active account/subscription/project/context before making changes.

## Useful pre-flight checks

```bash
# Linux identity and host
whoami
hostname

# Current directory and Git branch
pwd
git status

# Kubernetes context
kubectl config current-context

# AWS identity
aws sts get-caller-identity

# Azure subscription
az account show -o table

# Google Cloud project
gcloud config get-value project

# Claude Code authentication
claude auth status --text
```

## Contributing

Contributions should keep entries concise, testable and safe. Prefer commands that are broadly useful, include a one-line purpose, flag legacy/deprecated syntax, and add a caution note for destructive operations.

Suggested contribution flow:

```bash
git switch -c docs/add-command-category
git add commands/ README.md
git commit -m "docs: expand engineering command compendium"
git push -u origin docs/add-command-category
```

## Scope and portability

Most operating-system commands target Linux/POSIX shells. Distribution-specific package-management sections include Debian/Ubuntu, Fedora/RHEL, Arch, openSUSE and Homebrew examples. Cloud, Kubernetes and developer-tool commands require the corresponding CLI/tool to be installed and authenticated.

## License

Choose a license that matches how you want others to reuse and contribute to the repository (for example, MIT or Apache-2.0).
