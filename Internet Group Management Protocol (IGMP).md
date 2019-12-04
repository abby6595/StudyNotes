# Internet Group Management Protocol (IGMP)
## IGMP Introduction

- Stream Source: Multicast Sender
- Receiver: Hosts
- IGMP is operated on layer 2 switches and layer 3 routers/switches. It allows stram source transmits information to a selected and dynamic group of receivers by referring one Multicasting IP address.

## Multicast
Multicast allows source send messages to a group of destinations/receivers.

ps. There are three types of network transmissions: Braodcast, Multicast, and Unicast.

## Dynamic Multicasting
1. IGMP membership query
2. IGMP snooping

### Layer 3 Devices (Routers or Switches)
- Layer 3 devices maintain **Multicast routing tables**. 
- Routers will send **Quering messages (aka IGMP membership queries)** to confirm is there any port want to receive multicast messages. This mechanism will automatically executes in a period of time (severl seconds by setting)
- Routers/ layer 3 Switches listen **join/leave messages** from clients then update routing tables

### Layer 2 Devices (Switches)
- Layer 2 devices maintain **Multicast group tables** and manage it by **port**. Dynamically forward the traffic to only the ports participations in the group.
- **IGMP snooping** reads IGMP traffic between hosts (receivers) and routers (or queriers) IGMP membership queries when **ports** join/leave Multicast group tables
- If no join/leave messages -> **flooding**

## IGMP Membership Query
- Messages to well-known Multicast IP address 224.0.0.1 (All multicast-cabable hosts)
- Layer 3 devices kepp track of which ports belong to which Multicast groups.

ps. 224.0.0.2 (All Multicast routers)
pss. Multicast IP: 224-239 (Class D)

## Communication address
### IP based
224-239 (Class D): All Multicast routers
- 224.x.x.x
- 239.x.x.x
- 01:00:5E:xx:xx:xx
### BPDU based
