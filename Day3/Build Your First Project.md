# Build Your First Project using Infrastructure as Code.

- **Goal**: Build Your First Project using Infrastructure as Code.

## 3. Create a New Folder for Your Terraform Project

**Steps to Create a Folder in VS Code**
- Open VS Code
- Launch Visual Studio Code on your system.
- Open the Explorer Panel
- Click on the Explorer icon in the left-hand toolbar or press Ctrl+Shift+E (Windows/Linux) or Cmd+Shift+E (Mac).
- Choose a Workspace
- Open the location where you want to create the folder:
- Click on File > Open Folder.
- Browse to the desired directory.
- Click Select Folder (Windows/Linux) or Open (Mac).
- Create a New Folder
- In the Explorer panel, right-click on the parent directory or workspace.
- Select New Folder.
- Name the folder (**Example:terraform-project**).

## Steps to Create a Folder Using CMD
- Open Command Prompt
- Press Win + R, type cmd, and press Enter.
- Alternatively, search for "Command Prompt" in the Start menu and open it.
- Navigate to the Desired Location
- Use the cd command to change to the directory where you want to create the folder:
- **cd path\to\desired\location** (**Example:cd C:\Projects**)
- **Create the Folder**
- Use the **mkdir** (make directory) command to create the folder:
- mkdir folder-name (**Example:mkdir terraform-project**)
- To navigate into the folder in CMD: **cd folder-name** (**Example:C:\terraform-project**)


## 🧾 What is main.tf in Terraform?
- **main.tf** is the main configuration file in a Terraform project.
- **It defines**
- The cloud provider (Azure, AWS, GCP, etc.)
- The infrastructure resources (VMs, storage, networks, etc.)
- Any variables or outputs you need

## 🛠️ How to Create main.tf (Step-by-Step)
- Open VS Code
- Open the folder: File > Open Folder > E:\terraform-project
- Create a new file: **main.tf**

## 📄 Example Content of main.tf (for Azure)

![image](https://github.com/user-attachments/assets/7d894c2f-120d-423b-9581-7ead8c5f2027)


## 🧪 How to Use main.tf

- Login to Azure : az login
- Initialize Terraform : terraform init
- Preview What Will Be Created : terraform plan
- Create the Infrastructure : terraform apply
- You’ll be prompted : Do you want to perform these actions?
- Type: yes
- You’ve now used main.tf to create a Resource Group in Azure.
- You can check it in the Azure Portal under: Resource Groups → **example-rg**

## 📌 Summary

| Step              | Purpose                                |
| ----------------- | -------------------------------------- |
| `main.tf`         | Terraform configuration file           |
| `az login`        | Authenticate with Azure                |
| `terraform init`  | Download provider, set up project      |
| `terraform plan`  | Preview what will be created           |
| `terraform apply` | Actually create the resources in Azure |

