# FOOTPRINTING & NETWORK SCANNING

## INTRODUCTION
Reconnaissance, also known as footprinting, is the first stage of any cybersecurity assessment or real-world attack. During this phase, an attacker gathers as much publicly available information as possible about a target before attempting any direct interaction. This information may include domain ownership details, IP addresses, hosting providers, DNS records, email servers, web technologies, and security mechanisms such as firewalls. Since these details are collected from publicly accessible sources, the target organization is often unaware that it is being investigated, making reconnaissance one of the most effective and difficult-to-detect phases of an attack.

After information gathering, attackers typically move to the scanning phase, where they identify active hosts, open ports, services, and potential network entry points. One of the most widely used tools for this purpose is Nmap (Network Mapper). On Windows systems, Nmap is commonly accessed through Zenmap, its official graphical user interface (GUI). Zenmap is a free, open-source, and cross-platform security scanning tool that simplifies network discovery for beginners while providing advanced functionality for experienced cybersecurity professionals and penetration testers. It allows users to perform various network scans, save frequently used scan profiles, and visualize network information effectively.

This report demonstrates both phases of the security assessment process. The footprinting component focuses on gathering intelligence about the networkwalks.com domain using various Kali Linux reconnaissance tools, while the scanning component examines a local network using Zenmap. Together, these activities illustrate how a potential attacker progresses from collecting publicly available information about a target to identifying and mapping live systems within a network environment. For each task, the report includes the commands executed, the observed results, supporting screenshots, and a brief explanation of the significance of each finding from an attacker's perspective.

## What I did

<h4>Footprinting</h4>
<p>
In this lab, I footprinted the live website <b>networkwalks.com</b> using six built‑in Kali Linux tools. Each tool revealed a different piece of information about the target, and together they helped me build a full profile of it.

<ul>
<li>Whois:</li> I ran a whois lookup and I gathered the domain registration details, including registrar information and contact data.

<li>WhatWeb:</li> I used WhatWeb to identify the technologies running on the site, such as the web server, frameworks, and CMS.

<li>Nslookup:</li> I performed nslookup queries to resolve the domain name into IP addresses and to check DNS records.

<li>Curl:</li> I used curl to interact with the site directly, retrieving HTTP headers and testing responses.

<li>Wafw00f:</li> I ran Wafw00f to detect whether the site was protected by a Web Application Firewall (WAF).

<li>Dnsrecon:</li> I executed dnsrecon to enumerate DNS records and gather deeper insights into the domain’s infrastructure.
</ul>
I recorded every output carefully, because the information I collected here forms the foundation for planning my scanning and attacks. I know that I cannot attack what I have not first understood, so this footprinting stage was critical to my reconnaissance process.


## **whois**
  <img width="1076" height="983" alt="image" src="https://github.com/user-attachments/assets/60f3cbb5-c922-4e79-ba9f-c4280f00dbb0"/>

 ## **whatweb**
<img width="1194" height="339" alt="image" src="https://github.com/user-attachments/assets/7f4e823a-cdb5-4f6a-ac5b-6aabc357cb04"/>


## **nslookup**
<img width="325" height="207" alt="image" src="https://github.com/user-attachments/assets/ce41536b-2225-482c-9772-c75945afac57"/>

## **curl**
<img width="1200" height="343" alt="image" src="https://github.com/user-attachments/assets/d0813913-aa07-4f7a-b661-e8ae4476d3da"/>


## **wafw00f**
<img width="709" height="352" alt="image" src="https://github.com/user-attachments/assets/92835e66-a290-4516-9034-1636e25a870b"/>

## **ddnsrecon**
<img width="1126" height="421" alt="image" src="https://github.com/user-attachments/assets/35c4f366-c496-434d-9477-261d4e716f0a"/>
</p>

<h4>ZENMAP</h4>
<p>I also scanned my local network </p>


## Tools & Resources
| Tools, Devices and Commands   | Purpose                                                           |
|-------------------------------|-------------------------------------------------------------------|
| Kali Linux & Windows          | Operating systems used for reconnaissance activities              |
| WHOIS                         | Find domain registration details (owner, dates, name servers).    |
| whatweb                       | Fingerprint web technologies (server, CMS, plugins, IP).          |
| nslookup                      | Resolve the domain name to its IP address using DNS.              |
| curl -I                       | Read the HTTP response headers of the website.                    |
| wafw00f                       | Detect whether a Web Application Firewall protects the site.      |
| dnsrecon                      | Enumerate all DNS records (NS, MX, SPF, TXT, SRV).                |
| Zenmap (Nmap GUI)             | Scan the local subnet to find live hosts, IPs and MAC addresses.  |
| Windows CMD                   | Checking local IP and MAC address identification                  |


<ol>
  <p><li>Download & install Zenmap from official website on your Windows PC: </li>I downloaded zenmap from https://nmap.org/download.html and installed it.</p>
  <p></p><li>Find your local IP address & your LAN subnet: </li>I opened CMD & run ipconfig command to find my PC’s local IP address &
and local LAN subnet
<img width="850" height="550" alt="image" src="https://github.com/user-attachments/assets/66e3e3f6-99ed-4e40-99bf-8d02aec78b46" />
</p>
  <p><li>Find the list of live hosts/PC’s in your IP subnet: </li>I lunched Zenmap, input the local LAN subnet & select Ping Scan to find the list of
live hosts in your subnet
    <img width="850" height="550" alt="image" src="https://github.com/user-attachments/assets/0e10ff49-401a-4787-84b3-3550fa69d14c" />
  </p>
  <p><li>How many hosts are live in your subnet?</li>There were 2 live host which my PC was part.</p>
  <p><li>What are the IP addresses of the live hosts?</li>
    <ul>
      <li>10.101.231.189</li>
      <li>10.101.231.98</li>
    </ul>
</p>
  <p><li>What are the MAC addresses of the live hosts?</li>
    <ul>
      <li>BA:47:81:8A:1D:A0</li>
      <li>44-EF-BF-16-63-F7</li>
    </ul>
</p>
  <p><li>Display & save the output topology in PDF Format on your desktop: </li>
  <img width="1200" height="750" alt="image" src="https://github.com/user-attachments/assets/4cb194a8-6331-49c8-add7-43bbd8622b5e" />
  </p>
</ol>








# Conlusion
This project provided practical experience in both footprinting and network scanning using built-in Kali Linux tools and Zenmap. Reconnaissance and network discovery are critical phases in cybersecurity because they help security professionals understand a target environment before conducting further assessment activities.

During the footprinting phase, tools such as WHOIS, NSLookup, DNSRecon, WhatWeb, cURL, and WAFW00F were used to gather publicly available information about the target. These tools helped identify domain ownership details, IP addresses, DNS records, hosting providers, mail servers, web technologies, and security mechanisms such as web application firewalls. Although no direct interaction or attack was performed against the target systems, the information collected demonstrated how much valuable intelligence can be obtained from publicly accessible sources.

The Zenmap phase complemented this process by enabling the discovery of live hosts, open ports, running services, and network configurations. Through graphical Nmap scan profiles, it was possible to visualize network assets and identify potential entry points that could be exploited if left unsecured. The results emphasized the importance of regular network monitoring and vulnerability assessment in maintaining a strong security posture.

Overall, this exercise demonstrated that information gathering and network scanning are essential components of cybersecurity assessments. The insights obtained from both footprinting and Zenmap scans highlight how attackers and defenders rely on the same techniques to understand a target environment. For organizations, regularly performing these activities helps identify exposed information, reduce unnecessary visibility, strengthen defenses, and mitigate potential security risks before they can be exploited.


# Author
Kwabeng Jeffrey Kingsley
Cybersecurity Student B083

LinkedIn: www.linkedin.com/in/jeffery-kwabeng-aa53a82b5

## Project Information
Program Name: FOOTPRINTING AND ZENMAP BASED SCANNING | Week: 02 | Project: W2 FOOTPRINTING AND ZENMAP BASED SCANNING | Repository: https://github.com/kjk6031/FOOTPRINTING-NETWORK-SCANNING/tree/main | Project REPORT: https://docs.google.com/document/d/17Eij8_ZBuftxq4VNg0iz9VPmNPLk6wnHSWZeZcJpNxo/edit?usp=sharing


