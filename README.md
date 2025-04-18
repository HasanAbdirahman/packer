# 🚀 Packer - Build a Custom AWS AMI

This project uses **Packer** to build a custom **Amazon Machine Image (AMI)** on AWS. The AMI comes pre-installed with:

- Nginx (Web Server)
- Git
- Docker
- A sample website cloned from GitHub

---

## 📁 Files Included

- `packer.json` – Main Packer template  
- `packer-vars.json` – Holds AWS and instance-specific variables  
- `docker.service` – Custom Docker service configuration  
- `notes` – Brief explanation of what the build does

---

## ⚙️ How to Use

### 1. Install Packer
Download from: https://www.packer.io/downloads

### 2. Edit Variables  
Open the `packer-vars.json` file and **change the values** to match your AWS setup:

```json
{
  "aws_access_key": "YOUR_AWS_ACCESS_KEY",
  "aws_secret_key": "YOUR_AWS_SECRET_KEY",
  "region": "us-east-1",
  "source_ami": "ami-0abcdef1234567890",
  "instance_type": "t2.micro",
  "vpc_id": "vpc-xxxxxxxx",
  "subnet_id": "subnet-xxxxxxxx"
}
```

> ☑️ Make sure your AWS credentials and network IDs are correct!

### 3. Run the Build

```bash
    packer build -var-file=packer-vars.json packer.json
```

---

## 📄 Full Guide  
📘 [Google Docs – Notes on Packer and Many More](https://docs.google.com/document/d/1tH0UEhxeHBoIH6Pe49vY-rSj6mcFfh_pw2Dyd4cqEXY/edit?usp=sharing)

---

Created by [Hasan Abdirahman](https://github.com/HasanAbdirahman) 🚀
