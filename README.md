# FOOTPRINTING & RECONNAISSANCE ATTACKS

##INTRODUCTION
Reconnaissance (also called as footprinting) is the first step in any real attack or security test. Before touching a target, an attacker quietly collects as much public information about it as possible. This includes who owns the domain, its real IP address, the hosting provider, the web technologies it runs, its DNS and mail records, and whether a firewall is protecting it.
All of this comes from information the target has already made public, so the target never even knows it is being studied.
This is why recon is powerful and very hard to detect.

##What I did
In this lab, I footprinted the live website networkwalks.com using six built‑in Kali Linux tools. Each tool revealed a different piece of information about the target, and together they helped me build a full profile of it.
<ul>
<li>Whois:</li> I ran a whois lookup and I gathered the domain registration details, including registrar information and contact data.

<li>WhatWeb:</li> I used WhatWeb to identify the technologies running on the site, such as the web server, frameworks, and CMS.

<li>Nslookup:</li> I performed nslookup queries to resolve the domain name into IP addresses and to check DNS records.

<li>Curl:</li> I used curl to interact with the site directly, retrieving HTTP headers and testing responses.

<li>Wafw00f:</li> I ran Wafw00f to detect whether the site was protected by a Web Application Firewall (WAF).

<li>Dnsrecon:</li> I executed dnsrecon to enumerate DNS records and gather deeper insights into the domain’s infrastructure.
</ul>
I recorded every output carefully, because the information I collected here forms the foundation for planning my scanning and attacks. I know that I cannot attack what I have not first understood, so this footprinting stage was critical to my reconnaissance process.
