# Linux Server Administration Cheat Sheet

A comprehensive Linux server administration cheat sheet covering Ubuntu, Debian, AlmaLinux, Rocky Linux, and RHEL systems.

## Supported Operating Systems

### Debian-Based

* Ubuntu Server
* Debian

### Red Hat-Based

* Red Hat Enterprise Linux (RHEL)
* Rocky Linux
* AlmaLinux

---

## Contents

* System Information
* Navigation Commands
* File & Directory Management
* User Management
* File Permissions
* Process Management
* Memory & Disk Monitoring
* Network Commands
* Package Management
* Service Management
* Firewall Configuration
* SSH Management
* Archive & Compression Commands
* Log Monitoring
* Cron Jobs
* Server Reboot & Shutdown
* Web Server Locations

---

## Common Linux Commands

### Check System Information

```bash
hostnamectl
uname -a
cat /etc/os-release
uptime
```

### Check Memory Usage

```bash
free -h
```

### Check Disk Usage

```bash
df -h
du -sh *
```

### Check Running Processes

```bash
ps aux
top
htop
```

### Check Open Ports

```bash
ss -tulpn
```

---

## Package Management

### Ubuntu / Debian

```bash
apt update
apt upgrade -y
apt install nginx -y
```

### AlmaLinux / Rocky Linux / RHEL

```bash
dnf update -y
dnf install nginx -y
```

---

## Service Management

```bash
systemctl status nginx
systemctl start nginx
systemctl restart nginx
systemctl stop nginx
```

---

## Firewall Management

### Ubuntu / Debian

```bash
ufw allow 80
ufw allow 443
ufw enable
```

### AlmaLinux / Rocky Linux

```bash
firewall-cmd --permanent --add-service=http
firewall-cmd --reload
```

---

## SSH Access

```bash
ssh root@SERVER_IP
ssh-keygen -t rsa -b 4096
ssh-copy-id root@SERVER_IP
```

---

## Useful Commands

```bash
history
clear
sudo su -
reboot
shutdown -h now
```

---

## Web Server Locations

### Nginx

```text
/etc/nginx/
/var/log/nginx/
/etc/nginx/nginx.conf
```

### Apache

```text
/etc/apache2/
/var/log/apache2/
```

### OpenLiteSpeed

```text
/ usr/local/lsws/
/ usr/local/lsws/conf/
/ usr/local/lsws/logs/
```

---

## Contributing

Feel free to fork this repository, improve the command list, and submit pull requests.

## License

MIT License

---

**Maintained by RM Services**
