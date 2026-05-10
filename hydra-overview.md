# Hydra Overview

## What is Hydra?

Hydra is a password auditing and credential testing tool commonly used in cybersecurity labs and authorized penetration testing environment.

It can be used with numerous protocols, including:
- FTP
- SSH
- HTTP
- SMB
- RDP
- Telnet
- and many others

Hydra is frequently used to demonstrate the risk associated with:
- weak passwords
- default credentials
- poor authentication practices

---

## Purpose of the lab

In this project, Hydra was used in a controlled enviroment to perform a limited credential audit against an FTP service running on Metasploitable 2.

The objective was educational
- demonstrate password weaknesses
- validade credential security risks
- understand defensive remediation practices

---

## Command Used

hydra -L user-cred.txt -P user-pass.txt ftp://TARGET_IP -t 6

### Parameters

-L - Username list

-P - Password list

ftp:// - Target FTP service

-t 6 - Low thread count

---

## Important Note

This tool should only be used:
- in authorized environments
- on systems you own
- during approved security assessments

Unauthorized credential attacks may violate laws and policies.

---

## Official Resources

- Official THC-Hydra Github:
  https://github.com/vanhauser-thc/thc-hydra

- Kali Linux Hydra Tool Page:
  https://www.kali.org/tools/hydra/

- Nmap Official Website:
  https://nmap.org  
-

  - Nmap Official Website:
    https://nmap.org
