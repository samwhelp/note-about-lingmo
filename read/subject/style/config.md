---
title: 外觀設定介面
nav_order: 7010
has_children: true
parent: 外觀設定
---


# 外觀設定介面




## 主題

* [設定檔](#設定檔)
* [設定](#設定)
* [設定「桌面圖片」](#設定桌面圖片)
* [設定「Icon Theme」](#設定icon-theme)




## 設定檔

| 設定檔 |
| ----- |
| [~/.config/lingmoos/theme.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoos/theme.conf) |




## 設定

| 設定 | More |
| ---- | ---- |
| [設定「桌面圖片」](#設定桌面圖片) | [More](config/wallpaper) |




## 設定「桌面圖片」


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




## 設定「Icon Theme」


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
