---
title: 設定「桌面圖片」
nav_order: 7010
has_children: false
parent: 外觀設定介面
grand_parent: 外觀設定
---


# 設定「桌面圖片」

* [設定檔](#設定檔)
* [設定指令](#設定指令)




## 設定檔

| 設定檔 |
| ----- |
| [~/.config/lingmoos/theme.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoos/theme.conf) |





## 設定指令


> Wallpaper / set

執行下面指令，將「Lingmo」的「桌面圖片」設定為「/usr/share/backgrounds/lingmoos/grass1.jpg」。

``` sh
qdbus com.lingmo.Settings /Theme com.lingmo.Theme.setWallpaper "/usr/share/backgrounds/lingmoos/grass1.jpg"
```


> 設定片段： [~/.config/lingmoos/theme.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoos/theme.conf#L15)

``` ini
Wallpaper=/usr/share/backgrounds/lingmoos/grass2.jpg
```




> Wallpaper / get

執行下面指令，獲得「Lingmo」目前設定的「桌面圖片路徑」。

``` sh
qdbus com.lingmo.Settings /Theme com.lingmo.Theme.wallpaper
```

顯示

```
/usr/share/backgrounds/lingmoos/grass1.jpg
```
