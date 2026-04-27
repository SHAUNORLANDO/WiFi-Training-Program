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

**Simple understanding:**  
- DSSS → spread out  
- FHSS → jump around  

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

- Splits channel into smaller subcarriers  
- Sends data in parallel  

#### Advantages:
- Reduces interference  
- Improves data rate  
- Handles multipath fading  

Used in:
- 802.11a/g/n/ac/ax  

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

Guard Interval prevents overlapping of signals.

#### Types:
- Normal GI: 800 ns  
- Short GI: 400 ns  

#### Benefit of short GI:
- More data transmitted  
- Higher throughput  

**But:** needs good signal quality.

---

### 7. Describe the structure of an 802.11 PHY layer frame. What are its key components?

Main components:

- **Preamble** → synchronization  
- **Header** → info about data rate, length  
- **Payload** → actual data  

**Simple flow:**
Preamble → Header → Data

---

### 8. What is the difference between OFDM and OFDMA?

| Feature | OFDM | OFDMA |
|--------|------|-------|
| Users | Single user | Multiple users |
| Efficiency | Moderate | High |
| Used in | Wi-Fi 4/5 | Wi-Fi 6 |

**Simple:**  
- OFDM → one user at a time  
- OFDMA → many users together  

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

General idea:
Data Rate ∝ Bandwidth × Modulation × Streams


**Example:**
- More bandwidth → more speed  
- Higher QAM → more bits per symbol  
- More MIMO streams → higher throughput

---

