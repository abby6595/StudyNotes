# Internet Group Management Protocol (IGMP)
## IGMP Introduction

- **Stream Source**: Multicast Sender
- **Receiver**: Hosts
- IGMP, an intergrated part of **IP multicast**,  operates between a host and a **local multicast router** on IPv4 networks to establish multicast group memberships. It allows multicast sender transmits information to a selected and dynamic group of hosts by referring **one multicasting IP address**.
![](https://i.imgur.com/UJRtg7j.png)

- Multicast management on **IPv6** networks is handled by **Multicast Listener Discovery (MLD)**.
- Applications:
    - **One-to-many networking applicastions** such as online streaming vedio and gaming.
- Benifits: 
    
    - Prevent hosts on a local network from receiving multicast traffic they haven't explicitly joined.
    - Conserving **bandwidth** on communication links: 5 Unicast packets -> 1 packet (flooding)
![](https://i.imgur.com/EeLbtpX.png)


## Multicast
Multicast allows source send messages to a group of destinations/receivers by flooding multicast traffic to all the ports in a broadcast domain (or the VLAN equivalent). However, multicast can cause load on hosts by 

ps. There are three types of network transmissions: Braodcast, Multicast, and Unicast.

## Dynamic Multicasting
1. IGMP membership query
2. IGMP snooping

### Layer 3 Devices (Routers or Switches)
- Send to which **Subnet**
- Layer 3 devices maintain **Multicast routing tables**. 
- Routers will send **Quering messages (aka IGMP membership queries)** to confirm is there any port want to receive multicast messages. This mechanism will automatically executes in a period of time (severl seconds by setting)
    - IGMP general queries from the IGMP querier must be unconditionally forwarded by all switches involved in IGMP snooping.
- Routers/ layer 3 Switches listen **join/leave messages** from clients then update routing tables

### Layer 2 Devices (Switches)
- Send to which **host**
- Layer 2 devices maintain **Multicast group tables** and manage it by **port**. Dynamically forward the traffic to only the ports participations in the group.
- **IGMP snooping** listen to IGMP network traffic between hosts and routers and maintain a map of which links need which IP multicast transmission.
    - IGMP snooping with **proxy reporting (or report suppression)** actively filters IGMP packets in order to reduce load on the multicast router. A switch determines the router need the join/leave information or not (depens on it will affect the status of the group from the router's point of view).
- IGMP membership queries when **ports** join/leave Multicast group tables
- If no join/leave messages -> **flooding**
    - Using RSTP,RTP,RTCP protocols at the first time. If host can reads packets then take it.

## IGMP Membership Query
- Messages to well-known Multicast IP address 224.0.0.1 (All multicast-cabable hosts)
- Layer 3 devices kepp track of which ports belong to which Multicast groups.

ps. 224.0.0.2 (All Multicast routers)
pss. Multicast IP: 224-239 (Class D)

## Communication address
### IP based
224-239 (**Class D**): All Multicast routers
- 224.x.x.x
- 239.x.x.x
- 01:00:5E:xx:xx:xx
### BPDU based

## Versions
### v1
- Defines **Querier, Host**, Join
### v2
- Defines v1 + **leave** and **Specific group**
### v3
- /Black/Whitelist, Specific source, include/exclude, router alert(Without reading payload) 
## Practices
1. DA (224.10.7.100) 換算 Ethernet Multicast Add.
2. H/W 會遇到什麼問題&怎麼設定

## References
- [Internet Group Management Protocol](https://en.wikipedia.org/wiki/Internet_Group_Management_Protocol)
- [IGMP snooping](https://en.wikipedia.org/wiki/IGMP_snooping)