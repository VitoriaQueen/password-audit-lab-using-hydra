# Weak Password Audit Against FTP 
## Overview
Demonstrating (in a controlled lab environment) a password audit using kali linux, Metasploitable 2, and hydra, and the risk of weak passwords on legacy FTP services.

The lab focuses on:
- service enumeration
- credential auditin
- weak password identification
- remediation awareness

---

## Lab environment

### Attacker Machine
- Kali Linux

## Target Machine
- Metasploitable 2

### Network Configuration
- NAT Network
- Isolated lab environment

---

## Tools Used

- Nmap
- Hydra
- FTP client

---

## Objectives

- Identify FTP services
- Perform servicenenumeration
- Conduct a controlled password audit
- Validate discovered credentials

---

# Lab Workflow

## 1. Verify Network Connectivity

Check Kali Linux IP address:

ip a

Check connectivity to the target:

ping TARGET_IP

---

## 2. Service Enumeration

Perform a basic scan:

nmap TARGET_IP


Detect service versions:

nmap -sV TARGET_IP

## 3. Create Password List

Create a short password wordlist:

nano user-pass.txt

Example contents:

admin
user1
msfadmin
123456
car

---

## 4. Create Username List

Create a short username wordlist:

Example contents:

admin
root
msfadmin
ftp
password

---

## 5. Run Controlled Credential Audit

Execute Hydra against the FTP service:

hydra -L user-pass.txt -P user-pass.txt ftp://TARGET_IP -T 6

---

## 6. Validate Credentials

Connect manually to FTP:

ftp TARGET_IP

## Findings

The audit demonstrated how weak credentials on legacy FTP services can allow unauthorized access.

---

## Security Risks

Weak passwords may lead to:
- unauthorized access
- sensitive file exposure
- credential reuse attacks
- lateral movement opportunities

---

## Remediation

Recommended mitigation:
- enforce strong passwords
- disable legacy FTP where possible
- migrate to SFTP
- implement account lockout policies
- monitor authentication attempts


## Disclaimer

This project was conducted in a private lab environment for educational and authorized cybersecurity training purposes only.














  




  

