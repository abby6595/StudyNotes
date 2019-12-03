# Internet Group Management Protocol_20191203
## Introduction
- **Stream Source** send multicast packets
- IGMP allows L3 & L2 devices routing multicast packets
    - Has join/leave -> manage by **port**
        - Stream Source will send **Quering packet** to confirm is there any port want to receive multicast packets. This mechanism will automatically executes a period of time (severl seconds by setting)
    - No join/leave -> **flooding** (IGMP L2 Snooping)
- **Receivers** send **Join/Leave** request to require receiving a specific group multicast or not 

## Communication address
### IP based
- 224.x.x.x
- 239.x.x.x
- 01:00:5E:xx:xx:xx
- IP mapping MAC
### BPD_(?) based