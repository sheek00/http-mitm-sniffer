# HTTP MITM Sniffer (Python 2.7)

This project is a lightweight HTTP packet sniffer written in Python 2.7 using Scapy. It was created for learning purposes to understand how HTTP packets flow, how to inspect layers, extract URLs, and capture clear-text login credentials during Man-in-the-Middle (MITM) attacks.

## Features
- Capture HTTP requests in real time  
- Extract full URLs (Host + Path)  
- Identify login parameters (username & password)  
- Parse Raw packet payloads  
- Filter only useful login-related data  
- Fully compatible with Python 2.7  

## What I Learned While Building This
- Sniffing packets using Scapy  
- Understanding HTTP layers inside packets  
- Extracting Host and Path fields  
- Parsing login data from Raw payloads  
- Using loops, lists, and substring search in Python  
- How POST requests send form data  
- Filtering and analyzing traffic during MITM  

## Requirements
- Python 2.7  
- Scapy (Python 2 version)  
- scapy-http  

Install dependencies:
bash
pip install scapy
pip install scapy-http


## Usage
Run the sniffer on your network interface (example: eth0):
bash
python http-mitm-sniffer.py


Once the sniffer is running, it will:
- Capture HTTP traffic in real time  
- Display full URLs (Host + Path)  
- Extract potential username/password parameters  
- Print any login information found inside HTTP Raw packets  

Example output:

[+] HTTP Request >> testphp.vulnweb.com/login.php
[+] possible username/password >> uname=nopain&pass=nogain


## Disclaimer
This project is for educational and research purposes only. Do NOT use it on networks you do not own or without permission.
