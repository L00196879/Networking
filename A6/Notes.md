# Assigment 6 Diagram and Testing

## 1. Diagram
![Diagram](A6/Images/Diagram.png)

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

  
