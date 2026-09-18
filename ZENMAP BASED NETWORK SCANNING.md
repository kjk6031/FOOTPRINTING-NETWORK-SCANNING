NETWORK SCANNING USING ZENMAP

## INTRODUCTION
Zenmap is the official GUI version of Nmap which can be used on Windows PC. It is a security scanner
software tool which is used by Cybersecurity professionals & Hackers. It is a multi-platform (Linux, Windows,
Mac OS X, BSD, etc.) free and open source application which aims to make Nmap easy for beginners to use
while providing advanced features for experienced Nmap users. Frequently used scans can be saved as
profiles to make them easy to run repeatedly.

## What I did:
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

## Conclusion
The Zenmap-based network scanning exercise successfully demonstrated how graphical network reconnaissance tools can be used to identify active hosts, discover open ports, detect running services, and gather critical information about target systems. Through the use of Zenmap's various scan profiles, it was possible to perform efficient network enumeration while gaining a deeper understanding of the network's structure and exposed services.

The results highlight the importance of network scanning as a foundational step in cybersecurity assessments, penetration testing, and vulnerability management. By analyzing scan outputs, administrators and security professionals can identify potential security weaknesses, verify system configurations, and improve overall network security posture.

In conclusion, Zenmap provides an intuitive interface for leveraging Nmap's powerful scanning capabilities, making network discovery and analysis more accessible to both beginners and experienced security practitioners. Regular network scanning remains an essential practice for maintaining secure, reliable, and well-monitored network environments.



