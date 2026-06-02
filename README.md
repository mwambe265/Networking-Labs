# Networking-Labs
# Custom EVE-NG Network Topologies

Welcome to my personal repository of custom network topology files created using the **EVE-NG (Emulated Virtual Environment Next Generation)** platform. 

This repository serves as a central lab hub for importing, studying, testing, and validating various networking scenarios, protocols, and architectures.

---

## 🚀 Repository Contents

This repository is organized by technology and use-case. Each topology directory contains the exported `.zip` or `.unl` file, along with relevant startup configurations or documentation.

| Category / Technology | Description | Status |
| :--- | :--- | :--- |
| **Core Networking** | OSPF, BGP, MPLS, and advanced routing/switching labs. |🟡 In Progress  |
| **Telecom & Core Infrastructure** | DNS (BIND), PCRF, and mobile core architecture scenarios. | 🟡 In Progress |
| **Network Automation** | Labs integrated with Prometheus, Grafana, and automated health-checks. | 🟡 In Progress  |
| **Security & Edge** | Firewall deployments, NAT, and secure edge configurations. | 🟡 In Progress  |

---

## 🛠️ Prerequisites

To run these topologies, you will need:
* An active instance of **EVE-NG** (Community or Professional edition).
* Appropriate **QEMU / IOL / Dynamips images** matching the nodes used in the labs (e.g., Cisco IOS, Ubuntu/Linux servers, VyOS, Nokia, etc.). *Note: Image binaries are not included in this repository due to licensing.*

---

## 📥 How to Import and Use

### Method 1: Direct UI Upload (Recommended)
1. Download the desired `.unl` file or the exported topology `.zip` package from this repository.
2. Log into your EVE-NG Web GUI.
3. Click the **Import** button in the file manager.
4. Select the downloaded file and upload it.
5. Open the lab, ensure your nodes are mapped to the correct images, and power them on.

### Method 2: CLI Import via SSH
If you have a packaged `.zip` export, you can copy it directly to your EVE-NG server:
```bash
# SCP the zip file to your EVE-NG server's export directory
scp topology_name.zip root@<EVE-NG-IP>:/opt/unetlab/labs/

# Fix permissions on the EVE-NG server (Crucial Step!)
/opt/unetlab/wrappers/unl_wrapper -a fixpermissions
