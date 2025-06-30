#  Meow - Hack The Box 

> Difficulty: Easy  
> Category: Pwnbox   
> IP: 10.10.14.108 
> Author: Hack The Box

---

##  Description

**Meow** is the first box on Hack The Box. It introduces basic port scanning, service identification, and the use of `telnet` to retrieve a flag from a running service. No exploitation or scripting is required — just command-line basics and curiosity.

---

##  Tools Used

- `nmap` – For discovering open ports
- `telnet` – For connecting to the service
- Linux Terminal (via PwnBox or local machine)

---

##  Enumeration

###  Step 1: Nmap Scan

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

##  Exploitation

###  Step 2: Connecting to Telnet

We connect to the Telnet service:

```bash
telnet 10.129.12.143
```

**Output:**
```
Trying 10.129.12.143...
Connected to 10.129.12.143
Escape character is '^]'.
Welcome to Meow!
Flag: b40abdfe23665f766f9c61ecba8a4c19
```

---

## Flag

**User Flag: b40abdfe23665f766f9c61ecba8a4c19 **

```

```

---

##  Lessons Learned

- Basic usage of **nmap** for service discovery.
- How to use **telnet** to interact with a remote service.
- What a **flag** looks like and how to capture it.
- Importance of checking all open ports.

---

##  Conclusion

The **Meow** box is a gentle introduction to the Hack The Box platform. It’s perfect for new users to get a feel for port scanning and interacting with remote services using common Linux tools.

---


