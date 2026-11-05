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





