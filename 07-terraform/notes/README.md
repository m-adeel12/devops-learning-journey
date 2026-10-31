# Terraform Introduction 

- Terraform is an infrastructure as code tool that can deploy resources to different cloud providers such as AWS, Azure or GCP.
- This is done through the terraform registry where it will install certain plugins and it will use API calls to deploy to different providers.
  
# IAC with Version Control 

- Infrastructure as code can be stored in version control systems such as Git which allows you to track your changes, rollback to certain versions and collaborate with teams.

# Infrastructure Orchestration Vs Config management 

- Terraform as an orchestration tool will be used to deploy your severs such as EC2 instances, now how does config management tools integrate in to that. For example ansible can be used to configure your ec2 instances in order to run certain thing such as hosting a WordPress server. 

# What is Terraform ?

- HashiCorp Terraform is an infrastructure as code tool that lets you define both cloud and on-prem resources in human-readable configuration files that you can version, reuse, and share.

# Tips for when using Terraform 

- Go through the Terraform Documentation online
- Its important to thoroughly check your Terraform plan to see if it aligns with what you are trying to deploy as you dont want to be deleting important resources.
- Start small with a mvp (minimum viable product) then iterate
- Implement dry software engineering principles. Dry means do not repeat yourself 

# Terraform State File 

- Terraform State file is the blueprint - what that means is its essentially a record of your existing infrastructure. Its very important and it helps maintain item potency.
- In terms of Terraform item potency refers to your terraform configuration - no matter how many times it runs it will produce the same results.

# Desired State Vs Current State 

- Current state refers to the up to date record of your terraform infrastructure.
- Desired state refers to your terraform configuration of changes your trying to implement or things your trying to deploy.
- What terraform state file does is it compares this to your actual infrastructure
- So in simple words desired state is what your trying to achieve and current state is what actually exists.

# Terraform Provider 

- Terraform provider is essentially a plugin that allows you to interact with cloud platforms, services or technologies. The plugin is essentially what allows terraform to manage your resources in the cloud

# Terraform init

- Terraform init command initialises the backend of your infrastructure - it essentially sets up your environment 
- The backend is where terraform state stores the state of your infrastructure.

# Terraform Plan

- The terraform plan command allows you to preview the changes terraform will make to your infrastructure without actually applying them, allowing you to preview and verify modifications safely.

- + symbol means a resource is created
- dash symbol means the resource is updated
-  - symbol means the resource is deleted

# Terraform apply

- This means any resource that Terraform plans to create, update or destroy will actually be implemented when you run the Terraform apply command.
- Its where your desired infrastructure actually becomes reality.

# Terraform destroy

- Terraform destroy command is a convenient way to destroy all remote objects managed by a particular terraform configuration.

# Resource Block 

- In terraform a resource block is used to define a piece of infrastructure you want to manage. 
  
# Terraform Import

- Terraform Import allows us to bring our existing resources from the cloud in to terraforms management
- Terraform Import command is essentially used when you want to integrate terraform into an existing infrastructure setup.


# Local Vs Remote State Files 

- By default Terraform stores your state file locally in to your machine hence why its called local state files. Its very useful if your working along or building a small project.
- Local state files are best suited for environments where only one person is managing your infrastructure. You don't have to worry about other peoples input where it can affect your state file.
- By storing state files remotely multiple teams members can access and update the same infrastructure state without risking conflicts or inconsistencies.
- We also have consider automatic locking known as state locking , which prevents users from making changes at the same time which reduces the risk of state corruption. Remote backends like AWS can automatically backup your state file and apply encryption ensuring that your infrastructure state is both secure and recoverable.
