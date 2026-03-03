# 🔎 Nmap Port Scanning & Fingerprinting Lab

## 🖥 Lab Environment

- Attacker Machine: Kali Linux
- Target Machine: Metasploitable2
- Environment: VirtualBox Lab

---

## 📌 Step 1: Checking Network Configuration

```bash
ifconfig
```

Used to check Kali IP address.

---

## 📌 Step 2: Discover Live Hosts

```bash
nmap -sn 192.168.1.0/24
```

This identifies active machines in subnet.

---

## 📌 Step 3: SYN Scan

```bash
nmap -sS <Target-IP>
```

Stealth scan technique.

---

## 📌 Step 4: OS Detection

```bash
nmap -O <Target-IP>
```

Attempts to detect operating system.

---

## 📌 Step 5: Aggressive Scan

```bash
nmap -A <Target-IP>
```

Includes version detection, OS detection, scripts and traceroute.

---

## 🧠 Key Learnings

- Difference between scan types
- Host discovery techniques
- OS fingerprinting
- Saving scan results

---

## ⚠ Disclaimer

Performed inside a controlled virtual lab for educational purposes only.
