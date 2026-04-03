---
title : "Environment Setup"
date : 2024-01-01 
weight : 2 
chapter : false
pre : " <b> 4.2. </b> "
---

#### Required tools

- Terraform 1.14.6  
- Python 3.11  
- Node.js  
- uv  
- Docker  

#### Why these tools

- **Terraform 1.14.6**: Infrastructure as Code for AWS.
- **Python 3.11**: backend runtime and tooling.
- **Node.js**: build and run the frontend.
- **uv**: fast Python environment/dependency manager.
- **Docker**: consistent build and runtime images.

#### Install required packages (Windows)

1. **Install Chocolatey (if not installed)**
```
Set-ExecutionPolicy Bypass -Scope Process -Force
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
2. **Install Docker Desktop**
```
choco install docker-desktop -y
```
3. **Install Node.js (LTS)**
```
choco install nodejs-lts -y
```
4. **Install Python 3.11**
```
choco install python --version=3.11.9 -y
```
5. **Install uv**
```
powershell -ExecutionPolicy Bypass -c "irm https://astral.sh/uv/install.ps1 | iex"
```
6. **Install Terraform 1.14.6**
```
choco install terraform --version=1.14.6 -y
```
