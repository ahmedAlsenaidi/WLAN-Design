# WLAN Network Design and Configuration

This project showcases the design and configuration of a secure Wireless Local Area Network (WLAN) for a two-floor company. It involves the use of VLANs, RADIUS-based authentication, and differentiated access for various departments.

## 📚 Table of Contents
- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Network Design](#network-design)
- [Device Configurations](#device-configurations)
- [How to Use](#how-to-use)
- [Authors](#authors)

---

## 🔍 Introduction
The purpose of this project is to create a scalable and secure WLAN for a company with the following requirements:
- VLAN separation for departments.
- RADIUS-based authentication for secure access.
- Differentiated access control using multiple SSIDs.

---

## 🛠️ Technologies Used
- VLANs (10, 20, 30, 40) for traffic segmentation.
- RADIUS Server for authentication.
- DHCP Server for dynamic IP allocation.
- Cisco Switches (3560, 2960) for device configuration.
- Wireless LAN Controller (WLC) for wireless access management.

---

## 🏗️ Network Design
- **VLANs**:
  - VLAN 10: Management (10.10.10.0/24)
  - VLAN 20: HR Department (10.10.20.0/24)
  - VLAN 30: IT Department (10.10.30.0/24)
  - VLAN 40: Trainees (10.10.40.0/24)

- **Connections**:
  - Trunk links between core switch, AP switch, and server switch.
  - Access links for individual departments and servers.

- **Security**:
  - RADIUS for HR and IT authentication.
  - WPA2-PSK for trainees.

For a detailed network diagram, refer to the `diagrams/` folder.

---

## 📑 Device Configurations
### Core Switch (3560-24PS)
- VLANs created for segmentation.
- Trunking enabled for communication between switches.
- Sample configuration file: [Core Switch Config](configurations/core_switch_config.txt)

### Access Point (AP) Switch (2960 IOS15)
- Trunking configured for access points.
- Access ports set for HR and IT departments.
- Sample configuration file: [Access Point Config](configurations/access_point_config.txt)

### Server Switch
- Trunk link for server communication.
- Access links for DHCP and RADIUS servers.
- Sample configuration file: [Server Switch Config](configurations/server_switch_config.txt)
