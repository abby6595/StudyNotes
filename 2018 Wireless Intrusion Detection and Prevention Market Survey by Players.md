# 2018 Wireless Intrusion Detection and Prevention Market Survey by Players
* [Cisco-有](#Cisco)
* [Netscout-有](#Netscout)
* [AirWave (Aruba)-有](#Aruba)
* [Fortinet-有](#Fortinet)
* [HP-有查到的部分是做 802.11 ](#HP)
* [IBM-感覺是做第三層以上](#IBM)
* [Check Point-看不出](#CheckPoint)
* [Extreme Networks](#EN)
* [ForeScout-沒看到什麼](#ForeScout)
* [WatchGuard-感覺是做 802.11](#WatchGuard)
* Venustech 沒找到相關的文件
* Topsec 沒找到相關的文件
* Qihoo 360 沒找到相關的文件

<h1 id=Cisco>Cisco</h1>
<h2 id=wIPS>Cisco wIPS</h2>

![](https://i.imgur.com/sBfvT3t.png)
![](https://i.imgur.com/H3k3nRk.png)
![](https://i.imgur.com/yzxumvC.png)
![](https://i.imgur.com/ZA7oqoI.png)
![](https://i.imgur.com/VSUIm5a.png)
![](https://i.imgur.com/XkFvGFY.png)
![](https://i.imgur.com/jTGtAN6.png)

![](https://i.imgur.com/T5ienNa.png)

* There is no integrated mitigation of interference - normal RRM management of noise is expected to manage this
* Only 3 Interference types are detected
    * Microwave Oven (2.4 GHz only)
    * Continuous Wave (2.4 and 5 GHz)
    * SI-FHSS (2.4 and 5 GHz)
* SI cannot differentiate between multiple devices of the same type - BlueTooth, Dect Phone, and FHSS are all SI-FHSS and only one alert will be displayed regardless if there is 1 device or 10
* Device classifications are limited to presence - the waveform is present, or it is not
* SI does not calculate Air Quality (AQ)
* SI does not provide a Severity or Duty Cycle metric
* SI information is only visible at the controller - it is not sent off the controller to CPI, CMX, or MSE and is not coordinated between controllers
* SI information is 1 for 1 reporting - every AP that hears a device will report. There is no grouping algorithm to coordinate multiple reports into a single alert as CleanAir does
* An AP in client serving mode (local or Flex connect) will only report 1 interference type even if multiples are present
* An AP in Monitor Mode can report all 3 types if present

![](https://i.imgur.com/I577OoP.png)
![](https://i.imgur.com/Z14NxjI.png)


<h1 id=IBM>IBM</h1>
<h2 id=IBMWIDS>IBM WIDS</h2>

![](https://i.imgur.com/VZsY6oV.png)
![](https://i.imgur.com/TQxsnNI.png)
![](https://i.imgur.com/iqodqEt.png)

<h1 id=HP>HP</h1>
<h2 id=Mobility>Mobility Security IDS/IPS System</h2>

![](https://i.imgur.com/iQGwUaX.png)

<h1 id=Netscout>Netscout</h1>
<h2 id=AirMagnet>AirMagnet</h2>

![](https://i.imgur.com/Rp8g0Jg.png)

<h1 id=Aruba>Aruba</h1>
<h2 id=ArubaOS>ArubaOS & AirWave</h2>

![](https://i.imgur.com/cclSXc6.png)

<h1 id=EN>Extreme Networks</h1>
<h2 id=AireDefense>AireDefense</h2>

![](https://i.imgur.com/hk3yUTL.png)
![](https://i.imgur.com/c0nbdj8.png)
![](https://i.imgur.com/yoaKnxS.png)

<h1 id=ForeScout>ForeScout</h1>

<h1 id=CheckPoint>Check Point</h1>
<h2 id=></h2>

<h1 id=Fortinet>Fortinet</h1>
<h2 id= WM> Wireless Manager series</h2>

![](https://i.imgur.com/0lsJdMH.png)
![](https://i.imgur.com/61HICsP.png)

Spectrum Manager
![](https://i.imgur.com/nXaNmIx.png)

<h1 id=WatchGuard>Watch Guard</h1>
<h2 id=wg>Wireless Intrusion Prevention System (WIPS)</h2>

![](https://i.imgur.com/6JInNaM.png)
