# Sample repo showing how to store Terraform statefile locally

1. You need to have Terraform CLI installed
2. Fork or create your own main.tf file.
   
   Example of main.tf content:
   ```
   resource "null_resource" "helloWorld" {
    provisioner "local-exec" {
        command = "echo hello world"
    }
   }
   ```
   It can be any other resource.
 
3. Run `terraform init` and `terraform apply` 
   Now you have .terraform folder and terraform.tfstate file stored locally.
    
4. If you want to create your own repo it is important to create .gitingore file and put the .terraform folder and your state file in it so they do not get upload to github.
