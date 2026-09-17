# FOOTPRINTING & RECONNAISSANCE ATTACKS

## INTRODUCTION
Reconnaissance (also called as footprinting) is the first step in any real attack or security test. Before touching a target, an attacker quietly collects as much public information about it as possible. This includes who owns the domain, its real IP address, the hosting provider, the web technologies it runs, its DNS and mail records, and whether a firewall is protecting it.
All of this comes from information the target has already made public, so the target never even knows it is being studied.
This is why recon is powerful and very hard to detect.

## What I did
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
  whois reveals the registrar, registration and expiry dates, and name servers. Here the name servers point to HostGator, so an attacker instantly learns the hosting provider. Registration dates and abuse contacts help with social engineering and planning.
  
  <img width="1076" height="983" alt="image" src="https://github.com/user-attachments/assets/60f3cbb5-c922-4e79-ba9f-c4280f00dbb0" />

 ## **whatweb**
whatweb exposes the exact software and versions (here Wordpress 7.0.4 and WP Download Manager 3.3.58). An attacker read about these versions on vulnerability databases to find known exploits. It also leaks the server IP and an email address.

<img width="1194" height="339" alt="image" src="https://github.com/user-attachments/assets/7f4e823a-cdb5-4f6a-ac5b-6aabc357cb04" />


## **nslookup**
I resolved the domain name to its IP address using DNS.
nslookup turns a domain name into its real IP address (192.232.216.135). Knowing the IP lets an attacker scan the server directly, look up other sites on the same IP, and map the target's infrastructure.
<img width="325" height="207" alt="image" src="https://github.com/user-attachments/assets/ce41536b-2225-482c-9772-c75945afac57" />

## **curl**
I used curl with the (-I) flag to able to read Read the HTTP response headers to see the server banner, status, cookies and redirects.
HTTP headers leak the web server, caching stack and hidden endpoints (here the WordPress REST API at /wp-json/). Attackers read headers to fingerprint the stack and find entry points without even loading the full page.

<img width="1200" height="343" alt="image" src="https://github.com/user-attachments/assets/d0813913-aa07-4f7a-b661-e8ae4476d3da" />


## **wafw00f**
I used wafw00f to check whether a Web Application Firewall (WAF) is protecting the target site.
wafw00f tells an attacker if a firewall is watching. Here the site sits behind ModSecurity (SpiderLabs). Knowing a WAF is present shapes the whole attack: naive attempts will be blocked or logged, so the attacker must adapt or try to bypass it.

<img width="709" height="352" alt="image" src="https://github.com/user-attachments/assets/92835e66-a290-4516-9034-1636e25a870b" />

## **ddnsrecon**
I used dnsrecon with the (-d) flag to enumerate all DNS records: name servers, mail servers, SPF, TXT and service (SRV) records.
dnsrecon maps the target's entire DNS footprint: mail servers, DNS software version (Bind 9.16.23), SPF policy and cPanel service records. Each record is a potential foothold and helps an attacker understand the email and hosting setup.

<img width="1126" height="421" alt="image" src="https://github.com/user-attachments/assets/35c4f366-c496-434d-9477-261d4e716f0a" />


# Conlusion
