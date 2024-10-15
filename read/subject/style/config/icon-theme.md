---
title: 設定「Icon Theme」
nav_order: 7020
has_children: false
parent: 外觀設定介面
grand_parent: 外觀設定
---


# 設定「Icon Theme」

* [設定檔](#設定檔)
* [設定指令](#設定指令)




## 設定檔

| 設定檔 |
| ----- |
| [~/.config/lingmoos/theme.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoos/theme.conf) |





## 設定指令


> IconTheme / set

執行下面指令，將「Lingmo」的「Icon Theme」設定為「/usr/share/backgrounds/lingmoos/grass1.jpg」。

``` sh
qdbus com.lingmo.Settings /Theme com.lingmo.Theme.setIconTheme "Crule-dark"
```


> 設定片段： [~/.config/lingmoos/theme.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoos/theme.conf#L13)

``` ini
IconTheme=Crule-dark
```




> Icon Theme / get

執行下面指令，獲得「Lingmo」目前設定的「Icon Theme」。

``` sh
qdbus com.lingmo.Settings /Theme com.lingmo.Theme.iconTheme
```

顯示

```
Crule-dark
```
