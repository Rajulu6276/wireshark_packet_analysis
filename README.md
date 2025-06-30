# wireshark_packet_analysis
# 🛡️ Task 5 – Network Traffic Capture and Protocol Analysis using Wireshark (Kali Linux)

## 📌 Objective
Capture and analyze live network traffic using Wireshark on **Kali Linux**, identify common communication protocols, and understand how data is transmitted and secured over the network.

---

## 🧪 Activity Performed
1. Launched **Wireshark** in Kali Linux.
2. Captured traffic on the active network interface (`wlan0`).
3. Visited [testvulnweb.com](http://testvulnweb.com).(Note: Education purpose only)
4. Logged in using:
   - **Username:** `test`
   - **Password:** `test`
5. Modified data on the website to generate form activity.
6. Applied the following filters in Wireshark:
   - `http` — to view any unencrypted traffic
   - `dns` — to track domain resolution
   - `tls` — to inspect encrypted HTTPS communication
7. Saved the capture file as `task5_capture.pcap`.

---

## 🔍 Protocols Identified

| Protocol | Purpose |
|----------|---------|
| **HTTP** | Used for basic web communication; limited data seen as most traffic redirected to HTTPS. |
| **DNS**  | Resolved domain names like `testvulnweb.com`. |
| **TLS**  | Secured the login and form data via HTTPS; content encrypted. |

---

## 🧷 Key Findings

### 🔎 1. HTTP Traffic
- Detected a few initial HTTP requests.
- However, most sensitive operations (login, data change) redirected to HTTPS using TLS.

### 🔐 2. TLS (HTTPS) Secured Communication
- Used `tls` filter to confirm handshake and encryption.
- Credentials and form data were **not visible** in the capture — proving encryption was active.

### 🌐 3. DNS Resolution
- Used `dns` filter to trace domain resolution requests.
- Verified IP addresses corresponding to `testvulnweb.com`.

---

## 🧰 Tools Used
- **Wireshark** (in Kali Linux)
- **Firefox** browser
- **Filters Used**:
  - `http`
  - `dns`
  - `tls`

## Screenshots
-http
---user login credentials
---updated data
-dns
-tls

## 🧠 Concepts Observed

| Concept | Observation |
|--------|-------------|
| **Packet Capture** | Traffic was captured during live interaction with a test site. |
| **Protocol Filtering** | Used filters to isolate `http`, `dns`, and `tls` traffic. |
| **TLS Encryption** | Login and data-modification requests were secured via TLS. |
| **DNS Queries** | Showed domain-to-IP resolution before session initiation. |

---

## ✅ Outcome
- Practically explored packet capture and protocol analysis.
- Understood the visibility of data in plaintext (HTTP) vs encrypted (TLS).
- Demonstrated ability to isolate and analyze key network protocols.

> 🚨 Ethical Note: This test was done on a vulnerable test environment (`testvulnweb.com`) for educational purposes only.

