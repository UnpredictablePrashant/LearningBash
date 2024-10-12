
# Linux Commands Used in Various Roles

This document provides an overview of common Linux commands. For each command, I have included a use case, explanation, and example.

## Table of Contents
1. [Listing Files & Directories](#listing-files-&-directories)
2. [Changing Directories](#changing-directories)
3. [Creating Directories](#creating-directories)
4. [Copying Files & Directories](#copying-files-&-directories)
5. [Moving/Renaming Files](#moving/renaming-files)
6. [Removing Files & Directories](#removing-files-&-directories)
7. [Viewing File Contents](#viewing-file-contents)
8. [Searching Files with grep](#searching-files-with-grep)
9. [Viewing System Information](#viewing-system-information)
10. [Process Management](#process-management)
11. [Changing File Permissions](#changing-file-permissions)
12. [Changing File Ownership](#changing-file-ownership)
13. [Searching for Files](#searching-for-files)
14. [Archiving and Compressing Files](#archiving-and-compressing-files)
15. [Using sudo for Administrative Purposes](#using-sudo-for-administrative-purposes)
16. [Networking](#networking)
17. [Disk Usage](#disk-usage)
18. [Package Management](#package-management)
19. [SSH and Remote Management](#ssh-and-remote-management)
20. [System Maintenance](#system-maintenance)

---

## 1. Listing Files & Directories

**Scenario**: Listing contents of a directory.
**Example**:
```bash
ls -l # Long format listing with details (permissions, owner, size, data)
ls -a # Show hidden files (those starting with a dot)
ls -h # Human-readable sizes in long format
```

## 2. Changing Directories

**Scenario**: To go from one directory to another
**Example**:
```bash
cd.. # Go up one directory
cd~  # Goto home directory
cd-  # Goto last directory you were in
```

## 3. Creating Directories

**Scenario**: To create a directory for any purpose.
**Example**:
```bash
mkdir myFolder 	    # Creates a new directory
mkdir -p dir1/dir2  # Creates a nested directory
```

## 4. Copying Files & Directories

**Scenario**: Copying files from one location to another.
**Example**:
```bash
cp file.txt /home/user/backup/ 		     # Make a copy of existing file into a directory 
cp source.txt destination.txt 		     # Make a copy of the file
cp -r source/directory destination/directory # Copy directory recursively
```

## 5. Moving/Renaming Files

**Scenario**: Moving or renaming files.
**Example**:
```bash
mv oldfile.txt newfile.txt 		# Rename File
mv file.txt /path/to/destination	# Move File to another Location
```

## 6. Removing Files & Directories

**Scenario**: Removing files or directories.
**Example**:
```bash
rm file.txt		# Removes a file
rm -r directory		# Removes a directory and its contents
rm -rf directory/	# Force removes a directory, even if non-empty
```

## 7. Viewing File Contents

**Scenario**: Viewing contents present in a file.
**Example**:
```bash
cat file.txt		# Output the entire file
less file.txt		# Scroll through the file contents (using up/down keys)
head file.txt		# View the first 10 lines of a file
tail file.txt		# View the last 10 lines of a file
tail -f logfile.log	# Continuously outputs the end of a file (useful for logs)	
```

## 8. Searching Files with grep

**Scenario**: Searching file.
**Example**:
```bash
grep "search_term" file.txt	# Search for a term in file
grep -r "search_term" /path	# Recursively search within file in a directory
grep -i "search_term" file.txt	# Case insensitive search
```

## 9. Viewing System Information

**Scenario**: Searching file.
**Example**:
```bash
uname -a 	# Kernal Version and system information 
df -h 		# Disk usage of file systems
free -h 	# Displays memory usage
top 		# Realtime system resource monitoring
uptime 		# Provides system uptime and load average
du 		# Estimates file space usage
```

## 10. Process Management

**Scenario**: Mostly done for process management.
**Example**:
```bash
ps aux			# List all running processes
kill [pid]		# Terminate a process with its process ID (PID)
kill -9 [pid]		# Force kill a process
killall process_name	# Kill all processes with a specific name
```

## 11. Changing File Permissions

**Scenario**: Used for modifying user permissions.

There are particularly 3 main permissions
read, write & execute represented by r, w, x respectively in Linux
Where r = 4, w = 2, x = 1. Permissions are given by adding these numbers, like for read only 4, for read & write only 6, for all permissions 7
There are 3 kinds of users that require the permission 
owner, group & others

**Example**:
```bash
chmod 755 file.txt		# Assign read, write and execute permission (Owner: rwx, Group: r-x, Other: r-x)
chmod u+x script.sh		# Gives the owner execute permissions
chmod -R 777 /directory		# Grants all the users full permission on a directory recursively
useradd -m new_user		# Adds new users to the system
```

## 12. Changing File Ownership

**Scenario**: Changing the ownership of a file.
**Example**:
```bash
chown user:group file.txt	# Change owner and group
chown -R user:group /dir	# Recursively change ownership of all the files in a directory
```

## 13. Searching for Files

**Scenario**: Searching a file.
**Example**:
```bash
find /path -name 'file.txt'		# Search by filename
find /path -type f -size +100M		# Find files larger than 100MB
find /path -mtime -1			# Find file modified in last 24 hours
```

## 14. Archiving and Compressing Files

**Scenario**: archive/compress a file.
**Example**:
```bash
tar -cvf archive.tar /path		# Create a tar archive of a directory
tar -xvf archive.tar			# Extract a tar archive
tar -czvf archive.tar.gz /path		# Create a compressed gzip tar archive
tar -xzvf archive.tar.gz		# Extract a compressed gzip tar archive
```

## 15. Using sudo for Administrative Purposes 

**Scenario**: Administrative access
**Example**:
```bash
sudo command		# Run a command as superuser/roon
sudo su			# Switch to the root user
```

## 16. Networking

**Scenario**: Configuring network interfaces.
**Example**:
```bash
ifconfig eth0		# Displays network interface information
ping google.com		# Sends ICMP echo requests to test connectivity to a host
netstat -tuln		# Shows network-related statistics
ssh user@hostname	# Used to log into remote machines over a network
```

## 17. Disk Usage

**Scenario**: Used to operate on disk.
**Example**:
```bash
fdisk /dev/sda 			# Partitioning a disk
mount /dev/sdb1 /mnt/backup 	# Attaches file systems to the system
```

## 18. Package Management

**Scenario**: Installing or updating packages.
**Example**:
```bash
apt update # Installing packages (Debian/Ubuntu).
apt upgrade # Updating packages (Debian/Ubuntu).
yum install httpd # Installing or updating packages (RHEL/CentOS).
```

## 19. SSH and Remote Management

**Scenario**: Securely copying & syncing files between systems.
**Example**:
```bash
scp file.txt user@remote:/path/to/destination/		# Securely copying files between systems
rsync -av /src/ /dst/					# Syncing files between local and remote systems
```

## 20. System Maintenance

**Scenario**: System operation commands.
**Example**:
```bash
reboot 			# Immediately restarts the system
shutdown -h now 	# Powers off the system after a specified time
```

These are some of the many commands used in various scenarios across different roles. Proper usage of these commands has been critical for system management, troubleshooting, and automation over the years.
