# HITCON 2017 Free Talk - CCleaner 後門事件&2017駭客搶銀行

* 大量散佈的攻擊易取得樣本，容易阻擋->防火牆能擋。
* 若將 config 放在正常的第一線中繼站（Google drive/論壇/github等等），而將惡意程式放在第二個中繼站，則難以偵測。

### 水坑攻擊：網頁掛馬 SWC/軟體供應鏈SCA
## Strategic Wc Compromise, SWC: 在入口網站 政府網站 等有目標族群常來訪，透過瀏覽器 JavaScript Flash Player等漏洞下手

## Supply Chian Attack, SCA: 文書軟體 企業軟體等 有自動更新機制者佳，攻擊大眾常用之軟體公司的 update/download server，從受害者IP中選出真正想攻擊的人進行第二步攻擊。
* Example1: ALZip 的 update server 被入侵，攻擊者篩選出IP為ALZip公司IP之用戶下載時會被導向下載加料版的ALZip
* Example2: XCodeGhost: 被加料過的compiler，在 source socde加料。 
* CCleaner: download 被加料，鎖定科技廠商，植入二階段後門，從 github, wordpress 下載後門指令。卡巴斯基說該後門與APT17 片段 base64相似(?)。
    * 針對性攻擊：鎖定 Intel, Google, Microsoft, Cisco,...近20家科技廠商。（台灣有HTC, DLink,...受害）
    * Avast 原廠承認疏失，公布調查細節，其中中華電訊原在攻擊名單內，不過攻擊者發現已有13台連上，就將該公司徂從清單中移除。ps. 中華電表示連上的都是一般上網用的電腦，非營運用電腦。
    * 誤判原因：
        * 數位簽章是合法原廠的、母公司是Avast防毒公司。
        * Host-based 特徵碼偵測太久：08-15網站換置 09-14 開源 ClamAV社群病毒碼 09-18 公開後還不到十家偵測(?)
        * Network-based 偵測被加密：二線後門被放在 github/wordpress上，一是IP合法，二是SSL解開後，其行為和一般搜尋部落格內容的動作相同。





