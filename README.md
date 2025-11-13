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
provider "azurerm" {
  features {}
}

terraform {
  required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = "~> 3.0"
    }
  }
}
