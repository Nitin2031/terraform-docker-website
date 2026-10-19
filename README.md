Static Website Deployment Using Docker and Terraform on AWS
Project Overview

This project demonstrates the deployment of a responsive static website built using HTML, CSS, and JavaScript. The website is containerized using Docker and Nginx, while Terraform is used to automate AWS infrastructure provisioning.

The project showcases practical skills in web development, containerization, Infrastructure as Code (IaC), and cloud deployment.

Technologies Used
HTML5 – Website structure
CSS3 – Styling and responsive design
JavaScript – Interactive functionality
Docker – Application containerization
Nginx – Web server for serving static files
Terraform – Automated infrastructure provisioning
AWS EC2 – Cloud hosting environment
Git & GitHub – Version control and source code management
Project Architecture
HTML, CSS, and JavaScript are used to build the website.
Docker packages the website with Nginx into a container image.
Terraform provisions the required AWS infrastructure, including an EC2 instance and security group.
Docker runs the website container on the EC2 instance.
Users access the deployed website through a web browser.
Project Structure
terraform-docker-website/
├── website/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── Dockerfile
├── docker-compose.yml
├── terraform/
│   ├── main.tf
│   ├── provider.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── user_data.sh
├── .gitignore
└── README.md

Features
Responsive website design
Interactive JavaScript functionality
Docker-based application deployment
Nginx web server configuration
Automated AWS infrastructure provisioning using Terraform
Reproducible deployment process
Version-controlled project files
Prerequisites

Install or configure the following tools before starting:

Git
Docker
Terraform
AWS CLI
An AWS account with appropriate permissions
Run the Website Locally

Clone the repository:

git clone https://github.com/YOUR-USERNAME/terraform-docker-website.git
cd terraform-docker-website


Build the Docker image:

docker build -t terraform-docker-website .


Run the container:

docker run -d --name static-website -p 8080:80 terraform-docker-website


Open the following URL in your browser:

http://localhost:8080


To stop and remove the container:

docker stop static-website
docker rm static-website

Deploy on AWS Using Terraform
Configure AWS credentials securely using the AWS CLI.
Navigate to the Terraform directory.
Initialize Terraform.
Validate the Terraform configuration.
Review the proposed infrastructure changes.
Apply the configuration to provision AWS resources.
Verify the website using the deployment URL or public IP address provided by the project.

Example commands:

cd terraform
terraform init
terraform fmt -check
terraform validate
terraform plan
terraform apply


Review the plan before applying changes and ensure the configuration uses appropriate security rules.

Cleanup AWS Resources

When you finish testing, remove the resources managed by Terraform:

terraform destroy


Review the proposed deletions before confirming. Verify that any associated billable resources have been removed.

Learning Outcomes
Understanding Infrastructure as Code using Terraform
Building and running Docker containers
Serving static websites using Nginx
Provisioning cloud infrastructure on AWS
Working with Linux and cloud deployment workflows
Managing project source code using Git and GitHub
Future Enhancements
Implement CI/CD using GitHub Actions
Push Docker images to Docker Hub
Configure a custom domain and HTTPS
Add monitoring and logging
Introduce reusable Terraform modules
Author

Nitin Jangir

GitHub: https://github.com/Nitin2031
