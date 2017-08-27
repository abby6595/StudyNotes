# HITCON Community 2017 共同筆記 Collaborative Notes

歡迎大家來一起寫共筆！

即時口譯：http://interpreter.hitcon.org/
綿羊牆：http://sheep.hitcon.org/

## Wargame
* Score Board
    * https://mini.hitcon.org
    * https://badge.hitcon.org
    > 要登入HITCON wifi才能登入
* [Badge_Manual](https://github.com/x43x61x69/HITCON-Badge)

# 8/25 Day 1

### [R0]開幕


https://github.com/x43x61x69/HITCON-Badge
HITCON CMT 2017電子BADGE說明
 HITCON 大ALAN 主講
    我國第一次用電子BADGE，這是入場券加挑戰題目，稍後也到攤位可買，並加入挑戰
    雖然很難製作，因此只超限量。希望明年可繼續挑戰，歡迎提供改良意見
    可用電池或接USB，有藍芽與紅外線，有跑馬燈，有按鈕，有光感應器，有WIFI
    MTK 7697完全相容 可寫arduino語言
    貪食蛇遊戲
    第一個破題者，送明年門票
    請大家各抓各的寶，勿集中到某張BADGE
    跑馬燈可寫名字
    四樓有維修區+寫名字教學
    注意: 電子元件小心燙，建議用USB行動電源，有點耗電，除非可以用愛發電
    USB接座焊接別大力，相關說明IRC會貼
    後續會把設計稿公開，讓大家運用BADGE自行研究BLE加密、物聯網與韌體安全

### [R0]Keynote：臺灣資安人才教育 Cybersecurity Education in Taiwan
- 講師：吳宗成教授   
- 吳宗成教授   
- 台灣資安人才教育、吳宗成、台科大資訊管理系特聘教授、教育部資訊安全人才培育計畫主持人
- 資安人才養成過程：社群教育、自我學習、互動學習 (教育部只是要滿足個人需求, 更要滿足他人期待, 才是有效的"教育")
- 在學教育 / 在職教育 / 社群教育 (若三個情境可以融合在一起更能夠引發有成教的"教育")
- 教育目標：人手(know)→人才(have)→人物(who you are)：如何培育資安人才，達到以上的連結
  - What you know ==> 人手 (具有知識, 理解特定事物)
  - Why you have ==> 人才 (具有能力, 應用特定事物)
  - Who you are ==> 人物 (具有聲望, 被他人認可為特定事務的專家)

    - Note1: 業界似乎尋求人才勝於人物, 因為人物往往很難"被管理", 人物最後自行創業的比例較高, 所以可能要先理解自己想要領薪水還是發薪水.
    - Note2: 滿足他人期待對於教育來講是兩面刃, 因為培育領導者與培育被領導者是不同方向, 要滿足"老闆期待", 還是滿足"社會期待", 這個問題才是重點
    - Note3: 資安本來就是燒錢, 所以個人竊以為沒有過度投注的議題, 重點是國家是否要發展以及業界是否要發展, 方向確立後, 錢其實不是問題

- 人手/人才/人物的金字塔已經出現斷層, 人手很多, 但是人才有限, 人才有限, 但是人物更為稀有. (非線性的減少)
  - 人手的培育較能夠形塑一個固定的課程(學會寫程式是可以透過規劃的課程達成, 但是僅是會, 不便見得會應用); 人才的培育除了專業領域, 仍需要社會科學的引入(寫出一個有用的程式, 必須結合有效的SA/SD, 了解一個非資訊學科的人的程式需求, 就並非了解程式就足夠); 人物的培育更強調實務的歷練, 要能夠得到他人的認可, 除了專業知識與應用能力外, 還需要經營社群的能力.

    - 別人說什麼 自己跟著做什麼 (人物C級) ==> 工人
    - 自己做什麼 別人跟著做什麼 (人才B級) ==> 工頭
    - 自己做什麼 自己跟著想什麼 (人才B+級) ==> 監工
    - 自己做什麼 別人跟著想什麼 (人物A級) ==> 幹話王 XD (很煩XD)

- 人才學：探討人才開發、培訓、管理、使用的基本理論；探討人才成長規劃或制度，更好地發現、培養、推薦、使用人才
- 如何辨識人才：志、變、識、勇、性、廉、信
    - 人才→深：理論+技術/廣：跨領域運用與管理
    - 資安人才素養：基礎學科、依個人特性發展其專長領域
    - 進階能力：理論創新能力(密碼學、AI、機器學習)、工程研發能力(系統安全、網路安全、資料庫安全、雲端計算、行動運用、數位鑑識)、應用及管理能力(電子治理、隱私保護、智財保護)
    - 資訊安全領域可能需要的不只是資訊科學的專業, 基礎科學(數學)及其他領域(資料科學/工程研發/應用管理)的專業也是相當必要的. 
      
      個人知道的實例:
      
      - 勒索軟體鎖定部分醫療院所是因為醫療設備往往使用較舊的作業系統. 追求穩定缺乏升級, 且該領域缺乏資訊安全人才, 讓系統的運行與開發陷於資安風險(程式撰寫時, 往往直接綁定最高權限帳號進行運行; 為了便於維護, 同產品的系統密碼都是一致, 且不允許用戶修改), 僅需要一些簡單的攻擊就可以癱瘓特定產品.
      
      - 孟加拉銀行的SWIFT遭駭是因為其中一個突破點為列表機. 駭客不只是有專業知識, 也了解孟加拉銀行的作業程序中涉及到紙本簽核的流程, 透過"駭"入商業流程達到惡意行為, 相較駭入系統成本更低, 同樣的狀況一樣發生電子商務的領域, 許多商業駭客完全沒有程式基礎, 是精於商業流程漏洞探究.
      
      - 某些國家的電廠遭惡意斷電(我沒說是台灣阿!!), 是因為電廠的運作程式往往很古舊, 使用一些有漏洞的script/lib. 駭客只要能夠突破網路架構進到電廠內網, 就僅需要使用一些老漏洞, 就已經管理電廠了, 當然假如理解電廠程式, 可能可以做出更為細膩的遠端操控, 若結合電力或電力相關的期貨買賣, 可能就會成為另外一個惡意獲利的管道.

#### 資安與人文/政治領域的交流？
- 韓國BOB有三分之一是女性，我們可強化我國資安女力
- 我國應建立國家級資安試驗場域
- 台灣資安教育的現況：正規在學教育(科技部計畫、教育部計畫、大專院校產學合作計畫)/在職教育(補習班等)/社群
  - 有 Mentor 計畫，嘉義高中學生的報告很好！
- 數學重要，因為CTF很多演算法密碼學，可快速找到解法與途徑
很多數學系的畢業生，可用好方法解題
- 換句話說，程式語言能力很重要
- 日本有針對國高中生的CTF，美國有PICOCTF也是針對這
- 台灣資安教育未來之鑰，向下本土紮跟，接軌國際舞台
- 國際間大型CTF的排名，代表了國家蘊含的資安能量，例如前年韓國BOB計畫的DEFKOR，我國的HITCON與217等等
- 在學教育+社群教育+在職教育，教育部希望可以融合三者，並找出方法，把人手人才人物銜接起來
人才需要深度與廣度，才有價值，且要適性發展，人盡其才在學教育+社群教育+在職教育，教育部希望可以融合三者，並找出方法，把人手人才人物銜接起來
在學教育+社群教育+在職教育，教育部希望可以融合三者，並找出方法，把人手人才人物銜接起來
企業願意贊助，這樣的角色有助人才培育
數學重要，因為CTF很多演算法密碼學，可快速找到解法與途徑
很多數學系的畢業生，可用好方法解題
換句話說，程式語言能力很重要

教育部
[工商時間] AIS3 招生中～ 

ithome 記者問：過度把資源丟在資安精英人才身上，有沒有針對普羅大眾
先來釐清什麼叫過度
三百萬

過度的資源？人才投資一點都不容易，大眾誤解
怎麼讓學生把基本功練起來？資安要有不同人手人才人物，從解決人手欠缺的問題，精英的欠缺要有系統地挖掘，從高中開始，一兩年看不出效果，台中家商一位保送生跟了我十年參加世界資安比賽金牌，
台灣需要菁英，還是普及的資安教育？即使培養菁英並不容易？


### [R0] 11:00 一發入魂 One Gadget RCE
- 講師： david942j
我的投影片有貓，但是跟貓一點關係都沒有。
好多貓 XDDDD

DeASLR
Control PC = 控制程式流程，可以任意跳去其他地方執行。
DeASLR: 跳到 system，同時控制參數為 sh
中間等人補
execve(file, argv, envp)
利用這個來執行另一個程式？？
根據使用情境不同，argv 若是 NULL 會 crash
/bin/ls 對 NULL 取 dereference 就會炸
/bin/sh 不會crash
execve("/bin/sh", NULL, NULL)
envp 環境變數，~~毫無反應就是個環境變數~~

如果直接跳到 system 的中間，argv 就會沒有初始
就有機會成功 
execve("/bin/sh", NULL, environ)
One Gadget 很多個，~~貓也很多個~~。
多試試總會成功。

1. 先找 /bin/sh (可在DSO裡找，也可以Leak??)
2. 再找哪些地方用到 /bin/sh
3. execve
約半年前寫了個 one_gadget 的工具(在 github 上有)
1分鐘學會Symbolic Excution
是將未知的變數，保持為變數，再將其他相關內容轉換成以同一變數的表示方式，最後再根據希望達到的結果找出變數的範圍。

簡單來說，假設有以下程式碼:
```c
x = input() // 讀一個數字
y = 3*x - 2;
if( y == 10)
{
    success();
}
else
{
    failed();
}

```
如果要讓程式走到 `success()`，那麼我們會得到一個 constraint (限制式):
* `y == 10` --> `3x - 2 == 10` --> `x = 4` --> 我們就必須輸入 4
* Symbolic Execution 就是在做以下幾件事:
    * 收集 constraint
    * 解 constraint  
* 透過 symbolic exection, 我們可以解出 input = 4，讓我們有辦法得知哪些 input 可以讓程式走到我們想要的路徑

one_gadget 就是利用簡易的 symbolic execution 來解出需要成功呼叫 `execve("/bin/sh", argc, environ)` 的限制式
* 通常是 argv, `"/bin/sh"` 和 `environ` libc 會幫你擺好
* argv 的值根據當時 stack 記憶體的內容而定


條件重複的不留，條件較嚴苛的也不留。


### [R1] 11:00 Play with File Structure - Yet Another Binary Exploit
- 講師：Angelboy

* Introduction
read/write: 直接對 kernel 發 system call
FILE structure: 做 buffer 以降低 kernel system call 的次數
FILE 當中的 FILE_plus 結構當中有 vtable 存放相關的 function pointer
竄改 vtable 並觸發 function pointer -> RCE
* Exploitation - 直接竄改 FILE
    會死在 cmp : _IO_acquire_lock 必須要偽造 _IO_lock_t*，將其指向可寫的位置，否則會 segmentation fault
* Exploitation - 直接將 stderr/stdout 當中的 vtable 寫掉 (需要有 libc base address)

* FSOP - file oriented programming
    ![](https://i.imgur.com/1BhaB9o.png)


    - Powerful function: **_IO_flush_all_lockp**
    在程式即將結束的時候(abort, exit, main return) 會呼叫，會 call 到 vtable 當中的 function，觸發 function pointer。
    結構為一個 linked list 結構，偽造他就可以連續的 call 偽造好的 function pointer
    _IO_FILE *chain 會指向下一個 node 的位置
    - House of Orange
    [writeup](http://4ngelboy.blogspot.tw/2016/10/hitcon-ctf-qual-2016-house-of-orange.html)

* Vtable verification
    大家都在玩 FILE，只好加一些驗證QQ
    - vtable 必須要落在 _IO_vtable section 當中，不在裡面的話會有第二段檢查
    - check the foreign vtables
    
    有沒有可能繞過?
    - 蓋掉 IO_accept_foreign_vtables
    有 pointer guard 保護
    - 蓋掉 _dl_open_hook
    可以繞，但是不如直接改其他的點 e.g. malloc_hook, free_hook ...etc
    
* Make FILE structure great again
    - 任意讀 (Arbitrary memory reading)
    偽造 FILE 的結構成員，呼叫 fwrite
    

    - 任意寫 (Arbitrary memory writing)
    偽造 FILE 的結構成員，呼叫 fread
    
* 只要有 puts/scanf/printf 就可以直接修改 stdin 的內容(需要 libc address)    
    - stdin
    1. 竄改當中的 _IO_buf_end 成一個很大的值
    使用 unsorted bin attack: heap exp 當中常見的攻擊，可以將任意位置寫成一個 glibc 當中的 address
    2. call scanf("%d", &var);
    可以 read 到 _IO_buf_base 並 overflow
    3. 竄改其他的變數達成 RCE
    
Q&A: linked list -> 在 user space，每個 process 獨立

### [R2]Breaking Security Software Protections from the past to present: The Dawn of AV Self-Protection
- Entry-Point Obscuring (EPO)
    - 這是以前的病毒常採用的方式，透過假的Entry Point 來 bypass 防毒軟體
- Obfuscator
    - instruction level
    - virtual environment Obfuscator
        - 病毒透過要求一塊很大的記憶體，然後判斷牠的執行速度來判斷是否是執行在虛擬環境中
    - NSIS Obfuscator

- Virus & Anti-Virus
    - 一場貓抓老鼠的遊戲
        - 道高一尺，魔高一丈


- New Era of AV Detection Bypass
    - Why new AV detection bypass
        - Modern AV has multi-layer protections
        - Multi-layer protections more complex,more bugs,easy to be exploited
    - Inspired by Dridex
    - Basic:
        - Tampering AV signature files/configuration files:
        - Tampering AV registry keys
        - Exploit AV bad design and logic flaws
        - 

- Diving into the Self-Protection
    - AKA Self-defence
    - Self-defence debate



### [R0]人才招募閃電秀 Recruiting Lightning Show
- 主持人：Turkey
中午1230開始的人才招募專屬時段，分別有6個企業與組織，開出IOT資安工程、韌體研發、資安顧問、數據分析等7類的海內外熱門工作機會給現場的會眾們，並提出優渥的待遇與良好的管理機制。另外也在現場設置徵才攤位，偕同HITCON共同打造”人才與企業媒合管道”，在資安即國安之精神下，為國內資安人才之強化與加值努力。
 TWCERT/CC
    由中科院負責營運，主要以服務國內企業與個人為主
    四大核心業務:通報處理、應變協調、交流合作(聯防)與情資發佈
    WANNACRY事件時，CC提出”上班前第一件事”，協助民眾守護資訊資產
    以協助國防部協助守護數位國土為目標，希望大家加入
    善盡社會道德與責任~希望大家有相關資訊~可我們做通報
    問：有很多學生加入CCㄇ?
    答： 中小企業MIS收入不高，工作又複雜，NCSIST比較好
 安華聯網  Onward Security
    成立三年，主要做黑白箱測試，源碼檢測，自動化資安測試，滲透測試、社交工程，CIIP研究案、嵌入式系統檢測
    任何可聯網的東西都可，車用聯網設備、資安檢測顧問，自主產品研發，無線射頻資安研究，正爭取成為APP檢測之認證公司
    希望從網站等軟體資安測試加值為硬體測試公司。
    問：是否有收實習生??
    答：有，RD人員，大四生OK，可抵學分+接軌業界!!
 Synology 
    以NAS為主的公司，並在意資安議題，為了安全與便利，不停更新產品
    路由器獲得世界評價第一
    整合網路+APP+NAS，強化作業便利性，快速且簡易布建私有雲
    運用公司的服務，在私有雲領域傳輸效能極佳，有全快閃SSD NAS
    公有雲則以備份功能為主。災難回復可將資料損失控制在小於1小時，並在15分鐘內恢復
    公司在WannaCry事件時，在一天內提出CVE解決方案
    國內第一個被授權發布CVE的公司，也有提出Bounty計畫
    招募職務：及時防護與預測資安威脅，RD
    問：攤位有啥活動? 
    答：到攤位TAG後，可抽網路設備與NAS
 豪勉科技
    低調的公司，連續三十多年賺錢，這是新鮮人在投入職場時可納入考量的要素
    以Security為發展宗旨的公司
    公司重視內部同仁在職訓練與人才培育
 資策會(資安所)
    資安多變化，唯一的不變，就是持續在變
    要持續提升自己，因應未來挑戰
    近期發展以AI security為主，也有很多出國參訪與進修機會，因為工作多但人力難以短期擴增
    AI以機器感知、深度學習分析與資安隱私技術為要項，可應用於CII、園區等場域
    麻花捲理論=研發+實務
 PCHOME+露天
    HITCON CMT越來越熱門，早鳥票越來越難買，表示大家越來越重視資安，好現象
    問：工作上最有趣的事?
    答：十多年前，曾經寫過有留下姓名的發信程式，後來被很多公司COPY走且亂用，導致收到市政府的函文警告，要求不可再亂寄廣告信



### [R2] Breaking into the iCloud Keychain
- 講師：vkatalov

Cloud Service
- 資料同步
     - Password
     - 信用卡
     - Health Data
     - 通訊錄
     - Call log
     - etc...

Apple Keychains
- iOS keychain
    - Local (encrypted backup)
    - Local (not encrypted backup)
    - iClould
- OS X (macOS) keychain
- iCloud keychain
     - View : only when/if synced with local device
     - Protection:well, strong

iTunes backup password breaking
- Get manifest.plist ?
- Get BackupKeyBag ?
- Password
	- Hash is salted, hard to break
- iCloud


iCloud data protection
- Two-factor authentication
Key is stored along with the data (except ??...??)


iCloud sync modes
- Recovery Mode : recovery from keychain backup/
- Sync Mode

iCloud circle of trust
- Keychain syncing
	- Circle of trust
	- Public key
	- private key: iCloud password
	- syned item is encrypted
- Keychain recovery
    - No 2FA: iCloud security code is needed(+SMS)
    - No 2FA, no iCSC: recovery is not possible
    - 2FA: device passcode is needed
    - Hardware Security Module

iCloud keychain revocery mode
- 3:key version
- 6:record protection class
- 0x48
- ???

iCloud keychain recovery protection (no 2FA)
- Simple (4 or 6 digits, depends on iOS version)
- 

輸入密碼 -> SMS 驗證 -> explore keychain

Conclusion
- sync and recovery
- trusted circle: not hard to get in, but leaves traces
- - both can be used
- need to have credentials
- need trusted device or SMS
- need to know iCSC or device passcode


### [R2] 14:20 A hidden agent of fingerprint authentication in Android
- 講師：SungHyoun Song

Background
* password is the simplest and most representative authentication method
* Password vulnerability (frequent used passwords (ex. 123456 / qwerty))
* Credential stuffing 有 73% 的人會在不同 Application 用同一個密碼
* 用 GPU 算 password hash (leak from server side) (建立 Ranbow table)
* FIDO Alliance [應該就是這個吧](http://www.ithome.com.tw/news/92943)
* 2013, October 指紋掃瞄認證 in Android
* 指紋認證漏洞例子：HTC One Max 把指紋檔存在 /data/dbgraw.bmp with 0666 permision
* 呃.. 指紋認證 SDK 裡可以找到寫死的 AES Key (?)
* android 6.0 開始提供指紋辨識ＡＰＩ （ＴＥＥ）,TEE是一個獨立作業的區塊 就算root權限也無法access

Analysis
* 指紋辨識系統有獨立的 Daemon (開機時自動跑)
	* source: AOSP/system/core/fingerprintd 
* 指紋辨識系統
	* 沒有 user-interface

Vulnerability
* OS Level (一些 Android 上提權洞的列表整理)
	* Android 更新很慢(數個月)，容易被打 1-day
	* Android 版本太多維護困難
	* 一旦拿到root 幾乎無敵ＸＤ
* System Level
	* 雖然有很多混淆 app 的方式，但成功拿到 root 可以打系統 service (?)

Exploitation
* 攻擊目標：有用到 fingerprint API 的 app
* 直接攻擊ＢＩＮＤＥＲ控制 Ｉ/Ｏ
* HOOK IOCTL(in libbinder.so) to injection "libhook.so"
	* Log fingerprint auth 的 data 傳輸
	
Conclusion
用 1-day 拿 Android root, 利用 dynamic library hook 錄 fingerprint API 的資訊傳輸，搜集指紋資料。


### [R0] 14:20 Time Bomb: Universal Root Is Coming!
* 講師：林桐、姚俊

兩大重點
- Time Bomb : 一個跟Linux Timer有關漏洞
- Universal Root : 通用Root漏洞

#### timerfd
- A timer interface provided by linux for User
- 3 main system calls
	- timerfd_create()
	- timerfd_settime()
	- timerfd_fdtime()
- 漏洞發現於 settime()

#### Vulnerability
- CVE-2017-10661
- Reported to Google in Mar. 2017
- Made public in Android Security Bulletin - Aug. 2017

多執行緒並行造成的 race condition 問題
* `ctx-might_cancel` 設置 true 或 false 來保護，沒有用 lock 保護

timerfd_settime()->do timerfd_settime()->timerfd_setup-cancel()->list timerfd_setup-cancel()

* race condition 會造成 list 裡面的 node 被刪除兩次，造成 list corruption
* 或是 node 的 pointer 會被 free，但是並沒有從 list 裡面刪除，造成 node 的 pointer 變成 dangling pointer。


#### Exploitation
* call timefd_create() create timefd and alloc ctx
* 利用 race condition ，將 ctx 加入進 cancel_list多次
    * 讓 victim ctx 的 next 和 prev 都指向自己
* 之後 close(fd), kfree ctx
* heap spraying (堆噴射)
    * timefd_clock_was_set()->wake_up_locked()->_wake_up_commom(ctx)
    * 透過不斷的 allocate 可控的 buffer ，讓之後的 buffer 對到 cancel_list 理的 dangling pointer，之後透過控制 ctx 結構，讓之後 kernel 在遍歷 list 的時候，會走到我們控制的的結構，進而控制程式流程(ex. control function pointer)(ex. control function pointer)
    * 使用原生 system call 進行 heap spraying 
* This process can be achieve by combining other AOSP vulnerability

* race condition 如果用 code review 的方式很難發現，需要借助工具 
(是這個工具嗎　--> syzkaller)
    * syzkaller是kernel fuzzing 工具
講者結論：近年來Google一直致力於提高Android的安全性，因此要找到共通的Android缺陷也變得越來越具有挑戰性。因此，開發新的漏洞挖掘工具和積累穩定的漏洞利用技術是非常必要的。

#### Q & A
Q: 怎麼發現 race condition 漏洞的?
A: fuzz, 反組譯，從 kernel 裡面提取 symbol table...

Q：觀察內核的工具為何？
A：一般用內核的功能，使用的方式是內建的formpay(？)
    或開源都有內建的工具，使用刷機包解root，再做提權，然後做反匯編
    但可能透過工具可能會沒有符號表兒，所以需要從內核再提取符號表出來。
    
    工具的部份還是要求對工具的理解及應用；對工具的深度的優化較佳。
    專注在特定領域，一段時間後就會有成果
    
    
Q：如何驗證這個弱點？
A：弱點驗證方式會寫一個程式去實驗，如果真實的漏洞是可以被觀察出來的。或可以直接在手機上執行。

### [R2] 15:40 Challenge Impossible -- Multiple Exploit On Android
* 講者：温瀚翔、王曉東
    * 講解在 android 上的組合漏洞利用 

* mmap in Ashmem
	* mmap 回傳的記憶體大小有可能不是使用者 request 的size （原因沒聽懂ＱＱ）
	* 利用 size 不如預期的弱點來 free mmap 後面的 memory (達到 Use After Free 的效果)


* Wifi 提權利用 (CVE-2017-0437)
	* 選這個是因為這漏洞的利用穩定(stack overflow)
	* Bug in wlan_hdd_cig80211.c
	* Exploitation: Using ret2libc
	* Google 做的patch 是判斷複製次數如果等於16就結束複製




### [R0] 資安從業人員座談會
 - 主持人：Birdman
 - 與談人：
 - 石美琪(資策會，針對資訊安全、台灣領域與國際接軌、新創、產業推動)
     - 來自以色列人不得不的創新 2017/06出訪
 - 王歆綺(資策會技研所、鑑識、事件處理、研究+實務整合)
     - Panel Discussion
 - 邱柏森 小瓜呆(工程師、資安架構規劃)
     - 一線工程師的心酸血淚
 - TT(自稱為充數www)
 - FireEye 基哥
     - 以原廠角度看產業與人才
 -  
**來自以色列人不得不的創新**
石美琪：以色列的資安產業
>     if the arabs lay down their arms there will be no more war,but 
戰爭與衝突塑造以色列人(內唐亞胡_以色列總理)
所謂台灣市場太小？
- 人口為台灣的三分之一
- 土地為台灣的三分之二
- 公司上市(那斯達克)數量為世界第三
- intel第一個國外設廠的國家

以色列資安軟硬體產品市占率2%，僅次於美國
基礎思維：如何以最稀少的資源展出最多的功能

將技術轉化為商品的行動力→養活自己+出口
集體農場：約兩三百座，各為完整的社區
台灣：有技術，沒有商品化→商品化帶動產業升級

以色列：市場為全球
允許失敗的，鼓勵新創，"失敗者年會！"分享創業失敗的心得
如何製作出符合全球市場需要的商品？
或是：如何將以色列經驗化為全球可共同接受的商品/技術/經驗
(反觀台灣？甚麼樣的台灣經驗可以讓全球接受)
(在地化就是全球化？XD)
工商 免費資安小聚(MEETUP)，可以吃吃喝喝聽大大分享
以色列因國情與周遭環境的壓力，因此非常強調創新，也造就全球第二大市佔率之資安產業、
以阿戰爭時的名言：阿拉伯輸了頂多放下槍，以色列輸了就亡國。一碗水一顆種子，我們就能生存
以色列創新局扶植很多公司，整體發展以"將技術轉化為商品的能力、自己先ㄒ用後再做出口、一開始就以全球市場為定位"為主
以色列水資源管理的技術也很強
BirdMan補充：台灣不是市場小而是膽子小、大家可參加失敗者年會

**資安科技研究所 王歆綺**
資策會人才培育 
SOP不是一切
種花太STABLE
人才最需要熱忱
國內不是沒人力而是缺有能力的人
資安人應具備隨時能接受變動的心臟，並再精進自身技術的同時也培育接班人
資安幾乎都是花錢而非賺錢所以在企業中較弱勢


沒有證據可以證明受害，除了受害馬上重灌，或是設備不足

有關證據因為第一時間的處理而消失，導致事件還原的困難

**一線工程師的辛酸血淚 小瓜呆**
    痛久就不痛了 QQ
    銀行久了就發生問題了，(圖片太大，頻寬被塞好塞滿
    圖片不加密，恩網站就不安全了XDDD
    
日本的測速照相機有三塊固定牌子提醒
    台灣的牌子常騙人
    
    
(台灣人害怕失敗的原因？)
(是否失敗就不容易擁有再起的資源)
(應該解決讓台灣人害怕的根本原因)
    台灣文化不給失敗的空間阿，做錯只有下台辭職一條路

面對問題是解決問題的第一步
資安事件不算好事但絕不是壞事，面對、接受、處理、放下的心境
同仁應多多去外界接受刺激
做資安，最高主管的支持超級重要，所以應邀請主管也出門聽聽HITCON CMT或 Pacific

**機哥**(台灣第一代上DEFCON的講師)
(台灣是否充滿挑戰XDDDDD)
唬爛：了解客戶需求，產品與客戶目標一致
了解市場
政府如扶植台灣軟體產業？關稅保護的手法太老舊
(也許學習以色列是方法之一)
資安的人多甲方，多在溝通協調而非技術，所以較穩定。其次外SI商，這比較多挑戰。甲方須多強化館度與深度、再其次為顧問服務、新創在台灣沒啥成果、所以政府要如何扶植?若搞汽車關稅保護那套就完蛋，可學以色列。未來會缺IR與事件處理的人。台灣沒有軟體業!!!!要從底層基礎教育開始做。

**Birdman回應**
「台灣沒有軟體業！」
台灣的科學教育不夠扎實如何發展AI(等等
**TT回應**
該思考的問題：台灣人的邏輯為服務業
但台灣的研發人才與資安圈沒有連結→資安圈也很少研發
可行的路：試著投入產品研發→才能成為產業
成功經驗(思維)：把解決問題的經驗化為產品
**Birdman回應**
台灣優勢：
- 市場小但makreting容易成功
- 亞太工程師最多的地區(便宜忠誠度高/命賤便宜的優點)
- 全額拿政府補助款很難走出台灣
- 同樣，試著商品化
- 投資年輕人
- 不敢失敗：一失敗就家破人亡
     
**Q：如何搶年輕工程師**
**Q：團隊、資金、點子：下一代的資安產品？**
A：想解決甚麼問題？沒錢種摸半(如何賺長遠的錢？)→觀察三到五年後的市場
- 喜歡自己的產品
- 時常變動計畫
**機哥回應**
不要沉迷於技術、了解市場調整策略

**Q：資安是很routine的工作**
**Q：如何賺大錢？**
**Q：如何培養人才？**
**Q：資安法等等等沒聽清楚**

台灣很多做程式開發的人、但無資安背景、有寫CODE解決問題能力的人，就去做產品再變成產業
常說台灣的缺點，但有可多角度思考:如說人少市場小，但是否正因如此較好做TEST??常說台灣薪水低但工程師多，新加坡由於都是管理師，所以外商來台設研發TEAM。
新創公司別全靠政府資金挹注，否則幾乎可看到將因處理眾多官式流程與paper work而無暇思考如何走入國際市場
若新創不敢失敗就不會有躍進
為何VC不敢領投??因為無軟體規模。台灣人錢多但卻幾乎不敢領投，但國外VC因嘗過甜頭所以敢投
軟體是服務業而非製造業，強調服務品質、新創要用VC角度思考台灣資安產業
VC也有領頭羊效應、
組織同學同事搞讀書會試試看來磨練領導與溝通
新創的產品在初期別走免費POC的路，必須藉金流(即便是很少錢，或是前幾天免費之後收少少錢等)以證明這是市場可以接受的IDEA
新創工具通常是特別且世面少見，所以較易收到POC小錢
建議年輕一輩的資同仁勿進入暗黑世界，因為做暗黑事業沒有CREDIT與CONNCETION，所以要專注在對長期生涯規劃有幫助的事
下一代成功產品的目標就是要做能解決問題東東，也可看看商業書刊猜(抓)未來方向與議題、掌握VC近期方向，
新創要做自己都喜歡的產品
聰明的人是機動的，需找對問題+選對戰場+勿過度沉迷技術+機動調整策略、
資安有很多時候是做循環的工作，所以最高管理者一定要支持與授權、
資安法:雖然大家對這法令草案各有見解，但身為資安人，就應多去影響周遭的人，將資安變成生活化議題，創造大家都關心氛圍
資安業值得學子加入嗎??要看自身的價值定義，因為工作開心最重要!!
業界覺得怎樣做資安人才培育?頂尖資安人無法培養~只能發掘出來!!!但可訓練出資安工程師!!!
人才培養出來後完整的職涯規劃也是重點，所以政府應把打造國內完整的資安產業環境列為施政重要方針之一


### [R1] Vulnerability analysis of Wi-Fi dashboard camera using threat modeling
* 講者：oxqo
* 前面都沒記到...
* Vulnerability - Modified firmware update
    * Try Sniffing
    * Obtain user mac
    * Try bypassing auth

* Dashboard camera hacking scenario
    * Secenario - Worm virus
        * freely access Wi-Fi dashcam and public ap
        * AP access program (wpa_supplicant)
        * default mac
        * ...

* if auth is not strong enough, video may leaked

* Way to improve Wi-Fi dashcam
    * default mac auth bypass
    * model name/MD5/option BOF
    * ...

* Q&A
    * Could this issue found by source code scan?
        * it would be great :)

    * Have you report the issues to the vendor?
        * Sure, but we didn't connect the company. We report to the gov.



# 8/26 Day 2

### [R0]Keynote - A New Era of SSRF - Exploiting URL Parser in Trending Programming Languages! ###  

[slide](https://www.blackhat.com/docs/us-17/thursday/us-17-Tsai-A-New-Era-Of-SSRF-Exploiting-URL-Parser-In-Trending-Programming-Languages.pdf)
[Case Study - How I Chained 4 vulnerabilities on GitHub Enterprise, From SSRF Execution Chain to RCE!](http://blog.orange.tw/2017/07/how-i-chained-4-vulnerabilities-on.html)

講者Orange
謝謝大家選擇來聽我的演講…不對，這個時間只有我齁？謝謝大家這麼早起好了。
SSRF網頁安全的攻擊手法
* 2008被提出
* 因XXE而繁榮

SSRF漏洞一再出現在臉書和google中
- 預覽功能
- 網址上傳圖片（內網網址->無視防火牆保護去抓圖）

熟悉SSRF新的攻擊手法很重要，讓SSRF重返榮耀
SSRF漏洞：繞過防火牆碰觸到內網資源，企業內網越大，攻擊力越強
如何進一步利用SSRF？(很吃基本功：對**網路架構**的了解)
SSRF仍然常見，所以了解是必要的
SSRF可繞過防火牆去取得內網資源，內網資源越多，SSRF的觸碰面越多，被攻擊面也越多



從一些有趣的案例來介紹
* SSRF bypass 
* protocol smuggling
 


## what is SSRF
Server Side Request Forgery
* 繞過防火牆碰觸到內網資源
* 被戲稱為專打有錢人的漏洞, 因為有錢人的內網比較大
* ![內網中的服務使用的不同的lib，可能會有不同的解讀](https://i.imgur.com/zhwF8q5.png)
例如：python 抓某網址之內容時，不同之內建http lib的解析會不同。

## Protocol smuggling in SSRF
* Make SSRF more powerful
* HTTP based protocol: Elastic, CouchDB, MongoDB, Docker（可被攻擊的內網服務）
* Text-based protocol: FTP, SMTP
* 在原有的協議中走私其他的協議
* SMTP 的 protocol 是 line by line 
    * 利用 CR-LF injection 將 payload 插到 HTTP protocol 中
* 現在的SMTP Server 會阻止HTTP connection
    * if SMTP connection 第一行有 HTTP pattern then close connection
    * GOPHER???


### HTTPS 中偽造 SMTP(:25/)
HTTPS Protocol 所有訊息都會在SSL中被加密，那如何在HTTPS中偽造SMTP? ->思考有哪些東西在SSL/HTTPS中不會被加密？->SNI(Server Name Indication)(?)

#### 對攻擊目標之:25/送 HTTPS connection -> bypass

![](https://i.imgur.com/OgaleLo.png)

> 將攻擊payload 放在SSL SNI中
hello message 中 sni 的 extension 
如果我們能在 hostname 插一些奇怪的字元
在這個例子中黃色框框是一個空白
這個空白非常重要，因為能讓我們有機會塞一些奇怪的東西，但他還是能正常連上
這邊用到的 trick 在 linux 的 glibc 中 （//先記住，晚點說）

剛剛是用 16 進位的方式來看封包
現在用人類方式來看(?)
![](https://i.imgur.com/KlFqxjq.png)


## Make SSRF Great Again: 4 methods
URL Parsing Issues: URL parser and requester 對同一個網址有不同解釋
    * checking URL is defficult because WHATWG的RFC3986(?) 只有定義規格無定義實作。以人魚為例，spec 是半人半魚，但不知道哪一半是人哪一半是魚啊！實作成品會出乎意料之外。
    ![URL Components (RFC3968)](https://i.imgur.com/5lJi8vc.png)


#### 演練
![今天會涵蓋的漏洞列表](https://i.imgur.com/M7fdgMC.png)

這段 php code 只有 7 行
![A php code for read a file](https://i.imgur.com/GmupdP4.png)

programmers use parse_url(php內建的) method to check port & host are legal or not; However, RFC 只定義冒號(分隔 port&host) spec，但有的 parser 會從帽號前面來解釋，有的 parser 會從冒號後面來解釋
![Example1: Different parseres have different result](https://i.imgur.com/SujkMSw.png)

![Example2: Different parseres have different result](https://i.imgur.com/M0fptNm.png)
// PHP parse_url讀前面 PHP readfile讀後面


**How about CURL(?)**

Curl(A lib) 很大量的人用，用於抓取資源。內建 http lib很爛，故幾乎都改用 Curl，但給 Curl 更新之後，後續用一個空白一樣可以打穿這個弱點。
開發團隊回覆：無法過濾來源網址，請程式設計師自行檢查，只能用文件提醒大家… ((誰會看文件啊 XD

![Example3: Different parseres have different result](https://i.imgur.com/Ugjbf5q.png)

![Example4: Different parseres have different result](https://i.imgur.com/AQfkuDA.png)


##### Attack NodeJS by Unicode
![A Nodejs code](https://i.imgur.com/A2Oeviw.png)

- 使用者同名目錄當成家目錄（？），會檢查..以外的字（為了防止什麼攻擊？）-> 無法存取sandbox 以外的目錄：
- 假設現在有個密碼檔在根目錄下，如何繞過此限制存取到該檔案？-> 用 Unicode 全型字母 N。

**JavaScript 內部使用UCS2實作來處理全型字母**

- UCS2 處理全型字串->轉為十六進位->N = \xFF\x2E

![JavaScript UCS2 處理全型字母前之URL](https://i.imgur.com/wP1IZPM.png)
![JavaScript UCS2 處理全型字母後之URL1](https://i.imgur.com/IobWtQn.png)

Moreover, NodeJs(C++實作，以byte為單位) bufferString will discard the fist byte when encoding conversion.
![JavaScript UCS2 處理全型字母後之URL2](https://i.imgur.com/tGoQDLK.png)

. = \x2E

![JavaScript UCS2 處理全型字母後之URL3](https://i.imgur.com/ctxoqn6.png)


**若插換行呢？**
可以用剛剛這個 unicode 的特性 U+FF0D, U+FF0A 繞過這個保護(when BufferString, FF會被拿掉->變換行符號)

#### GLibc NSS 的特性
![GLibc sourcecode](https://i.imgur.com/y4WZAyA.png)

- RFC1035: DNS 支援十進位的轉換。For example, or\\097nge = orange

- 反斜線後面若非數字，會把反斜線直接拿掉->用一堆反斜線來混淆host name域名。(python@linux). For example, \o\r\a\n\g\e\.\o\r\g

- Getaddressinfo(): 合法IP address+空白字元後面的東西給過濾掉![linux'll return 127.0.0.1](https://i.imgur.com/Cy7qyYN.png)

#### 攻擊URL parsing (?)32:40

![](https://i.imgur.com/s23miFF.png)

![](https://i.imgur.com/LS0qDHF.png)

換行 & 可以用相同的 Host 塞奇怪的東西進來，以"換行"參雜其他協定。(繞過相同的Host，傳送至其他的Request)


**Attacks by Glibc NSS feature**
- HTTP 1.1 要求 a Host header; 網址 host name will put in request host header. 34:00
- .......(?)
![參雜radis protocol(?)](https://i.imgur.com/kfBmOGw.png)

SET foo 0 60 5\r\n:443/
![\t](https://i.imgur.com/gra14xi.png)

![\t URL encode](https://i.imgur.com/Om6rYdS.png)

![\t URL double encode](https://i.imgur.com/sbVARLt.png)

感謝 Redis 跟 memcached
用前面的空白去繞過亦可。 (用於多一個空白，可用於最新版本的python)


#### Attack IDNA

- IDNA => 定義Unicode的標準 //複雜的排版上是否為合法之類的標準
- IDNA standars 目前常用的標準有兩個 2003, 2008  過渡期：2003+UTS46->如果 URL 的 parser 跟 url requester 用不同標準就會有問題
![](https://i.imgur.com/o48d5nr.png)

- 拉丁字母 ß (德母的字母沒有相對應的大寫字母，就會轉成兩個大寫s) However, ss!=ß; 但如果用瀏覽器去開啟，會有可以繞過黑名單的洞。For example, WordPreß = WordPress -> 目前還沒修 XD

繞過 IIS 的方式：找出標準中的不一致，就可以達到繞過的方式。

### Case study: 3個繞過的方法
1. Time-of-check to time-of-use(TOCTTOU) problem
![三者對SSRF的防禦方法](https://i.imgur.com/YNeEavM.png)
- URL parser: 檢查網址是否在白名單內
- DNS checker:確保IP不再黑名單內
- URL requstster:存取網址(此時會再產生一次DNS query)並抓回內容

BUT!!!!若檢查時狀態與使用時狀態不同！！
![TOCTTOU問題之精髓（？）41:00](https://i.imgur.com/E2c3lVr.png)

2. 對 IDNA 標準支援的差異
CURL 支援 Unicode 域名自動轉換但PHP之gethostbyname()不支援-> SSRF bypass

3. URL parser and URL requester 的解讀不一致-> bypass


即使 curl 7.54, PHP 後來修復了 SSRF 的問題，但是大多數專案(ex. Ubuntu 17.0.1?的 curl)沒有跟上
**空白的弱點**，curl 永遠不會修復XD

#### SSRF Execution Chain: 4個漏洞串成RCE (?)44:00

GitHub WebHuck 用了一個Ruby gem 作為黑名單保護，然而
可以用 0 輕鬆繞過。**在 linux 中 0 = localhost**->有一個SSRF

但，此SSRF有以下限制導致無法利用此漏洞做事情：
1. 只能用http/https的skin(?)&沒有302跳轉(?)可以轉換成其他skin
2. 無法控制POST header&其他內容
3. 前面介紹的CR LF injection(?)在這邊都無法做到
-> 無法做到 protocol smuggling

那，內網中的http服務中有什麼可以做利用咧？
localhost:8000 有個服務會抓GET()參數並訪問->第二個SSRF->用兩個 SSRF 結合成Chain，偽造 protocol


&url=127.0.0.1:6379/%0D%0ASET...
一個假造協定，一個假造目標（？）


為什麼Github 能存下 ruby object (？)
用marshal(?)的方式包起來

![完全不懂（？）](https://i.imgur.com/igtt4Qj.png)

#### Prevent(Mitigation)

1. Software(Application): 唯一IP and hostname，不要reuse使用者提供的IP(?)
2. Network: firewall/network policy 阻擋intranet traffics(?) Some library you can use like SafeCurl or Advocate


### [R0] Triton and Symbolic excution on GDB


* symbolic execution tool
    * system level -- S2E
    * angr
    * code base -- klee

https://triton.quarkslab.com



Triton Structure
Symbolic execution engine
* 會有 table 去記 registers 的 symbolic variable

SSA form :可以幫我們省略很多不必要的運算
Tracer: 負責去 trace instruction execute 過後的狀態
* intel pin tracer

SMT solver is based on Z3
* https://github.com/Z3Prover/z3
1. * 
AST Representations 
設定 architecture
load segment
define fake stack
symbolize user input
start to processing opcodes
get symbolic expression and sovle it

GDB Python API

整個 Triton 在解的過程實在太繁雜(需要設定一堆東西)
很多東西其實可以透過 gdb 的輔助，來幫我們直接設定好像是 stack 之類的memory 

直接把GDB的CONTEXT複製到TRITON
* 要不然 gdb triton 的 context 可能會不同步
* 這樣triton 在解symbolic時context就不會影響到gdb


Triton 並不支援 GNU libc，且無法做 path exploration ( 自動解路徑 )

SymGDB: https://gi
thub.com/SQLab/symgdb

PEDA 
Triton versus Angr
                      triton       angr
architecture support  x86 x64     x86 x64 ....
GNU c library
path explore



### [R1] Tracking Mimikatz by Sysmon and Elasticsearch
https://github.com/sisoc-tokyo/mimikatz_detection 

聽到一半補記，抄不完細節

Mimikaz:針對ad攻擊的惡意程式
Sysmon：free software for monitor ms
藉由追蹤mimikaz執行時讀取的dll偵測

在不同環境下，ex win7, server2008 win10 或不同版本取不同dll
取通用的三個dll做檢測 advapi32.dll crypt32.dll

隨版本有些進化，傾向讀取更多dll

ELK,Elasticsearch
資料整理framework

Q：為什麼用追蹤dll，不使用 api call segment，感覺比較容易誤判？
A：會再研究
Q：使用elasticsearch是一個即時監控還是事後檢查
A：事後檢查
Q：能不能不使用sysmon，使用系統本身的？
A：其他工具應該也能做到，只是我們主要研究windows上的open source 工具



### [R2] Harden your program the hard way

哈味

Terms
- Vulnerability vs Exploit
- PoC
- Mitigation (緩解)
- Buffer overflow
- Moving Target Defense (MTD), confuse your enemy

Buffer overflow

- override return address

Use after free

- override vtable pointer

Linux Mitigations
- ASLR

- DEP
不給執行 

- stack guard

FP overwrite

ROP

BROP

offset2lib
OS versiob, libc version

#### Home made mitigations

- FP protection
- Function Padding
- Variable re-order
- Two birds



### [R4] 那些年，怎麼寫都錯的PHP by UCCU ###
PHP 冷知識
?O.O=O_O (底層 -> 空白、點 會被解析成底線)
0e8787 == e023213312132123213 (by pass password check)

shellshock

Remote Code Execution 
重複跳脫結果沒有跳脫 is Good

XSS 
跨站腳本攻擊
Post: img=demo.png onerror=<scrtip><alert>XSS</alert></script>

PDO 用錯 (字串拼接)

wordpress 常出錯的是 plugin
exploit wordpress database 


### [R1] 11:10 Pwned in Translation - from Subtitles to RCE
* 講者：Omri Herscovici、Omer Gull

主持人說這場難度滿高的
如何以字幕進行RCE攻擊

#### 新概念：字幕偷渡式攻擊→非漏洞，字幕也可能是威脅來源

在家看電視看電影的方式越來越普及，每天下載字幕的下載量從七百萬次到上千萬次，對於非英文母語使用人事而言將帶來很大的危險
字幕很危險!
SRT+SUB為兩個字幕基礎格式
還有加有字幕字形設定和編碼等等其他格式，格式包山包海：
字幕 format (> 25 types):
* .SRT html based
* .SUB custom control codes
* .SSA -> .ASS
	* 支援畫圖
	* System Commands(!)
	* 系統指令可遷入字幕系統中

所以→**字幕缺乏統一規範，因此使攻擊者有機可趁**
線上字幕庫包括各種版本的字幕供使用者選擇，如下↓↓↓
- opensubtitles.org


#### PopcornTime(電影播放器):
* natice application with web support
    * electron (將web app 轉成 desktop app)

nodejs 中，xss 會導致 RCE (直接使用 script 呼叫 program)

PopcornTime 轉字幕時 (轉成 srt 格式)，裡面會有 html 格事的 tag
因此，轉換時，如果插些 xss 進去的話，就會造成RCE
* demo 時，load 進 malicious subtitles時，就會連revserse shell 回攻擊者機器

字幕網站的智慧搜尋功能
惡意字幕可製造其在字母網站中的偽評等指標
透過影片命名與字幕命名的高吻合度等
加入字母網站使用者評等的要素
↓↓↓
要讓 popcorntime載到攻擊者的字幕檔，就要想辦法讓字幕檔的分數高一點 
* 命名是重點。其中一個是將字幕黨的黨名跟影片檔鳴對上 (特性)
    eg. 將電影檔明拆解成總共8個tag，而其中有3個tag與字幕檔吻合，計算下來他所得的分數就為2
* 或是上傳多個字幕檔，上傳很多字幕檔的話，rank也會提高

#### KODI
* 40 million users

智慧電視的常見介面
攻擊者可完整掌握fildname的屬性，
使用 KODI 下載字幕
控制 url get 參數
如果一開始 srt 下載失敗，會嘗試去下載 link 參數只像的url
放個 zip 的連結，之後會使用xbextract去解壓

CVE-2017-8314 demo 
	* 因為我們在 opensubitils 上 fantastic 的 rank ，前三名字幕都我們的ＸＤＤ

**任意從KODI下載檔案的行為會有甚麼結果？**
被監看啦！裸奔～

#### streamio
* user the same trick that's used on popcorntime, didn't work 
* code review
    * 有做 sanitize (把 script 拿掉?)
    * 用 a href tag 把 img 包在裡面來繞過 (讓使用者點一下（？）)
    
		* `<a src='http://demo.com/evil.js'><img src='support.jpg'/></a>`
* demo ，彈了個小算盤

popucorn
WebKit based Player GG

#### 下個目標 VLC Player -0-
字幕為危險的攻擊途徑來源，VLC有一億八千萬使用者，支援各式平台
VLC有自己開發的解碼器
藉由讀取buffer中的"<"作為開始，直到">"當作結束
攻擊範例：
Decoder
Demuxers

用個 while loop 去parse tag，但式結束條件沒做好，導致 out of bound read


用 afl fuzzing VLC
* 先用正常字幕檔(corpus)當seed，之後afl用這些input file 來 fuzz
* fuzz 出有漏洞的 function: ParseJSS()
* out of bound read, 被 AFL 找出crash
	* CVE-2017-8313

另外也有 heap overflow，做越界讀寫，最後導致RCE
* CVE-2017-8311

沒開PIE，這樣就不用 leak address，gadget超好找

demo (同樣彈出calc)


#### 總結：
有25種以上的字幕格式
沒有stander的字幕庫
可以置入惡意字幕資料於字幕庫

#### Q&A
Q：廠商如何做patch
A：

Q: 你還有在用 VLC 嗎
A: 有但不是用來看電影ＸＤＤＤ

Q：有推薦的字幕格式嗎？
A：各家都有優點啦

Q：字幕庫有任何 ranking 機制上的改進嗎？
A：廠商以為主講們是要跟他們賣產品www
主講覺得不見得要修，實際上也不是漏洞，只是他們的 ranking 機制能被操作而已


### [R4] 那些年我們遇過的資安事件 by TDOH ### 

概念篇

蒐集分析 DDOS 攻擊事件 2014~2015 

專家對資安事件是看風險值

資訊安全事件往往事出有因, 在攻擊的背後都存在著更實際的原因
- 實例分享: ATM Hacking

  - 在2008年以前無論是新聞或是實作都少, 其主因是因為缺乏實際可以練習的環境(一般人無法取得ATM)
  - 在2009年開始逐步佔據版面, 主因是因為金融海嘯後, 許多銀行倒閉, 而銀行清算拍賣時將ATM主機也進行拍賣, 讓一般人得以取得ATM. 另外ATM的常用平台也在2008年底推出最後一個SP, 讓底層系統的漏洞逐漸變成可視額不可補
  - 在2010年時開始在駭客大會中成會話題, 其實利用的即是微軟不再修補的漏洞, 但是此刻當下, 金融界對於此議題重視有限.
  - 在2011年以後, 相關的惡意程式逐步成熟, 且銀行陳舊的ATM體系逐漸被駭客理解, 相關惡意程式的開發開始蓬勃, 逐漸在各國開始有新聞發現ATM的安全不再是可以透過厚鋼板來進行防護, 此刻犯罪集團已經開始介入
  - 在2014年以後, 就已經傳出可以遠端操作ATM的工具, 無論是惡意程式植入或是偽卡近端操作都成為可能之犯罪手法, 大筆盜領的事件開始出現(其實在2016年台灣發生事件前, 年初東南亞就有類似犯罪, 年中日本就發生現金卡盜領事件, 雖然事後似乎研判不相關(東南亞疑似相關而日本應該不相關), 但是台灣相關單位的無感間接導致了此嚴重的事件.

  - Note: 其實資訊安全事件並非全然是技術的突破, 若可以掌握事件的脈絡, 可能可以在初期以更少的資源進行防護, 而不會要在事後再尋找系統復原或數位鑑識等高單價的服務.不過換個角度而言, 若沒有此一重大事件, 資訊安全視乎僅會被視為花錢而沒有效益的課題.

### [R0]  11:10 Mitigating the unknown, when your SMB exploit fails
Nicolas Joly
世界上首次發生「國家級數位火庫外洩，導致全球產業遭駭」的事件，同時也提醒我們保持系統漏洞修補機制正常運作的重要性。

* EternalBlue
	* 原因 將Ulong變數當成Ushort變數，造成integer overflow
* EternalChampion

* EternalRoance
    * 


HITCON pacific & CTF 2017/12/6~9

奇葩獎
由BirdMan主持，介紹何謂奇葩獎? 希望藉由批判荒誕之資安新聞，以詼諧的方式讓大家了解資安的重要性。



### [R0]  13:40 What happened to my 18 months IoT honeypot
Tan Kean Siong

攻擊、感染或利用物聯網（IoT）設備是近期資安圈熱門話題。講者分享相關趣聞與自建之偽IoT設備在為期一年半的時間中所蒐集到之現象。

* Dionaea
    - UPnP Udp port 1900
        6.5 milion connections in 2016 and 300K requests in 2017 new year eve 
    - MQTT broker TCP port
        

glutton-all eating honeypot








### [R1] Automating vulnerability scanning with Vuls

作者
https://github.com/future-architect/vuls

Kota KANBE & Teppei FUKUDA

open-source, agent-less
based on information from NVD, OVAL, etc.

#### features

There are Docker, AWS, Azure,...
There are Ubuntu, CentOS, FressBSD...
Admin so tired...

Vuls comes to help! %%%%%

Agent-less: 
- ssh
- install vuls in local if you cannot use ssh

Penetration Testing? No
Non-intrusive sacns

OVAL
https://oval.mitre.org/

Compare versions
Debian: vesion well defined
RedHat: read doc and guess


Detect processes which needs restart after update
debian: checkrestart
red hat: needs-restarting

Features in the future
- Detect vulnerabilities for which there's no update yet
- Metasploit, ExploitDatabase





### [R2] ZeroDay 發表會

lan
*Allen


今天主要是說明漏洞通報的經驗

ZeroDay 漏洞通報平台

TWCERT/CC主任

TWCERT/CC為政府通報的流程

Chris Lin
三個案例
1.OO銀行電子帳單多個漏洞導致GetShell

BILLHUNTER
帳號列舉攻擊

2.OO網銀多個驗證碼漏洞

ZD-2016-00032

TensorFlow
GSA Captcha Breaker

3.OO電信被入侵

木棍
購物app漏洞
BrupSuite
jadx
### [R4] 滲透測試基本技巧與經驗分享 by趙偉捷
入門web
* 滲透測試
    - 協助企業尋找網站漏洞
    - 有企業授權很重要
    - 滲透標準
        - OWASP
        - OSSTMM
        - PETS

RECON > SCAN > EXPLOIT > 回報
 or
           提權 & 持續存取



1. 進攻第一步：偵察
Recon工具:
    - Element Inspector (Network -> 查看每個 Request 的 HTTP Header) 
    - 插件 "EditThisCookie" (查找及修改 Cookie 名稱及內容)
    - 插件 "Wappalyzer" (查看這個網站做甚麼軟件製成)

    > google hacking 的技巧   google hacking database 
    > inurl:a_domain.com
    > intext:has_texts
    > site:site.com
    > intitle:"Index of"
    > filetype:"pdf"
    > ext: "pdf"

    > GHDB
    > https://www.exploit-db.com/google-hacking-database/

找旁注
一個機器可能 host 其他網頁

* nmap
* nikto 
> 編按：IP查找可以到 bgp.he.net 尋找更精準的資訊

**資料洩露**
情境二：
外星人申請東東，申請完得到一個可以列印的連結，會發生什麼事呢？
可能導致資料洩漏   例如：id=100 ，如果權限沒設好，改 id 就能得到別人的資料

SQL Injection (SQLi)
在有input box的地方,輸入SQL語法,或是故意輸入錯誤語法'讓他報錯。
union select 技巧
把兩個 select 語句接在一起，查詢兩次把兩個結果串在一起


> DB: user
> | Username | Password | Email |
> | -------- | -------- | -------- |
> | john.appleseed     | p@55w0rd!    | hi@exmaple.com     |
> ---
> SELECT email FROM user WHERE password="$pwd"
> 當提交了一個 SQL Injection(**" OR 1=1**)，就可以繞過登入了
> SELECT email FROM user WHERE password="**" OR 1=1**

schema <--> table <--> column 

* Blind Inject
    * 使用 binary search 的技巧提昇效率
* sqlmap
    * 防禦 SQLi：將使用者傳入的資料給參數化
* Cross-Site Script (XSS)
    * 在網頁中注入代碼，讓進入到這一頁的使用者觸發
    * 儲存型
        * 被注入的代碼儲存在DB中，讀取到資料時就會去觸發執行代碼
    * 反射型

    * 防禦 XSS
        * Server header reply with X-XSS-Protection
        * htmlentity

    * XSS Games:
        * https://xss-game.appspot.com/
        * http://alf.nu/alert1

***更正：社交工程是「Social Engineering」*** 

**漏洞利用 - XST**
使用目的: 繞過 http only
http only cookie 讓 JS 無法存取 document.cookie
set-cookie: my_cookie=123; HttpOnly

http 用來測試的 method - TRACE 
你傳什麼給伺服器他就會回什麼

send js request with TRACE method

CSRF

by 

img

or 

iframe



**File upload**
情境七：
今天有網站可以上傳檔案，沒有限制檔案型態，會發生什麼事？

* upload a php webshell if u can find file path after upload


**CVE**

http://cve.mitre.org/

用 docker 或虛擬機架設，不建議設在實體機上  

* POC (proof of Concept)
    * google POC 
    * nmap nse or metasploit
    * write script

open source intelligence

WEBGOAT
DVWA
Mutillidae



### [R0] 14:40 Neural Blacklisting
Sean Park
從防守者的角度來看，及時阻止用戶連線到DGAs產生的大量惡意URL是非常重要的，但可惜的是，過去這類工作多是仰賴人工來判斷。近年因深度學習領域快速發展，已可用來解決上述大量依賴人工的現象。講者提出以LSTM檢測惡意URL，並運用全球CDN領導者Akamai的記錄檔來進行驗證後的成果。


* Traditional ML works? I won't do that.
* Deep Learning?


 Use Recurrent Neutral Network(RNN) to do the
    * suspicious URLs classification. 

 
### [R1] 14:40 看我如何搭配黑帽 SEO 玩轉網站排名流量
AZ

- SEO 概論：何謂黑帽白帽
    - 純技術的領域裡面沒有黑與白
    - 白帽 SEO：優化網站頁面、改善友情連結品質、改善 UX、照搜尋引擎規則，要做比較久
    - 黑帽 SEO：搜尋引擎作弊、黑色產業（博奕、色情）、業界競爭（保險、旅遊、電商）、騙不懂的客戶
- 黑帽 SEO 目標：政府、學校、新聞、高權重
- 在網路的世界裡，網站流量=錢
- 有流量能做什麼？
    - 黑色產業：賭博、色情，短時間暴利
    - Google 廣告
- 黑帽 SEO 案例：阿明師太陽餅。網頁快照劫持：攻擊者拿下 WebShell 之後攥改內容並讓搜尋引擎收錄，完成後再改回
- 把病毒碼寫進 DNA 裡面
- 泛站群：
    - 如何搞出這麼多網站（上千個）：
        - Godaddy 現在一個 $43
        - Gandi
        - 黑市有更便宜的，一元一個 domain
    - 使用站群軟體一次管理數百數千個網站
    - 打下 WebShell 吸取別人的流量
    - 大量生成關鍵字
    - 使用蜘蛛池自動生成大量外連
    - 鏡像站：將 A 記錄解析別人 IP 並 Mirror 一模一樣的站點吸引流量之後再把流量導回
        - 如何防範："intitle: 你的網站標題" 看有沒有人用跟你一樣的網站標題、Ban Server IP
    - 若 Webshell 太麻煩... 可以用買的... 一個 20 人民幣，拿來做黑帽
- 黑鏈
    - 打下網站之後埋他的連結
    - 偽造 pdf、jpg：因為 google 會優先處理 pdf 但是不會去看內容（？）
- XSS 攻擊：偷 cookie 比較沒用，用跳轉的
    - 像是 <script>window.location.href...
- 組合計：站群+鏡像站、WebShell 跳轉
- 可以上 104 找黑帽 SEO 高手（可能有點貴）
- 黑帽 SEO 缺點
    - 易涉及違法
    - 容易被K站：被 Google 發現之後就扣分了
    - 容易造成用戶反感

- 主動防禦：
    - 滲透測試 
    - Ban server ip
