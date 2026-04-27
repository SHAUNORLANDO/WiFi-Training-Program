# Wi-Fi Training Program  
## Assignment – Module 2  

---
    
### 1. Brief about Split-MAC architecture and how it improves AP performance

In Split-MAC architecture, the MAC functions are divided between:

- **Access Point (AP)** → handles real-time operations  
- **Wireless LAN Controller (WLC)** → handles control and management  

#### Split:
- **AP (Local MAC):**
  - Beacon transmission
  - Frame forwarding
  - Real-time communication

- **WLC (Central MAC):**
  - Authentication
  - Security policies
  - Roaming decisions

#### Why it's better:
- Reduces load on AP  
- Centralized management  
- Faster roaming  
- Easier configuration for large networks  

---

### 2. Describe about CAPWAP, explain the flow between AP and Controller

**CAPWAP = Control And Provisioning of Wireless Access Points**

It is a protocol used for communication between AP and WLC.

#### Flow:

1. AP boots up  
2. Gets IP address (DHCP)  
3. Discovers WLC (via DHCP/DNS/manual)  
4. Establishes CAPWAP connection  
5. Downloads configuration from WLC  
6. Starts serving clients  

---

### 3.  Where this CAPWAP fits in OSI model, what are the two tunnels in CAPWAP and its purpose

- Works mainly at:
  - **Layer 3 (Network Layer)** → uses IP/UDP

#### Two tunnels in CAPWAP:

1. **Control Tunnel**
   - Used for management messages
   - Authentication, configuration

2. **Data Tunnel**
   - Used for actual client data traffic

---

### 4.  Whats the difference between Lightweight APs and Cloud-based APs

| Feature | Lightweight AP | Cloud-based AP |
|--------|---------------|---------------|
| Controller | Physical WLC | Cloud |
| Management | On-premise | Remote |
| Setup | Complex | Easy |
| Scalability | Limited | High |
| Example | Cisco WLC setup | Meraki |

---

### 5. How the CAPWAP tunnel is maintained between AP and controller

- Uses **UDP ports:**
  - 5246 → Control
  - 5247 → Data  

#### Maintained by:
- Keep-alive messages  
- Heartbeat between AP and WLC  
- If no response → AP tries reconnect  

---

### 6. Whats the difference between Sniffer and monitor mode, use case for each mode

| Feature | Sniffer Mode | Monitor Mode |
|--------|-------------|-------------|
| Purpose | Capture packets | Scan network |
| Use | Troubleshooting | Security |
| Data | Full packet capture | Detect rogue APs |

#### Use cases:

- **Sniffer Mode:**
  - Debugging Wi-Fi issues  
  - Packet analysis using tools like Wireshark  

- **Monitor Mode:**
  - Detect unauthorized devices  
  - Intrusion detection  

---

### 7. If WLC deployed in WAN, which AP mode is best for local network and how?

Best mode: **FlexConnect Mode**

#### Why:
- AP can work independently if WLC is far away  
- Local switching of traffic  
- Still controlled by WLC centrally  

#### Benefit:
- No latency issues  
- Works even if WAN is slow  

---

### 8. What are challenges if deploying autonomous APs (more than 50) in large network like university

Managing many standalone APs is tough:

- No centralized control  
- Manual configuration for each AP  
- Difficult firmware updates  
- Poor scalability  
- Roaming issues  
- Hard to troubleshoot  

#### In real life:
Not practical for large campuses → controllers are preferred

---

### 9.  What happens on wireless client connected to Lightweight AP in local mode if WLC goes down.

- AP loses connection to WLC  
- New clients **cannot connect**  
- Existing clients:
  - May continue temporarily  
  - Eventually disconnect  

#### Reason:
- All control is with WLC  
- AP depends on controller for operation  

---

- `[ADD PACKET CAPTURE SCREENSHOT IF DONE]`

---
