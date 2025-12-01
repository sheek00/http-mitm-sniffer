# HTTP MITM Sniffer (Python 2.7 + Scapy)

A Python 2.7 based HTTP packet sniffer designed for *Man-in-the-Middle (MITM)* attacks using *ARP Spoofing*.  
This tool captures HTTP traffic, extracts *URLs, and identifies login **credentials (username & password)* sent in clear text.

> ⚠️ *Educational & Ethical Use Only*  
This project is created for learning network security, packet inspection, and red teaming techniques.

---

## 🚀 Features
- Capture HTTP traffic in real-time  
- Extract username & password sent via HTTP forms  
- Display full URLs (Host + Path)  
- Analyze packet layers (HTTP, TCP, Raw)  
- Works during ARP Spoofing MITM attacks  
- Fully compatible with *Python 2.7*

---

## 🧠 How It Works
1. Execute ARP Spoofing to become the *Man-in-the-Middle*  
2. Victim traffic flows through your machine  
3. The sniffer analyzes every packet and extracts:
   - HTTP requests  
   - Raw login parameters  
   - URL data (host + path)  
4. It prints only useful information (credentials + URLs)

This tool does *not* capture HTTPS credentials.

---

## 📦 Requirements
- Python 2.7  
- Scapy (Python 2 version)  
- scapy-http  

Install dependencies:
```bash
 pip install scapy
 pip install scapy-http

## Usage

Run the sniffer on your network interface (example: eth0):

```bash
python http-mitm-sniffer.py

Once the sniffer is running, it will:
	•	Capture HTTP traffic in real-time
	•	Display full URLs (Host + Path)
	•	Extract potential login credentials from Raw payloads
	•	Print any username/password parameters detected inside HTTP requests
