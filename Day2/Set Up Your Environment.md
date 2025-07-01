# Install Terraform :

- **Goal**: Install Terraform.

## Install Terraform
- Navigate to this URL (https://developer.hashicorp.com/terraform/install) and Download based on the operating system. 
- Extarct the file and save in C drive or some other drive copy the folder path ( **Ex:** C:\terraform ).
- in the Windows search bar and select **Edit the system environment variable**. This will open the System Properties window. Click the **Environment Variables**
- **Edit the PATH variable:** In the **System variables** section find the **Path** variable and select it.
- Click **New**
- Paste or type the path to the Terraform executable folder ( **Ex:** C:\terraform ).
- Click **OK** to save the new path.
- Click **OK** on all open windows to close them.
- **Test** Open a new command prompt or PowerShell window and type **terraform -version(or)terraform -v** If the Terraform version is displayed, the environment variable is set correctly.

  - **![image](https://github.com/user-attachments/assets/6edc7a32-35a8-4725-89f8-57c5382e4a90)**

## Create a Free Azure Account
- Go to: **https://azure.microsoft.com/free**
- Sign in with a Microsoft account.

## Install Azure CLI 
- Download Azure CLI: **Azure CLI for Windows (MSI Installer:https://aka.ms/installazurecliwindows)**
- **Step 1: Confirm Azure CLI Is Installed** : (**C:\Program Files (x86)\Microsoft SDKs\Azure\CLI2\wbin**)
- open Command Prompt / PowerShell windows
- Run: **az version** (You should now see the Azure CLI version details) 

## Manually Step : Azure CLI was not added to your system's PATH after installation.Let’s fix this step-by-step.

- Manually Add to Environment Variables
- in the Windows search bar and select **Edit the system environment variable**. This will open the System Properties window. Click the **Environment Variables**
- **Edit the PATH variable:** In the **System variables** section find the **Path** variable and select it.
- Click **New**
- Paste or type the path to the Terraform executable folder (**C:\Program Files (x86)\Microsoft SDKs\Azure\CLI2\wbin**).
- Click **OK** to save the new path.
- Click **OK** on all open windows to close them.
- open Command Prompt / PowerShell windows
- Run: **az version** (You should now see the Azure CLI version details)
- **![image](https://github.com/user-attachments/assets/fcb6cbe0-5cec-4217-866c-8fbcd8c67c53)**

## 🔑 To log in:

- Open Command Prompt (cmd) or PowerShell, run:**az login**
- It will open your browser to authenticate with your Azure account.


## ✅ Day 2 Recap: Environment Setup Done

| Task                       | Status  |
| -------------------------- | ------- |
| Terraform installed        | ✅       |
| Azure CLI installed        | ✅       |
| Azure account created      | ✅ or 🔜 |
| `az login` done (optional) | ✅ or 🔜 |
