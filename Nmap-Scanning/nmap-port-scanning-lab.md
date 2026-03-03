# 🔎 Nmap Port Scanning & Fingerprinting Lab

## 🖥 Lab Environment

- Attacker Machine: Kali Linux
- Target Machine: Metasploitable2
- Virtualization Platform: VirtualBox
- Purpose: Network Scanning & OS Fingerprinting Practice

---

## 🔧 Initial Setup

Logged into Kali Linux:

Username: kali  
Password: kali  

Opened terminal to begin scanning process.

---

## 📌 Step 1: Checking Network Configuration

```bash
ifconfig
```

Used to identify Kali machine IP address.

```bash
netstat -na | more
```

Displays active network connections and listening ports.

---

## 📌 Step 2: Nmap Help Menu

```bash
nmap
```

Displays available scan options and usage information.

---

## 📌 Step 3: Discover Live Hosts in Subnet

```bash
nmap -sn 192.168.1.0/24
```

- `-sn` → Ping scan (no port scan)
- Used to identify active hosts in network range.

---

## 📌 Step 4: Scan Target Without Ping (Treat Host as Online)

```bash
nmap -Pn <Metasploitable2-IP>
```

- `-Pn` → Skips host discovery
- Useful if ICMP is blocked.

Scan entire subnet without ping:

```bash
nmap -Pn <subnet>
```

---

## 📌 Step 5: SYN Scan (Stealth Scan)

```bash
nmap -sS <Metasploitable2-IP>
```

- Half-open TCP scan
- Faster and stealthier than full connect scan.

---

## 📌 Step 6: Fast Scan

```bash
nmap -F <Metasploitable2-IP>
```

- Scans top 100 most common ports.
- Faster but less comprehensive.

---

## 📌 Step 7: TCP Connect Scan

```bash
nmap -sT <Metasploitable2-IP>
```

- Completes full TCP handshake.
- More detectable than SYN scan.

---

## 📌 Step 8: UDP Scan (Specific Ports)

```bash
nmap -sU -p53,137 <Metasploitable2-IP>
```

- `-sU` → UDP scan
- `-p` → Specifies ports
- Used to detect services like DNS (53) and NetBIOS (137)

---

## 📌 Step 9: OS Detection

```bash
nmap -O <Metasploitable2-IP>
```

Attempts to detect the operating system of target machine.

---

## 📌 Step 10: Aggressive Scan

```bash
nmap -A <Metasploitable2-IP>
```

Includes:
- OS detection
- Version detection
- Script scanning
- Traceroute

Provides detailed information about services.

---

## 📌 Step 11: Save Scan Output to File

```bash
nmap -sS <Metasploitable2-IP> -oN kiddie.txt
```

- `-oN` → Saves output in normal format
- Output stored in file `kiddie.txt`

---

## 📂 Step 12: View Saved File

```bash
ls
```

Lists files in current directory.

```bash
mousepad kiddie.txt
```

Opens saved scan result in text editor.

---

## 🧠 Key Learnings

- Understood subnet scanning
- Learned difference between TCP, SYN and UDP scans
- Practiced OS fingerprinting
- Saved scan results for documentation
- Observed open ports and running services

---

## ⚠ Disclaimer

All activities were performed inside a controlled virtual lab environment using Kali Linux and Metasploitable2 for educational purposes only.
