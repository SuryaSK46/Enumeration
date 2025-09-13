# Explore Google hacking and enumeration 
## NAME:SURYA SK
## REG NO:212222100052
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

<img width="1913" height="976" alt="image" src="https://github.com/user-attachments/assets/b204636d-0713-4f8e-8942-a794dd246214" />



# INURL
<img width="1916" height="972" alt="image" src="https://github.com/user-attachments/assets/cc3f26ae-8ace-49fd-a128-018b75231ca0" />


# INTITLE
<img width="1918" height="971" alt="image" src="https://github.com/user-attachments/assets/821b8ed8-255c-4174-81a1-2acab6f7e527" />



# FILETYPE
<img width="1911" height="970" alt="image" src="https://github.com/user-attachments/assets/c4c11c34-2384-45d7-872a-cbca749cf3e1" />


# INTEXT
<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/017b71d8-f97f-4483-9a96-2aa2b1fa226c" />


# LINK
<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/e10e6cdd-5def-4769-8e88-2a5f2ac9cbe2" />


# CACHE
<img width="1919" height="966" alt="image" src="https://github.com/user-attachments/assets/0c4a848c-d8c6-44e3-acc0-9725a2dbe979" />


# EXT
<img width="1919" height="974" alt="image" src="https://github.com/user-attachments/assets/6e205bfc-0cc5-447e-b4f0-644214a59805" />

# DNS Enumeration
<img width="740" height="460" alt="Screenshot 2025-09-13 092335" src="https://github.com/user-attachments/assets/0bdbf7b7-e981-4130-9000-f45792c86548" />


## DNS Recon
<img width="928" height="493" alt="Screenshot 2025-09-13 092408" src="https://github.com/user-attachments/assets/6dac28c5-66af-40d2-bc46-990e4377a283" />


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
<img width="934" height="757" alt="Screenshot 2025-09-13 092429" src="https://github.com/user-attachments/assets/a95a29f9-5335-4f61-a70f-d487d3b556f8" />



# DIG
<img width="825" height="597" alt="Screenshot 2025-09-13 092501" src="https://github.com/user-attachments/assets/101da328-8c75-46e2-967e-67ed368bc77a" />


# HOST
<img width="648" height="409" alt="Screenshot 2025-09-13 092511" src="https://github.com/user-attachments/assets/49d460a7-a501-4eb1-ba8b-882be50645d7" />



# DNSSENUM

<img width="694" height="479" alt="Screenshot 2025-09-13 092530" src="https://github.com/user-attachments/assets/6ee63358-e318-4507-aaeb-3b1645e57022" />


# DNSRECON

<img width="640" height="503" alt="Screenshot 2025-09-13 092551" src="https://github.com/user-attachments/assets/70f87d67-6bdb-44a9-9951-8277091468f0" />

# FIERCE
<img width="659" height="344" alt="Screenshot 2025-09-13 092628" src="https://github.com/user-attachments/assets/f640d81e-525f-4c80-bc00-977556d52253" />


# HARVESTER
<img width="608" height="323" alt="Screenshot 2025-09-13 092655" src="https://github.com/user-attachments/assets/d5540fac-161f-4a38-bcf5-f3ccee50de58" />



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

<img width="740" height="460" alt="Screenshot 2025-09-13 092335" src="https://github.com/user-attachments/assets/2f960fed-ad5d-419f-80d2-42354d4e6d6d" />




## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```
  
 ## Output
<img width="702" height="359" alt="image" src="https://github.com/user-attachments/assets/64ff9a7e-e40f-42e7-8cd3-373c1872af80" />



## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:


<img width="565" height="193" alt="Screenshot 2025-09-13 092843" src="https://github.com/user-attachments/assets/fe25cb16-53a4-4657-92b8-6fc13a13b992" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
