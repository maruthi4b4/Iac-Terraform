# Understand the Basics (Hour-by-Hour Breakdown):

## What is Cloud Computing?
- Cloud Computing is the delivery of computing services over the internet — instead of owning and managing physical servers and infrastructure, you use someone else's (like Microsoft, Amazon, or Google).

- ✅ You rent servers, storage, and services over the internet, and pay only for what you use

  ## What is Infrastructure as Code (IaC)?

- Infrastructure as Code (IaC) is the practice of managing and provisioning IT infrastructure using code, rather than manually setting things up via cloud portals or command-line tools.

**IaC = Write code to create and manage cloud infrastructure**

**💡 Why IaC is Important**

| Benefit                       | Explanation                                         |
| ----------------------------- | --------------------------------------------------- |
| 🔁 **Repeatable**             | Same code = same infrastructure every time          |
| 📜 **Version-controlled**     | Store in Git like app code; track changes           |
| ⚡ **Faster deployments**      | Deploy full environments in minutes                 |
| 🧪 **Testable**               | Test infrastructure in pipelines (CI/CD)            |
| 🚫 **Fewer errors**           | No more manual clicking/mistakes in UI              |
| 👨‍👩‍👧‍👦 **Team-friendly** | Share code with others and review via pull requests |

  
- **🔄 IaC Lifecycle Example**
  
- ✍️ Write code (e.g., Terraform .tf files)
- 🧪 Review/test it (maybe in CI/CD)
- 🚀 Deploy it (e.g., terraform apply)
- 🧹 Update/change it by modifying code
- ❌ Destroy when done (e.g., terraform destroy)

**📂 Example IaC Tools**

| Tool               | Type        | Works With          |
| ------------------ | ----------- | ------------------- |
| **Terraform**      | Declarative | Multi-cloud         |
| **Bicep**          | Declarative | Azure only          |
| **Ansible**        | Imperative  | Config management   |
| **Pulumi**         | Declarative | Uses real languages |
| **CloudFormation** | Declarative | AWS only            |

**Declarative vs Imperative IaC**

| Style           | Description                                                 | Example Tool           |
| --------------- | ----------------------------------------------------------- | ---------------------- |
| **Declarative** | You define *what* you want, and the tool figures out *how*. | Terraform, Bicep, ARM  |
| **Imperative**  | You define *how* to build infrastructure step-by-step.      | Ansible, Shell Scripts |


**Declarative**: “I want a pizza with mushrooms and olives.” (The chef figures out how.)

**Imperative**: “First roll the dough, then add sauce, then mushrooms...” (You give step-by-step instructions.)



##  differences between Terraform, Bicep, and YAML

| **Feature**          | **Terraform**                             | **Bicep**                          | **YAML**                                    |
| -------------------- | ----------------------------------------- | ---------------------------------- | ------------------------------------------- |
| **What it is**       | IaC tool by HashiCorp                     | IaC language by Microsoft          | File format used by many tools              |
| **Used for**         | Managing infra across all cloud platforms | Managing infra on Azure only       | Configuration files (CI/CD, Ansible)        |
| **Language Type**    | HCL (HashiCorp Configuration Language)    | Domain-Specific Language (DSL)     | Data serialization format                   |
| **Cloud Support**    | Multi-cloud: Azure, AWS, GCP              | Azure only                         | Not a tool—used **with** other tools        |
| **Tool Type**        | IaC engine and language                   | IaC language (used with Azure CLI) | Syntax format used by tools                 |
| **State Management** | Yes (tracks state in `.tfstate` files)    | Managed internally by Azure        | Depends on the tool (not built-in)          |
| **Difficulty**       | Moderate (more powerful)                  | Easy to learn (Azure focused)      | Very easy to read and write                 |
| **CI/CD Friendly**   | Yes (GitHub Actions, Terraform Cloud)     | Yes (Azure DevOps, GitHub Actions) | Yes (used in pipelines like GitHub Actions) |

