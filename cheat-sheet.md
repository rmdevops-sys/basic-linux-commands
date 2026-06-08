# Linux Server Administration Cheat Sheet

## System Information

```bash
hostnamectl
uname -a
cat /etc/os-release
uptime
date
free -m
lscpu
```

---

# Navigation Commands

```bash
pwd
ls
ls -la
cd /var/www
cd ..
cd ~
```

---

# File Management

## Create Files

```bash
touch file.txt
nano file.txt
vim file.txt
```

## View Files

```bash
cat file.txt
less file.txt
head file.txt
tail file.txt
tail -f logfile.log
```

## Copy Files

```bash
cp file.txt backup.txt
cp -r source_folder destination_folder
```

## Move / Rename Files

```bash
mv old.txt new.txt
mv file.txt /home/user/
```

## Delete Files

```bash
rm file.txt
rm -rf foldername
```

---

# Directory Management

```bash
mkdir test
mkdir -p app/storage/logs
rmdir test
rm -rf test
```

---

# Search Commands

```bash
find / -name "*.log"
find /var/www -type f

grep "error" logfile.log
grep -R "APP_NAME" .
```

---

# User Management

## Current User

```bash
whoami
id
```

## List Users

```bash
cat /etc/passwd
```

## Create User

```bash
adduser username
```

## Change Password

```bash
passwd username
```

## Delete User

```bash
userdel username
userdel -r username
```

## Add Sudo Access

```bash
usermod -aG sudo username
groups username
```

---

# File Permissions

## View Permissions

```bash
ls -l
```

## Change Permissions

```bash
chmod 755 file.sh
chmod 644 file.txt
chmod -R 755 folder
```

## Change Owner

```bash
chown user:user file.txt
chown -R www-data:www-data /var/www/html
```

---

# Process Management

## View Running Processes

```bash
ps aux
top
htop
```

## Kill Process

```bash
kill PID
kill -9 PID
pkill nginx
```

## Find Process

```bash
ps aux | grep nginx
```

---

# Memory & Disk

## Memory Usage

```bash
free -h
```

## Disk Usage

```bash
df -h
du -sh *
lsblk
fdisk -l
```

---

# Network Commands

## IP Address

```bash
ip a
hostname -I
```

## Test Connectivity

```bash
ping google.com
```

## DNS Lookup

```bash
nslookup google.com
dig google.com
```

## Open Ports

```bash
netstat -tulpn
ss -tulpn
```

## Download Files

```bash
wget https://example.com/file.zip
curl -O https://example.com/file.zip
```

## Public IP

```bash
curl ifconfig.me
```

---

# Package Management (Ubuntu / Debian)

## Update Repositories

```bash
apt update
```

## Upgrade Packages

```bash
apt upgrade -y
```

## Install Package

```bash
apt install nginx -y
```

## Remove Package

```bash
apt remove nginx -y
```

## Search Package

```bash
apt search nginx
```

## List Installed Packages

```bash
apt list --installed
```

---

# Package Management (AlmaLinux / Rocky Linux / RHEL)

## Update System

```bash
dnf update -y
```

## Install Package

```bash
dnf install nginx -y
```

## Remove Package

```bash
dnf remove nginx -y
```

## Search Package

```bash
dnf search nginx
```

## List Installed Packages

```bash
dnf list installed
```

---

# Service Management

## Check Status

```bash
systemctl status nginx
```

## Start Service

```bash
systemctl start nginx
```

## Stop Service

```bash
systemctl stop nginx
```

## Restart Service

```bash
systemctl restart nginx
```

## Reload Service

```bash
systemctl reload nginx
```

## Enable Service

```bash
systemctl enable nginx
```

## Disable Service

```bash
systemctl disable nginx
```

---

# Firewall Commands

## Ubuntu / Debian (UFW)

```bash
ufw status
ufw allow 22
ufw allow 80
ufw allow 443
ufw enable
ufw reload
```

## AlmaLinux / Rocky Linux

```bash
firewall-cmd --state
firewall-cmd --permanent --add-service=http
firewall-cmd --permanent --add-service=https
firewall-cmd --reload
```

---

# SSH Commands

## Connect Server

```bash
ssh root@SERVER_IP
```

## Generate SSH Key

```bash
ssh-keygen -t rsa -b 4096
```

## Copy SSH Key

```bash
ssh-copy-id root@SERVER_IP
```

---

# Archive Commands

## ZIP

```bash
zip -r backup.zip folder
unzip backup.zip
```

## TAR

```bash
tar -cvf backup.tar folder
tar -xvf backup.tar

tar -czvf backup.tar.gz folder
tar -xzvf backup.tar.gz
```

---

# Disk Monitoring

```bash
iostat
vmstat
sar
```

---

# Log Monitoring

## System Logs

```bash
journalctl -xe
journalctl -u nginx
```

## Live Logs

```bash
tail -f /var/log/syslog
tail -f /var/log/messages
```

---

# Cron Jobs

## Edit Cron

```bash
crontab -e
```

## List Cron Jobs

```bash
crontab -l
```

## Example

```bash
0 0 * * * /home/user/backup.sh
```

---

# Useful Commands

```bash
history
clear
alias ll='ls -la'
which php
whereis nginx
```

---

# Server Reboot & Shutdown

## Reboot

```bash
reboot
```

## Shutdown

```bash
shutdown -h now
```

## Schedule Shutdown

```bash
shutdown -h +30
```

---

# Root Access

```bash
sudo su -
sudo -i
```

---

# Check Server Resources

```bash
free -h
df -h
top
htop
uptime
```

---

# Check Running Services

```bash
systemctl list-units --type=service
```

---

# Check Listening Ports

```bash
ss -tulpn
netstat -tulpn
```

---

# Common Web Server Locations

## Nginx

```bash
/etc/nginx/
/var/log/nginx/
/etc/nginx/nginx.conf
```

## Apache

```bash
/etc/apache2/
/var/log/apache2/
/etc/apache2/apache2.conf
```

## OpenLiteSpeed

```bash
/usr/local/lsws/
/usr/local/lsws/conf/
/usr/local/lsws/logs/
```
