# CISCO-Network-Troubleshooting-Lab
This lab covers IPv4 addressing, DHCP, routing, and connectivity issues

SMALL OFFICE NETWORK TROUBLESHOOTING LAB
CISCO PACKER TRADER

REASON:
A small office neeeds a network for their Administration and Sales departments. As the simulated IT technician, I am configuring the network, testing connectivity, and documenting troubleshooting incidents.

TOOLS:
1 Cisco 2911 router 
2 Cisco 2960 switches 
4 PCs, with 2 per department 
Router connected through separate subnets
DHCP used for automatic IP configuration

ADDRESSING
Device                       |      IP address    |  Subnet Mask   |  Default gateway
Office-R1 G0/0-Administration|      192.168.10.1  |  255.255.255.0 |    N/A
Office-R1 G0/1- Sales        |      192.168.20.1  |  255.255.255.0 |    N/A
Admin-PC1                    |      192.168.10.21 |  255.255.255.0 |    192.168.10.1
Admin-PC2                    |      192.168.10.22 |  255.255.255.0 |    192.168.10.1
Sales-PC1                    |      192.168.20.21 |  255.255.255.0 |    192.168.20.1
Sales-PC2                    |      192.168.20.22 |  255.255.255.0 |    192.168.20.1


CONFIGURATION
> Verified the routers interfaces to show up/up
> Confirming all 4 PCs received addresses from their department's subnet
> Made sure Administration and Sales got their own separate DHCP pools 
> Labeled and connected all the network devices

CONNECTIVITY TESTING
Routers uses directly connected routers for communication between the subnets.
The Admin-PC1 reached their gateway that being 192.168.10.1. The Sales-PC1 also reached 
theirs, 192.168.20.21. Which returned all packets at 0% packet loss.


## Screenshots

### Network Topology
<img width="650" height="276" alt="Screenshot 2026-11-09 at 5 56 24 PM" src="https://github.com/user-attachments/assets/e8f6c0a5-853f-439d-80fb-217244c3cf81" />

### Router Interfaces
<img width="658" height="510" alt="ROUTER" src="https://github.com/user-attachments/assets/6d303dfd-97de-4613-82be-c3d51eb8756a" />

### DHCP Configuration
<img width="650" height="220" alt="DHCP" src="https://github.com/user-attachments/assets/221ab8df-2f8f-4a05-82f5-a7eea4da499a" />

### DHCP Address Assignment
<img width="1178" height="201" alt="DHCP ADDRESS " src="https://github.com/user-attachments/assets/8f25f1a7-1883-491a-b969-b757e568ac65" />


### Administration-to-Sales Connectivity
<img width="303" height="467" alt="Admin connection 2" src="https://github.com/user-attachments/assets/fa15dbdb-df6a-4279-9b4a-93ed25e87cd6" />

