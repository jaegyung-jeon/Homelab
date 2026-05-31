# opnsense installation $ setup

Networking homelab


                           HOME NETWORK TOPOLOGY

                                    Internet
                                        │
                                        │
                              ┌─────────────────┐
                              │  ISP Home Router│
                              └─────────────────┘
                                        │
                                        │
                                 WAN Network
                                        │
                                        ▼
                     ┌─────────────────────────────┐
                     │     PC03 <I350 T2 NIC>      │
                     │      OPNsense Firewall      │
                     │                             │
                     │                             │
                     └─────────────────────────────┘
                                   │
                                   │
                                   │ LAN Network
                                   ▼
                            ┌─────────────┐
                            │ 8-Port      │
                            │ Switch      │
                            └─────────────┘
                                  │
                      ┌─────────────────────────┐
                      │           │             │
                      ▼           ▼             ▼
                   PC01          PC02        pc03
                 




Hardware List:
- PC01 (Client, Widows 11)  (Dell Optiplex i5-10500T, 32GB RAM)
- PC02 (Client, Linux bare metal)  (Lenovo Tiny   i5-8500T,  16GB RAM)
- PC03 (OPNsense VM Host, Proxmox bare metal)  (Lenovo Tiny   i5-8500T,  16GB RAM,  Dual port I350 NIC Installed)
- 8-Port Gigabit Switch

Current Objectives:
- Install and configure OPNsense
- Configure WAN/LAN networks
- Provide DHCP and DNS services
- Connect client devices through OPNsense




## 1. Install & Verify double port NIC card on pc03

![IIS Test](03screenshots/16.png)

>>* enp1s0f0 : NIC port 1
>>* enp1s0f1 : NIC port 2
>>* nic0     : Onboard Ethernet port
>>* wlp3s0   : WIFI card


## 2. Install opnsense

![IIS Test](03screenshots/18.png)


configure 2 ports to WAN/LAN
>vmbr1 - WAN(internet)

>vmbr2 - LAN(local)

## 3. Check LAN/WAN ip address

![IIS Test](03screenshots/19.png) 

LAN-STATIC IP ADDRESS ; because it is supposed to be switch connected device's gateway</br>
WAN-DHCP ASSIGNED ADDRESS ; client side of ISP router
