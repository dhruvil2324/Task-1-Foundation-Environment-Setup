# Linux Cheat Sheet – Task 1

This document contains essential Linux commands and concepts practiced during the lab setup and security testing. These commands form the foundation for system administration and cybersecurity operations.

---

# 1️⃣ File System Navigation

Understanding file system navigation is critical in Linux because almost everything in Linux is treated as a file.

## Print Working Directory


    pwd


Displays the current directory path.  
Useful for confirming where you are before executing commands.

---

## List Directory Contents


    ls
    ls -la


- `ls` → Lists files and folders.
- `ls -la` → Shows hidden files, permissions, owner, size, and timestamps.

This command helps in analyzing directory structure and checking file attributes.

---

## Change Directory


    cd foldername
    cd ..
    cd /


- `cd foldername` → Move into a folder.
- `cd ..` → Move one level up.
- `cd /` → Move to root directory.

Navigation is essential during log analysis, configuration editing, and security testing.

---

# 2️⃣ File & Directory Permissions

Linux uses a permission model to control access to files and directories.

Each file has:
- Owner
- Group
- Others

Permissions:
- r = read
- w = write
- x = execute

---

## Change File Permissions


    chmod 755 filename
    chmod +x script.sh


- `chmod 755` → Grants full access to owner, read/execute to others.
- `chmod +x` → Makes a file executable.

This is important when running scripts or configuring secure access.

---

## Change Ownership


    chown user:group filename


Used to change file owner and group.

This is crucial in server environments where proper ownership prevents unauthorized access.

---

# 3️⃣ Package Management (APT)

APT is used in Debian-based systems like Kali Linux.

---

## Update Package List


    sudo apt update


Fetches latest package information from repositories.

---

## Upgrade Installed Packages


    sudo apt upgrade


Installs updates for existing packages.

Keeping packages updated is important for security patching.

---

## Install a Package


    sudo apt install nmap


Used to install tools required for security testing.

---

## Remove a Package


    sudo apt remove package-name


Removes unnecessary or vulnerable software.

---

# 4️⃣ Networking Commands

Networking commands are essential in cybersecurity labs for reconnaissance and troubleshooting.

---

## Show Network Configuration


    ifconfig
    ip a


Displays:
- IP address
- Network interface
- MAC address

Used to confirm proper lab network setup.

---

## Test Connectivity


    ping 192.168.1.15


Checks communication between two machines.

Helps verify if attacker and target machines can interact.

---

## View Active Connections & Open Ports


    netstat -tulnp


Shows:
- Listening ports
- Active connections
- Running services

Useful for identifying exposed services.

---

## Trace Network Path


    traceroute 8.8.8.8


Displays the path packets take to reach a destination.

Used in network diagnostics and routing analysis.

---

# 5️⃣ Process Management

Monitoring processes is important to detect suspicious activities.

---

## View Running Processes


    ps aux


Lists all running processes along with CPU and memory usage.

---

## Kill a Process


    kill PID


Stops a running process.

Important during troubleshooting or stopping malicious programs.

---

# 6️⃣ Disk Usage & System Information

---

## Check Disk Space


    df -h


Displays available and used disk space in human-readable format.

---

## Check Memory Usage


    free -h


Shows RAM usage.

---

# 7️⃣ Nmap Commands (Security Tool Practice)

---

## Basic Scan


    nmap target-ip


Identifies open ports on the target system.

---

## Service Version Detection


    nmap -sV target-ip


Identifies:
- Running services
- Software versions

Helps in vulnerability assessment.

---

# 8️⃣ OpenSSL Commands (Encryption Practice)

---

## Encrypt a File


    openssl enc -aes-256-cbc -in file.txt -out encrypted.txt


Encrypts a file using AES-256 encryption.

---

## Decrypt a File


    openssl enc -aes-256-cbc -d -in encrypted.txt -out decrypted.txt


Decrypts previously encrypted file.

Used to demonstrate symmetric encryption principles.

---

# Summary

This cheat sheet covers essential Linux commands used during:

- Lab environment setup
- Network configuration
- Connectivity testing
- Service scanning
- Encryption demonstration
- Basic system administration
