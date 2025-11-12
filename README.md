# terraform-project
Pre-requisite = AWS CLI must to be installed.
1. Installed terraform in the linux(ubuntu) machine
   
     sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
   **Install HashiCorp's GPG key.**
     wget -O- https://apt.releases.hashicorp.com/gpg | \
     gpg --dearmor | \
     sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null
   **Verify the GPG key's fingerprint.**
     gpg --no-default-keyring \
     --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
     --fingerprint
   **Add the official HashiCorp repository to your system.**
      echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(grep -oP '(?<=UBUNTU_CODENAME=).*' /etc/os-release || lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
   **Update apt to download the package information from the HashiCorp repository.**
      sudo apt update
   **Install Terraform from the new repository.**
      sudo apt-get install terraform

2. write the configuration in the terraform file (cerating ec2 instance in aws)
3. terraform init ---> to intialize
   <img width="1020" height="418" alt="Screenshot 2025-11-12 103958" src="https://github.com/user-attachments/assets/c98e0bfe-3dc7-4909-bb54-d8f56c2161e8" />
4.terrraform plan -----> to review the configuration
   <img width="1575" height="804" alt="Screenshot 2025-11-12 104016" src="https://github.com/user-attachments/assets/acf8bbd3-479e-4ed7-81a8-d0d91143698f" />
5. terraform apply ----> to apply the comfiguration
   <img width="1586" height="799" alt="Screenshot 2025-11-12 104109" src="https://github.com/user-attachments/assets/08e2611b-fec1-4f0f-bdcf-0de2580662e7" />
  <img width="1378" height="716" alt="Screenshot 2025-11-12 104136" src="https://github.com/user-attachments/assets/5cbbf732-13a0-408f-8d83-881d3a5caabc" />

6. terraform destroy -----> to remove the files which are created by terraform.




