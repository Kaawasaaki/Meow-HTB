# 🐱 Meow - Hack The Box (Beginner Level)

> Difficulty: Very Easy  
> Category: Pwnbox / Intro  
> IP: [your assigned IP]  
> Author: Hack The Box

---

## 🧠 Description

**Meow** is the first and easiest box on Hack The Box, designed for complete beginners. It introduces basic port scanning, service identification, and the use of `telnet` to retrieve a flag from a running service. No exploitation or scripting is required — just command-line basics and curiosity.

---

## 🛠️ Tools Used

- `nmap` – For discovering open ports
- `telnet` – For connecting to the service
- Linux Terminal (via PwnBox or local machine)

---

## 🔍 Enumeration

### 🔎 Step 1: Nmap Scan

We begin with a full TCP port scan using `nmap`:

```bash
nmap -sV -p- -T4 <IP>
```

**Output:**
```
PORT   STATE SERVICE VERSION
23/tcp open  telnet  Linux telnetd
```

- Only **port 23** is open, running the **telnet** service.

---

## ⚙️ Exploitation

### 🔌 Step 2: Connecting to Telnet

We connect to the Telnet service:

```bash
telnet <IP>
```

**Output:**
```
Trying <IP>...
Connected to <IP>.
Escape character is '^]'.
Welcome to Meow!
HTB{<your_flag_here>}
```

---

## 🎯 Flag

**User Flag:**

```
HTB{redacted}
```

> 💡 Note: No `root` access is needed; the flag is printed directly when connected.

---

## 📚 Lessons Learned

- Basic usage of **nmap** for service discovery.
- How to use **telnet** to interact with a remote service.
- What a **flag** looks like and how to capture it.
- Importance of checking all open ports.

---

## ✅ Conclusion

The **Meow** box is a gentle introduction to the Hack The Box platform. It’s perfect for new users to get a feel for port scanning and interacting with remote services using common Linux tools.

---

## 📝 Bonus Tips

- Telnet is an outdated but still useful protocol for CTF-style challenges.
- Always scan **all ports** when you’re unsure where services are running.
- Keep documenting your progress – it helps both learning and job interviews!

---

> 🚀 On to the next box? Try **Fawn** – it introduces FTP enumeration!
