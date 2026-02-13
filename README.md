# aws-cloud-services
documentation
AWS Account Creation

Root User creation

**Identify & Access Management**

Create user groups and users
IAM - Identity & Access Management
IAM provides the Authentication and Authorization

**What is Authentication**
Authentication is nothing but a user/belongs have access to application/services

**What is Authorization****
Authorozation is nothing but user/group must have certain roles/polices must be assigned perform operation like read, write ,update ,detete of any of aws service

**Lauch EC2 Instance**
- Navigate AWS Services
- Selecvt EC2 Instances 
- Launch Instance
- Instance Name  - devops-demo
- Select Operating System - Unbutu 24.x
- Instance Type T2.large
- Default vpc , security group
- create kepairs - name : devops-demo.pem --> select RSA
- Enable auto assigned public ip 
- Click Launch and wait for instance to be available

- Copy public ip 
- Open Gitbach/any commond line tool 
- Navigate to the path where devops-demo.pem file saved
- Downloads $  ssh -i devops-demo.pem ubuntu@pulic ip 
