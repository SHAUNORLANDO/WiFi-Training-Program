# WiFi Training Program  
## Assignment – Module 1  

---

### 1. In which OSL layer the Wi-Fi standard/protocol fits.

Wi-Fi mainly works in:
- **Layer 1 (Physical Layer)** → handles signals, frequency (2.4GHz / 5GHz), transmission
- **Layer 2 (Data Link Layer)** → handles MAC addressing, frames, error detection  

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

### 3. what is BSS and ESS?

- **BSS (Basic Service Set):**  
  One access point + connected devices  
  (like one Wi-Fi router in a room)

- **ESS (Extended Service Set):**  
  Multiple access points connected together  
  (like Wi-Fi across entire college campus)

---

### 4. what are the basic functionalities of Wi-Fi Accesspoint

- Provides wireless connectivity  
- Assigns IP address (via DHCP usually)  
- Handles authentication (password/security)  
- Routes traffic to internet  
- Manages multiple devices  

It acts as a bridge between wireless devices and internet.

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

- **IEEE (Institute of Electrical and Electronics Engineers):**  
  Defines standards (like 802.11)

- **WFA (Wi-Fi Alliance):**  
  Certifies devices (ensures compatibility)

Simple:
- IEEE → creates rules  
- WFA → checks if devices follow rules  

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

#### Observation:
Connection is generally stable, but speed fluctuation can happen during peak hours compared to full fiber (FTTH) connections.

---

### 10. List down the Wi-Fi topologies and use cases of each one.

| Topology | Description | Use Case |
|---------|------------|----------|
| Infrastructure Mode | Devices connect via AP | Home, office |
| Ad-hoc Mode | Device-to-device | File sharing |
| Mesh Network | Multiple APs connected | Large buildings |
| Point-to-Point | Direct link | Building-to-building |

---
