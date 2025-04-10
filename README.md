# terraform-nginx

🚀 TASK 3: Infrastructure as Code (IaC) with Terraform

✅ Objective

Provision a local Docker container (NGINX) using Terraform.

🛠️ Tools & Technologies

Terraform

Docker Desktop

NGINX

GitHub (for version control)

Docker Provider for Terraform (kreuzwerker/docker)


📁 Project Structure

main.tf – Terraform configuration file

execution.log – Output logs from terraform apply

README.md – Documentation


🔧 Steps Performed

🔹 a. Install and Set Up Terraform

Downloaded and installed Terraform (version 1.11.4 for Windows).

Added Terraform to system PATH.

Verified installation using: terraform -v.

🔹 b. Create main.tf File

Wrote Terraform code to:

Configure Docker provider.

Pull the latest nginx Docker image.

Launch a container from that image.

Map host port 8080 to container port 80.

🔹 c. Initialize Terraform

Ran the following command to initialize the working directory and download the Docker provider:

terraform init

🔹 d. Plan Infrastructure

Previewed changes Terraform would make:

terraform plan

🔹 e. Apply Terraform Configuration

Provisioned the infrastructure:

terraform apply

To save logs to a file:

terraform apply | tee execution.log

Verified NGINX is running by visiting: http://localhost:8080

🔹 f. Check Terraform State

Listed managed resources:

terraform state list

Inspected a specific resource:

terraform state show docker_container.nginx_container

🔹 g. Destroy Infrastructure

Cleaned up all resources with:

terraform destroy

✅ Resultgit add README.md


Successfully provisioned and destroyed a Dockerized NGINX container using Terraform on a local environment. All infrastructure is now defined and managed as code.

📎 Notes

Ensure Docker Desktop is installed and running before starting.

The container will be accessible at: http://localhost:8080

This project demonstrates basic Infrastructure as Code (IaC) using Terraform and Docker.