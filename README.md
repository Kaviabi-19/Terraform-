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
#Security Groups

resource "aws_security_group" "mysg9" {
  name        = "mysg9"
  description = "Allow inbound traffic"
  vpc_id      = aws_vpc.myvpc9.id

  ingress {
    description      = "HTTP"
    from_port        = 80
    to_port          = 80
    protocol         = "tcp"
    cidr_blocks      = ["0.0.0.0/0"]
  }

  ingress {
    description      = "SSH"
    from_port        = 22
    to_port          = 22
    protocol         = "tcp"
    cidr_blocks      = ["0.0.0.0/0"]
  }

  egress {
    from_port        = 0
    to_port          = 0
    protocol         = "-1"
    cidr_blocks      = ["0.0.0.0/0"]
    ipv6_cidr_blocks = ["::/0"]
  }

  tags = {
    Name = "mysg9"
  }
}


