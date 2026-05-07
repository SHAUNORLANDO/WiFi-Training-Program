# WiFi Training Program  
## Assignment – Module 1  

---

### 1. In which OSI layer the Wi-Fi standard/protocol fits.

Wi-Fi mainly works in:
- **Layer 1 (Physical Layer)** → (PCLP, PMD) - handles signals, frequency (2.4GHz / 5GHz), transmission
- **Layer 2 (Data Link Layer)** → (MAC, LLC) - handles MAC addressing, frames, error detection  

So basically, Wi-Fi = Physical + Data Link layers.

---

### 2. Can you share the Wi-Fi devices that you are using day to day life, share that device's wireless capability/properties after connecting to network. Match your device to corresponding Wi-Fi Generations based on properties

Here are some of my daily devices:

| Device | Wi-Fi Standard | Band | Max Speed (approx) | Generation |
|-------|---------------|------|--------------------|------------|
| Laptop | 802.11ac | 2.4GHz + 5GHz | ~867 Mbps | Wi-Fi 5 |
| Smartphone | 802.11ax | 2.4GHz + 5GHz | ~1 Gbps+ | Wi-Fi 6 |
| Smart TV | 802.11n | 2.4GHz | ~150 Mbps | Wi-Fi 4 |

**Observation:**  
Newer devices support dual-band and higher speeds. Older ones mostly stick to 2.4GHz.

---

## 3. What is BSS and ESS?

# BSS (Basic Service Set)

A **Basic Service Set (BSS)** is the **smallest building block of a Wi-Fi network**.  
It consists of:

- One **Access Point (AP)** → Wi-Fi router/base station
- Multiple wireless devices (stations) connected to that AP:
  - Laptop
  - Mobile phone
  - Tablet
  - Printer

### Simple Definition
A BSS is a **single Wi-Fi coverage area created by one access point**.

### Example
- A Wi-Fi router inside a classroom
- All students connected to that router
- Together they form **one BSS**

### Important Features of BSS
- Uses only **one access point**
- Devices communicate through the AP
- Has limited coverage area
- Each BSS has a unique identifier called **BSSID**
  - Usually the MAC address of the AP
- Suitable for small areas like:
  - Homes
  - Classrooms
  - Small offices

### Diagram

          Laptop
             |
Phone ---- Access Point ---- Tablet
             |
          Printer

Entire setup = One BSS

---

# ESS (Extended Service Set)

An **Extended Service Set (ESS)** is formed when **multiple BSSs are connected together** through a wired network called the **Distribution System (DS)**. i.e, Multiple access points working together to provide one large Wi-Fi network.

### Why ESS is Needed
A single AP cannot cover large places such as:
- College campus
- Hospital
- Airport
- Large office building

So multiple APs are installed in different locations.

### How ESS Works
- Each AP creates its own BSS
- All APs are connected using:
  - Ethernet cable
  - Switch
  - Network backbone
- Usually all APs use:
  - Same SSID (Wi-Fi name)
  - Same password
- Users can move between APs without disconnecting

This movement is called **Roaming**.

### Example
In a college:
- AP1 → Ground floor
- AP2 → First floor
- AP3 → Library

All APs are connected together.

This complete network is called an **ESS**.

### Diagram

   [AP1] ----\
               \
   [AP2] ------ Switch/Network ------ Internet
               /
   [AP3] ----/

Each AP = One BSS  
All connected APs together = ESS

---

# Difference Between BSS and ESS

| Feature | BSS | ESS |
|---|---|---|
| Full Form | Basic Service Set | Extended Service Set |
| Number of APs | One AP | Multiple APs |
| Coverage Area | Small | Large |
| Network Size | Limited | Extended |
| Roaming Support | No | Yes |
| Example | Home Wi-Fi | Campus Wi-Fi |
| Structure | Single wireless cell | Multiple connected cells |

---

### 4. What are the basic functionalities of Wi-Fi Access point>

# Basic Functionalities of a Wi-Fi Access Point

A Wi-Fi Access Point (AP) is a networking device that connects wireless devices to a wired network and provides internet access.

- Provides wireless connectivity to devices such as laptops, mobiles, and tablets through Wi-Fi signals.

- Assigns IP addresses to connected devices using DHCP for communication within the network.

- Handles authentication and security using passwords and protocols like WPA2/WPA3 to prevent unauthorized access.

- Routes data traffic between wireless devices and the internet.

- Manages multiple connected devices and controls network communication efficiently.

Thus, a Wi-Fi Access Point acts as a bridge between wireless devices and the internet/network.

---

### 5. Difference between Bridge mode and Repeater mode

| Feature | Bridge Mode | Repeater Mode |
|--------|------------|--------------|
| Purpose | Connect two networks | Extend Wi-Fi coverage |
| Connection | Wired/Wireless bridge | Wireless only |
| Speed | Better | Reduced (due to repeating) |
| Use case | Connecting LANs | Increasing range |

---

### 6. what are the differences between 802.11a and 802.11b.

| Feature | 802.11a | 802.11b |
|--------|--------|--------|
| Frequency | 5 GHz | 2.4 GHz |
| Speed | Up to 54 Mbps | Up to 11 Mbps |
| Range | Less | More |
| Interference | Less | More |

---

### 7. Configure your modem/hotspot to operate only in 2.4Ghz and connect your laptop/Wi-Fi device , and capture the capability/properties in your Wi-Fi device. Repeat the same in 5Ghz and tabulate all the differences you observed during this

#### Setup:
- 2.4GHz config:
<img width="900" height="682" alt="2 4" src="https://github.com/user-attachments/assets/8979359b-507f-4816-a103-988979993d97" />

 <img width="801" height="500" alt="5_1" src="https://github.com/user-attachments/assets/9df318d8-8565-49d3-8b89-58d97ea070b9" />

- 5GHz config:
  <img width="902" height="680" alt="5" src="https://github.com/user-attachments/assets/88f304c4-f449-4b37-970a-8a40d29f41c3" />

<img width="776" height="462" alt="2 4_1" src="https://github.com/user-attachments/assets/bf9606c0-562e-4e51-8881-17a5d5726f8b" />

#### Observations:

| Parameter | 2.4 GHz | 5 GHz |
|----------|--------|------|
| Signal Strength | Strong | Medium |
| Speed | Lower | Higher |
| Range | More | Less |
| Interference | High | Low |

**Conclusion:**  
- 2.4GHz → better for range  
- 5GHz → better for speed  

---

### 8. What is the difference between IEEE and WFA

# Difference Between IEEE and WFA

| IEEE | WFA |
|---|---|
| Stands for Institute of Electrical and Electronics Engineers | Stands for Wi-Fi Alliance |
| Develops and defines wireless communication standards | Certifies Wi-Fi devices for compatibility |
| Creates standards such as IEEE 802.11 | Ensures devices follow IEEE standards properly |
| Focuses on technical specifications and protocols | Focuses on interoperability and testing |
| Defines how Wi-Fi technology should work | Ensures devices from different companies work together |

- IEEE → Creates the rules and standards  
- WFA → Tests and certifies devices based on those standards  

---

### 9. List down the type of Wi-Fi internet connectivity backhaul, share your home/college's wireless internet connectivity backhaul name and its properties

**Type:** Cable Broadband  
**Provider:** Hathway  
**Backhaul:** Hybrid Fiber-Coaxial (HFC)

#### Properties:
- Moderate to high speed (typically 50 Mbps – 300 Mbps depending on plan)
- Latency is low to moderate  
- Uses fiber till local node + coaxial cable to home  
- Performance may vary during peak usage time  
- Supports multiple devices (phones, laptop, TV, IoT devices)

#### Usage:
Used for:
- Online classes / browsing  
- Streaming (YouTube, OTT)  
- Coding and project work  
- IoT applications (ESP32 web server, dashboards)

---

### 10. List down the Wi-Fi topologies and use cases of each one.

| Topology | Description | Use Case |
|---|---|---|
| Infrastructure Mode | Devices connect through an Access Point (AP) | Home, office, campus networks |
| Ad-hoc Mode | Devices communicate directly without an AP | File sharing, temporary networks |
| Mesh Network | Multiple APs interconnected to extend coverage | Large buildings, smart cities |
| Point-to-Point Mode | Direct wireless link between two locations | Building-to-building communication |
| Bridge Mode | Connects two wired networks wirelessly | Connecting LANs across buildings |
| Repeater Mode | Receives and retransmits Wi-Fi signals to extend range | Expanding Wi-Fi coverage |
| WGB (Workgroup Bridge) Mode | Connects wired devices to a wireless network through an AP | Connecting printers, switches, or IP cameras |
| Mobile Hotspot Mode | Mobile device shares cellular internet through Wi-Fi | Internet sharing using smartphones |

---
