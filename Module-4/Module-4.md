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
- Scanning
- Authentication
- Association/Reassociation

Control Plane:
- RTS (Request to Send)
- CTS (Clear to Send)
- ACK (Acknowledgment)
- Block ACK

Data Plane:
- Data transmission
- Fragmentation
- Retransmission
- QoS handling

---

### 4. Explain the scanning process and its types in detail

Scanning helps client find WiFi networks.

Types:

Passive Scanning:
- AP sends beacon frames
- Client listens
- Low power but slower

Active Scanning:
- Client sends probe request
- AP replies with probe response
- Faster but uses more power

---

### 5. Brief about the client association process

Steps:
1. Scanning
2. Authentication
3. Association
4. IP assignment (DHCP)

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

Keys:

- PMK: Derived from password
- PTK: Used for unicast encryption
- GTK: Used for broadcast traffic

---

### 7. Describe the power saving scheme in MAC layer and explore on the types of Power saving mechanisms

Used to reduce battery usage.

Types:

Legacy Power Save:
- AP buffers data
- Client wakes periodically

U-APSD:
- Client triggers data transmission

TWT (Target Wake Time):
- Scheduled wake-up time
- Efficient for IoT devices

---

### 8. Describe the Medium Access Control methodologies

CSMA/CA:
- Listen before transmitting

Backoff Algorithm:
- Random wait time

RTS/CTS:
- Avoid hidden node problem

---

### 9. Brief about the Block ACK mechanism and its advantages

- Multiple frames sent together
- Single acknowledgment returned

Advantages:
- Reduces overhead
- Improves throughput
- Efficient transmission

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
