# NETWORKWALKS-SAMUEL-B084N-WEEK1-PM1-CYBERSECURITY-LAB-SETUP
A documented record of my Week 1 cybersecurity internship assessment, covering lab setup, configuration, verification, and troubleshooting.

# Cybersecurity Lab Setup: Networkwalks Week 1 Assessment

## 1. Project Overview

* **Project Title:** Cybersecurity Lab Setup and Network Configuration
* **Program:** Networkwalks Cybersecurity Internship
* **Assessment:** Week 1
* **Virtualisation Platform:** Oracle VirtualBox
* **Guest Operating System:** Kali Linux
* **Network Type:** NAT Network
* **Network Name:** NatNetwork

**Summary:** This project documents the setup of a virtualised cybersecurity lab using Oracle VirtualBox and Kali Linux. The assessment involved configuring a dedicated NAT Network, setting up the Kali Linux network adapter, inspecting network settings, and successfully testing network connectivity.

---

## 2. Lab Environment and Configuration

The following environment and network settings were used for the lab setup.

* **Host Operating System:** Windows 11
* **Virtualisation Software:** Oracle VirtualBox
* **Guest Operating System:** Kali Linux
* **Network Name:** NatNetwork
* **IPv4 Network Prefix:** `10.0.0.0/24`
* **DHCP:** Enabled
* **IPv6:** Disabled

---

## 3. VirtualBox NAT Network Configuration

A dedicated NAT Network named `NatNetwork` was configured in VirtualBox to provide network connectivity for the Kali Linux virtual machine.

The following settings were applied:

* **Network Name:** NatNetwork
* **IPv4 Prefix:** `10.0.0.0/24`
* **Enable DHCP:** Enabled
* **Enable IPv6:** Disabled

DHCP was enabled to allow connected virtual machines configured for automatic addressing to obtain IPv4 addresses from the network's DHCP service.

### Screenshot: NAT Network Configuration

![VirtualBox NAT Network Configuration](Screenshot%20(469).png)

---

## 4. Kali Linux Network Adapter Configuration

The Kali Linux virtual machine's network adapter was configured to connect to the `NatNetwork` NAT Network.

The following settings were applied:

* **Enable Network Adapter:** Enabled
* **Attached to:** NAT Network
* **Name:** NatNetwork
* **Promiscuous Mode:** Deny
* **Cable Connected:** Enabled

Promiscuous Mode was set to `Deny` for the initial lab setup, as monitoring traffic belonging to other virtual machines was not required for this configuration.

### Screenshot: Kali Linux Network Adapter

![Kali Linux Network Adapter Configuration](Screenshot%20(460).png)

---

## 5. Network Configuration Inspection

After configuring the virtual network and adapter, Kali Linux was started and its network configuration was inspected using the following commands.

```bash
ip -4 addr
ip route
```

* `ip -4 addr` was used to inspect the IPv4 addresses assigned to the network interfaces.
* `ip route` was used to inspect the routing table and identify the default route, where configured.

These commands helped verify the network interface's addressing and routing configuration.

### Screenshot: IP Address and Routing Table

![Kali Linux IP Address and Routing Table](Screenshot%20(473).png)

---

## 6. Network Connectivity Test

A network connectivity test was performed after the network configuration was completed.

**Result:** Successful.

The successful test confirmed that the tested network connection was working as expected. This was an important verification step before proceeding with further cybersecurity lab activities.

### Screenshot: Successful Connectivity Test

![Successful Kali Linux Network Connectivity Test](Screenshot%20(472).png)

---

## 7. Troubleshooting and Verification

The network configuration was inspected to confirm that the Kali Linux virtual machine was connected to the intended NAT Network.

The verification process included:

* Reviewing the NAT Network configuration in VirtualBox.
* Checking the Kali Linux network adapter settings.
* Inspecting the IPv4 address configuration.
* Reviewing the routing table.
* Performing a network connectivity test.

The connectivity test completed successfully, confirming that the tested connection was operational.

---

## 8. Shared Clipboard and Drag-and-Drop Configuration

To improve interaction between the Windows 11 host system and the Kali Linux virtual machine, the VirtualBox shared clipboard and drag-and-drop features were configured.

The following settings were used:

* **Shared Clipboard:** Bidirectional
* **Drag and Drop:** Bidirectional

Bidirectional mode allows supported text and file drag-and-drop operations between the host and guest operating systems.

These features help make the lab environment easier to use by allowing information to be transferred between Windows and Kali Linux without manually retyping content.

### Screenshot: Shared Clipboard and Drag-and-Drop Settings

![VirtualBox Shared Clipboard and Drag and Drop Configuration](Screenshot%20(463).png)

---

## 9. Shared Folder Configuration

A shared folder was configured in VirtualBox to provide a convenient way to exchange files between the Windows host system and the Kali Linux virtual machine.

The shared folder feature allows an assigned host directory to be accessed from the guest operating system, subject to the configured permissions and Guest Additions support.

The configuration involved:

* Selecting the shared folder option in the Kali Linux virtual machine settings.
* Choosing the appropriate folder on the Windows host.
* Configuring the folder name and access options.
* Enabling automatic mounting where configured.
* Checking access to the shared folder from Kali Linux.

### Screenshot: VirtualBox Shared Folder Settings

![VirtualBox Shared Folder Configuration](Screenshot%20(464).png)

### Shared Folder Verification

After configuring the shared folder, its accessibility from Kali Linux was checked.

![VirtualBox Shared Folder Verification](Screenshot%20(474).png)


---


## 10. Key Learnings

Through this assessment, I gained practical experience in:

* Preparing a virtualised cybersecurity lab environment.
* Configuring a NAT Network in Oracle VirtualBox.
* Enabling DHCP for automatic IPv4 address assignment.
* Configuring Kali Linux virtual machine network settings.
* Inspecting IP addresses and routing information using Linux commands.
* Verifying network connectivity.
* Documenting technical configurations with screenshots.

---

## 11. Conclusion

The Week 1 lab setup assessment provided practical experience in preparing a virtualised environment for cybersecurity learning.

The `NatNetwork` NAT Network was configured with the IPv4 prefix `10.0.0.0/24`, DHCP enabled, and IPv6 disabled. The Kali Linux network adapter was connected to the network, and the connectivity test was successful.

This environment provides a foundation for subsequent cybersecurity exercises and practical lab activities.
![Kali Linux](Screenshot%20(471).png)


---

## 12. Repository Evidence

The `screenshots` contain visual evidence of the lab configuration and verification process.

The screenshots document the VirtualBox NAT Network settings, Kali Linux adapter configuration, network inspection commands, and successful connectivity test.

**Author:** Samuel Adekoya

**Program:** Networkwalks Cybersecurity Internship

**Assessment:** Week 1 — Lab Setup
