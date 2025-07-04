# Terraform-

# create IAM user
1. create IAM user -> add permissions -> Create access key -> Get access & security key

   Access key - AKIA5GORBLCE5JWJ3BH5
   
   Secure Access key - 23rOZ4dzaC7FJ/UIJPX32Ad8cLIgmySA1oOeLWq3
![image](https://github.com/user-attachments/assets/a3b22d0a-7464-4a4f-a03b-720aeb4d802f)


3. Open VS Cide -> Create a folder -> create aws.tf file-> add the below script

provider "aws" {
  region     = "ap-south-1"
  access_key = "AKIA5GORBLCE5JWJ3BH5"
  secret_key = "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"
}
https://app.layers.md/pages/bba51c6a-ea07-4899-9396-f15c757ccce2


