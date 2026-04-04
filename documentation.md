# Home Network Documentation

**Author:** Lateefah Alli  
**Date:** March 31, 2026  
**Version:** 1.1  

---

## 1. Physical Topology

The home network follows a star topology, where all devices connect to a central wireless router. All devices connect wirelessly through the router’s WLAN interface, while the modem connects via Ethernet to the router’s WAN port. This creates a centralized communication structure where the router acts as the hub of the network.

### Devices and Connections:

* **ISP Modem (Living Room)**
  - Connected to the router using an Ethernet cable (WAN port)

* **Wireless Router (Living Room)**
  - WAN Interface: Connected to ISP modem
  - LAN Interface: Internal network gateway (192.168.1.1)
  - Wireless Interface (WLAN0): Provides Wi-Fi connectivity

* **iMac (Basement)**
  - Connected via Wi-Fi (WLAN0)

* **Smart TV (Living Room)**
  - Connected via Wi-Fi (WLAN0)

* **Laptops (Various Rooms)**
  - Connected via Wi-Fi (WLAN0)

* **iPad (Bedroom)**
  - Connected via Wi-Fi (WLAN0)

* **Smartphones (Various Rooms)**
  - Connected via Wi-Fi (WLAN0)




---

## 2. Logical Topology

The network operates on a **private IP addressing scheme** using a star topology, with all communication managed by the router.

* **Network Type:** Star Topology  
* **IP Range:** 192.168.1.0/24  

### Communication Flow:

All devices communicate through the router:

* **Internal Communication:** 
  - The router directs traffic within the local network

* **External Communication (Internet Access):**
  - The router uses NAT to translate private IP addresses into a public IP

### Network Segmentation:

The network operates on a **single subnet (192.168.1.0/24)** with no VLAN segmentation. All devices share the same broadcast domain.

### Address Assignment:

* Router uses a static IP address (192.168.1.1)
* All other devices receive IP addresses dynamically via DHCP

---

## 3. Addressing Documentation

| Device       | IP Address     | Type |
|-------------|---------------|--------|
| Router      | 192.168.1.1   | Static |
| iMac        | 192.168.1.101 | DHCP   |
| Smart TV    | 192.168.1.102 | DHCP   |
| Laptop      | 192.168.1.103 | DHCP   |
| Smartphone  | 192.168.1.104 | DHCP   |
| iPad        | 192.168.1.105 | DHCP   |

---

## 4. Network Settings

* **Subnet Mask:** 255.255.255.0  
* **Default Gateway:** 192.168.1.1  
* **DHCP Range:** 192.168.1.100 – 192.168.1.200  
* **DNS Server:** Provided by ISP  

---

## 5. Network Devices & Services

### Devices:

* ISP Modem  
* Wireless Router  
* iMac  
* Laptops  
* Smartphones  
* Smart TV  
* iPad  

### Services:

* **DHCP (Dynamic Host Configuration Protocol):**  
  Automatically assigns IP addresses to devices on the network.

* **NAT (Network Address Translation):**  
  Converts private IP addresses to a public IP address for internet communication.

* **DNS (Domain Name System):**  
  Translates domain names (e.g., google.com) into IP addresses.

* **Wi-Fi (Wireless Networking):**  
  Provides wireless connectivity to all devices in the network.

---

## 6. Device Configurations

### Router Configuration:

* SSID: Home_Network  
* Security Type: WPA2/WPA3  
* Frequency Bands: 2.4 GHz and 5 GHz  
* DHCP: Enabled  
* DHCP Range: 192.168.1.100 – 192.168.1.200  
* NAT: Enabled  
* Firewall: Enabled (basic traffic filtering)  

---

### End Devices (iMac, Laptops, Smartphones, iPad, Smart TV):

* DHCP enabled (automatic IP configuration)  
* Connected via Wi-Fi  
* No manual IP configuration required  

---

## 7. Storage of Passwords

Login credentials are stored securely using a password manager.

* Password Manager: Bitwarden  
* Passwords are encrypted and not stored in plain text  
* Two-factor authentication (2FA) is enabled for added security  

No sensitive credentials are included in this documentation to maintain security.

---

## 8. Network Diagram

The network diagram was created using draw.io to visually represent both the physical and logical topology.

![Network Topology](network.drawio(1).png)

---


## 9. Summary

This documentation provides a complete overview of the home network, including physical layout, logical operation, addressing, and services. The network is designed for simplicity, efficiency, and secure internet access using standard home networking technologies.

