# WiFi Training Program
## Module 5-Assignment Questions

### 1. What are the key features of Wi-Fi 6, 6E and 7 and how do they differ from previous standards like Wi-Fi 5 (802.11ac)?

**Wi-Fi 5 (802.11ac):**
- Operates only in 5 GHz band
- Uses OFDM (single user transmission at a time)
- Supports high speed but struggles in crowded networks
- Limited efficiency when many devices are connected

**Wi-Fi 6 (802.11ax):**
- Works in both 2.4 GHz and 5 GHz
- Introduces OFDMA (multi-user transmission)
- Better performance in dense environments
- Improved battery efficiency using TWT
- Higher throughput and reduced latency

**Wi-Fi 6E:**
- Extends Wi-Fi 6 into the 6 GHz band
- Provides more channels and wider bandwidth
- Less interference because the band is new and less crowded

**Wi-Fi 7 (802.11be):**
- Supports extremely high speeds
- Uses 320 MHz wide channels
- Introduces Multi-Link Operation (MLO)
- Uses 4K QAM for higher data rates
- Very low latency and high reliability

Difference summary:
- Wi-Fi 5 → High speed but less efficient
- Wi-Fi 6 → High efficiency + supports many devices
- Wi-Fi 6E → Same as Wi-Fi 6 + cleaner spectrum
- Wi-Fi 7 → Next-level speed + ultra low latency

---

### 2. Explain the role of OFDMA in Wi-Fi 6 and how it improves network efficiency.

OFDMA (Orthogonal Frequency Division Multiple Access) is one of the main improvements in Wi-Fi 6.

In older WiFi:
- One device uses the entire channel at a time

In Wi-Fi 6:
- Channel is divided into smaller units called Resource Units (RUs)
- Multiple devices can transmit simultaneously

How it improves efficiency:
- Reduces waiting time for devices
- Supports multiple users at once
- Minimizes delay (latency)
- Works well in crowded places like classrooms, offices

Simple idea:
Instead of one big road → multiple lanes for different users

---

### 3. Discuss the benefits of Target Wake Time (TWT) in Wi-Fi 6 for IoT devices.

Target Wake Time (TWT) allows devices to schedule when they wake up to communicate with the access point.

Working:
- AP and client agree on specific wake-up times
- Device sleeps when not needed

Benefits:
- Saves battery power significantly
- Reduces unnecessary communication
- Avoids collisions between devices
- Ideal for IoT devices like sensors and smart devices

Example:
A sensor wakes every 10 minutes, sends data, then goes back to sleep

---

### 4. Explain the significance of the 6 GHz frequency band in Wi-Fi 6E.

The 6 GHz band is a new frequency band added in Wi-Fi 6E.

Significance:
- Provides large additional spectrum
- Supports more channels (especially wide channels like 80 MHz and 160 MHz)
- Less congestion compared to 2.4 GHz and 5 GHz

Advantages:
- Higher data rates
- Lower interference
- Better performance in dense environments

Limitation:
- Shorter range and less penetration through walls

---

### 5. Compare and contrast Wi-Fi 6 and Wi-Fi 6E in terms of range, bandwidth, and interference.

Range:
- Wi-Fi 6: Better range (supports 2.4 GHz and 5 GHz)
- Wi-Fi 6E: Slightly lower range due to 6 GHz characteristics

Bandwidth:
- Wi-Fi 6E has more available bandwidth because of additional spectrum

Interference:
- Wi-Fi 6: May face interference in crowded bands
- Wi-Fi 6E: Very low interference (new band)

Conclusion:
Wi-Fi 6E gives cleaner and faster performance, but Wi-Fi 6 has better coverage

---

### 6. What are the major innovations introduced in Wi-Fi 7 (802.11be)?

Key innovations:

- 320 MHz channel bandwidth (double of Wi-Fi 6)
- 4K QAM (higher data encoding efficiency)
- Multi-Link Operation (MLO)
- Extremely low latency
- Better spectrum utilization

Result:
- Very high throughput
- Suitable for AR/VR, gaming, 8K streaming

---

### 7. Explain the concept of Multi-Link Operation (MLO) and its impact on throughput and latency.

Multi-Link Operation (MLO) allows a device to use multiple frequency bands at the same time.

Example:
A device can send data using both 5 GHz and 6 GHz simultaneously

Impact:

Throughput:
- Data is transmitted over multiple links → higher speed

Latency:
- Traffic can switch to less congested link → lower delay

Reliability:
- If one link fails, another continues communication

Simple idea:
Using multiple internet lanes at the same time

---

### 8. What is the purpose of 802.11k and v, and how does it aid in roaming?

802.11k:
- Provides information about neighboring access points
- Helps client identify better APs nearby

802.11v:
- Allows network to suggest optimal AP for connection
- Helps in load balancing

How it helps roaming:
- Faster decision making
- Client does not need to scan all channels again

---

### 9. Explain the concept of Fast BSS Transition (802.11r) and its benefit in mobile environments.

802.11r enables fast roaming between access points.

Normal roaming:
- Full authentication process → takes time

With 802.11r:
- Pre-authentication is done
- Key information is shared in advance

Benefits:
- Faster handoff
- No noticeable delay
- Important for voice calls, video streaming

---

### 10. How do 802.11k/v/r work together to provide seamless roaming in enterprise networks?

These three standards work together:

**802.11k:**
- Tells client about nearby APs

**802.11v:**
- Suggests the best AP to connect

**802.11r:**
- Performs fast authentication when switching

Combined result:
- Smooth roaming experience
- No connection drops
- Low latency handoff

Real-life example:
Moving inside a college or office while on a call → no interruption

---
