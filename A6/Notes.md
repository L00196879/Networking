# Assigment 6 Diagram and Testing

## 1. Diagram
![Diagram](Images/Diagram.png)

## 2. Notes
### Network Overview
* Data Centre 1 - **DC01**
* Data Centre 2 - **DC02**
* Head Office - **HO**
* Portmarnock site 47 - **EP47**

### Firewalls
  | Name | IP Address | Location |
   |-----|------|------|
  |FW-DC01|192.168.122.191| Datacentre 1 |
  |FW-DC02|192.168.122.248|Datacentre 2|
  |FW-HO|192.168.122.96|Head Office|
  |FW-EP47|192.168.122.96|Portmarnock|
 ### Firewall Interfaces
 | Interface | Role | Description |
 |-----------|------|-------------|
 | port1     | WAN  | NAT        |
 | port2     | LAN  | Internal users        |
 | port3 (DC01 & DC02)    | DMZ  | Web Servers |
 
## 3. Internet Test
To test internet connectivity, pings were ran to the NAT gateway from a PC and a router set up as a server on each site.
| Name  | Site | IP Address | Static/DHCP | Result |
|---------|---------------|-------------|------|---------|
| DC01-PC1| Data Centre 1 | 10.1.14.100 | DHCP | Success |
| DC01-SRV01| Data Centre 1 | 10.1.14.50 | Static | Success |
| DC02-PC1| Data Centre 2 | 10.2.14.100 | DHCP | Success |
| DC02-SRV01| Data Centre 2 | 10.2.14.60 | Static | Success |
| HO-PC1| Head Office | 10.0.14.100 | DHCP | Success |
| EP47-PC1| Portmarnock site | 10.47.14.100 | DHCP | Success |

## 4. Access for external partys
The DMZ should have been set up to allow access for external partys via the WAN, so web servers can be hosted on there
For external contractors, guest access can be configured to allow them limited access, which can be done via the user groups in the GUI of the Forigate. 
Additional authorisation should, be implemented, such as username and password, as well as 2FA if possible
Network segmentation should also be used, and logs should be taken of user activity.
