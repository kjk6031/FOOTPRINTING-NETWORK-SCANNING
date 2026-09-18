# FOOTPRINTING & RECONNAISSANCE ATTACKS

## INTRODUCTION
Reconnaissance (also called as footprinting) is the first step in any real attack or security test. Before touching a target, an attacker quietly collects as much public information about it as possible. This includes who owns the domain, its real IP address, the hosting provider, the web technologies it runs, its DNS and mail records, and whether a firewall is protecting it.
All of this comes from information the target has already made public, so the target never even knows it is being studied.
This is why recon is powerful and very hard to detect.

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


