# 🔐 Week 3 Project: Enterprise Password Auditing & AI-Powered Cracking (JTR, NW Tools & HexStrike MCP)

**Intern:** Md Mohaiminul Islam  
**Organization:** NetworkWalks  
**Domain:** Cybersecurity & Penetration Testing  
**Week:** 03 (Modules: W3-PM1, W3-PM2 & W3-Optional AI Lab)

---

## 📌 Project Overview
In Week 3 of my Cybersecurity Internship at **NetworkWalks**, I explored both traditional and next-generation cryptographic auditing techniques. The objective of this project was to understand password hashing mechanisms, extract cryptographic hashes from encrypted PDF documents, and perform dictionary/brute-force attacks using industry-standard tools—culminating in an **AI-driven offensive security workflow** integrating **Claude Desktop** with **HexStrike MCP Server** on Kali Linux.

---

## 🛠️ Tools & Technologies Used
* **Operating Systems:** Kali Linux VM & Windows
* **Password Auditing Tools:** John the Ripper (JTR), Johnny GUI, `pdf2john`, NetworkWalks Dictionary Attack Lab
* **AI & Automation Stack:** Claude Desktop, HexStrike MCP (Model Context Protocol) Server, Python Virtual Environment (`venv`)
* **Wordlists:** `rockyou.txt` & Custom Dictionaries

---

## 🚀 Lab Execution & Methodology

### 🔹 Module 1 (W3-PM1): Password Cracking with John the Ripper & Johnny GUI
1. **Environment Setup:** Configured John the Ripper (`john.exe`) and linked it with the **Johnny GUI** frontend.
2. **Hash Extraction:** Extracted the `$pdf$` cryptographic hash values from target encrypted files (`My Locked PDF1.pdf`, `PDF2`, and `PDF3`).
3. **Cracking & Flag Retrieval:** Executed wordlists and rule-based attacks to recover plaintext passwords and capture the embedded flags.

<img width="870" height="690" alt="image" src="https://github.com/user-attachments/assets/e33376ce-87fd-4797-ae61-29bb26050361" />

<br> <br>

<img width="449" height="636" alt="WhatsApp Image 2026-11-19 at 11 17 59 AM" src="https://github.com/user-attachments/assets/65824235-4643-40e8-905b-413a8ccb2a0e" />

<br><br>
---

### 🔹 Module 2 (W3-PM2): Password Auditing with NetworkWalks (NW) Tools
1. **Hash Identification & Extraction:** Isolated the encryption hash from the target lab PDF.
2. **Dictionary Attack:** Utilized the **NetworkWalks Dictionary Attack Lab** tool to test high-probability password combinations, successfully recovering the credential (`1qaz2wsx`) and unlocking the target document.

<img width="564" height="795" alt="WhatsApp Image 2026-11-19 at 11 22 44 AM" src="https://github.com/user-attachments/assets/5ff08064-9419-405b-89be-a254b9565caf" />

<br><br>
<img width="1165" height="813" alt="WhatsApp Image 2026-11-19 at 3 30 29 PM" src="https://github.com/user-attachments/assets/df78cb18-3e97-4700-89c6-8ea3caae3af4" />

<br>
---

### 🔹 Optional Advanced Lab (W3-OPTIONAL1): AI-Powered Password Cracking with Claude & HexStrike MCP
To bridge **Artificial Intelligence with Offensive Security**, I deployed a local **HexStrike MCP Server** on Kali Linux and connected it to **Claude Desktop**:
1. **MCP Server Deployment:** Configured a dedicated Python environment on Kali Linux, resolved dependency conflicts, and launched the HexStrike API server on `localhost:8888`.
2. **Claude Desktop Integration:** Configured `claude_desktop_config.json` to grant Claude secure local tool execution access via the Model Context Protocol.
3. **Autonomous Execution:** Using natural language prompts, instructed Claude to verify JTR installation, extract the PDF hash via `pdf2john`, decompress `rockyou.txt`, and execute the cracking sequence autonomously.
   <br>
<img width="1391" height="853" alt="WhatsApp Image 2026-11-19 at 2 35 08 PM" src="https://github.com/user-attachments/assets/28b5bde9-50bf-4382-afdc-5e9c88a634bf" />
<br><br>
<img width="1600" height="809" alt="WhatsApp Image 2026-11-19 at 3 08 50 PM" src="https://github.com/user-attachments/assets/f7eda9a5-4748-49c3-af15-2d0dadb8c2e8" />

<br>
---

## 🧠 Challenges & Troubleshooting
* **Dependency Resolution in Python 3.14:** Encountered package backtracking loops with heavy binary analysis libraries (`angr`) during MCP installation. Resolved by isolating core MCP/FastMCP dependencies and streamlining the virtual environment.
* **Hash Format Validation:** Distinguished between standard file integrity checksums (MD5/SHA-256) and PDF encryption hashes (`$pdf$`) to ensure accurate JTR compatibility.

---

## 🎯 Key Takeaways
* Deep understanding of how weak passwords leave encrypted files vulnerable to offline hash-cracking attacks.
* Hands-on proficiency with both CLI (`pdf2john`, `john`) and GUI (`Johnny`) password auditing workflows.
* Practical experience in building **AI-assisted security pipelines** using MCP servers to automate repetitive reconnaissance and auditing tasks.

  Github Link: https://github.com/mohaiminul1185/NETWORKWALKS-B084-WK3-CYBERSECURITY-INTERNSHIP-/tree/main

  Linked in: https://lnkd.in/p/gXj6uyUG
