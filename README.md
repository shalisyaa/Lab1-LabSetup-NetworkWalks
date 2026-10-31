# Lab1-LabSetup-NetworkWalks
Setup VirtualBox and Kali Linux
# Kali Linux Lab Setup Using VirtualBox

## Project Overview

This cybersecurity practical lab project involved me setting up a virtual environment with the use of Oracle VirtualBox and Kali Linux.

The primary aim was to gain an understanding of how virtual machines function, to set up a virtual network, and to get the Kali Linux environment ready for subsequent cybersecurity exercises.

### Lab Setup and Configuration

Throughout this lab, I worked on:

- Setting up and configuring Kali Linux within Oracle VirtualBox.
- Configure a NAT network with the subnet 10.0.0.0/24.
- Set a static IP address of 10.0.0.2/24 on Kali Linux.
- Set the default gateway to 10.0.0.1.
- Setting up DHCP and verifying the IP address range that it has been assigned.
- Make it possible to use shared folders, share the clipboard, and use drag-and-drop functionality.
- Checking the network connectivity and investigating configuration problems.
- Setting up the virtual environment for upcoming cybersecurity practical exercises.

## Challenges Faced

A major challenge for me was setting up the network connection between Kali Linux and VirtualBox.

Even though the network adapter was turned on and the NAT Network settings looked correct, Kali Linux kept on failing to make a connection.

The main issues included:

1. **Ethernet Connection Problems:** The eth0 interface was detected, but it would at times remain disconnected or stay in the connecting state.
2. **Static IP Address Conflict:** NetworkManager found that the IP address `10.0.0.2` was already in use, which stopped the connection from being activated.
3. **DHCP Configuration:** I looked into whether the DHCP settings were causing the problem and checked the address allocation range.
4. **Network Troubleshooting:** Rather than depend solely on the graphical settings, I used commands from Linux and VirtualBox to investigate the connection.

Some of the commands I explored included:

```bash
ip -4 addr
ip -br link
nmcli device status
nmcli connection show
journalctl -u NetworkManager
arping
```

I also used VBoxManage on Windows to check the DHCP and NAT network settings in VirtualBox.

The troubleshooting process took longer than I had expected, but it did help me to understand the relationship between virtual network adapters, IP addressing, DHCP, and network connectivity.

## Skills and Knowledge Gained

Through this lab, I gained practical experience in:

- Virtual machine setup and configuration
- Linux command-line operations
- IPv4 addressing and subnet configuration
- NAT networking and DHCP
- Network diagnostics and troubleshooting
- Identifying and investigating IP address conflicts
- Problem-solving and technical documentation

## Conclusion

This lab has enabled me to gain a better understanding of how virtual machines and network configurations function in a cybersecurity environment.

The hardest aspect was getting the network connection on Kali Linux working, particularly since the system kept showing an IP address conflict. Even though it was sometimes very frustrating, the situation did lead me to look into the error messages, understand what the various commands did, and tackle technical problems in a more systematic way.

The project as a whole served as a useful introduction to carrying out practical cybersecurity work and it made me realize that troubleshooting is an important element of learning IT, just as much as it is necessary to understand why a problem occurs to get the system to work.
