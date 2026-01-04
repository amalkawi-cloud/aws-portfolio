# AWS Project 4: Automated Serverless Infrastructure (Terraform + CloudFront CDN)
## 🎯 Goal
To transition from manual cloud configuration to Infrastructure as Code (IaC) by automating the deployment of a secure, globally-distributed static website. This project focuses on repeatability, security-first architecture, and professional DevOps workflows.

## 🛠️ AWS Services & Tools Demonstrated
Terraform (IaC): Used to define and provision the entire infrastructure stack through declarative HCL code.

Amazon S3: Configured as a private origin for static object storage.

Amazon CloudFront (CDN): Implemented to cache content at Edge Locations globally and enforce secure delivery.

WSL (Ubuntu) & AWS CLI: Utilized a local Linux environment for infrastructure management and object synchronization.

## ⚙️ Key Configuration Details
Origin Access Control (OAC): Implemented the latest AWS best practice for S3 security, ensuring the bucket remains private and only accessible via CloudFront.

Security: Enforced HTTPS redirection via Viewer Protocol Policies to ensure data-in-transit encryption.

Infrastructure Automation: Used a standard sequence of terraform init, plan, and apply to maintain state and prevent manual configuration drift.

## 🛡️ Advanced Troubleshooting & Engineering Insights
TLS/MTU Resolution: During deployment in a restricted network environment (Airport Wi-Fi), encountered a tls: bad record MAC error.

Diagnosis: Identified the issue as packet fragmentation/corruption caused by the network's transparent proxy and MTU settings.

Resolution: Successfully resolved the issue by manually synchronizing the system clock in WSL and adjusting the MTU (Maximum Transmission Unit) to 1300 to ensure packet integrity during the secure handshake with the Terraform registry.
