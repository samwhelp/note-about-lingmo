---
title: 透過「Variety」設定桌面圖片
nav_order: 7020
has_children: false
parent: 如何
---


# 透過「Variety」設定桌面圖片




## 主題

* [Variety](#variety)
* [設定腳本](#設定腳本)
* [說明](#說明)




## Variety

| Link | GitHub |
| ---- | ------ |
| [Variety](https://peterlevi.com/variety/) | [GitHub](https://github.com/varietywalls/variety) |




## 設定腳本

| 設定腳本 |
| --------|
| [variety](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/tool-config/part/variety) |




## 說明

因為目前「Variety」，並沒有支援到「Lingmo」，

所以我們必須做些許的微調，才能讓「Variety」在「Lingmo」環境有作用。

應用我們在『[透過「Dbus」設定桌面圖片](https://samwhelp.github.io/note-about-lingmo/read/howto/set-wallpaper-by-dbus.html)』這篇提到的指令。

我們需要稍微修改「[~/.config/variety/scripts/get_wallpaper](#)」和「[~/.config/variety/scripts/set_wallpaper](#)」這兩個腳本。


| 檔案　| 修改後 | 修改前　|
| ---- | ----- | ----- |
| [~/.config/variety/scripts/get_wallpaper](#) | [修改後](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/variety/scripts/get_wallpaper#L13-L16) | [修改前](https://github.com/varietywalls/variety/blob/master/data/scripts/get_wallpaper#L17)　|
| [~/.config/variety/scripts/set_wallpaper](#) | [修改後](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/variety/scripts/set_wallpaper#L208-L213) | [修改前](https://github.com/varietywalls/variety/blob/master/data/scripts/set_wallpaper#L207)　|




## 修改「get_wallpaper」




## 修改「set_wallpaper」



## 注意事項
