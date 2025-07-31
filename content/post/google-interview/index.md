---
title: 2025 上半年 Google 面試心得
date: 2025-07-31
draft: false
slug: 2025-google-interview-sharing
image:
categories:
    - 日常
---

2025 是我出社會第五年，也是我第三次挑戰 Google 面試  
本篇分享一下面試時程跟內容還有我準備跟面試的心得

## 面試時程

2/26 Recruiter 寄信聯絡  
3/3 跟 recruiter 聊天表示自己要刷題復健一下，安排三周後面試  
3/27 phone screen interview，sliding window 的題目，Medium 偏簡單  
4/10 recruiter feedback 可以進到下階段  
4/22 早上 technical interview 1  
4/22 下午 technical interview 2  
4/25 technical interview 3  
4/28 recruiter feedback 並安排 behavioral interview  
5/8 behavioral interview  
5/9 recruiter feedback BQ 結果 positive 並安排 team matching  
5/13 fit talk 1  
5/15 fit talk 2  
5/16 fit talk 3  
5/20 fit talk 4  
5/21 recruiter 說原本 fit talk 2 的 manager 有意願送 internal packet review  
6/11 聯繫 recruiter，她表示因為某些原因(我不太方便公開透露)，要額外花時間 review & approve 我的申請  
7/2 recruiter 聯繫，offer get

## 面試內容

### technical interview 1

英文面試，面試官是在台北的日本人  
難度是 medium 偏 hard  
我沒有寫出最佳解，但面試官說 acceptable  
follow up 有問我能不能再 optimize 但我努力了一下想不出來最後時間到

### technical interview 2

中文面試  
Medium  
主要是 recursive 跟資料結構設計  
雖然不難但是要 code 的量偏多，中間邏輯有點小打結被面試官提示了一下才解掉  
壓線寫完，面試官看了一下說沒問題，沒有 follow up question

### technical interview 3

中文面試  
本來 HR 跟我說會有兩輪英文，我跟面試官確認之後他說沒有特別寫要用英文就還是用中文面了  
medium 經典 dijkstra 問題 聽完題目就知道秒殺  
follow up 兩題 加了一些 graph 的 constraint 我不確定我答得對不對 面試官反應我也看不太出來

### BQ

中文面試  
我一開始以為是 HR 之類的面，結果聊到最後才知道他也是工程師  
沒什麼太 tricky 的問題，就盡量以大局為重不傷和氣回答就好了  
排 45 分鐘結果我 30 分不到就結束了，以為涼涼

## 心得

這是第三次面試 google 前面兩次都是在 phone screen 就被刷掉  
這次複習我請 chatgpt 幫我整理了一些筆記，主要是看到什麼關鍵字比較容易跟什麼算法有關係，我覺得滿實用的  
有幫助我在面試的時候比較冷靜，不會聽完題目腦袋一片空白不知道怎麼開始  
刷題的話因為我從大學就一直有在寫 Leetcode，所以題數沒什麼參考價值，總題數是 363/590/77，周賽 Rating 1933  
複習題的話刷 leetcode 75，另外針對 dijkstra, topo sort, union find 這種比較特定需要記憶的算法加強練習  
HR 說如果有需要可以幫忙安排 mock interview，沒有面過的話可以用一下這個資源

程式題面試的部分  
一開始跟面試官確定好條件還滿重要的，以免往錯誤的方向想  
可以先說你會用的算法跟大概的流程會是什麼 (譬如我會用 bfs 或是我會用 topo sort 去解之類的)  
接下來就是設計 input/output structure 跟你過程中會用到的一些 variable 要長怎樣 (譬如會用到 stack，那 stack 裡面要塞啥)  
在做這些事情的時候最好是邊說邊記錄在文件上，方便面試官理解，等下也可以直接複製貼上  
這些確定完就可以跟面試官確認可以開始寫了  
在寫的時候也別忘了邊寫邊說自己在幹嘛，為什麼要這樣寫，寫完一個小 block 也可以加一下註解以免面試官沒有跟上，或是自己大腦突然斷線  
有些面試官會沒有反應一直聽你說，就一直自言自語碎碎念一直寫就是了  
寫完要用 sample test case 手動試跑一下，不用太複雜的 test case，不然有些 for loop 很簡單但又要跑很多圈我覺得很尷尬 XD  
最後面試官通常會問你時間跟空間複雜度，看你能不能再 optimize  
有時間會再問 follow up 問題，如果時間不夠會要你口頭解釋就好，時間夠的話可以複製一份 code 直接從原本的 code 改省時間

這次的 recruiter 是中國那邊的外包 recruiter，信箱有 xWF 字眼  
人還滿好的，給了很多幫忙也很好溝通，安排 team matching 很快  
如果過程中需要什麼資源或是幫助應該都可以跟 recruiter 問問看  
大概是這樣
