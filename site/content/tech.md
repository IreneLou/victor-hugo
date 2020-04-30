---
title: install ubuntu 18.04 網路設定
date: {}
draft: false
published: true
---

# Install ubuntu 18.04 網路設定 😸

Ctrl+Alt+F2 切換畫面進入cmd狀態，可下指令確認網路狀態
(Ctrl+Alt+F1 視覺化界面、Ctrl+Alt+F2~F7  文字介面tt2~tt7 terminal)

Note 1.
**確認網孔接線、與IP設定的網卡有無匹配(注意!!注意!!注意!!)**
如果配對成功會有Running，設定不吻合安裝介面會error

>ifconfig

![image.png]({{site.baseurl}}/site/content/image.png)

Note 2.
確認網路線從對的IP pool牽出來
`  ping Gateway  
  ping NameServer (8.8.8.8)  
  ping www.google.com  `

Note 3.
確認安裝完的網路設定以及可修改的位置

vim /etc/netplan/XX-cloud-init.yaml or /etc/network/interfaces + /etc/resolv.conf!

![image_2.png]({{site.baseurl}}/site/content/image_2.png)


## EXTRA

**dhclient --- 可以重新取得IP，但是其他網卡的網路不會中斷**

dhclient是主動向DHCP Server要求IP的指令，若只想針對eth0這張網卡要求新的IP時可以輸入: 

 > dhclient eth0

如果沒有指定網卡，會讓系統內全部的網卡重新抓取IP喔!

https://david50.pixnet.net/blog/post/27179542

