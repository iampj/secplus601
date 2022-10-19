# **Securing Your Network**

## **Exploring Advanced Security Devices**

### **Understanding IDSs and IPSs**
`Intrusion detection systems` (IDS) monitor a network and send alerts when they detect suspicious events on a system or network.

`Intrusion prevention systems` (IPS) react to attacks and prevent them from reaching systems and networks.

#### **HIDS**
`Host-based intrusion detection system` is additional software installed on a system such as a workstation or server. It protects the individual host, can detect potential attacks, and protects critical operating system files.

#### **NIDS**
`Network-based intrusion detection system` monitors activity on the network. NIDS cannot detect anomalies on individual systems or workstations unless the anomaly causes a significant difference in network traffic.

#### **Sensor and Collector Placement** 
Depends on what you want to measure...

 - `Internet side` - will see all traffic and attacks on your network.
 - `Internal side` - will see what attacks make it into your network.
 - `Both sides` - lol just have two sensors duh.

#### **Detection Methods**
There are two primary detection methods:
 - `Signature-based (also called definition-based)` - uses a database of known vulnerabilities or known attack patterns.
 - `Heuristic- or behavioral-based (also called anomaly-based)` - Starts by collecting data on the network identifying the networks regular operation or normal behavior.

#### **Data Sources and Trends**
IDS commonly include an `aggregator` to store log entries from dissimilar systems. The IDS can analyze these log entries to provide insight to trends.

#### **Reporting Based on Rules**
IDS reports on events of interest based on rules configured within the IDS.

#### **False Positives Versus False Positives**

|                   | **Accurate**                       | **Not Accurate**                    |
|-------------------|------------------------------------|-------------------------------------|
| **No Attack**     | True Negative _(No alarm/alert)_   | False Positive _(Alarm/alert sent)_ |
| **Actual Attack** | True Positive _(Alarm/alert sent)_ | False Negative _(No alarm/alert)_   |


---

### **IPS Versus IDS-Inline Versus Passive**
| **IPS** 🛡                                                                                             | **IDS** 👀                                                                                                        |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Can detect, react to, and prevent attacks                                                            | Monitors and will respond after detecting an attack, but it doesn't prevent attacks                             |
| Is inline with traffic (all traffic passes through the IPS, and the IPS can block malicious traffic) | Is out-of-band with traffic. (it does monitor network traffic, but the traffic does not travel through the IDS) |

### **Honeypots** 🍯
A `honeypot` is a sweet looking server, or at least to an attacker. The server is often poorly locked down as to bait in an attack as the admins can analyze the attack and harden the main servers while not losing any of the CIA triad. Main goals being:
 - `Deceive the attackers and divert them from the live network`
 - `Allow observation of an attacker`

### **Honeynets** 🍯🍯🍯
A `honeynet` is a group of honeypots within a separate network or zone but accessible from an organization's primary network.

### **Honeyfile** 🍯📄
A `honeyfile` is a file designed to attract the attention of an attacker. The primary way a file can attract an attacker is by the name. (_i.e. password.txt_) 😂

### **Fake Telemetry**
Telemetry refers to collecting information such as statistical data and measurements and forwarding it to a centralized system for processing. `Fake telemetry` corrupts the data sent to monitoring systems and can disrupt a system.

---

## **Securing Wireless Networks**

### **Reviewing Wireless Basics**
 - `Access Point` - connects wireless clients to a wired network. However, many APs also have routing capabilities.
 - `All wireless routers are APs` - These are APs with an extra capability-routing.
 - `Not all APs are wireless routers` - Many APs do not have any additional capabilities.

#### **Band Selection and Channel Overlaps**
 - `2.4GHz` - far reaching / steady 
 - `5GHz` - near reaching / faster speeds

#### **Access Point SSID**
Wireless networks are identified by a service set identifier (SSID), which is simply the wireless network name.

#### **Enabling MAC Filtering**
The `MAC` address (also called a physical address or hardware address) is a 48-bit hexadecimal address used to identify network interface cards (NICs). `Media access control (MAC) filtering` can be enabled on many wireless routers. 

Note:
```
MAC filtering can restrict access to a wireless network to specific devices. However an attacker can use a sniffer to discover allowed MAC addresses and proceed to MAC clone (change its MAC signature on their machine to gain access to the network) aka "MAC cloning attack"
```

---

### **Site Surveys and Footprinting** 🗺 🦶
`Site surveys` examine  the wireless env to identify potential issues such as areas with noise or other devices operating on the same frequency bands. They can often also generate `heat maps` of the physical location, which gives you a color-coded representation of wireless signals. Wireless `footprinting` creates a detailed diagram of APs and hotspots within an organization. By overlaying the heat map onto a basic architectural drawing of an organization's space. It's possible to see the location of the APs along with the `dead spots` and `hotspots`.

### **Wireless Access Point Placement**
The most commonly used wireless antenna on both APs and wireless devices is an omnidirectional (or omni) antenna.

### **Wireless Cryptographic Protocols**
Because wireless networks broadcast over the air, anyone who has a wireless can intercept the transmissions.

Note:
```
In the early days of wireless networks, security 
```

#### **WPA2 and CCMP**

#### **Open, PSK, and Enterprise Modes**

#### **WPA3 and Simultaneous Authentication of Equals**

---

### **Authentication Protocols**

### **IEEE 802.1X Security** 

### **Controller and Access Point Security**

### **Captive Portals**

---

## **Understanding Wireless Attacks**

### **Disassociation Attacks**

### **Wi-Fi Protected Setup**

### **Rogue Access Point**

### **Evil Twin**

### **Jamming Attacks**

### **IV Attacks**

### **Near Field Communication Attacks**

### **RFID Attacks**

### **Wireless Replay Attacks**

### **War Driving and War Flying**

---

## **Using VPNs for Remote Access** 

### **VPNs and VPN Appliances**

### **Remote Access VPN**

#### **IPsec as a Tunneling Protocol**

#### **SSL/TLS as a Tunneling Protocol**

#### **Split Tunnel Versus Full Tunnel**

#### **Site-to-site VPNs**

#### **Always-On VPN**

#### **L2TP as a Tunneling Protocol**

#### **HTML5 VPN Portal**

---

### **Network Access Control**

#### **Host Health Checks**

#### **Agent Versus Agentless NAC**

---

### **Authentication and Authorization Methods**

#### **PAP**

#### **CHAP**

#### **RADIUS**

#### **TACACS+**
