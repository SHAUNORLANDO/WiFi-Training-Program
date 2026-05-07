# WiFi Training Program
## Module 4 - Assignment Questions


### 1. What is the significance of MAC layer and in which position it is placed in the OSI model

The MAC (Medium Access Control) layer controls how devices access the wireless medium.

- Prevents collisions between devices
- Handles frame transmission and acknowledgements
- Manages authentication and association

Position in OSI Model:
- Part of Data Link Layer (Layer 2)
- Between Physical Layer and Network Layer

Simple idea:
MAC decides who transmits and when in WiFi.

---

### 2. Describe the frame format of the 802.11 MAC header and explain the purpose of each fields

Fields in MAC frame:

<img width="1536" height="808" alt="image" src="https://github.com/user-attachments/assets/5b5ae7ed-904a-4f34-89aa-f6dcf2723080" />

- Frame Control: Defines type of frame
- Duration/ID: Used for channel reservation (NAV)
- Address 1: Receiver address
- Address 2: Transmitter address
- Address 3: Destination/BSSID
- Address 4: Used in special cases
- Sequence Control: Maintains order and avoids duplicates
- Payload: Actual data
- FCS: Error detection

---

### 3. Please list all the MAC layer functionalities in all Management, Control and Data plane

Management Plane:
- Beacon generation
- Scanning - Active and Passive
- Authentication
- Client Association/Reassociation
- QoS Management
- Power Management

Control Plane:
- RTS (Request to Send)
- CTS (Clear to Send)
- ACK (Acknowledgment)
- Block ACK
- Medium Access Control - PCF, DCF, EDCA

Data Plane:
- Data transmission
- Fragmentation
- Retransmission
- Aggregation - No, AMPDU, AMSDU, AMSDU in AMPDU

---

### 4. Explain the scanning process and its types in detail

Scanning is the process by which a wireless client discovers available Wi-Fi networks and access points before establishing a connection.

During scanning, the client collects information such as:
- SSID (network name)
- Signal strength
- Supported data rates
- Security type

Scanning helps the client select the best available Access Point (AP) for communication.

## Types of Scanning

| Type | Description |
|---|---|
| Passive Scanning | Client listens for beacon frames sent by APs |
| Active Scanning | Client actively sends probe requests to discover APs |

---

# Passive Scanning

In passive scanning, the Access Point periodically broadcasts beacon frames.

The wireless client listens to these beacon signals and gathers network information.

### Process

- AP continuously sends beacon frames  
- Client listens on different channels  
- Client identifies available networks  
- Client selects and connects to a suitable AP

### Advantages

- Low power consumption  
- Less network traffic  
- Simple scanning method

### Disadvantages

- Slower scanning process  
- Client must wait for beacon transmission

---

# Active Scanning

In active scanning, the wireless client actively searches for networks.

The client sends a probe request frame, and nearby APs respond with probe response frames.

### Process

- Client sends probe request  
- AP receives the request  
- AP sends probe response  
- Client collects network details and selects an AP

### Advantages

- Faster network discovery  
- Quick connection establishment

### Disadvantages

- Higher power consumption  
- Increased network traffic

---

# Difference Between Passive and Active Scanning

| Passive Scanning | Active Scanning |
|---|---|
| AP initiates communication using beacon frames | Client initiates communication using probe requests |
| Slower | Faster |
| Lower power consumption | Higher power consumption |
| Less traffic overhead | More traffic overhead |

Thus, scanning enables wireless devices to discover and connect to available WLAN networks efficiently.

---

### 5. Brief about the client association process

# Client Association Process in WLAN

The client association process is the procedure by which a wireless device connects to a Wi-Fi network through an Access Point (AP).

## Steps in Client Association Process

### Scanning

The wireless client searches for available Wi-Fi networks using:
- Passive scanning
- Active scanning

The client identifies nearby Access Points and selects a suitable network.

### Authentication

The client and Access Point verify each other before connection.

Authentication may involve:
- Open authentication
- WPA/WPA2/WPA3 security authentication

If authentication is successful, the client proceeds to the next step.

### Association

The client sends an association request to the Access Point.

The AP responds with an association response and allocates resources for communication.

After successful association, the client becomes part of the wireless network.

### IP Address Assignment

The client obtains an IP address from the DHCP server.

The IP address allows the client to communicate within the network and access the internet.

Thus, the client association process enables secure and proper connection of wireless devices to a WLAN network.

---

### 6. Explain each steps involved in EAPOL 4-way handshake and the purpose of each keys derived from the process

Used in WPA2/WPA3 security.

<img width="1288" height="1131" alt="image" src="https://github.com/user-attachments/assets/d3c0a0ae-52bb-4bab-91b8-043167c8b258" />

Steps:

Step 1:
AP sends ANonce

Step 2:
Client sends SNonce and MIC
PTK is derived

Step 3:
AP sends GTK encrypted

Step 4:
Client sends acknowledgment

<img width="720" height="813" alt="image" src="https://github.com/user-attachments/assets/ccf95d81-1b85-4fb0-8db5-ebf298a90d65" />

Keys:

- PMK: Derived from password
- PTK: Used for unicast encryption
- GTK: Used for broadcast traffic
  
---

### 7. Describe the power saving scheme in MAC layer and explore on the types of Power saving mechanisms

# Power Saving Scheme in MAC Layer and its Mechanisms

The power saving scheme in the MAC layer is used to reduce battery consumption in wireless devices by allowing them to enter sleep mode when communication is not required.

The Access Point (AP) stores buffered data for sleeping clients and delivers it when the client becomes active.

## Types of Power Saving Mechanisms

| Mechanism | Description |
|---|---|
| Legacy Power Save | Client periodically wakes up to check buffered data |
| U-APSD | Client triggers data transmission when required |
| TWT (Target Wake Time) | AP and client schedule specific wake-up times |

---

# Legacy Power Save

In this mechanism, the client enters sleep mode to save power.

The Access Point buffers incoming data for the client.

The client periodically wakes up and checks for pending data using beacon information.

### Features

- Simple power-saving method  
- Reduces battery usage  
- Suitable for basic WLAN devices

---

# U-APSD (Unscheduled Automatic Power Save Delivery)

In U-APSD, the client controls when it wants to receive buffered data.

The client sends a trigger frame, and the AP delivers the stored packets.

### Features

- Reduces unnecessary wake-up time  
- Improves battery efficiency  
- Commonly used in voice and multimedia applications

---

# Target Wake Time (TWT)

TWT is an advanced power-saving mechanism introduced in Wi-Fi 6.

The AP and client negotiate scheduled wake-up times for communication.

The client remains in sleep mode until the scheduled time.

### Features

- Highly efficient power management  
- Reduces channel contention  
- Ideal for IoT and low-power devices  
- Improves battery life significantly

Thus, MAC layer power-saving mechanisms improve energy efficiency and extend battery life in wireless devices.

---

### 8. Describe the Medium Access Control methodologies

# Medium Access Control (MAC) Methodologies in WLAN

Medium Access Control (MAC) methodologies are techniques used in WLAN to control how multiple wireless devices access and share the communication channel efficiently without collisions.

## CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)

CSMA/CA is the primary access method used in WLAN.

Before transmitting data, a device listens to the channel:
- If the channel is free → transmission starts
- If the channel is busy → device waits

This helps in avoiding collisions in wireless communication.

---

# Backoff Algorithm

When the channel is busy, the device waits for a random period before retransmitting.

This random waiting time is called the backoff time.

### Purpose

- Reduces collision probability  
- Prevents multiple devices from transmitting simultaneously  
- Improves channel efficiency

---

# RTS/CTS Mechanism

RTS/CTS stands for:
- Request To Send
- Clear To Send

It is used to solve the hidden node problem.

### Working

- Sender sends RTS frame  
- Receiver replies with CTS frame  
- Other devices wait until communication completes

### Advantages

- Reduces collisions  
- Improves communication reliability

---

# DCF (Distributed Coordination Function)

DCF is the basic MAC access method in IEEE 802.11 WLAN.

It uses:
- CSMA/CA
- Backoff algorithm

### Features

- Distributed access method  
- Contention-based communication  
- All devices get equal chance to access the medium

---

# PCF (Point Coordination Function)

PCF is a centralized access method controlled by the Access Point.

The AP polls devices and grants permission for transmission.

### Features

- Contention-free communication  
- Suitable for time-sensitive applications  
- Less commonly used in modern WLANs

---

# EDCA (Enhanced Distributed Channel Access)

EDCA is an enhanced version of DCF introduced in IEEE 802.11e for Quality of Service (QoS).

It provides different priorities for different traffic types.

### Traffic Categories

- Voice  
- Video  
- Best effort  
- Background traffic

### Advantages

- Prioritizes important traffic  
- Reduces delay for voice and video  
- Improves multimedia performance

Thus, MAC methodologies help WLAN devices share the wireless medium efficiently while reducing collisions and improving network performance.

---

### 9. Brief about the Block ACK mechanism and its advantages

# Block ACK Mechanism and its Advantages

Block ACK is a mechanism in WLAN where multiple data frames are transmitted together, and a single acknowledgment is sent for all the received frames instead of sending separate acknowledgments for each frame.

This mechanism improves transmission efficiency in high-speed wireless networks.

### Working of Block ACK

- Sender transmits multiple data frames in sequence  
- Receiver stores the received frames  
- Receiver sends one Block Acknowledgment frame containing the status of all received frames

### Advantages of Block ACK

- Reduces acknowledgment overhead  
- Improves network throughput  
- Reduces channel usage  
- Increases transmission efficiency  
- Supports high-speed data communication

Thus, the Block ACK mechanism enhances WLAN performance by reducing control overhead and enabling efficient data transmission.

---

### 10. Explain about A-MSDU, A-MPDU and A-MSDU in A-MPDU

A-MSDU:
- Multiple packets in one frame
- Same destination
- Less overhead but full retransmission on error

A-MPDU:
- Multiple frames aggregated
- Separate error checking
- Partial retransmission possible

A-MSDU in A-MPDU:
- Combination of both
- High efficiency
