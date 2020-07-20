---
title: OBS錄影直播
tags: 軟體使用
description: 使用OBS進行錄影、直播、導播的介紹
---

# OBS 快速上手

[![hackmd-github-sync-badge](https://hackmd.io/Vlr3zWc5S-aFxHpAB9Vjmg/badge)](https://hackmd.io/Vlr3zWc5S-aFxHpAB9Vjmg)

:::info
OBS 是一套開源跨平台的錄影與串流直播程式，許多的直播主都是利用此軟體擔任串流直播的重責大任。
:::

![](https://i.imgur.com/ODlhFQm.png)

## 簡介
Open Broadcaster Software（OBS Studio）是由 OBS Project主導的開源跨平台(Windows/Mac/Linux)錄影與串流直播程式。
OBS Studio使用 C 和 C++ 語音編寫，提供即時影音擷取與混和、多種來源組成場景、場景切換特效、基礎混音功能、錄影和串流。資料傳輸主要通過即時訊息協定（RTMP）完成，可以傳送到任何支援RTMP的目的地，包括YouTube、Twitch、Instagram 和 Facebook 等串流媒體網站。
OBS Studio 同時提供了強大的 API 與插件，或以 Lua 、Python 等語言進行客製化的調整。

![](https://i.imgur.com/nPyKfRm.png)

## 使用環境準備

### 1. 器材
- 筆電(需含webcam與麥克風)
- 螢幕(進行雙螢幕操作)
- 選用
    - 影像擷取盒
    - 攝影機
    - 混音器
    - 麥克風
    - 相關線材

### 2. 下載與安裝
請至 [OBS Studio 官網](https://obsproject.com/) 或 Github 上的 [obs-studio 專案](https://github.com/obsproject/obs-studio/releases)下載對應的版本，下載後安裝時若遇到缺乏執行階段元件的狀況(Visual C++的可轉散發套件)，系統會自動下載安裝該套件。

另外也可安裝 streamlabs 公司的 [Streamlabs OBS](https://streamlabs.com/streamlabs-obs)，它是羅技公司以 OBS 搭配 streamlabs 這套手機端開串流直播的免費編碼軟體所改寫的版本。
<!-- 
streamlabs obs
![](https://i.imgur.com/13hFEgk.png)
![](https://i.imgur.com/7Z4CbXT.png) 
-->

### 3. 設定
首次使用 OBS Studio軟體時，OBS Studio 會執行『自動設定精靈』，此精靈可以針對『串流』或『錄影』的場合來做最佳化的設定，此處請按否。
![](https://i.imgur.com/KeD0ZFX.png)
之後若需要的話，可在選單中的工具，選擇自動設定精靈，此處讓我們以手動方式設定各項參數，請按畫面右下角的設定
![](https://i.imgur.com/xLRjEDh.png)
以下介紹最重要的三大類設定：

#### 3.1 影像
我們知道影片是由連續的影像組合而成的，此處是定義單張影像所使用的解析度、壓縮方式以及每秒多少幀(Frame Per Second; FPS)。

![](https://i.imgur.com/qs19EE3.png)

#### 3.2 輸出
此處是串流與錄影的影片編碼設定，通常建議串流部分編碼器選擇硬體編碼，而錄影部分選擇 x264(CPU編碼)，而串流部分因為牽扯到上傳頻寬、串流平台限制以及觀眾下載頻寬等因素，還要額外設定影音的位元率(可用向外流的水管大小比喻)。

當輸出模式調整為『進階』時，可進行更細部的控制。

![](https://i.imgur.com/tZgYASp.png)

#### 3.3 串流
在此輸入串流平台的伺服器與金鑰，目前支援的平台有 Twitch、Youtube、Facebook、Vimeo、Twitter...等，可按服務欄位右側展開看到所有支援的清單。

![](https://i.imgur.com/NVCzpGD.png)
> Youtube 首次啟用直播的帳戶要等待24小時。

### 4. 來源
首次使用必須設定影像的來源，請按下圖的 :heavy_plus_sign: 

![](https://i.imgur.com/0D9G66h.png)

通常有雙螢幕時選擇顯示器擷取，單螢幕時使用視窗擷取，以下是所有支援的訊號來源

![](https://i.imgur.com/IhysUw0.png)

#### 4.1 顯示器擷取
選擇顯示器擷取後，此處可命名此顯示器名稱(左螢幕、右螢幕亦可)，按下確定

![](https://i.imgur.com/kxszSZA.png)

選擇與 OBS 軟體所在不同的螢幕

![](https://i.imgur.com/apHWBGZ.png)

設定好之後如下圖，此時若要移除該來源，請點擊下方的 :heavy_minus_sign: 

![](https://i.imgur.com/4hK8g2E.png)

:::danger
可能遭遇問題：
- 筆電無法擷取螢幕畫面：通常是因為筆電配有內顯(整合圖形省電GPU)與獨顯(高效能GPU)二種顯示卡，但桌面顯示使用到的是內顯，而 OBS 使用的是獨顯，所以無法擷取到內顯的畫面，此時只要在顯示器的設定中，更改圖形的喜好設定應用程式，找到 OBS 的選項，更改為使用內顯GPU即可，詳細步驟可參考：[解法1](https://russquan.gitlab.io/obs-black-screen-fix-win10/)，[解法2](https://www.kjnotes.com/freeware/99#toc--obs-win10-)
:::

#### 4.2 視窗擷取
若只有一個螢幕可操作，或有多個應用程式的視窗想擷取，則可用此模式

![](https://i.imgur.com/npYVSbO.png)

此處可點選視窗這欄位的下拉選單，OBS會呈現出目前運作中的程式視窗，通常上方的預覽畫面會呈現出該視窗的內容，若仍是黑黑一片，則可能要調整下方的擷取方式。

![](https://i.imgur.com/Y8k2oZv.png)

:::danger
可能遭遇問題：
- 擷取不到瀏覽器的畫面：可試試關閉瀏覽器的硬體加速功能
![](https://i.imgur.com/g6RWhVT.png)
:::

#### 4.3 視訊擷取裝置
也可以抓取 webcam 或來自擷取卡/盒的訊號，此處可命名為該裝置的名稱以資辨別。

![](https://i.imgur.com/eQFEGX3.png)

此處選擇 webcam 後按確定

![](https://i.imgur.com/v7NUUmz.png)

可用滑鼠拖曳改變不同來源所占畫面的大小

![](https://i.imgur.com/nkAguqW.png)

#### 4.4 文字 (GDI+)
若要加上標題或跑馬燈之類的文字，可利用文字 (GDI+)功能。

![](https://i.imgur.com/ercKkMa.png)

打入所需要的文字，並設定相關屬性

![](https://i.imgur.com/H3ftxjo.png)

在加入的文字來源上按下滑鼠右鍵，選擇濾鏡功能

![](https://i.imgur.com/1jqnuYj.png)

選擇捲動濾鏡

![](https://i.imgur.com/bXwQ3Au.png)
![](https://i.imgur.com/y6lJvqu.png)

設定捲動的水平速度

![](https://i.imgur.com/TgmaohS.png)

### 5. 場景
場景是存放來源的容器，場景可以由多個來源組成，並可快速切換，至少要有一個場景存在，剛才設定的來源預設都在第一個場景中，以下建立第二個場景

![](https://i.imgur.com/mwcDg8C.png)

輸入場景名稱後，按確定

![](https://i.imgur.com/clYDvAI.png)

此時場景位於場景 2，來源未設定，請設定為視窗擷取

![](https://i.imgur.com/cNvpQ6G.png)

之後請切換不同的場景，可看見包含的來源也跟著切換

![](https://i.imgur.com/FLa25wl.gif)

## 錄影
按下右下角的開始錄製，會針對目前OBS的主視窗開始錄製。

![](https://i.imgur.com/NZWthhK.png)

錄製中可按下停止錄製，或右邊的暫停，下方會顯示目前錄製的時間。

![](https://i.imgur.com/lzGu4rC.png)

錄製的檔案預設會放在使用者家目錄的影片資料夾，以副檔名 mkv 存放。

![](https://i.imgur.com/2a2htu3.png)

若要改變預設值，可到設定->輸出->錄影->錄影路徑中更改。

![](https://i.imgur.com/XP9sxzZ.png)

## 導播
導播功能其實就是實作導播機上的 Program(節目) 與 Preview(預覽) ，此功能至少要設定二個場景之後才能使用。此時請按下右側的工作室模式，再按一次則離開此模式。

![](https://i.imgur.com/CBxBzJj.png)

目前停留的場景一開始會出現在右側的 Program(節目)與左側的Preview(預覽)。

![](https://i.imgur.com/jn1amr5.png)

此時按下另一個場景時，會變動的是 Preview(預覽)，以避免影響Program(節目)的進行。

![](https://i.imgur.com/kA8RaxZ.png)

此時可按下中間的轉場選單，切換Preview(預覽)與Program(節目)。

![](https://i.imgur.com/cxr0T9Z.png)

若要將每個場景呈現畫面預覽，OBS提供了如同硬體導播機常見的 Multi View 功能，最多可同時檢視 8 個場景，位於如下圖的檢視選單中

![](https://i.imgur.com/B5ub8hc.png)

以視窗方式呈現 Multi View
![](https://i.imgur.com/Xbp5Wxq.png)

## 直播
要進行串流直播前，需先至設定的「串流」與「輸出」中，將金鑰、影像位元率等先設定好，然後按下右下角的「開始串流」

![](https://i.imgur.com/kex7M9T.png)

直播時，下方的狀態列會出現 Live 的經過時間以及目前上傳的頻寬耗用，若出現黃燈或紅燈則代表頻寬不夠用了，要去看看設定中的 FPS 與影音位元率的數值是否合理，不然就是頻寬被其他裝置佔用了。要停止直播的話，請按下停止串流。

![](https://i.imgur.com/SWYfRHL.png)

## 參考
* [OBS Studio 專業的螢幕錄製與串流直播免費軟體安裝教學](https://www.kjnotes.com/freeware/99)
* [OBS 開台教學、實況直播軟體下載設定](https://tw.pikolive.com/liveteach/obs)
* [OBS教學，強大的直播錄影軟體設定與應用](https://medium.com/@yuchuanlee/obs%E6%95%99%E5%AD%B8-%E5%BC%B7%E5%A4%A7%E7%9A%84%E7%9B%B4%E6%92%AD%E9%8C%84%E5%BD%B1%E8%BB%9F%E9%AB%94%E8%A8%AD%E5%AE%9A%E8%88%87%E6%87%89%E7%94%A8-4d65785dfa71)
* [OBS-Studio的x264直播設定方法](https://blog.xuite.net/knight.ex/blog/503222355)
* [OBS Studio 虛擬攝影棚開講](https://sites.google.com/view/obs-tw/obs-studio-%E8%99%9B%E6%93%AC%E6%94%9D%E5%BD%B1%E6%A3%9A%E9%96%8B%E8%AC%9B)
* [實況直播工具集](https://hackmd.io/@Eotones/stream/%2F%40Eotones%2FrJP1WLpI4)
* [直播讀書會](https://newsveg.tw/blog/3641)
* [手把手教你做直播！4K直播了解一下？](https://youtu.be/SRWpUvBtnZI)
* [麥克風音量好小怎麼辦?](https://suwife.pixnet.net/blog/post/310240847)

:::success
- Author：朱孝國
- Last Modified：2020/07/20
:::