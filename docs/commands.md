"# EC2 Commands" 

# EC2 Web Server Project — Commands Used (Day 2)

## 1. AWS EC2 Setup
- Launched Ubuntu 22.04 LTS instance
- Instance type: t2.micro (Free Tier)
- Security group:
  - Inbound: SSH (22) from My IP
  - Outbound: Allow all

## 2. SSH Key Commands (Windows PowerShell)
List downloads:
    Get-ChildItem "$HOME\Downloads"

Set permissions:
    icacls "$HOME\Downloads\my_day-2_key.pem" /inheritance:r
    icacls "$HOME\Downloads\my_day-2_key.pem" /grant:r "$($env:USERNAME):(R)"

SSH into EC2:
    ssh -i "$HOME\Downloads\my_day-2_key.pem" ubuntu@<13.223.200.133>

## 3. On EC2 Server (Ubuntu)
Update:
    sudo apt update
    sudo apt upgrade -y

Check system:
    hostname
    lsb_release -a
