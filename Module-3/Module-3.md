# Wi-Fi Training Program  
## Assignment – Module 3  

---

### 1. What are the different 802.11 PHY layer standards? Compare their characteristics.

| Standard | Band | Max Speed | Key Tech |
|---------|------|----------|----------|
| 802.11b | 2.4 GHz | 11 Mbps | DSSS |
| 802.11a | 5 GHz | 54 Mbps | OFDM |
| 802.11g | 2.4 GHz | 54 Mbps | OFDM |
| 802.11n | 2.4/5 GHz | 600 Mbps | MIMO |
| 802.11ac | 5 GHz | ~3.5 Gbps | MU-MIMO |
| 802.11ax | 2.4/5 GHz | ~9.6 Gbps | OFDMA |

**Observation:**  
Speed improves mainly due to better modulation + MIMO + channel usage.

---

### 2. What are DSSS and FHSS? How do they work?

#### DSSS (Direct Sequence Spread Spectrum)
- Spreads signal across wide frequency
- Uses chip sequence
- More resistant to noise

#### FHSS (Frequency Hopping Spread Spectrum)
- Signal jumps between frequencies
- Less interference
- More secure (hard to track)

<img width="337" height="126" alt="image" src="https://github.com/user-attachments/assets/07a70a7b-391a-4039-bff3-ef0ee5e145c1" />

---

### 3. How do modulation schemes work in the PHY layer? Compare different modulation schemes and their performance across various Wi-Fi standards.

Common modulations:
- BPSK
- QPSK
- 16-QAM
- 64-QAM
- 256-QAM
- 1024-QAM (Wi-Fi 6)

#### Comparison:

| Modulation | Speed | Reliability |
|-----------|------|-------------|
| BPSK | Low | High |
| QPSK | Medium | Good |
| 64-QAM | High | Moderate |
| 1024-QAM | Very High | Low (needs strong signal) |

**Real idea:**  
Higher modulation = more speed but needs better signal.

---

### 4. What is the significance of OFDM in WLAN? How does it improve performance?

**OFDM = Orthogonal Frequency Division Multiplexing**

OFDM (Orthogonal Frequency Division Multiplexing) is a modulation technique used in Wireless LAN (WLAN) standards.

In OFDM, a wireless channel is divided into multiple smaller subcarriers, and data is transmitted in parallel through these subcarriers.

### Significance of OFDM in WLAN

- Efficient utilization of available bandwidth  
- Supports high-speed data transmission  
- Improves reliability of wireless communication  
- Reduces signal interference between subcarriers

<img width="684" height="325" alt="image" src="https://github.com/user-attachments/assets/b0dd933b-22a2-4a0f-afaa-70cbe8c169af" />

### How OFDM Improves Performance

- Reduces the effect of interference and noise  
- Handles multipath fading effectively  
- Increases data transmission rate  
- Improves spectral efficiency  
- Provides stable communication in indoor environments

### WLAN Standards Using OFDM

OFDM is used in:
- IEEE 802.11a  
- IEEE 802.11g  
- IEEE 802.11n  
- IEEE 802.11ac  
- IEEE 802.11ax

Thus, OFDM improves WLAN performance by enabling high-speed, reliable, and interference-resistant wireless communication.

---

### 5. How are frequency bands divided for Wi-Fi? Explain different bands and their channels.

#### Main bands:

- **2.4 GHz**
  - Range: High  
  - Speed: Low  
  - Channels: 1–13  

- **5 GHz**
  - Range: Medium  
  - Speed: High  
  - More channels  

- **6 GHz (Wi-Fi 6E)**
  - Very high speed  
  - Less congestion  

---

### 6. What is the role of Guard Intervals in WLAN transmission? How does a short Guard Interval improve efficiency?

A Guard Interval (GI) is a small time gap inserted between transmitted symbols in WLAN communication.

Its main purpose is to prevent overlapping of signals caused by multipath propagation and delay.

### Types of Guard Interval

- Normal Guard Interval → 800 ns  
- Short Guard Interval → 400 ns  

### Role of Guard Interval

- Prevents Inter Symbol Interference (ISI)  
- Reduces the effect of multipath fading  
- Improves reliability of wireless transmission  
- Ensures accurate data reception

### Short Guard Interval and Efficiency Improvement

A Short Guard Interval reduces the waiting time between symbol transmissions.

This improves efficiency by:
- Increasing data transmission speed  
- Improving throughput  
- Allowing more data symbols to be transmitted in less time

However, Short GI requires good signal quality and low interference for reliable communication.

---

### 7. Describe the structure of an 802.11 PHY layer frame. What are its key components?

Main components:

- **Preamble** → synchronization  
- **Header** → info about data rate, length  
- **Payload** → actual data
  
<img width="613" height="429" alt="image" src="https://github.com/user-attachments/assets/7c7a1207-eb1b-4549-a877-ce7cbb3997cf" />

---

### 8. What is the difference between OFDM and OFDMA?

# Difference Between OFDM and OFDMA

| Feature | OFDM | OFDMA |
|---|---|---|
| Full Form | Orthogonal Frequency Division Multiplexing | Orthogonal Frequency Division Multiple Access |
| Number of Users | Supports one user at a time | Supports multiple users simultaneously |
| Channel Usage | Entire channel used by a single user | Channel divided among multiple users |
| Efficiency | Moderate | High |
| Latency | Higher | Lower |
| Performance in Crowded Networks | Less efficient | More efficient |
| Used In | Wi-Fi 4 and Wi-Fi 5 | Wi-Fi 6 and later |

### Simple Difference

- OFDM → One user transmits at a time  
- OFDMA → Multiple users transmit together using different subcarriers

### Advantage of OFDMA

- Better bandwidth utilization  
- Improved network efficiency  
- Reduced delay in dense networks  
- Supports many connected devices simultaneously

 ---

### 9. What is the difference between MIMO and MU-MIMO?

| Feature | MIMO | MU-MIMO |
|--------|------|---------|
| Users | Single | Multiple |
| Streams | Multiple streams | Shared streams |
| Efficiency | Good | Better |

**Idea:**
- MIMO → faster for one device  
- MU-MIMO → better for many devices  

---

### 10. What are PPDU, PLCP, and PMD in the PHY layer?

- **PPDU (Physical Protocol Data Unit)**  
  → Actual transmitted frame  

- **PLCP (Physical Layer Convergence Protocol)**  
  → Converts data into transmittable format  

- **PMD (Physical Medium Dependent)**  
  → Handles signal transmission over air  

---

### 11. What are the types of PPDU? Explain the PPDU frame format across different Wi-Fi generations.

Different Wi-Fi generations use different PPDU formats:

| Standard | PPDU Type |
|---------|----------|
| 802.11a/g | Legacy PPDU |
| 802.11n | HT PPDU |
| 802.11ac | VHT PPDU |
| 802.11ax | HE PPDU |

#### Basic structure:
- Preamble  
- Header  
- Data  

---

### 12. How is the data rate calculated?

Data rate depends on:

- Bandwidth  
- Modulation  
- Coding rate  
- Number of streams
- Guard Interval

General idea:
Data Rate ∝ Bandwidth × Modulation × Streams

<img width="428" height="149" alt="image" src="https://github.com/user-attachments/assets/cca414d0-3dcd-4cb6-a7cc-aea0a2eea8f6" />


**Example:**
- More bandwidth → more speed  
- Higher QAM → more bits per symbol  
- More MIMO streams → higher throughput

---
