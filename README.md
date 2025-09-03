# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

| Operator    | Description                        | Example Usage           |
| ----------- | ---------------------------------- | ----------------------- |
| `site:`     | Search within a specific domain    | `site:example.com`      |
| `inurl:`    | Search in URL                      | `inurl:admin`           |
| `intitle:`  | Search in page title               | `intitle:"index of"`    |
| `filetype:` | Search by file type                | `filetype:pdf`          |
| `intext:`   | Search inside page text            | `intext:"confidential"` |
| `link:`     | Pages that link to a specific site | `link:example.com`      |
| `cache:`    | View cached version of a site      | `cache:example.com`     |
| `ext:`      | Same as filetype                   | `ext:xls`               |

 ## Architecture 
 ```
+----------------------+
|   Attacker / Hacker  |
|   (Browser & Google) |
+----------+-----------+
           |
           | Google Dork Queries
           v
+---------------------------+
|       Google Search       |
+---------------------------+
           |
           | Indexed Public Content
           v
+---------------------------+
|   Target Websites / Data  |
| - Leaked files            |
| - Open directories        |
| - Sensitive info          |
+---------------------------+

```

# Output:

# SITE:

<img width="1899" height="967" alt="479903484-09f05aea-ded5-4189-a2db-eced6b99efcf" src="https://github.com/user-attachments/assets/251b8f95-17ab-4cb7-9d53-e32b3ff8958e" />

# INURL:

<img width="1919" height="975" alt="479904070-d0a543be-43e1-41f0-af57-9311ad26eb7e" src="https://github.com/user-attachments/assets/1bf4c325-b30d-4fb3-b82d-da301548109f" />

# INTITLE:

<img width="1919" height="971" alt="479904435-be357411-eb33-4925-9f9b-ecec410dd00b" src="https://github.com/user-attachments/assets/093a5ebb-ebdb-4f47-88fa-c931d9d2a59c" />

# FILETYPE:

<img width="1912" height="979" alt="479905486-6b980189-dcd4-45b4-900d-bee8b09da35b" src="https://github.com/user-attachments/assets/f8233e44-55d0-4e17-87bf-22dc7c0232c0" />

# INTEXT:

<img width="1919" height="926" alt="479906017-dca34c6b-b9ba-4889-8977-d14cea758881" src="https://github.com/user-attachments/assets/9caedccc-3609-417d-a2f0-190c7845c0ba" />

# LINK:

<img width="1919" height="909" alt="479906411-eed34eb3-0452-4371-aaa6-047b1d4ca585" src="https://github.com/user-attachments/assets/fec007cc-3649-49b8-81f9-bfd76a2fe2a8" />

# CACHE:

<img width="1919" height="919" alt="479906656-67a2166e-1b49-43a9-b826-dba5f340539e" src="https://github.com/user-attachments/assets/9f149b4c-5f49-4d76-92f4-a173a4f87b61" />

# EXT:

<img width="1915" height="907" alt="479906911-ecf411ee-d04a-44eb-9aeb-3063101824fa" src="https://github.com/user-attachments/assets/fc2940ca-44e4-4f21-8c30-bbb2f1c844ff" />

# DNS Enumeration

<img width="736" height="534" alt="479908719-bf43a1f9-19f3-4a90-a049-14e850f3db49" src="https://github.com/user-attachments/assets/bc8683d9-b894-4a43-aaf1-e4b5bd3f8f3a" />


## DNS Recon

 provides the ability to perform:
 Check all NS records for zone transfers
 Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
 Perform common SRV Record Enumeration
 Top level domain expansion

<img width="746" height="603" alt="479907906-bb21a594-6fae-4950-9a29-98392372574c" src="https://github.com/user-attachments/assets/ca09ee91-6e21-4013-a032-91d87af35d18" />

| Record Type | Meaning                        | Example Output                   |
| ----------- | ------------------------------ | -------------------------------- |
| A           | Host to IPv4 address           | `example.com -> 93.184.216.34`   |
| AAAA        | Host to IPv6 address           | `example.com -> ::1`             |
| MX          | Mail server info               | `mail.example.com`               |
| NS          | Name servers                   | `ns1.example.com`                |
| TXT         | Misc data (SPF, verifications) | `v=spf1 include:_spf.google.com` |
| CNAME       | Canonical names (aliases)      | `www -> example.com`             |

## Common Tools Used (Kali Linux)

| Tool           | Description                                | Usage Example                           |
| -------------- | ------------------------------------------ | --------------------------------------- |
| `nslookup`     | DNS lookup tool (simple queries)           | `nslookup example.com`                  |
| `dig`          | DNS lookup utility (detailed)              | `dig example.com any`                   |
| `host`         | Simple DNS querying tool                   | `host example.com`                      |
| `dnsenum`      | Perl script to enumerate DNS info          | `dnsenum example.com`                   |
| `fierce`       | DNS scanner to locate non-contiguous IPs   | `fierce -dns example.com`               |
| `dnsrecon`     | Powerful DNS enumeration script            | `dnsrecon -d example.com -a`            |
| `theHarvester` | Subdomain enumeration using search engines | `theHarvester -d example.com -b google` |


## OUTPUT:

# NSLOOKUP
<img width="752" height="812" alt="479909190-4d09669d-a5d7-43e9-983a-b87b395dd52f" src="https://github.com/user-attachments/assets/37129fa6-9732-4ad7-9120-09217c3323aa" />

# DIG

<img width="726" height="564" alt="479909853-fec89592-9804-48d2-91a5-5e5636741f9b" src="https://github.com/user-attachments/assets/2195584a-275d-4ae7-a500-f63d4d0a5f25" />

# HOST 

<img width="750" height="447" alt="479909984-67f39315-8ad0-4d37-8536-155e1731829d" src="https://github.com/user-attachments/assets/4cc159fa-cbb6-43d9-b483-e0fd06561256" />

# DNSENUM

<img width="733" height="543" alt="479910262-7c1e5164-50a3-4edc-b3c2-f1d8fb7342f1" src="https://github.com/user-attachments/assets/81b47aae-2231-42e5-a7db-938d0d02ec7f" />

# DNSRECON

<img width="746" height="603" alt="479907906-bb21a594-6fae-4950-9a29-98392372574c" src="https://github.com/user-attachments/assets/e594606e-c21c-4c05-b0d1-706b0c63ceb3" />

# FIERCE

<img width="742" height="762" alt="479912158-3836a9af-37da-448a-ac8d-ae7fbbcee8dd" src="https://github.com/user-attachments/assets/7662a785-2a0c-4ac4-ab89-46e6b3719003" />

# HARVESTOR

<img width="739" height="705" alt="479913848-f31dcc14-9a74-41ee-8ca0-b1bc96359f82" src="https://github.com/user-attachments/assets/c94911ec-fe39-4521-9df1-a84d2984dbe0" />


## Architecture Diagram 
```
+-------------------+        +------------------+       +------------------+
|                   |        |                  |       |                  |
|   Attacker (You)  +------->|   Target Server   +<----->+    DNS Server    |
| Kali Linux / Parrot|       | (Mail / DNS Host) |       |  (Authoritative) |
+---------+---------+        +---------+--------+       +---------+--------+
          |                            ^                          ^
          |                            |                          |
          |                            |                          |
          |           +-----------------------------+            |
          |           |      Information Tools      |            |
          |           |-----------------------------|            |
          |           | smtp-user-enum              |            |
          |           | nmap --script smtp-enum-*   |            |
          |           | dnsenum                     |<-----------+
          |           +-----------------------------+
          |
          v
+-----------------------------+
|   Output/Report             |
|  - Usernames Found          |
|  - MX Records / Zones       |
|  - Subdomains / IPs         |
+-----------------------------+

```

## dnsenum
**Purpose:** A multithreaded Perl script to enumerate information from DNS servers.

**Use case:** Performs DNS zone transfers, brute force subdomains, and gather host IPs.

```
dnsenum example.com
```

## Output:

<img width="736" height="510" alt="479914657-95163872-8224-47b5-adeb-68db81607fb4" src="https://github.com/user-attachments/assets/4810b157-2aee-49de-b157-29a8f5c24610" />


## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```
  
 ## Output
  
<img width="747" height="415" alt="479915623-df055f43-0a50-48ec-ab9e-9e27218eef4d" src="https://github.com/user-attachments/assets/6c88313e-0b7d-470e-808c-8f1e3cb49187" />


## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:

<img width="680" height="142" alt="479915907-bf2982f5-e7bb-4537-9a7d-bc5bfed15ad2" src="https://github.com/user-attachments/assets/424de1b0-4fc9-4f79-b1cc-c1dc0bc43deb" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
