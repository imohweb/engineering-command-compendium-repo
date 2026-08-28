# Cloud Services

> **Section:** 22  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `aws configure` | Configure AWS CLI credentials/defaults. | Source |  |
| `aws s3 cp file.txt s3://bucket-name/` | Copy a file to an S3 bucket. | Source |  |
| `aws ec2 describe-instances` | Describe EC2 instances. | Source |  |
| `aws ec2 start-instances --instance-ids ID` | Start an EC2 instance. | Source |  |
| `aws ec2 stop-instances --instance-ids ID` | Stop an EC2 instance. | Source |  |
| `aws s3 sync LOCAL/ s3://BUCKET/PREFIX/` | Synchronize a directory to S3. | Source |  |
| `az login` | Sign in with Azure CLI. | Source |  |
| `az vm list` | List Azure virtual machines. | Source |  |
| `az vm start --name VM --resource-group RG` | Start an Azure VM. | Source |  |
| `az storage blob upload` | Upload a blob to Azure Storage. | Source |  |
| `az group create --name RG --location REGION` | Create an Azure resource group. | Source |  |
| `gcloud auth login` | Sign in with Google Cloud CLI. | Source |  |
| `gcloud compute instances list` | List Compute Engine instances. | Source |  |
| `gcloud compute instances stop INSTANCE` | Stop a Compute Engine instance. | Source |  |
| `gcloud app browse` | Open the current App Engine application in a browser. | Source |  |
| `aws sts get-caller-identity` | Show the active AWS identity/account. | Added |  |
| `aws configure list` | Show where AWS CLI configuration values came from. | Added |  |
| `aws configure --profile PROFILE` | Configure a named AWS CLI profile. | Added |  |
| `aws s3 ls` | List S3 buckets or objects. | Added |  |
| `aws logs tail LOG_GROUP --follow` | Follow CloudWatch Logs output. | Added |  |
| `aws eks update-kubeconfig --name CLUSTER --region REGION` | Update kubeconfig for an Amazon EKS cluster. | Added |  |
| `az account show` | Show the active Azure subscription and tenant. | Added |  |
| `az account list -o table` | List Azure subscriptions. | Added |  |
| `az account set --subscription SUBSCRIPTION` | Select the active Azure subscription. | Added |  |
| `az group list -o table` | List resource groups. | Added |  |
| `az resource list -o table` | List resources in the current subscription. | Added |  |
| `az vm list -d -o table` | List VMs with power state and public IP information. | Added |  |
| `az aks get-credentials -g RG -n CLUSTER` | Merge AKS credentials into kubeconfig. | Added |  |
| `gcloud auth list` | Show authenticated Google Cloud accounts. | Added |  |
| `gcloud config list` | Show active gcloud configuration. | Added |  |
| `gcloud config set project PROJECT_ID` | Set the active Google Cloud project. | Added |  |
| `gcloud projects list` | List accessible projects. | Added |  |
| `gcloud compute instances start INSTANCE --zone ZONE` | Start a Compute Engine VM. | Added |  |
| `gcloud storage ls` | List Cloud Storage buckets/objects. | Added |  |
| `gcloud container clusters get-credentials CLUSTER --region REGION` | Update kubeconfig for a GKE cluster. | Added |  |
| `gcloud logging read "resource.type=gce_instance" --limit=20` | Read recent Cloud Logging entries matching a filter. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
