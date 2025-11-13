# Azure VM + Storage Deployment (Terraform)

This project uses **Terraform** to deploy basic Azure infrastructure including:

- Resource Group  
- Virtual Network + Subnet  
- Network Security Group  
- Public IP + NIC  
- Virtual Machine  
- Storage Account  

It serves as a simple Infrastructure-as-Code example for learning and portfolio use.

---

## Requirements

- **Terraform** installed  
  https://developer.hashicorp.com/terraform/downloads  

- **Azure CLI** installed  
  https://learn.microsoft.com/cli/azure  

- **Provider file (`provider.tf`)** containing:

```hcl
terraform {
  required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = "4.50.0"
    }
  }
}

provider "azurerm" {
  features {}

  client_id       = "<your_client_id>"
  client_secret   = "<your_client_secret>"
  tenant_id       = "<your_tenant_id>"
  subscription_id = "<your_subscription_id>"
}

```


Usage:

az login
terraform init
terraform plan
terraform apply


To destroy:

terraform destroy


