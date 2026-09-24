**Password Cracking REPORT**

W3-PM-FINAL | CYBERSECURITY | NETWORKWALKS

| Cybersecurity Professional Name | Abel Alex |
| :---- | :---- |
| Program/Batch | B083-Networkwalks |
| Date | 24 September 2026 |
| Modules completed | W3-PM1 Password Cracking With JTRW3-PM2 Password Cracking With NETWORKWALKS TOOLSW3-PM3 Password Cracking With Hexstrike-AI MCP server with Claude desktopW3-PM4 Password Cracking With JTR JOHN with the help of AI (Hexstrike-AI MCP with Claude |

**1\. Liability Disclaimer**

I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.

**2\. Introduction**

Password cracking is a critical process utilized by security professionals to evaluate password strength and demonstrate the vulnerabilities associated with weak passwords. During Week 3 of the Networkwalks Cybersecurity training, practical lab modules were executed to understand how file protection mechanisms work and how they can be compromised. This report documents the methodologies used to extract password hashes from encrypted PDF files and crack them using traditional tools like John the Ripper, online web tools, and modern AI-assisted MCP frameworks.

**3\. Tools Used**

The table below lists each tool used:

| Tool | Purpose |
| :---- | :---- |
| John the Ripper (JTR) | A fast password cracking tool used to perform dictionary attacks against extracted PDF hashes. |
| Johnny GUI | A graphical user interface for John the Ripper, simplifying the cracking process for beginners. |
| Online Hash Extractor | Web-based tool (onlinehashcrack.com) used to extract crackable hashes from protected PDF files. |
| Networkwalks Hash Calculator | Online tool to securely extract \$pdf\$ formatted hashes from encrypted documents. |
| Networkwalks Password Cracker | Web-based cracking tool that uses built-in dictionaries to break extracted hashes. |
| Claude AI Desktop | Large Language Model interface used for prompt-based analysis and command execution. |
| Hexstrike-AI MCP Server | An offensive intelligence framework integrating AI (Claude) with local Kali Linux cybersecurity tools like JTR. |

**4\. Activities Performed**

***4.1 Module 1: Password Cracking with JTR***

In this module, an encrypted file named 'My Locked PDF1.pdf' was targeted. The first step involved extracting the password hash using the onlinehashcrack.com PDF hash extractor tool. The extracted hash (starting with \$pdf\$4\*4\*128...) was saved to a local text file (hash1.txt). Subsequently, John the Ripper, via the Johnny GUI interface, was configured on a Windows machine. The hash file was loaded into Johnny, and a dictionary attack was initiated. JTR successfully cracked the hash, revealing the password as 'password1', which was then used to unlock the PDF.

***4.2 Module 2: Password Cracking with NETWORKWALKS TOOLS***

This module demonstrated a browser-based approach. The target was again 'My Locked PDF1.pdf'. The Networkwalks Hash Calculator was used to upload the PDF and extract its hash securely. The complete hash was copied and pasted into the Networkwalks Password Cracker tool. The tool ran a dictionary attack using a built-in list of 100 common passwords. The attack yielded a successful match ('password1'), demonstrating that short, common passwords can be cracked almost instantly without installing local software.

***4.3 Module 3: Setup Hexstrike-AI MCP server***

To integrate AI into the cracking workflow, a Kali Linux virtual machine was configured with the HexStrike-AI MCP server and Claude desktop. The Claude desktop application for Debian was installed via APT repository. The Hexstrike-AI repository was cloned from GitHub, a Python virtual environment was created, and necessary dependencies (requirements.txt) were installed. The Hexstrike server (server.py) was initiated, and the MCP server configuration in Claude desktop was updated to link to the local Python executable and hexstrike\_mcp.py file. A health check confirmed the server was active and communicating with Claude.

***4.4 Module 4: AI-Assisted Password Cracking***

With the Hexstrike-AI MCP server active, Claude AI was utilized to autonomously crack 'hash3.networkwalks\_flag1.pdf'. Through natural language prompts in the Claude interface, the AI first verified the installation of John the Ripper on the Kali system. It then calculated the MD5, SHA-1, and SHA-256 hashes of the target file. Finally, Claude was instructed to use JTR and the rockyou.txt wordlist to crack the PDF. The AI executed the necessary backend commands via MCP, extracted the PDF hash format, ran JTR against it, and successfully cracked the password ('password'), presenting the results directly in the chat interface.

**5\. Risk Analysis / Impact**

The labs demonstrate that relying on simple passwords (like 'password1' or 'password') provides a false sense of security. Encrypted documents store their protection keys as hashes, which can be easily extracted using both web tools and command-line utilities. Once a hash is extracted, an attacker can perform offline dictionary or brute-force attacks without triggering security lockouts or alerts. The impact of a compromised password can be severe, leading to unauthorized data access, intellectual property theft, and regulatory compliance violations. The integration of AI (like Hexstrike MCP) further lowers the barrier to entry, allowing attackers to automate the extraction and cracking process rapidly.

**6\. Recommendations**

1\. Password Complexity: Enforce strong password policies requiring a minimum of 12 characters, utilizing a mix of uppercase, lowercase, numbers, and special symbols.  
2\. Avoid Dictionary Words: Educate users to avoid common dictionary words, sequential patterns (e.g., 123456), or easily guessable phrases, as these are present in wordlists like rockyou.txt.  
3\. Strong Encryption Standards: When encrypting documents, utilize modern, strong encryption algorithms (e.g., AES-256) rather than legacy standards that produce easily crackable hashes.  
4\. Password Managers: Encourage the use of secure password managers to generate and store complex, unique passwords for protected files.

**7\. Conclusion**

During Week 3 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering multiple facets of password cracking. I successfully utilized traditional tools like John the Ripper and Johnny GUI, explored accessible browser-based tools provided by Networkwalks, and implemented advanced AI-driven offensive techniques using the Hexstrike-AI MCP server with Claude. These modules provided practical, hands-on experience in hash extraction and dictionary attacks, strongly reinforcing the critical necessity of robust password policies in protecting sensitive digital assets.

**8\. Evidences Collected**

***4.1 Module 1: Password Cracking with JTR***

\- Hash Extraction: Successfully extracted hashes in the format starting with \$pdf\$ from encrypted files.

![][image1]

The password for 'My Locked PDF1.pdf' was identified as good-luck using JTR.

![][image2]

***4.2 Module 2: Password Cracking with NETWORKWALKS TOOLS***

![][image3]

Uploaded a custom wordlist to check for the password  
![][image4]

***4.3 Module 3: Setup Hexstrike-AI MCP server***

***![][image5]***

***![][image6]***

***![][image7]***

***4.4 Module 4: AI-Assisted Password Cracking***