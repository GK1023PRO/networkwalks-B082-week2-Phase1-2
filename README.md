# PENETRATION TESTING REPORT

## FOOTPRINTING & NETWORK SCANNING PHASES

### W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS

| Field | Details |
|---|---|
| **Pentester Name (Cybersecurity Professional)** | Georges Khoury |
| **Program/Batch** | B082-Networkwalks |
| **Date** | 19 August 2026 |
| **Modules Completed** | W2-PM1 – Footprinting with Multiple Kali Tools<br>W2-PM2 – GHDB-Based Footprinting Attacks<br>W2-PM3 – Maltego-Based Footprinting Attacks<br>W2-PM4 – theHarvester-Based Footprinting Attacks<br>W2-PM5 – Zenmap-Based Network Scanning |
| **Client/Target** | 1. Networkwalks (secured written permission already)<br>2. My own local LAN Network |
| **Permission secured from client?** | Yes |
| **Phases Covered** | **Phase 1:** Reconnaissance & Footprinting<br>**Phase 2:** Scanning & Network Discovery |

---

## 1. Liability Disclaimer

I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.

## 2. Introduction

This report documents the practical activities completed during Week 2 of the Networkwalks Cybersecurity Program, covering the Reconnaissance, Footprinting, Scanning, and Network Discovery phases. The completed modules include W2-PM1 (Footprinting with Multiple Kali Tools), W2-PM2 (GHDB-Based Footprinting Attacks), W2-PM3 (Maltego-Based Footprinting Attacks), W2-PM4 (theHarvester-Based Footprinting Attacks), and W2-PM5 (Zenmap-Based Network Scanning).

For W2-PM1, I used Kali Linux to perform authorized footprinting against the `networkwalks.com` domain using multiple reconnaissance tools. For W2-PM2, I used the Google Hacking Database (GHDB) and Google search operators to perform footprinting and identify publicly indexed information. For W2-PM3, I used Maltego on a Windows PC to perform footprinting, gather publicly available information, and visualize relationships between discovered entities. For W2-PM4, I used theHarvester on Kali Linux to perform OSINT-based reconnaissance and gather publicly available information related to the authorized target.

For W2-PM5, I used Zenmap on a Windows PC to perform network discovery on my own local LAN. I first identified my local IPv4 address and LAN subnet and then performed a Ping Scan against the subnet. The scan identified 24 live hosts, and I documented the discovered IP addresses, available MAC addresses, device information, and network topology.

All activities documented in this report were performed only within the authorized scope of the assigned cybersecurity practicals or against systems and networks that I own. This report documents the tools and techniques used, the activities performed, the results observed, the evidence collected, the associated security risks, and the recommended mitigation measures.

## 3. Tools Used

The table below lists each tool used in this report and its purpose.

| Tool | Purpose |
|---|---|
| **Kali Linux & Windows** | Operating systems used for reconnaissance, footprinting, OSINT, and network scanning activities. |
| **WHOIS** | Find domain registration details, including registration dates, registrar, and name servers. |
| **WhatWeb** | Fingerprint web technologies, including web servers, frameworks, and other detectable technologies. |
| **nslookup** | Resolve domain names and retrieve DNS information. |
| **curl -I** | Retrieve and inspect HTTP response headers from a web server. |
| **wafw00f** | Detect whether a website is protected by a Web Application Firewall (WAF). |
| **dnsrecon** | Perform DNS reconnaissance and enumerate available DNS records. |
| **Zenmap (Nmap GUI)** | Scan the local LAN subnet to discover live hosts and identify available IP and MAC addresses. |
| **Windows CMD** | Identify the local IPv4 address, subnet mask, default gateway, and local network configuration. |
| **Google / GHDB** | Perform search-engine-based footprinting using Google search operators and GHDB queries. |
| **Maltego** | Gather and correlate publicly available information and visualize relationships between discovered entities. |
| **theHarvester** | Perform OSINT-based reconnaissance and gather publicly available information from supported external sources. |

## 4. Activities Performed

### 4.1 Footprinting & Reconnaissance — W2-PM1

I performed authorized reconnaissance against the `networkwalks.com` domain using six Kali Linux tools: **WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon**. Each tool was used to collect a different type of publicly available information about the target.

First, I used **WHOIS** to obtain publicly available domain registration information and identify the domain's name servers. The results provided information related to the domain registration and associated infrastructure.

I then used **WhatWeb** to identify technologies used by the website. The results identified **WordPress 7.0.4** and **WP Download Manager 3.3.58**, along with other information exposed by the website.

Using **Nslookup**, I resolved the domain name to its IP address. The result identified **192.232.216.135**.

I used **Curl** with the `-I` option to inspect the HTTP response headers returned by the website. The results provided additional information about the web application and exposed a reference to the WordPress REST API endpoint `/wp-json/`.

Next, I used **Wafw00f** to determine whether a Web Application Firewall (WAF) was protecting the website. The result identified **ModSecurity (SpiderLabs)**.

Finally, I used **DNSRecon** to perform DNS reconnaissance. The results provided information related to name servers, mail servers, SPF/TXT records, service records, and other available DNS information.

### 4.2 GHDB-Based Footprinting Attacks — W2-PM2

I performed footprinting activities using the **Google Hacking Database (GHDB)** and advanced Google search operators, commonly referred to as **Google dorks**. The objective was to understand how search engines can reveal publicly indexed information that may unintentionally expose files, directories, services, or Internet-accessible systems.

During this module, I used different search operators such as `intitle:`, `inurl:`, `filetype:`, and combinations of keywords to locate information indexed by search engines.

One activity involved identifying publicly accessible webcam interfaces using GHDB queries. The results demonstrated how improperly exposed or publicly indexed camera interfaces may become discoverable through search engines.

Another activity involved locating listings containing downloadable mathematics PDF documents. Search operators were used to identify publicly indexed directories and PDF resources related to mathematics.

This module demonstrated the importance of controlling search-engine indexing and preventing sensitive resources, administrative interfaces, directories, and unintended services from becoming publicly discoverable.

**Evidence:** Insert your W2-PM2 screenshots and completed tables directly below this subsection.

### 4.3 Maltego-Based Footprinting Attacks — W2-PM3

I performed footprinting and information-gathering activities using **Maltego on a Windows PC**. Maltego provides a graphical approach to collecting and correlating publicly available information about a target.

The activities involved using Maltego transforms to gather information and visualize relationships between discovered entities. Instead of presenting reconnaissance information only as command-line output, Maltego represented the collected data as interconnected entities within a graph.

This module demonstrated how information obtained from publicly available sources can be correlated to create a clearer representation of a target's digital footprint. It also showed the value of graphical link analysis during the reconnaissance phase of a security assessment.

**Evidence:** Insert the screenshots and results from your actual W2-PM3 Maltego project here.

### 4.4 theHarvester-Based Footprinting Attacks — W2-PM4

I performed reconnaissance using **theHarvester in Kali Linux**. The purpose of this module was to gather publicly available information related to the assigned target through open-source intelligence techniques.

theHarvester was used to collect information available from supported public data sources. The activity demonstrated how automated reconnaissance tools can assist in gathering and organizing information about a target during the footprinting phase.

The results obtained during the exercise were reviewed and documented as evidence. This demonstrated how publicly available information can contribute to understanding an organization's external digital footprint before more active security-testing phases are performed.

**Evidence:** Insert your actual W2-PM4 commands, output, and screenshots here.

### 4.5 Network Scanning with Zenmap

I performed network discovery on **my own local LAN** using **Zenmap**, the graphical interface for Nmap. Before scanning, I used the Windows `ipconfig` command to identify the active network configuration.

My active Wi-Fi interface had the following configuration:

- **Local IPv4 address:** `192.168.1.191`
- **Subnet mask:** `255.255.255.0`
- **Default gateway:** `192.168.1.1`
- **LAN subnet:** `192.168.1.0/24`

I then entered `192.168.1.0/24` as the target in Zenmap and selected the **Ping Scan** profile. The resulting command was:

```text
nmap -sn 192.168.1.0/24
```

The scan examined 256 IP addresses and reported **24 live hosts** on the local subnet. The results included the IP addresses of the discovered hosts and, where available, their MAC addresses and hardware vendors.

The scan identified devices from vendors including **Netgear, LG Innotek, Ring, Amazon Technologies, Intel Corporate, Night Owl SP**, and others. My own system, `192.168.1.191`, was also identified as active.

Finally, I opened the **Topology** tab in Zenmap and enabled the **Legend**. The topology provided a graphical representation of the discovered hosts and their relationship to the scanning system. I then used **Save Graphic** to preserve the topology as evidence for the project.

This activity demonstrated how host discovery can be used to understand the devices connected to an authorized local network and establish an inventory of active systems before conducting further security assessment.

**Evidence:** Place your Zenmap topology PDF/screenshot and Nmap output immediately after this subsection.

## 5. Risk Analysis / Impact

Based on the information collected during the footprinting, reconnaissance, OSINT, and network-scanning activities performed in W2-PM1 through W2-PM5, I identified the following potential security risks. These findings represent information exposure and reconnaissance observations rather than confirmed vulnerabilities.

| # | Risk / Finding | Evidence / Observation | Potential Impact | Risk Level |
|---|---|---|---|---|
| 1 | Web technology information exposed | WhatWeb identified technologies used by the target website, including WordPress and WP Download Manager. | Technology and version information may assist an attacker in identifying components that require further security investigation. | Medium |
| 2 | Server IP address identifiable | Nslookup resolved the target domain to its associated IP address. | Reveals infrastructure information that may assist further authorized reconnaissance. | Low |
| 3 | HTTP technical information exposed | Curl returned HTTP response headers and exposed information such as the `/wp-json/` endpoint. | May assist technology fingerprinting and further enumeration of publicly available web resources. | Low |
| 4 | WAF technology identifiable | Wafw00f identified ModSecurity (SpiderLabs) as the Web Application Firewall technology. | Reveals information about the target's defensive architecture that could be considered during further reconnaissance. | Low |
| 5 | DNS infrastructure information exposed | DNSRecon identified DNS, mail, TXT/SPF, name-server, and service-related information. | Public DNS information can contribute to building a broader infrastructure profile of the target. | Medium |
| 6 | Multiple live hosts visible on local network | Zenmap identified **24 live hosts on the 192.168.1.0/24 local subnet**. | Unknown or unauthorized devices may potentially be present on a network. | Medium |
| 7 | OSINT information can be correlated | Maltego demonstrated how publicly available information can be collected and represented as interconnected entities. | Correlating multiple public data sources can provide a more complete picture of an organization's digital footprint. | Medium |
| 8 | Public information can be gathered automatically | theHarvester demonstrated automated collection of publicly available information from supported data sources. | Automated OSINT collection can accelerate reconnaissance and increase visibility into an organization's external footprint. | Medium |
| 9 | Multiple devices discoverable on the local network | Zenmap identified **24 live hosts** on the `192.168.1.0/24` local subnet. | A large number of discoverable devices increases the network's visible attack surface and highlights the importance of maintaining an accurate device inventory. | Medium |
| 10 | Device vendor information exposed on LAN | Zenmap/Nmap returned MAC addresses and identified vendors for several discovered devices, including Netgear, Ring, Intel, Amazon Technologies, and others. | Vendor information may assist device fingerprinting and help identify systems that require additional authorized security assessment. | Low |

**Risk level key:** Critical | Medium | Low

The risks identified above are observations from the reconnaissance, footprinting, OSINT, and network-discovery exercises and should **not be interpreted as confirmed vulnerabilities**. The activities primarily involved passive information gathering, publicly available information analysis, and authorized host discovery. No exploitation or vulnerability validation was performed as part of these modules.

The presence of information such as an IP address, software technology, DNS record, publicly indexed resource, MAC address, or device vendor does not by itself indicate that a system is vulnerable. Further authorized security testing would be necessary to determine whether any identified information could contribute to an exploitable security weakness.

## 6. Recommendations

Based on the observations obtained during the footprinting, reconnaissance, OSINT, and network-scanning activities performed in W2-PM1 through W2-PM5, I recommend the following security improvements:

1. **Review publicly exposed technology information**  
   Organizations should regularly review information publicly available about their websites, CMS platforms, plugins, software versions, and other technologies. Unnecessary technology disclosure should be minimized where technically feasible.

2. **Keep software and web components updated**  
   CMS platforms, plugins, themes, web servers, and other software components should be regularly patched and updated according to vendor security advisories.

3. **Review HTTP headers and exposed web resources**  
   HTTP response headers, application endpoints, and other publicly accessible resources should be reviewed to determine whether unnecessary technical information is being disclosed.

4. **Review DNS records regularly**  
   DNS, MX, TXT, SPF, name-server, and service-related records should be periodically reviewed to ensure that only required and accurate information is publicly available.

5. **Properly configure and monitor the Web Application Firewall**  
   The WAF should remain properly configured, regularly updated, and monitored. Its rules should be periodically reviewed to ensure that appropriate protection remains in place.

6. **Monitor search-engine indexing and publicly accessible resources**  
   Organizations should periodically review what their domains expose through search engines. Unintentionally indexed directories, documents, administrative interfaces, or sensitive resources should be appropriately restricted or removed from public exposure.

7. **Monitor the organization's external OSINT footprint**  
   Organizations should periodically assess publicly available information about their domains and infrastructure using authorized OSINT techniques. This can help identify information that could be correlated during reconnaissance.

8. **Minimize unnecessary public information exposure**  
   Information discoverable through OSINT tools and public data sources should be reviewed to determine whether unnecessary infrastructure or organizational details can be reduced without affecting legitimate business requirements.

9. **Perform regular internal network discovery**  
   Organizations should periodically scan their own authorized networks to maintain an accurate inventory of active hosts and identify unexpected or unauthorized devices.

10. **Investigate and verify unknown devices**  
    Devices discovered during authorized network scanning that cannot be immediately identified should be investigated and verified before being considered trusted network assets.

11. **Maintain accurate network documentation**  
    Network topology, IP address assignments, device inventories, MAC addresses, and device ownership information should be documented and kept current.

12. **Perform security testing only with authorization**  
    Reconnaissance, OSINT collection, network scanning, and other security-testing activities should only be performed against systems for which explicit authorization has been obtained.

## 7. Conclusion

During Week 2 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering footprinting, reconnaissance, Open-Source Intelligence (OSINT), and network scanning through modules W2-PM1 to W2-PM5.

In **W2-PM1**, I used six Kali Linux tools—WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon—to collect publicly available information about the target domain. These activities demonstrated how domain registration information, web technologies, IP addresses, HTTP headers, Web Application Firewall information, and DNS records can contribute to the reconnaissance process.

In **W2-PM2**, I performed GHDB-based footprinting activities using advanced search operators and Google dorks. This demonstrated how search engines can reveal publicly indexed resources, documents, directories, and Internet-facing information and highlighted the importance of controlling unnecessary public exposure.

In **W2-PM3**, I used Maltego on Windows to perform graphical OSINT and footprinting activities. This module demonstrated how publicly available information can be collected, correlated, and represented through relationships between different entities, providing a broader understanding of a target's digital footprint.

In **W2-PM4**, I used theHarvester in Kali Linux to perform automated OSINT and footprinting activities. This demonstrated how information from supported public data sources can be collected efficiently and used as part of the reconnaissance process.

In **W2-PM5**, I used Zenmap to identify my local network configuration and scan the `192.168.1.0/24` subnet. The Ping Scan identified **24 live hosts**, and the results provided IP addresses, MAC addresses, vendor information, and a graphical network topology. This activity demonstrated the importance of network discovery, asset identification, and maintaining visibility of devices connected to a local network.

Overall, these exercises demonstrated that reconnaissance is a fundamental phase of cybersecurity assessment. Publicly available information and network-discovery results can provide valuable insight into an organization's external footprint and internal network environment. However, the information collected during these activities represents reconnaissance observations and should not automatically be considered evidence of exploitable vulnerabilities.

The activities also reinforced the importance of clearly documenting the methodology, tools, observations, potential risks, and appropriate security recommendations. Most importantly, I learned that footprinting, OSINT collection, reconnaissance, and network scanning must always be performed within an **authorized scope** and for legitimate educational or security-testing purposes.

## 8. Evidences Collected

### 8.1 W2-PM1 — Footprinting with Multiple Kali Tools

Evidence collected while performing authorized footprinting and reconnaissance using Kali Linux.

---

#### 8.1.1 WHOIS

WHOIS was used to retrieve publicly available domain registration information for the authorized target, including registration details, name-server information, and related domain infrastructure.

**Evidence:**

![WHOIS Evidence](screenshots/W2-PM1/WHOIS.png)

---

#### 8.1.2 WhatWeb

WhatWeb was used to identify technologies exposed by the authorized target website. The results identified WordPress 7.0.4 and WP Download Manager 3.3.58, along with other information exposed by the website.

**Evidence:**

![WhatWeb Evidence](screenshots/W2-PM1/WhatWeb.png)

---

#### 8.1.3 Nslookup

Nslookup was used to resolve the authorized target domain name to its associated IP address. The result identified the following IP address:

`192.232.216.135`

**Evidence:**

![Nslookup Evidence](screenshots/W2-PM1/Nslookup.png)

---

#### 8.1.4 Curl

Curl was used with the `-I` option to inspect the HTTP response headers returned by the authorized target website. The results provided additional information about the web application and exposed a reference to the WordPress REST API endpoint `/wp-json/`.

**Command:**

```bash
curl -I https://networkwalks.com
```

**Evidence:**

![Curl Evidence](screenshots/W2-PM1/Curl%20(curl%20-I).png)

---

#### 8.1.5 WafW00f

WafW00f was used to determine whether a Web Application Firewall (WAF) was protecting the authorized target website. The result identified ModSecurity (SpiderLabs) as the Web Application Firewall technology.

**Evidence:**

![WafW00f Evidence](screenshots/W2-PM1/WafW00f.png)

---

#### 8.1.6 DNSRecon

DNSRecon was used to perform DNS reconnaissance against the authorized target. The results provided information related to name servers, mail servers, SPF/TXT records, service records, and other available DNS information.

**Evidence:**

![DNSRecon Evidence](screenshots/W2-PM1/DNSRecon.png)

---

#### 8.1.7 Problems Encountered & Solutions

During W2-PM1, I encountered network and DNS resolution problems while attempting to use the reconnaissance tools from Kali Linux.

**Problem Encountered**

The WHOIS command initially failed and returned the following error:

```text
getaddrinfo(whois.verisign-grs.com): Temporary failure in name resolution
```

The problem indicated that Kali Linux was unable to properly resolve the WHOIS server hostname. Additional connectivity and DNS tests were performed to determine whether the issue was related to Internet connectivity, DNS configuration, or the virtual machine network configuration.

**Solution**

The network configuration of the Kali Linux virtual machine was reviewed and corrected. The VirtualBox network adapter was configured using the required NAT Network configuration.

After correcting the network configuration, Kali Linux received the appropriate network settings, including:

```text
IP Address:      10.0.2.3/24
Default Gateway: 10.0.2.1
```

Connectivity and DNS resolution were tested again. Once Internet connectivity and DNS name resolution were restored, the WHOIS command successfully connected to the remote WHOIS service and returned the publicly available registration information for the authorized target.

The remaining footprinting tools — WhatWeb, Nslookup, Curl, WafW00f, and DNSRecon — could then be executed successfully as part of the authorized reconnaissance exercise.

**Problems Encountered & Solutions Evidence:**

The following screenshots document the problems encountered during the W2-PM1 practical exercise, the troubleshooting process performed, and the solutions applied.

![Problem Encountered and Solution 1](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions.png?raw=1)

![Problem Encountered and Solution 2](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(2).png)

![Problem Encountered and Solution 3](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(3).png)

![Problem Encountered and Solution 4](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(4).png)

![Problem Encountered and Solution 5](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(5).png)

![Problem Encountered and Solution 6](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(6).png)

![Problem Encountered and Solution 7](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(7).png)

![Problem Encountered and Solution 8](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(8).png)

![Problem Encountered and Solution 9](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(9).png)

![Problem Encountered and Solution 10](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(10).png)

![Problem Encountered and Solution 11](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(11).png)

![Problem Encountered and Solution 12](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(12).png)

![Problem Encountered and Solution 13](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(13).png)

![Problem Encountered and Solution 14](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(14).png)

![Problem Encountered and Solution 15](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(15).png)

![Problem Encountered and Solution 16](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(16).png)

![Problem Encountered and Solution 17](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(17).png)

![Problem Encountered and Solution 18](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(18).png)

![Problem Encountered and Solution 19](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(19).png)

![Problem Encountered and Solution 20](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(20).png)

![Problem Encountered and Solution 21](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(21).png)

![Problem Encountered and Solution 22](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(22).png)

![Problem Encountered and Solution 23](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(23).png)

![Problem Encountered and Solution 24](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(24).png)

![Problem Encountered and Solution 25](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(25).png)

![Problem Encountered and Solution 26](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(26).png)

![Problem Encountered and Solution 27](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(27).png)

![Problem Encountered and Solution 28](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(28).png)

![Problem Encountered and Solution 29](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(29).png)

![Problem Encountered and Solution 30](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(30).png)

![Problem Encountered and Solution 31](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(31).png)

![Problem Encountered and Solution 32](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(32).png)

![Problem Encountered and Solution 33](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(33).png)

![Problem Encountered and Solution 34](screenshots/W2-PM1/Problems%20Encountered%20%26%20Solutions%20(34).png)
---
### Saved Command Outputs

In addition to the screenshot evidence, the raw outputs generated during the W2-PM1 footprinting activities were preserved as text files.

| Tool | Saved Output |
|---|---|
| WHOIS | [View WHOIS Output](outputs/W2-PM1/whois-networkwalks.txt) |
| WhatWeb | [View WhatWeb Output](outputs/W2-PM1/whatweb-networkwalks.txt) |
| Nslookup | [View Nslookup Output](outputs/W2-PM1/nslookup-networkwalks.txt) |
| cURL | [View cURL Header Output](outputs/W2-PM1/curl-networkwalks.txt) |
| WafW00f | [View WafW00f Output](outputs/W2-PM1/wafw00f-networkwalks.txt) |
| DNSRecon | [View DNSRecon Output](outputs/W2-PM1/dnsrecon-networkwalks.txt) |

The saved outputs provide the raw command-line evidence corresponding to the reconnaissance activities documented in the screenshots.
---

## 8.2 W2-PM2 — GHDB-Based Footprinting Attacks

This practical module focused on Google Hacking Database (GHDB) techniques and advanced Google search operators for passive information gathering and footprinting.

The activities involved identifying publicly indexed information using Google dorks and documenting the results obtained during the exercise.

> **Ethical Use Notice:**  
> The activities documented in this section were performed strictly for educational and cybersecurity training purposes. Publicly indexed resources were observed only. No authentication bypass, credential guessing, exploitation, configuration changes, or unauthorized modification was performed.

---

### Objective

The objective of this practical module was to:

- Explore the Exploit Database and Google Hacking Database.
- Understand the purpose of Google dorks.
- Use advanced Google search operators for passive footprinting.
- Identify publicly indexed webcam interfaces.
- Identify publicly indexed directories containing mathematics PDF resources.
- Document the search queries and results obtained during the exercise.

---

## Task 1 — Publicly Accessible Security Camera Listings

The first task required finding **10 live security-camera links exposed and accessible from the Internet** and recording the relevant Google dork used to identify each result.

No usernames or passwords were used during this exercise.

---

### Step 1 — Access the Exploit Database

The Exploit Database was accessed to begin exploring publicly available security research resources.

![Exploit Database](screenshots/W2-PM2/01-Exploit-Database.png)

---

### Step 2 — Access the Google Hacking Database

The Google Hacking Database (GHDB) section of Exploit Database was opened.

GHDB contains search queries that demonstrate how advanced Google search operators can locate publicly indexed information.

![Google Hacking Database](screenshots/W2-PM2/02-Google-Hacking-Database.png)

---

### Step 3 — Locate a Webcam-Related Google Dork

The GHDB listings were reviewed for queries related to webcams and Internet-accessible camera interfaces.

A webcamXP-related query was identified for the exercise.

![GHDB Webcam Dork Selection](screenshots/W2-PM2/03-GHDB-Webcam-Dork-Selection.png)

One of the identified queries was:

```text
intitle:"webcamXP" inurl:8080
```

Additional queries used during the task included:

```text
intitle:"webcam 7" inurl:'/gallery.html'
```

```text
intitle:webcam 7 inurl:8080 -intext:8080
```

```text
intitle:"webcamxp" "Flash JPEG Stream"
```

---

### Step 4 — Search Google Using the Webcam Dork

The selected GHDB query was copied and used as a Google search query.

![GHDB Webcam Dork Google Search](screenshots/W2-PM2/04-GHDB-Webcam-Dork-Google-Search.png)

---

### Step 5 — Execute the Webcam Search Query

The webcam-related Google dork was entered into Google Search to identify publicly indexed webcamXP interfaces.

![Google Webcam Dork Query](screenshots/W2-PM2/05-Google-Webcam-Dork-Query.png)

---

### Step 6 — Review the Search Results

Google returned publicly indexed results matching the webcam-related search operators.

The results were manually reviewed as part of the passive footprinting exercise.

![Google Webcam Dork Results](screenshots/W2-PM2/06-Google-Webcam-Dork-Results.png)

The same search and verification process was repeated using the relevant Google dorks until the required **10 listings** were identified.

---

### Task 1 Results

| No. | Link | Relevant Dork | Username / Password |
|---:|---|---|---|
| 1 | `http://109.233.191.130:8080/` | `intitle:"webcamXP" inurl:8080` | --- |
| 2 | `http://109.206.96.249:8080/` | `intitle:"webcam 7" inurl:'/gallery.html'` | --- |
| 3 | `http://68.115.218.130:32479/` | `intitle:"webcam 7" inurl:'/gallery.html'` | --- |
| 4 | `http://72.199.200.5:8080/` | `intitle:"webcamXP" inurl:8080` | --- |
| 5 | `http://139.64.168.120:8080/` | `intitle:"webcamXP" inurl:8080` | --- |
| 6 | `http://85.93.53.175:8080/` | `intitle:"webcamXP" inurl:8080` | --- |
| 7 | `http://75.149.26.30:1024/` | `intitle:"webcamXP" inurl:8080` | --- |
| 8 | `http://109.206.96.75:8080/` | `intitle:webcam 7 inurl:8080 -intext:8080` | --- |
| 9 | `http://178.71.15.232:8080/` | `intitle:"webcamxp" "Flash JPEG Stream"` | --- |
| 10 | `http://91.3.84.143:8080/` | `intitle:"webcamxp" "Flash JPEG Stream"` | --- |

**Task 1 Result:** 10/10 required listings were documented.

---

## Task 2 — Mathematics PDF Listings

The second task required finding **10 listings containing downloadable mathematics ebooks in PDF format**.

The Google dork used during the exercise was:

```text
intitle:index.of "parent directory" mathematics pdf
```

---

### Step 7 — Search for Mathematics PDF Directories

The Google dork was entered into Google Search to identify publicly indexed directories containing mathematics-related PDF resources.

![Task 2 Mathematics PDF Google Search](screenshots/W2-PM2/07-Task2-Mathematics-PDF-Google-Search.png)

The returned results were manually reviewed, and the same process was repeated until the required **10 listings** were documented.

---

### Task 2 Results

| No. | Link | Relevant Dork | Username / Password |
|---:|---|---|---|
| 1 | `http://erewhon.superkuh.com/library/Math/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 2 | `https://ochicken.net/library/Mathematics/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 3 | `https://www.unm.edu/~megrad/Math/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 4 | `https://math.dartmouth.edu/~carlp/PDF/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 5 | `https://www.netlib.org/math/docpdf/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 6 | `https://education.giakonda.org.uk/Maths/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 7 | `https://docs.bartonccc.edu/syllabus/Master/MATH/?C=S;O=A` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 8 | `https://maths.nuigalway.ie/~rquinlan/linearalgebra/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 9 | `https://sajapuriacollege.ac.in/pdf/pdf/MATHEMATICS/` | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 10 | `https://www.pndascollege.in/pdf/academic-calendar/mathematics/` | `intitle:index.of "parent directory" mathematics pdf` | --- |

**Task 2 Result:** 10/10 required mathematics PDF listings were documented.

---

## Key Observations

This practical exercise demonstrated how search-engine indexing can unintentionally expose information and Internet-facing services.

The main concepts demonstrated were:

- Google Hacking Database reconnaissance.
- Advanced Google search operators.
- `intitle:` filtering.
- `inurl:` filtering.
- `intext:` filtering.
- Directory-index discovery.
- Passive information gathering.
- Publicly indexed service discovery.
- OSINT-oriented footprinting.
- Security implications of Internet-exposed resources.

---

## Security Considerations

The exercise demonstrates the importance of properly securing Internet-facing systems and controlling which resources are indexed by search engines.

Administrators should:

- Avoid exposing unnecessary services directly to the Internet.
- Require authentication for sensitive interfaces.
- Disable directory listing where it is not required.
- Apply appropriate firewall and access-control rules.
- Keep Internet-facing applications and devices updated.
- Review publicly indexed information associated with organizational infrastructure.
- Prevent sensitive files and administrative interfaces from being indexed by search engines.

---

## Completion Status

| Task | Requirement | Status |
|---|---|---|
| Task 1 | Find 10 publicly accessible security-camera listings | ✅ 10/10 |
| Task 2 | Find 10 mathematics PDF listings | ✅ 10/10 |

**W2-PM2 — GHDB-Based Footprinting Attacks: Completed ✅**
---

### 8.3 W2-PM3 — Maltego-Based Footprinting Attacks

Evidence collected while performing footprinting and OSINT activities using Maltego Graph on a Windows PC.

#### Objective

The objective of this practical module was to install and configure Maltego Graph and use its OSINT capabilities to gather publicly available information associated with the authorized training domain `networkwalks.com`.

---

#### Step 1 — Access the Official Maltego Website

The official Maltego website was accessed to obtain Maltego Graph for Windows.

![Maltego Official Website](screenshots/W2-PM3/01-Maltego-Official-Website.png)

The Maltego download page was then opened.

![Maltego Download Menu](screenshots/W2-PM3/02-Maltego-Download-Menu.png)

---

#### Step 2 — Download Maltego Graph for Windows

Maltego Graph for Windows was selected from the official download page.

![Maltego Graph Windows Download](screenshots/W2-PM3/03-Maltego-Graph-Windows-Download.png)

The Windows installer was downloaded successfully.

![Maltego Installer Downloaded](screenshots/W2-PM3/04-Maltego-Installer-Downloaded.png)

---

#### Step 3 — Run the Maltego Installer

The downloaded Maltego installer was executed with administrator privileges.

![Maltego Run as Administrator](screenshots/W2-PM3/05-Maltego-Run-as-Administrator.png)

---

#### Step 4 — Install Java Runtime Environment 17

The Maltego setup required Java Runtime Environment 17. The JRE installation process was started as instructed.

![Maltego JRE17 Prerequisite](screenshots/W2-PM3/06-Maltego-JRE17-Prerequisite-Instructions.png)

The Eclipse Temurin JRE 17 installation was initiated.

![JRE17 Installation](screenshots/W2-PM3/07-JRE17-Installation-Instructions.png)

The Java Runtime Environment installation completed successfully.

![JRE17 Installation Completed](screenshots/W2-PM3/08-JRE17-Installation-Completed.png)

---

#### Step 5 — Complete Maltego Installation

After installing the required Java Runtime Environment, the Maltego installation continued.

![Maltego Installation Progress](screenshots/W2-PM3/09-Maltego-Installation-In-Progress.png)

After installation, Maltego was launched with administrator privileges.

![Maltego Run as Administrator Desktop](screenshots/W2-PM3/10-Maltego-Run-as-Administrator-Desktop.png)

---

#### Step 6 — Configure Maltego

Maltego Graph was launched and the Maltego ID activation option was selected.

![Maltego Activation Options](screenshots/W2-PM3/11-Maltego-Activation-Options.png)

The license agreement was reviewed and accepted.

![Maltego License Agreement](screenshots/W2-PM3/12-Maltego-License-Agreement-Accepted.png)

The browser login option was then used to authenticate the Maltego account.

![Maltego Browser Login Option](screenshots/W2-PM3/13-Maltego-Browser-Login-Option.png)

---

#### Step 7 — Authenticate the Maltego Account

The Maltego authentication page was opened in the browser.

> **Privacy Note:** Personal account information should be redacted before this screenshot is published in a public repository.

![Maltego Login Page](screenshots/W2-PM3/14-Maltego-Login-Page.png)

Authentication completed successfully.

![Maltego Authentication Complete](screenshots/W2-PM3/15-Maltego-Authentication-Complete.png)

The Maltego desktop client confirmed that the browser login was successful.

![Maltego Browser Login Successful](screenshots/W2-PM3/16-Maltego-Browser-Login-Successful.png)

---

#### Step 8 — Configure Maltego Data Sources

The required data sources were selected during the initial Maltego configuration.

![Maltego Select Data Sources](screenshots/W2-PM3/17-Maltego-Select-Data-Sources.png)

The configuration process completed successfully and Maltego became ready for use.

![Maltego Configuration Ready](screenshots/W2-PM3/18-Maltego-Configuration-Ready.png)

---

#### Step 9 — Create the Target Domain Entity

A new Maltego graph was created for the footprinting exercise.

![Maltego New Domain Graph](screenshots/W2-PM3/19-Maltego-New-Domain-Graph.png)

The Domain entity was configured with the authorized training target:

`networkwalks.com`

![NetworkWalks Domain Configured](screenshots/W2-PM3/20-NetworkWalks-Domain-Configured.png)

---

#### Step 10 — Search for Email Transforms

The available Maltego transforms were searched for email-related OSINT capabilities.

The Utilities transform used during the investigation was:

`To Emails @domain [Search Engine]`

![Maltego Email Transforms](screenshots/W2-PM3/21-Maltego-Email-Transforms.png)

---

#### Step 11 — Execute the Email Transform

The selected transform was executed against the `networkwalks.com` Domain entity.

The transform returned the following publicly discoverable email address:

`info@networkwalks.com`

![NetworkWalks Email Transform Result](screenshots/W2-PM3/22-NetworkWalks-Email-Transform-Result.png)

---

#### Step 12 — Verify the Final Result

The completed graph displayed the relationship between the target domain and the email address returned by the Maltego transform:

```text
networkwalks.com
       |
       v
info@networkwalks.com
```

## 8.4 W2-PM4 — theHarvester-Based Footprinting Attacks

### Objective

The objective of this practical module was to perform passive footprinting and Open-Source Intelligence (OSINT) reconnaissance using **theHarvester** on Kali Linux.

theHarvester is an OSINT reconnaissance tool that can collect publicly available information associated with a target domain from multiple search engines, APIs, and external data sources.

During this practical activity, theHarvester was launched and examined, a targeted Baidu reconnaissance scan was performed, and a broader multi-source scan was executed. The activity also demonstrated how some external OSINT sources require API keys before they can be queried successfully.

> **Ethical Use Notice:** This practical activity was performed strictly for authorized educational and cybersecurity training purposes. The activity was limited to passive OSINT collection of publicly available information. No exploitation, unauthorized access, credential attacks, or modification of external systems was performed.

---

### Step 1 — Launch theHarvester

theHarvester was located from the Kali Linux application menu and launched in the Kali Linux virtual machine.

This confirmed that the reconnaissance tool was available in the environment and ready for use.

![theHarvester Application](screenshots/W2-PM4/01-theHarvester-Application.png)

---

### Step 2 — Review theHarvester Help Options

Before performing reconnaissance, the available theHarvester options were reviewed.

The help output provides information about parameters such as:

- Target domain
- Search result limit
- Data source selection
- DNS-related options
- Screenshots
- Output files
- Wordlists
- API scanning
- Supported OSINT sources

![theHarvester Help Options](screenshots/W2-PM4/02-theHarvester-Help-Options.png)

---

### Step 3 — Execute theHarvester Help Command

The following command was executed to display theHarvester's command-line help:

```bash
theHarvester -h
```

The command displayed the available syntax and parameters supported by the installed version of theHarvester.

The help information was reviewed before beginning the reconnaissance activity to ensure that the correct command syntax and data-source parameters were used.

![theHarvester Help Command](screenshots/W2-PM4/03-theHarvester-Help-Command.png)

---

### Step 4 — Perform a Baidu-Based Reconnaissance Scan

A targeted reconnaissance scan was performed against the assigned public domain using the **Baidu** data source.

The following command was executed:

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

Command explanation:

- `theHarvester` — launches the reconnaissance tool.
- `-d microsoft.com` — specifies `microsoft.com` as the target domain.
- `-l 1000` — specifies the maximum number of search results.
- `-b baidu` — instructs theHarvester to use Baidu as the search source.

The tool then began searching the selected source for publicly available information associated with the target domain.

![theHarvester Baidu Scan](screenshots/W2-PM4/04-theHarvester-Baidu-Scan.png)

---

### Step 5 — Review the Baidu Reconnaissance Results

The Baidu-based reconnaissance scan completed and returned publicly available information associated with the target domain.

The captured results showed:

```text
Target: microsoft.com
Source: Baidu
IPs found: 0
Emails found: 1
People found: 0
Hosts found: 2
```

The email address displayed by the tool was:

```text
viva-noreply@microsoft.com
```

The hosts displayed in the results were:

```text
hxd.research.microsoft.com
officedn.microsoft.com
```

These findings demonstrated how passive OSINT reconnaissance can identify publicly exposed domain-related information without exploiting or gaining unauthorized access to the target infrastructure.

![theHarvester Baidu Results](screenshots/W2-PM4/05-theHarvester-Baidu-Results.png)

---

### Step 6 — Open a New Terminal

After completing the targeted Baidu reconnaissance activity, a new Kali Linux terminal session was opened.

The new terminal was used to perform a broader reconnaissance scan involving multiple available theHarvester sources.

![theHarvester New Terminal](screenshots/W2-PM4/06-theHarvester-New-Terminal.png)

---

### Step 7 — Execute an All-Sources Reconnaissance Scan

A broader reconnaissance scan was initiated using the following command:

```bash
theHarvester -d microsoft.com -l 50 -b all
```

Command explanation:

- `theHarvester` — launches the OSINT reconnaissance tool.
- `-d microsoft.com` — defines the target domain.
- `-l 50` — limits the number of results.
- `-b all` — instructs theHarvester to attempt reconnaissance using its available sources.

This command allowed the behavior of multiple OSINT providers to be observed during a single reconnaissance operation.

![theHarvester All Sources Scan](screenshots/W2-PM4/07-theHarvester-All-Sources-Scan.png)

---

### Step 8 — Observe Initial API-Key Errors

During the all-sources scan, theHarvester attempted to access several external reconnaissance services.

Some services could not be queried because their API keys were not configured.

The output displayed messages indicating missing API keys or failed searches for some providers.

This demonstrated an important limitation of the `-b all` option: although theHarvester supports many external sources, some of them require separate credentials or API keys.

![theHarvester API Key Errors 01](screenshots/W2-PM4/08-theHarvester-API-Key-Errors-01.png)

---

### Step 9 — Continue Reviewing API-Key Requirements

The reconnaissance operation continued processing additional sources.

More API-dependent services displayed missing-key or configuration messages.

Examples visible during the broader scan included services such as:

- Bevigil
- Bitbucket
- BuiltWith
- Brave Search
- Censys
- Criminal IP
- Dehashed
- DNSDumpster

These messages did not indicate a failure of theHarvester itself. Instead, they showed that individual external providers required credentials that were not configured in the local environment.

![theHarvester API Key Errors 02](screenshots/W2-PM4/09-theHarvester-API-Key-Errors-02.png)

---

### Step 10 — Continue Processing External Sources

theHarvester continued attempting to query additional supported OSINT services.

Additional API-dependent sources were encountered, including services such as:

- FullHunt
- GitHub
- GitHub Code
- Have I Been Pwned
- Hunter
- HunterHow
- IntelX
- Netlas

The output demonstrated that theHarvester can integrate with many external reconnaissance services, but full functionality requires appropriate API configuration for providers that do not permit anonymous queries.

![theHarvester API Key Errors 03](screenshots/W2-PM4/10-theHarvester-API-Key-Errors-03.png)

---

### Step 11 — Review Additional Source Requirements

The all-sources scan continued through further OSINT providers.

Additional API requirements were displayed for sources such as:

- Onyphe
- PentestTools
- ProjectDiscovery
- RocketReach
- SecurityScorecard
- SecurityTrails
- Shodan
- Tomba
- Venacus
- VirusTotal
- WhoisXML
- ZoomEye

Although some sources were unavailable because credentials were missing, theHarvester continued processing other sources that were accessible.

![theHarvester API Key Errors 04](screenshots/W2-PM4/11-theHarvester-API-Key-Errors-04.png)

---

### Step 12 — Monitor the Multi-Source Search Progress

The reconnaissance scan continued after processing the API-dependent providers.

The terminal showed theHarvester moving through multiple search sources and attempting to retrieve publicly available information associated with the target domain.

This demonstrated the automated multi-source reconnaissance capabilities provided by theHarvester.

![theHarvester Search Progress](screenshots/W2-PM4/12-theHarvester-Search-Progress.png)

---

### Step 13 — Review Hudson Rock Results

During the broader reconnaissance scan, **Hudson Rock** successfully processed information associated with the target domain.

The captured terminal output showed Hudson Rock processing the target and extracting host-related information.

The screenshot also demonstrated that theHarvester continued moving to additional sources after processing the Hudson Rock results.

![theHarvester HudsonRock Results](screenshots/W2-PM4/13-theHarvester-HudsonRock-Results.png)

---

### Step 14 — Review Additional Search Results

After the Hudson Rock stage, theHarvester continued searching additional available OSINT sources.

The scan demonstrated that a single theHarvester operation can cycle through numerous reconnaissance providers and aggregate information where those providers are accessible.

Some sources produced results, while others generated errors because of unavailable API credentials or provider-specific restrictions.

![theHarvester Additional Search Results](screenshots/W2-PM4/14-theHarvester-Additional-Search-Results.png)

---

### Step 15 — Review the Final Reconnaissance Results

The final stage of the multi-source reconnaissance operation was reviewed.

The complete exercise demonstrated several important aspects of OSINT-based footprinting:

- Using Kali Linux for passive reconnaissance.
- Launching and operating theHarvester.
- Reviewing command-line parameters.
- Selecting a specific reconnaissance source.
- Performing domain-based reconnaissance.
- Discovering publicly available email information.
- Discovering publicly available host information.
- Running a broader multi-source reconnaissance operation.
- Understanding API-key requirements.
- Identifying unavailable external sources.
- Monitoring reconnaissance progress.
- Reviewing information returned by accessible OSINT sources.
- Documenting the reconnaissance workflow through screenshots.

![theHarvester Final Results](screenshots/W2-PM4/15-theHarvester-Final-Results.png)

---

### Commands Used

The primary commands used during W2-PM4 were:

```bash
theHarvester -h
```

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

```bash
theHarvester -d microsoft.com -l 50 -b all
```

---

### Key Findings

The targeted Baidu reconnaissance scan successfully returned publicly available information associated with the selected domain.

The captured output included:

```text
Emails found: 1
Hosts found: 2
IPs found: 0
People found: 0
```

The broader `-b all` reconnaissance scan demonstrated that theHarvester supports numerous external OSINT providers. However, many of these providers require API credentials before their data can be accessed.

This highlighted the difference between freely accessible reconnaissance sources and API-dependent intelligence providers.

---
### Saved Command Outputs

In addition to the screenshot evidence, the raw command-line outputs generated during the W2-PM4 theHarvester activities were preserved as text files.

| Activity | Saved Output |
|---|---|
| Baidu Reconnaissance Scan | [View Baidu Output](outputs/W2-PM4/theHarvester-baidu.txt) |
| Multi-Source Reconnaissance Scan | [View All-Sources Output](outputs/W2-PM4/theHarvester-microsoft-all.txt) |

The saved outputs provide the raw command-line evidence corresponding to the theHarvester reconnaissance activities documented in the screenshots.
---
### Skills Practiced

This practical module provided hands-on experience with:

- Open-Source Intelligence (OSINT)
- Passive reconnaissance
- Domain footprinting
- Email discovery
- Host discovery
- Kali Linux
- Linux terminal commands
- theHarvester
- Search-source selection
- Multi-source reconnaissance
- API-dependent OSINT services
- Reconnaissance result analysis
- Cybersecurity documentation

---

### W2-PM4 Result

**W2-PM4 — theHarvester-Based Footprinting Attacks was completed successfully.**

The activity demonstrated how theHarvester can be used during the reconnaissance and footprinting phase of a cybersecurity assessment to collect publicly available information associated with a target domain.

A targeted Baidu search successfully returned publicly available email and host information. A broader all-sources scan was then used to demonstrate multi-source OSINT reconnaissance and the API-key requirements associated with several external intelligence providers.

The exercise remained within passive OSINT and educational cybersecurity activities. No exploitation, unauthorized system access, credential attacks, or modification of the target infrastructure was performed.

---

## 8.5 W2-PM5 — Zenmap-Based Network Scanning

Evidence collected while performing authorized network discovery on my own local LAN using Zenmap on a Windows PC.

> **Scope:** All network discovery and scanning documented in this section was performed against my own local network for educational and authorized cybersecurity practice.

---

### Step 1 — Access the Official Zenmap Website

The official Nmap website was accessed to obtain Zenmap, the graphical user interface for Nmap.

![Zenmap Official Website](screenshots/W2-PM5/01-Zenmap-Official-Website.png)

---

### Step 2 — Open the Zenmap Download Page

The official download page was opened to locate the appropriate Nmap/Zenmap installer for Windows.

![Zenmap Download Page](screenshots/W2-PM5/02-Zenmap-Download-Page.png)

---

### Step 3 — Launch the Zenmap Installer

The downloaded Nmap/Zenmap installer was launched on the Windows system.

![Zenmap Installer Launch](screenshots/W2-PM5/03-Zenmap-Installer-Launch.png)

---

### Step 4 — Configure the Installation

The installation setup was reviewed and configured before proceeding with the installation.

![Zenmap Installation Setup](screenshots/W2-PM5/04-Zenmap-Installation-Setup.png)

---

### Step 5 — Monitor Installation Progress

The installer began copying and configuring the required Nmap and Zenmap components.

![Zenmap Installation Progress](screenshots/W2-PM5/05-Zenmap-Installation-Progress.png)

---

### Step 6 — Complete the Installation

The installation process completed successfully.

![Zenmap Installation Complete](screenshots/W2-PM5/06-Zenmap-Installation-Complete.png)

---

### Step 7 — Review Zenmap Setup Configuration

The final setup configuration was reviewed to ensure Zenmap and its associated Nmap components were installed correctly.

![Zenmap Setup Configuration](screenshots/W2-PM5/07-Zenmap-Setup-Configuration.png)

---

### Step 8 — Finalize Zenmap Configuration

The remaining configuration process was allowed to complete.

![Zenmap Configuration Progress](screenshots/W2-PM5/08-Zenmap-Configuration-Progress.png)

---

### Step 9 — Verify Installation Completion

The installer confirmed that the Zenmap/Nmap installation process had finished.

![Zenmap Installation Finished](screenshots/W2-PM5/09-Zenmap-Installation-Finished.png)

---

### Step 10 — Launch Zenmap

Zenmap was launched successfully on the Windows system.

![Zenmap Application Launch](screenshots/W2-PM5/10-Zenmap-Application-Launch.png)

---

### Step 11 — Check the Local Network Configuration

Before scanning, the Windows network configuration was checked to identify the active network interface and local IPv4 configuration.

![Network Configuration Check](screenshots/W2-PM5/11-Network-Configuration-Check.png)

---

### Step 12 — Identify the Local IP Configuration

The local IP configuration was examined to determine the system's IPv4 address and the network information required to define the authorized scanning scope.

![Network IP Configuration](screenshots/W2-PM5/12-Network-IP-Configuration.png)

---

### Step 13 — Configure the Authorized Target

The appropriate local network target was entered into Zenmap based on the identified LAN configuration.

Only the authorized local network was used as the scan target.

![Zenmap Target Configuration](screenshots/W2-PM5/13-Zenmap-Target-Configuration.png)

---

### Step 14 — Configure the Zenmap Scan

The Zenmap scan profile and target were reviewed before starting network discovery.

![Zenmap Scan Configuration](screenshots/W2-PM5/14-Zenmap-Scan-Configuration.png)

---

### Step 15 — Execute the Network Scan

The configured scan was executed against the authorized local network.

Zenmap used Nmap to perform network discovery and return information about reachable hosts and discovered network services.

![Zenmap Scan Results](screenshots/W2-PM5/15-Zenmap-Scan-Results.png)

---

### Step 16 — Review Host Discovery Results

The discovered hosts were reviewed through the Zenmap interface.

This stage demonstrated how Nmap-based network discovery can identify systems that respond within an authorized network scope.

![Zenmap Host Discovery](screenshots/W2-PM5/16-Zenmap-Host-Discovery.png)

---

### Step 17 — Review the Nmap Output

The raw Nmap output generated by Zenmap was reviewed for additional information about the scan and discovered hosts.

![Zenmap Nmap Output](screenshots/W2-PM5/17-Zenmap-Nmap-Output.png)

---

### Step 18 — Analyze the Network Topology

Zenmap's topology visualization was used to inspect the discovered network structure graphically.

The topology view provides a visual representation of discovered hosts and their relationship to the scanning system.

![Zenmap Network Topology](screenshots/W2-PM5/18-Zenmap-Network-Topology.png)

---

### Step 19 — Verify the Scan from the Terminal

The network discovery process was additionally verified through Nmap from the command line.

This demonstrated the relationship between Zenmap as the graphical frontend and Nmap as the underlying network scanning engine.

![Nmap Terminal Verification](screenshots/W2-PM5/19-Nmap-Terminal-Verification.png)

---

### Step 20 — Review the Topology Results

The resulting network topology was reviewed after completing the discovery process.

This provided another visual method for analyzing the hosts discovered during the authorized local network scan.

![Zenmap Topology Results](screenshots/W2-PM5/20-Zenmap-Topology-Results.png)

---

### Step 21 — Final Network Topology

The final Zenmap topology view was captured as evidence of the completed network discovery exercise.

![Zenmap Final Network Topology](screenshots/W2-PM5/21-Zenmap-Final-Network-Topology.png)

---

### W2-PM5 Skills Practiced

- Zenmap installation and configuration
- Nmap fundamentals
- Local network identification
- IPv4 network configuration analysis
- Authorized network scanning
- Network discovery
- Host discovery
- Nmap output analysis
- Zenmap scan profiles
- Network topology visualization
- Command-line verification
- Cybersecurity reconnaissance fundamentals
- Network enumeration
- Cybersecurity documentation

---

### W2-PM5 Result

**W2-PM5 — Zenmap-Based Network Scanning was completed successfully.**

Zenmap and Nmap were installed and configured on the Windows environment, after which the local network configuration was examined to establish the authorized scanning scope.

The exercise demonstrated how Zenmap can provide a graphical interface for Nmap-based network discovery, host identification, scan-result analysis, and network topology visualization. The underlying Nmap output was also reviewed and command-line verification was performed to reinforce the relationship between Zenmap and Nmap.

All network scanning documented in this activity was performed against my own authorized local network for educational cybersecurity purposes. No unauthorized external systems were targeted.

---

## 👤 Report Prepared By

**Georges Khoury**  
Cybersecurity & Ethical Hacking Intern  
**Batch:** B082 – NetworkWalks

## 👤 Instructor / Original Template Author

**Waqas Karim CCIE**  
Cybersecurity Professional B082

## 📌 Project Information

- **Program Name:** Cybersecurity Program at NetworkWalks
- **Week:** 02
- **Final Project:** W2-PM-FINAL – Penetration Testing Report
- **Modules Completed:** W2-PM1, W2-PM2, W2-PM3, W2-PM4, W2-PM5
- **Phases Covered:** Reconnaissance, Footprinting, OSINT & Network Scanning
- **Date:** 19 August 2026
- **Repository:** GitHub

---

**-End-**
