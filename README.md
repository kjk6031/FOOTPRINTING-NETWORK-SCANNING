# FOOTPRINTING & NETWORK SCANNING

## INTRODUCTION
Reconnaissance, also known as footprinting, is the first stage of any cybersecurity assessment or real-world attack. During this phase, an attacker gathers as much publicly available information as possible about a target before attempting any direct interaction. This information may include domain ownership details, IP addresses, hosting providers, DNS records, email servers, web technologies, and security mechanisms such as firewalls. Since these details are collected from publicly accessible sources, the target organization is often unaware that it is being investigated, making reconnaissance one of the most effective and difficult-to-detect phases of an attack.

After information gathering, attackers typically move to the scanning phase, where they identify active hosts, open ports, services, and potential network entry points. One of the most widely used tools for this purpose is Nmap (Network Mapper). On Windows systems, Nmap is commonly accessed through Zenmap, its official graphical user interface (GUI). Zenmap is a free, open-source, and cross-platform security scanning tool that simplifies network discovery for beginners while providing advanced functionality for experienced cybersecurity professionals and penetration testers. It allows users to perform various network scans, save frequently used scan profiles, and visualize network information effectively.

This report demonstrates both phases of the security assessment process. The footprinting component focuses on gathering intelligence about the networkwalks.com domain using various Kali Linux reconnaissance tools, while the scanning component examines a local network using Zenmap. Together, these activities illustrate how a potential attacker progresses from collecting publicly available information about a target to identifying and mapping live systems within a network environment. For each task, the report includes the commands executed, the observed results, supporting screenshots, and a brief explanation of the significance of each finding from an attacker's perspective.

## What I did
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

<p>I also</p>


## Tools & Resources
------------
|Kali      |
|whois     |
|whatweb   |
|nslookup  |
|curl -I   |
|wafw00f   |
|dnsrecon  |
------------
# Conlusion
Through this project I have used in-built kali tools for information gathering. Reconnaissance is the first stage of every real attack. Before touching a target, an attacker quietly builds a complete profile of it using only public information, exactly the tools in this task. whois and DNS tools (nslookup, dnsrecon) reveal who owns the domain, its real IP address, its hosting provider and its mail servers. whatweb and curl fingerprint the exact software and versions running, which an attacker matches against known vulnerabilities. wafw00f warns them whether a firewall is watching, so they know how careful to be.
None of these tools attack the target. They only read what is already public, which is exactly why footprinting is so powerful and so hard to detect. The more an organization leaks, the easier every later stage of the attack becomes. This is also why defenders run the same tools on themselves: to see what an attacker would see, and to reduce it.



# Author
Kwabeng Jeffrey Kingsley
Cybersecurity Student B083

LinkedIn: www.linkedin.com/in/jeffery-kwabeng-aa53a82b5

## Project Information
Program Name: FOOTPRINTING-RECONNAISSANCE-ATTACKS | Week: 02 | Project: FOOTPRINTING & RECONNAISSANCE
ATTACKS WITH MULTIPLE KALI TOOLS | Repository: GitHub


