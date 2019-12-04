# 20191128 STP Note by AB
## Note
- 為何需要 redundent network?
    - 避免單點故障
    - 有其他通訊路線可走
- STP: Redundent Protocol
    - 找根(找到根就不會成環，一個網路只有一個switch設為根)
        - Multicast BPDU(控制封包):只有支援STP的才需要讀懂與處理此封包
            - BridgeID=Priority+MAC address
            - Hello time: default 2-second 丟一次
        - 比 Priority
            - Bandwidth
            - Priority
            - Port#(以Root port#愈小愈優)
        - 比出優劣後 switch 指向 root
            - flood root packet 但不會自己產生
    - Root Port: 每一台switch找出離root最優之路線(On non-root switch)
        - 各switch決定自己的 root port, 不需要也不用知道其他人的 root port 是哪一個 
    - Designated Port: 每一條connection上一定要有一個

## QA
1. 為何一個廣播封包就能癱瘓成環網路?
好比在一個狹小空間中對麥克風說話，聲音透過擴大機放大後，再由喇叭送出。然而放大後的聲音對到了麥克風產生噪音，而麥克風收到的聲音不斷地放大，若不中止此循環，該噪音最後就會大到無法工作。
![](https://i.imgur.com/SXVymxf.png)
舉例:
A 發送一個廣播 -> B, D 收到廣播後又會分別 flood 給 C
C 收到 B 的廣播 flood 給 D 並且將 D 的廣播 flood 給 B
B 收到 C 的廣播 flood 給 A -> A 收到 B 的廣播 flood 給 D
D 收到 C 的廣播 flood 給 A -> A 收到 D 的廣播 flood 給 B
=> switch 每收發送一次就會產生一個封包而這些封包又無網路設備處理終止循環
=> switch 不斷轉發接收廣播封包 => 系統資源耗盡 => 癱瘓
![](https://i.imgur.com/xG5JSQa.png)


3. MAC 如何用來判斷優先順序?

Just compare the numbers together until you get to the first number that are not alike, whichever is lower that is the lower MAC address

0010.7bcc.73**3**a
0010.7bcc.73**4**7
=> 3 is lower then 4 so the first one is lower

0010.7bcc.732**0**
0010.7bcc.732**d**
=> 0 is lower than d so the first one is lower.

## References
- 校園網路障礙：接線迴圈(LOOP)簡介: http://hc.cyc.edu.tw/modules/tadnews/index.php?nsn=49
- How to choose which mac-address has lower value in STP: https://community.cisco.com/t5/switching/how-to-choose-which-mac-address-has-lower-value-in-stp/td-p/1375853
