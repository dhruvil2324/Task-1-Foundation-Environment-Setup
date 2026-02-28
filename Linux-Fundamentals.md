# Linux Fundamentals

Linux fundamentals are essential for cybersecurity and penetration testing. Understanding basic commands helps in navigating the system, managing files, installing tools, and analyzing network activity.

---

## 1. File System Navigation

Linux uses a hierarchical file system structure. The following commands are used to navigate and manage directories:

### pwd (Print Working Directory)
Displays the current directory path.

Example:

    pwd


---

### ls (List Files)
Lists files and directories inside the current directory.

Examples:

    ls
    ls -l
    ls -la


- `ls -l` shows detailed file information.
- `ls -la` shows hidden files as well.

---

### cd (Change Directory)
Used to move between directories.

Examples:

    cd Documents
    cd ..
    cd /home/kali

- `cd ..` moves one level up.
- `cd /path` moves to a specific directory.

---

## 2. File & Directory Permissions

Linux controls access to files using permission settings.

### chmod (Change Mode)
Used to modify file permissions.

Example:

    chmod 777 file.txt

Permission structure:
- Read (r)
- Write (w)
- Execute (x)

Numeric values:
- 7 = Read + Write + Execute
- 6 = Read + Write
- 5 = Read + Execute

---

### chown (Change Owner)
Changes file ownership.

Example:

    chown kali:kali file.txt


This changes both the user and group ownership of the file.

---

## 3. Package Management

Linux uses package managers to install and manage software.

### apt (Advanced Package Tool)
Used to install and update software.

Examples:

    sudo apt update
    sudo apt upgrade
    sudo apt install nmap

- `apt update` updates package lists.
- `apt upgrade` upgrades installed packages.
- `apt install` installs new software.

---

### dpkg (Debian Package Manager)
Used to install `.deb` packages manually.

Example:

    sudo dpkg -i package-name.deb


---

## 4. Networking Commands

Networking commands help in diagnosing connectivity and analyzing network activity.

### ifconfig
Displays network interface details and IP address.

Example:

    ifconfig

---

### ping
Checks connectivity between systems.

Example:

    ping 192.168.56.101
    
---

### netstat
Displays network connections and listening ports.

Example:

    netstat -tulnp

---

### traceroute
Shows the path taken by packets to reach a destination.

Example:

    traceroute google.com
    
---
