# Wi-Fi Training Program  
## Assignment – Module 2  

---
    
### 1. Brief about Split-MAC architecture and how it improves AP performance

# Split-MAC Architecture and its Performance Improvement

In Split-MAC architecture, the MAC layer functions are divided between the Access Point (AP) and the Wireless LAN Controller (WLC).

The MAC layer is split into:

- **Lower MAC (Real-time MAC)** → Present in the Access Point  
- **Upper MAC (Non real-time MAC)** → Present in the Wireless LAN Controller

The split occurs between the MAC sublayer and LLC (Logical Link Control) functions.

### Functions of Access Point (Lower MAC)

- Beacon transmission  
- Frame acknowledgement  
- Frame forwarding  
- Real-time wireless communication  
- Time-critical operations

### Functions of Wireless LAN Controller (Upper MAC)

- Authentication  
- Security management  
- Roaming control  
- QoS and policy management  
- Network configuration and monitoring

### Advantages of Split-MAC Architecture

- Reduces processing load on the Access Point  
- Provides centralized management through the WLC  
- Simplifies configuration and maintenance  
- Improves roaming performance between APs  
- Enhances scalability in large enterprise networks

Thus, Split-MAC architecture improves AP performance by separating time-sensitive operations from centralized control functions.

---

### 2. Describe about CAPWAP, explain the flow between AP and Controller

**CAPWAP = Control And Provisioning of Wireless Access Points**

It is a protocol used for communication between AP and WLC.

<img width="300" height="217" alt="Introduction-to-CAPWAP-300x250" src="https://github.com/user-attachments/assets/7701abf3-ff4a-459d-8adb-36566835bb05" />


<img width="300" height="164" alt="DTLS-Encryption-300x250" src="https://github.com/user-attachments/assets/c00fcce3-31d8-486f-8813-ac5fa5fa1c76" />

# CAPWAP and Communication Flow Between AP and Controller

CAPWAP (Control And Provisioning of Wireless Access Points) is a protocol used for communication between the Access Point (AP) and the Wireless LAN Controller (WLC).

It enables centralized management, configuration, and control of wireless access points in a network.

### Functions of CAPWAP

- Establishes communication between AP and WLC  
- Transfers configuration files from WLC to AP  
- Supports centralized monitoring and management  
- Carries control and data traffic between AP and controller

### Flow Between AP and Controller

- The Access Point boots up and initializes hardware.

- AP obtains an IP address using DHCP.

- AP discovers the Wireless LAN Controller through:
  - DHCP option
  - DNS lookup
  - Manual configuration

- AP establishes a secure CAPWAP tunnel with the WLC.

- The WLC authenticates the AP and downloads configuration settings.

- AP applies the configuration and starts broadcasting Wi-Fi services.

- Client devices can now connect through the AP, while the WLC manages and monitors the network centrally.

### Advantages of CAPWAP

- Centralized network management  
- Simplified AP configuration  
- Improved scalability  
- Better security and monitoring  
- Easier maintenance in large wireless networks

#### Flow:

1. AP boots up  
2. Gets IP address (DHCP)  
3. Discovers WLC (via DHCP/DNS/manual)  
4. Establishes CAPWAP connection  
5. Downloads configuration from WLC  
6. Starts serving clients  

---

### 3.  Where this CAPWAP fits in OSI model, what are the two tunnels in CAPWAP and its purpose

CAPWAP (Control And Provisioning of Wireless Access Points) mainly operates at the **Network Layer (Layer 3)** of the OSI model.

It uses:
- IP for communication
- UDP for transport

### CAPWAP Tunnels

CAPWAP creates two separate tunnels between the Access Point (AP) and the Wireless LAN Controller (WLC).

#### Two tunnels in CAPWAP:

1. **Control Tunnel**
   - Used for management messages
   - Authentication, configuration

2. **Data Tunnel**
   - Used for actual client data traffic

| Tunnel | Purpose |
|---|---|
| Control Tunnel | Used for management and control communication |
| Data Tunnel | Used for transmitting actual client data traffic |

### Control Tunnel

The control tunnel carries management-related messages between the AP and WLC.

Functions include:
- AP authentication
- Configuration download
- Security policies
- Network management messages

### Data Tunnel

The data tunnel carries user/client traffic through the controller.

Functions include:
- Client data transmission
- Forwarding wireless traffic
- Centralized traffic handling

Thus, CAPWAP enables centralized control and communication between APs and the Wireless LAN Controller using separate control and data tunnels.

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

The CAPWAP tunnel between the Access Point (AP) and Wireless LAN Controller (WLC) is maintained using UDP communication.

### UDP Ports Used

- UDP Port 5246 → Control Tunnel  
- UDP Port 5247 → Data Tunnel  

### Tunnel Maintenance Process

- The AP and WLC continuously exchange keep-alive or heartbeat messages.
- These messages verify that the connection between the AP and controller is active.
- If the AP does not receive a response from the WLC within a certain time, the CAPWAP tunnel is considered disconnected.
- The AP then attempts to reconnect and re-establish the CAPWAP tunnel with the controller.

### Purpose

- Ensures continuous communication between AP and WLC  
- Detects controller failure or network issues  
- Maintains stable wireless network operation 

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
- New clients cannot connect  
- Existing clients:
  - May continue temporarily  
  - Eventually disconnect  

#### Reason:
- All control is with WLC  
- AP depends on controller for operation  

---
