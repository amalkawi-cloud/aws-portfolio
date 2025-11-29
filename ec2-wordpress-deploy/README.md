# AWS Project 2: WordPress Blog Deployment on EC2 (LAMP Stack)

## 🎯 Goal
To launch a functional, dynamic website (WordPress blog) on AWS, demonstrating proficiency in Compute, Networking, and Database management.

## 🛠️ AWS Services Demonstrated
* **EC2 (Compute):** Hosted the application on an Amazon Linux 2023 instance (`t3.micro`).
* **VPC (Networking):** Secured the instance using an Inbound Security Group.

## ⚙️ Key Configuration Details
### 1. Security Group Rules (The Firewall)
| Port | Protocol | Source | Purpose |
| :--- | :--- | :--- | :--- |
| **22** | TCP | My IP | **Crucial:** Used for secure SSH access for setup and administration. Locked to my IP only. |
| **80** | TCP | Anywhere | Allows the public (internet) to view the blog via HTTP. |

### 2. Software & Database Setup
* **Web Server:** Apache (httpd)
* **Database:** MariaDB (MySQL)
* **Database Security:** Applied initial security hardening to the database and created a dedicated user (`wp_user`) for the WordPress application.

### 3. Key Technical Challenges Overcome
* **File Permissions:** Successfully resolved the complex file ownership and permissions issue (chown/chmod) to allow the Apache web server to write PHP session files, enabling user login to the WordPress dashboard.
* **Password Management:** Learned to securely set and manage database passwords in the Linux environment.

## 🔗 Live Demo
* **Live Blog URL:** [18.221.129.60]
* **Status:** [Running]

## 💡 Lessons Learned
This project was a deep dive into **Infrastructure as a Service (IaaS)**. It proved I can configure a server from scratch, manage network security via Security Groups, and troubleshoot common Linux/PHP configuration errors in a real-world cloud environment.
