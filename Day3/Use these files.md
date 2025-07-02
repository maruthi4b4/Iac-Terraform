# Use these files: - main.tf, variables.tf, outputs.tf

**Step-by-Step File Creation Order**

| **Order** | **File**       | **Purpose**                                               | **What to Include**                                                                                                                                     |
| --------- | -------------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1**     | `variables.tf` | Define input values (e.g., resource group name, location) | `hcl<br>variable "resource_group_name" { default = "example-resources" }<br>variable "location" { default = "East US" }`                                |
| **2**     | `main.tf`      | Main configuration — where resources are declared         | `hcl<br>provider "azurerm" { features = {} }<br>resource "azurerm_resource_group" "example" { name = var.resource_group_name location = var.location }` |
| **3**     | `outputs.tf`   | Display useful values after deployment                    | `hcl<br>output "rg_name" { value = azurerm_resource_group.example.name }`                                                                               |


**💡 Why This Order?**
- **variables.tf** must be created first so you can use var.<name> in main.tf.
- **main.tf** uses the variables to define the resource (e.g., resource group).
- **outputs.tf** comes last — optional, but helps to verify and reuse values.

# 🧠 What is a Variable in Terraform?
- A **variable** in Terraform is a named input value that you define to make your configuration **dynamic, reusable, and flexible** — instead of hardcoding values directly in your code.
 
# 🎯 Purpose of variables.tf
- Keeps all input values (like resource names, locations, etc.) in one place
- Makes it easier to reuse and update your Terraform code
- Helps you make your code dynamic, instead of using fixed values

# 🧾 Example of provider.tf

provider "azurerm" {
  features {}
}


# 🧾 Example of variables.tf

variable "resource_group_name" {
  description = "Name of the Azure resource group"
  type        = string
  default     = "RG-YOGA-TFTEST-USE"
}

variable "location" {
  description = "Azure region"
  type        = string
  default     = "East US"
}

- This defines two variables:
- **resource_group_name**: the name for your Azure resource group
- **location**: the Azure region (e.g., East US)

  # 🧾 Example of main.tf

  resource "azurerm_resource_group" "rg" {
  name     = var.resource_group_name
  location = var.location
}

  # 🧾 Example of outputs.tf

  output "resource_group_name" {
  description = "The name of the created Azure resource group"
  value       = azurerm_resource_group.rg.name
}

output "resource_group_location" {
  description = "The Azure region of the resource group"
  value       = azurerm_resource_group.rg.location
}

## ✅ Step-by-Step Terraform Commands

| **Command**       | **Purpose**                                         |
| ----------------- | --------------------------------------------------- |
| `terraform init`  | 🔧 Initializes your project and downloads providers |
| `terraform plan`  | 🧠 Shows what Terraform will create or change       |
| `terraform apply` | 🚀 Applies the configuration to Azure (creates RG)  |

When prompted, type:**yes**

# 📌 Example Output After terraform apply:

**Apply complete! Resources: 1 added, 0 changed, 0 destroyed.**

**Outputs:**

resource_group_name = **"RG-YOGA-TFTEST-USE"**
resource_group_location = **"East US"**
