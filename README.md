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

Evidence collected while performing authorized footprinting and
reconnaissance using Kali Linux.

<!-- PM1 screenshots will be inserted here -->

### 8.2 W2-PM2 — GHDB-Based Footprinting Attacks

Evidence collected while performing the assigned GHDB-based
footprinting activities using Google search operators.

<!-- PM2 screenshots will be inserted here -->

### 8.3 W2-PM3 — Maltego-Based Footprinting Attacks

Evidence collected while performing footprinting and OSINT activities
using Maltego on a Windows PC.

<!-- PM3 screenshots will be inserted here -->

### 8.4 W2-PM4 — theHarvester-Based Footprinting Attacks

Evidence collected while performing OSINT-based reconnaissance using
theHarvester on Kali Linux.

<!-- PM4 screenshots will be inserted here -->

### 8.5 W2-PM5 — Zenmap-Based Network Scanning

Evidence collected while performing authorized network discovery on
my own local LAN using Zenmap on a Windows PC.

<!-- PM5 screenshots will be inserted here -->

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
