---
title: Stream Live 手機直播
tags: 軟體使用
description: 使用 Stream Live APP 進行 Youtube 直播
---

# Stream Live 快速上手

:::success
此處介紹如何利用手機安裝 Stream Live 這款免費的直播 APP，將現場畫面直播至 Youtube 過程中無須額外配合攝影機與擷取卡，在頻寬穩定，手機性能還不差的情況下，是個快速又靈活的解決方案 (以下說明皆以 iPhone 為範例 )。
:::

![](https://i.imgur.com/ZmHFfu8.png)

## 前言
Youtube 早期的 APP 在 24 小時的審核期通過後就能夠直播，但後來增加了頻道訂閱人數必須超過 1000 人的限制，因此對於沒有在經營頻道的人來說，只能用第三方的直播軟體了，以下介紹的是 Streamlabs 的 Stream Live 這個APP。

:::info
羅技於 2019 年 9 月以 8,900 萬美元收購了擁有桌面串流軟體 Streamlabs OBS 與行動串流軟體 Stream Live 二項重量級開源直播軟體廠商的 Streamlabs 公司，透露出其踏足實況直播市場的野心。
:::

Stream Live 這款直播 APP 有二種常用的直播方式，
- 第一種方法要先在 Youtube 後台設定直播頻道，再用本軟體以 Upcoming Event 模式直播。
- 第二種方法只要以本軟體開啟 Create Event 模式，直接啟用 Youtube 後台直播頻道，就能將串流訊號上傳，可謂一氣呵成，非常適合在外臨時需要直播的場合使用。

雖然感覺第二種方法很方便，但之前測試時感覺這方式比較不穩定，有時候會失敗，甚至要整個 APP 移除後重裝再試才會成功，因此本網頁介紹的是第一種方法，以下開始說明。

## YT端設定直播
登入欲開啟的直播的 Youtube 後台，按下右上方的拍攝圖示，選取進行直播。

![](https://i.imgur.com/GMwtJPp.png)

:::danger
第一次啟用直播功能的帳戶，會遇到 24 小時啟用的審核機制

![](https://i.imgur.com/mIxaSjY.png)
:::

至少輸入本次直播名稱，選擇是否開放搜尋本直播，設定是否為兒童打造等三項資訊後，按下建立直播頻道。

![](https://i.imgur.com/KX5j6NO.png)

就會看到此畫面，等待串流軟體傳遞訊號中...

![](https://i.imgur.com/vg125U2.png)

## 手機端安裝與設定 Stream Live

搜尋 streamlabs 安裝後點擊進入

![](https://i.imgur.com/y5yNAdW.png)

### 以 YT 的帳密進行登入

![](https://i.imgur.com/kmJ0seF.gif)


### 開啟硬體使用權限與選用軟體插件
開啟相機與麥克風權限

![](https://i.imgur.com/SOo8k24.gif)

選擇軟體插件

![](https://i.imgur.com/XS9pe40.png)

完成安裝準備開始囉

![](https://i.imgur.com/YFIWN67.png)

### 直播設定
主畫面預設會驅動後相機顯示，請按左上角的選單

![](https://i.imgur.com/F2xTko3.jpg)

按 Settings 進行影片耗用頻寬的調校

![](https://i.imgur.com/dRLeDCI.png)

首先針對 Broadcast 中的 Max Video Bitrate 最大的影像傳輸速率進行調整，其預設為 2500 kbps，若網路還算穩定時，可如下圖往上調到 4000 kbps

![](https://i.imgur.com/UyNGRJG.gif)

<!-- ![](https://i.imgur.com/qMHv3TH.png)
![](https://i.imgur.com/EDgDmhc.png)
![](https://i.imgur.com/nSQ6zyR.png)
 -->

回上層選單後，其次對 Audio 聲音的取樣頻率進行調整，預設為 Very High，在此調降為 High，若要直播音樂類型的活動則不需調整。

![](https://i.imgur.com/Cm3A5bg.gif)

<!-- ![](https://i.imgur.com/KtlDbFV.png)
![](https://i.imgur.com/sj7hD58.png)
 -->

## 手機開始串流訊號給 YT
按下直播鍵後，選擇直播方式中的第三項：Upcoming Event，此時請點在YT後臺設定的直播頻道名稱：手機直播測試，正常傳送訊號時左上角會出現 fps 與 bps。

![](https://i.imgur.com/pOIGO5g.gif)

<!-- ![](https://i.imgur.com/d3svkek.jpg)
![](https://i.imgur.com/DCsbkEl.png)
![](https://i.imgur.com/rpfzyuQ.jpg)
![](https://i.imgur.com/rBk1Atu.jpg) -->


## YT 端接收後之設定
在確定預覽畫面有訊號進來後，請點選右上角的進行直播

![](https://i.imgur.com/T2clBcl.png)

此時請按右上角的分享圖示，將直播網址複製出來公布

![](https://i.imgur.com/35OAnx2.png)

## 手機端停止直播或暫停直播
手機畫面按下停止鍵，將停止傳送訊號，接下來軟體會詢問是要結束此次直播還是暫停，若本次直播想結束，請選擇 Finish Event，若是想暫時休息，請按 Keep Event。

![](https://i.imgur.com/eSXyhVw.gif)

:::info
若暫時休息後再開始傳送訊號時，請選擇 Active Event 才能挑選上次保留下來的直播頻道。
:::
<!-- ![](https://i.imgur.com/KgVlywp.jpg)
![](https://i.imgur.com/SU0PgoZ.jpg) -->

## YT端收到直播結束訊號
Youtube 後台收到直播結束的訊號後，會跳出直播結束的視窗

![](https://i.imgur.com/Dv55G2O.png)

## 參考網站
- [2.3 手機直播：Streamlabs: Stream Live](https://www.asustor.com/online/College_topic?topic=131&lan=zh_tw#2.3)
- [Streaming on iOS using the Streamlabs App](https://support.blueye.no/hc/en-us/articles/360012453939-Streaming-on-iOS-using-the-Streamlabs-App)

:::success
- Author：朱孝國
- Last Modified：2020/07/16
:::