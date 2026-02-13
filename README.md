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

**Launch EC2 Instance**
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


**Install Docker: On this machine**
- Search Docker Install  https://docs.docker.com/engine/install/ubuntu/
- Add Ubuntu user to the docker group
- sudo usermod -aG docker ubuntu --> Now you should be able to run docker ps without sudo

**Install kubectl**
- kubectl is commanline interface to connect kubernetes cluster i.e how we use awscli to connect aws services
- search install kubectl
- https://kubernetes.io/docs/tasks/tools/ select install kubectl on linux
- https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-kubectl-binary-with-curl-on-linux
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
- Download the kubectl checksum file curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
- Validate the kubectl binary against the checksum file:  echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check

install kubctl
- sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
kubectl version --client
kubectl version
   
**Terraform Installation**
- search for install terraform - Alway go for official documents on installtion page up to date.
- https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli 
- linux ubuntu
- sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
- wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null

-verify finger print
gpg --no-default-keyring \
--keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
--fingerprint

**Section 4 : Run the project locally on EC2 Instance we setup**

- docker compose -h  ( docker compose can run multiple containers)
