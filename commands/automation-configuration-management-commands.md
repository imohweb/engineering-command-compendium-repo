# Automation and Configuration Management

> **Section:** 20  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `ansible all -m ping` | Ping all inventory hosts using Ansible. | Source |  |
| `ansible-playbook playbook.yml` | Run an Ansible playbook. | Source |  |
| `ansible HOST -m command -a 'COMMAND'` | Run an ad-hoc command on a target host. | Source |  |
| `ansible-playbook --check playbook.yml` | Run a playbook in check/dry-run mode where supported. | Source |  |
| `ansible-playbook --limit HOST playbook.yml` | Limit a playbook run to a host/group. | Source |  |
| `ansible-playbook --extra-vars "key=value" playbook.yml` | Pass extra variables. | Source |  |
| `terraform init` | Initialize a Terraform working directory. | Source |  |
| `terraform plan` | Preview proposed infrastructure changes. | Source |  |
| `terraform apply` | Apply Terraform changes. | Source |  |
| `terraform destroy` | Destroy Terraform-managed infrastructure. | Source | Destructive; review plan and target carefully. |
| `terraform validate` | Validate Terraform configuration. | Source |  |
| `terraform show` | Show Terraform state or a saved plan. | Source |  |
| `puppet apply manifest.pp` | Apply a Puppet manifest locally. | Source |  |
| `puppet agent --test` | Run a one-off Puppet agent cycle. | Source |  |
| `puppet resource` | Show or manage Puppet resource state. | Source |  |
| `ansible-inventory --graph` | Display inventory hierarchy. | Added |  |
| `ansible-playbook --syntax-check playbook.yml` | Validate playbook syntax. | Added |  |
| `ansible-playbook --diff playbook.yml` | Show file/template differences produced by a playbook. | Added |  |
| `ansible-playbook --tags TAG playbook.yml` | Run only tasks matching a tag. | Added |  |
| `ansible-vault encrypt FILE` | Encrypt a sensitive Ansible data file. | Added |  |
| `ansible-vault view FILE` | View an encrypted Ansible Vault file. | Added |  |
| `terraform fmt -recursive` | Format Terraform files recursively. | Added |  |
| `terraform providers` | Show provider requirements. | Added |  |
| `terraform state list` | List resources recorded in Terraform state. | Added |  |
| `terraform output` | Display Terraform output values. | Added |  |
| `terraform workspace list` | List workspaces. | Added |  |
| `terraform import ADDRESS ID` | Import an existing object into Terraform state. | Added |  |
| `puppet parser validate manifest.pp` | Validate Puppet manifest syntax. | Added |  |
| `puppet apply --noop manifest.pp` | Preview Puppet changes without enforcing them. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
