
# Linux Commands Used in Various Roles

This document provides an overview of common Linux commands. For each command, I have included a use case, explanation, and example.

## Table of Contents
1. [File Management](#file-management)
2. [Process Management](#process-management)
3. [Networking](#networking)
4. [System Monitoring](#system-monitoring)
5. [Disk Usage](#disk-usage)
6. [User and Permissions Management](#user-and-permissions-management)
7. [Package Management](#package-management)
8. [SSH and Remote Management](#ssh-and-remote-management)
9. [System Maintenance](#system-maintenance)

---

## 1. File Management

### `ls`
**Scenario**: Listing contents of a directory.
**Explanation**: `ls` lists files and directories in the current working directory.
**Example**:
```bash
ls -lah
```

### `cp`
**Scenario**: Copying files from one location to another.
**Explanation**: `cp` copies files and directories.
**Example**:
```bash
cp file.txt /home/user/backup/
```

### `mv`
**Scenario**: Moving or renaming files.
**Explanation**: `mv` is used to move or rename files.
**Example**:
```bash
mv oldfile.txt newfile.txt
```

### `rm`
**Scenario**: Removing files or directories.
**Explanation**: `rm` deletes files or directories.
**Example**:
```bash
rm -rf /tmp/mydir/
```

---

## 2. Process Management

### `ps`
**Scenario**: Viewing currently running processes.
**Explanation**: `ps` displays information about active processes.
**Example**:
```bash
ps aux
```

### `top`
**Scenario**: Monitoring system processes and resource usage in real-time.
**Explanation**: `top` shows real-time system statistics including CPU and memory usage.
**Example**:
```bash
top
```

### `kill`
**Scenario**: Terminating a process.
**Explanation**: `kill` sends signals to terminate processes by PID.
**Example**:
```bash
kill -9 1234
```

---

## 3. Networking

### `ifconfig`
**Scenario**: Configuring network interfaces.
**Explanation**: `ifconfig` displays network interface information.
**Example**:
```bash
ifconfig eth0
```

### `ping`
**Scenario**: Checking network connectivity.
**Explanation**: `ping` sends ICMP echo requests to test connectivity to a host.
**Example**:
```bash
ping google.com
```

### `netstat`
**Scenario**: Checking network connections, routing tables, and listening ports.
**Explanation**: `netstat` shows network-related statistics.
**Example**:
```bash
netstat -tuln
```

### `ssh`
**Scenario**: Accessing remote systems securely.
**Explanation**: `ssh` is used to log into remote machines over a network.
**Example**:
```bash
ssh user@hostname
```

---

## 4. System Monitoring

### `uptime`
**Scenario**: Checking how long the system has been running.
**Explanation**: `uptime` provides system uptime and load average.
**Example**:
```bash
uptime
```

### `df`
**Scenario**: Viewing disk space usage.
**Explanation**: `df` displays the available and used disk space for file systems.
**Example**:
```bash
df -h
```

### `du`
**Scenario**: Checking disk usage of files and directories.
**Explanation**: `du` estimates file space usage.
**Example**:
```bash
du -sh /var/log
```

---

## 5. Disk Usage

### `fdisk`
**Scenario**: Partitioning a disk.
**Explanation**: `fdisk` manages disk partitions.
**Example**:
```bash
fdisk /dev/sda
```

### `mount`
**Scenario**: Mounting file systems.
**Explanation**: `mount` attaches file systems to the system.
**Example**:
```bash
mount /dev/sdb1 /mnt/backup
```

---

## 6. User and Permissions Management

### `useradd`
**Scenario**: Creating a new user.
**Explanation**: `useradd` adds new users to the system.
**Example**:
```bash
useradd -m newuser
```

### `chmod`
**Scenario**: Changing file permissions.
**Explanation**: `chmod` modifies file and directory access permissions.
**Example**:
```bash
chmod 755 /home/user/scripts/
```

### `chown`
**Scenario**: Changing file ownership.
**Explanation**: `chown` changes the owner of files or directories.
**Example**:
```bash
chown user:group file.txt
```

---

## 7. Package Management

### `apt`
**Scenario**: Installing or updating packages (Debian/Ubuntu).
**Explanation**: `apt` is a package manager for Debian-based systems.
**Example**:
```bash
apt update && apt upgrade
```

### `yum`
**Scenario**: Installing or updating packages (RHEL/CentOS).
**Explanation**: `yum` is a package manager for RHEL-based systems.
**Example**:
```bash
yum install httpd
```

---

## 8. SSH and Remote Management

### `scp`
**Scenario**: Securely copying files between systems.
**Explanation**: `scp` copies files over SSH.
**Example**:
```bash
scp file.txt user@remote:/path/to/destination/
```

### `rsync`
**Scenario**: Syncing files between local and remote systems.
**Explanation**: `rsync` efficiently transfers and synchronizes files between systems.
**Example**:
```bash
rsync -av /src/ /dst/
```

---

## 9. System Maintenance

### `reboot`
**Scenario**: Restarting the system.
**Explanation**: `reboot` immediately restarts the system.
**Example**:
```bash
reboot
```

### `shutdown`
**Scenario**: Shutting down the system.
**Explanation**: `shutdown` powers off the system after a specified time.
**Example**:
```bash
shutdown -h now
```

---

These are some of the many commands used in various scenarios across different roles. Proper usage of these commands has been critical for system management, troubleshooting, and automation over the years.
