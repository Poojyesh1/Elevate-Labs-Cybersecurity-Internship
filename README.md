# 🛰️ Local Network Port Scan

## 📌 Objective
To discover open ports on devices within the local network using Nmap, and optionally analyze packet captures using Wireshark, in order to understand network exposure and identify potential security risks.

---

## 🛠️ Tools Used

- **Nmap 7.95** (Kali Linux)
- **Wireshark** – For capturing and analyzing network traffic
- **Kali Linux Terminal**

---

## 🌐 IP Range Scanned

- Local IP Address: `192.168.1.124`
- Subnet Range: `192.168.1.0/24`

---

## 💻 Commands Used

```bash
ifconfig 192.168.1.124
nmap -sS 192.168.1.0/24
```

---

## 🧾 Key Findings

6 devices responded within the scanned subnet.

Device `192.168.1.141` had several open ports, including:

- **Port 22** – SSH  
- **Port 80** - http
- **Port 135** - msrpc
- **Port 1801** - msmq
- **Port 2103** - zephyr-clt
- **Port 8443** - https-alt

Other hosts had mostly filtered.

---

## 🖼️ Screenshots

### ✅ IP of Host Device
<img width="935" height="325" alt="Image" src="https://github.com/user-attachments/assets/c1479df4-561d-4ffa-b982-671ed5d57ae2" />

### ✅ Nmap Scan Output
<img width="950" height="464" alt="Image" src="https://github.com/user-attachments/assets/231007f6-ca46-4700-949c-e9401efab798" />

### ✅ Wireshark SYN Filter
<img width="931" height="454" alt="Image" src="https://github.com/user-attachments/assets/9487a333-d423-4d0f-a499-f86a886857a3" />

#### Filter used:
```bash
ip.addr == 192.168.1.124
```

---

## ✅ Conclusion

This task provided hands-on experience in scanning a local network and analyzing the underlying traffic. 
It helped:

- Identify potentially vulnerable services  
- Understand how SYN scans operate at the packet level  
- Reinforce the importance of reducing exposed ports to enhance network security

> 🛑 **Note:** All scans were performed in a safe, authorized lab environment for educational purposes only.
