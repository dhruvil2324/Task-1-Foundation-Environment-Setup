# Lab Environment Setup

To perform security testing in a safe and controlled manner, a virtual lab environment was created. This lab allows practical learning without affecting real systems.

---

## 1. Installing Virtualization Software

A virtualization platform is required to create and manage virtual machines.

### VirtualBox
Official Website: https://www.virtualbox.org  
Download Page: https://www.virtualbox.org/wiki/Downloads  

VirtualBox was used to create separate virtual machines for the attacker and target systems.

(Alternatively, VMware Workstation Player can be used.)

### VMware Workstation Player
Official Website: https://www.vmware.com  
Download Page: https://www.vmware.com/products/workstation-player.html

---

## 2. Installing Kali Linux (Attacker Machine)

Kali Linux is a penetration testing operating system that comes pre-installed with security tools.

Official Website: https://www.kali.org  
Download Page: https://www.kali.org/get-kali/ 

Configuration used:
- RAM: 4 GB
- CPU: 2 Cores
- Storage: 40 GB (Dynamically Allocated)
- Network Mode: Host-Only Adapter

After installation, the system was updated using:

    sudo apt update && sudo apt upgrade


Kali Linux was used to perform scanning, analysis, and testing within the lab.

---

## 3. Installing Target Machine (Metasploitable2 / DVWA)

A vulnerable target machine was set up to simulate real-world security weaknesses.

### Option 1: Metasploitable2
Metasploitable2 is a deliberately vulnerable Linux virtual machine used for penetration testing practice.

Official Page: https://sourceforge.net/projects/metasploitable/  

### Option 2: DVWA (Damn Vulnerable Web Application)
DVWA is a vulnerable web application designed for practicing web-based attacks such as SQL Injection and Cross-Site Scripting (XSS).

Official Website: https://dvwa.co.uk  
GitHub Repository: https://github.com/digininja/DVWA  

The target machine was configured on the same virtual network as Kali Linux.

---

## 4. Configuring Private Lab Network (Host-Only Adapter)

To ensure safe testing, a Host-Only Adapter network was configured. This setup allows communication between virtual machines without exposing them to the public internet.

Steps performed:
- Set both Kali Linux and the target machine to use Host-Only Adapter.
- Verified IP addresses using:

      ifconfig
  
- Tested connectivity using:

      ping <target-ip>

- Confirmed communication using:

      nmap <target-ip>


This configuration ensured that both machines could communicate securely within an isolated lab environment.