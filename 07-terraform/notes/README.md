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
