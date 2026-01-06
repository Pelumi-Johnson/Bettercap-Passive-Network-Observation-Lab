# 🛡️ Bettercap Passive Network Observation Lab

 📄 **Full Lab Report:**  
👉 [Click here to open the complete lab report](https://github.com/Pelumi-Johnson/Bettercap-Passive-Network-Observation-Lab/blob/main/Bettercap%20Passive%20Network%20Observation%20Lab.pdf)

## 📌 Overview
This project documents a **passive network observation lab** conducted using **Bettercap** on an **Ubuntu virtual machine**.  
The goal was to understand how devices naturally communicate on a local network, how traffic appears during normal connections, and how encryption impacts visibility — **without performing any active attacks or interference**.

This lab focuses on **observation, analysis, and understanding**, not exploitation.

---

## 🎯 Objective
- Observe how devices announce themselves on a local network
- Understand how connections begin at the packet level
- Compare visibility between HTTP and HTTPS traffic
- Learn why trust and connection enable network visibility
- Build foundational knowledge relevant to detecting rogue or evil twin activity

---

## 🧰 Tools & Environment
- **Operating System:** Ubuntu Linux (Virtual Machine)
- **Virtualization:** Oracle VirtualBox (Bridged Networking)
- **Tool:** Bettercap
- **Network Mode:** Passive listening only

---

## 🧪 Lab Scope (Important)
✔ Passive observation only  
✔ No packet injection  
✔ No impersonation  
✔ No deauthentication  
✔ No credential interception  

This lab mirrors **SOC-level visibility**, not offensive exploitation.

---

## ⚙️ Lab Steps Summary

### 1️⃣ Network Setup
- Verified VM was using **bridged networking**
- Confirmed VM had its own IP in the `192.168.1.0/24` range
- Ensured VM behaved as a separate device on the network

---

### 2️⃣ Launching Bettercap
- Started Bettercap in interactive mode
- Bound Bettercap to the VM’s active network interface
- No activity occurred until modules were manually enabled

---

### 3️⃣ Passive Network Discovery (`net.recon`)
- Enabled passive reconnaissance
- Observed devices appearing and disappearing naturally
- Logged IP and MAC addresses through existing ARP traffic

**Key observation:** Devices reveal themselves without being queried.

---

### 4️⃣ Local Name Discovery (mDNS)
- Observed `.local` hostname queries
- Identified devices such as phones, tablets, and a Raspberry Pi
- Demonstrated how devices find each other without centralized DNS

---

### 5️⃣ HTTP Traffic Observation
- Observed HTTP GET requests in clear text
- Destination domains and request types were visible
- Demonstrated the risk of unencrypted traffic

---

### 6️⃣ HTTPS Traffic Observation
- Observed HTTPS connections using SNI
- Domain names were visible, but content was encrypted
- Demonstrated how encryption protects data but not all metadata

---

### 7️⃣ Device Presence Changes
- Observed `endpoint.new` and `endpoint.lost` events
- Devices appeared and disappeared naturally due to sleep, movement, or disconnects
- Reinforced how dynamic networks are

---

## 🧠 Key Concepts Learned
- ARP and mDNS leak useful network information passively
- Network visibility starts **after trust and connection**
- HTTP traffic exposes content; HTTPS protects it
- Passive monitoring reveals patterns without interaction
- Evil twin attacks succeed due to **trust**, not technical magic

---

## 📸 Screenshots
Screenshots captured during the lab show:
- Passive device discovery
- mDNS name resolution
- HTTP vs HTTPS traffic visibility
- Endpoint appearance and loss events

*(Screenshots intentionally omit sensitive data.)*

---

## 🧾 Conclusion
This lab demonstrated how much information is visible on a local network through **passive observation alone**.  
Understanding normal traffic behavior is essential before studying detection or defense against rogue access points and evil twin attacks.

This foundational knowledge directly supports **SOC monitoring, threat detection, and network defense** roles.

  
