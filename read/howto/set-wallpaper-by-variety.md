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
* [安裝](#安裝)
* [調整說明](#調整說明)
* [修改「get_wallpaper」](#修改get_wallpaper)
* [修改「set_wallpaper」](#修改set_wallpaper)
* [注意事項](#注意事項)
* [相關討論](#相關討論)




## Variety

| Link | GitHub |
| ---- | ------ |
| [Variety](https://peterlevi.com/variety/) | [GitHub](https://github.com/varietywalls/variety) |




## 設定腳本

| 設定腳本 |
| --------|
| [variety](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/tool-config/part/variety) |




## 安裝

執行下面指令，安裝「[variety](https://packages.debian.org/stable/variety)」這個「Debian Package」。

``` sh
sudo apt-get install variety
```




## 調整說明

因為目前「Variety」，並沒有支援到「Lingmo」，

所以我們必須做些許的微調，才能讓「Variety」在「Lingmo」環境有作用。

應用我們在『[透過「Dbus」設定桌面圖片](https://samwhelp.github.io/note-about-lingmo/read/howto/set-wallpaper-by-dbus.html)』這篇提到的指令。

我們需要稍微修改「[~/.config/variety/scripts/get_wallpaper](#修改get_wallpaper)」和「[~/.config/variety/scripts/set_wallpaper](#修改set_wallpaper)」這兩個腳本。


| 檔案　| 修改後 | 修改前　|
| ---- | ----- | ----- |
| [~/.config/variety/scripts/get_wallpaper](#修改get_wallpaper) | [修改後](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/variety/scripts/get_wallpaper#L17-L20) | [修改前](https://github.com/varietywalls/variety/blob/master/data/scripts/get_wallpaper#L17)　|
| [~/.config/variety/scripts/set_wallpaper](#修改set_wallpaper) | [修改後](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/variety/scripts/set_wallpaper#L208-L213) | [修改前](https://github.com/varietywalls/variety/blob/master/data/scripts/set_wallpaper#L207)　|




## 修改「get_wallpaper」

> 加入程式碼片段: [~/.config/variety/scripts/get_wallpaper](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/variety/scripts/get_wallpaper#L17-L20)

``` sh
# Lingmo OS
elif [ "$XDG_CURRENT_DESKTOP" == "Lingmo" ]; then

        qdbus com.lingmo.Settings /Theme com.lingmo.Theme.wallpaper
```




## 修改「set_wallpaper」

> 加入程式碼片段: [~/.config/variety/scripts/set_wallpaper](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/variety/scripts/set_wallpaper#L208-L213)

``` sh
# Lingmo OS
if [ "$XDG_CURRENT_DESKTOP" == "Lingmo" ]; then

    qdbus com.lingmo.Settings /Theme com.lingmo.Theme.setWallpaper "$WP" 2> /dev/null

fi
```




## 注意事項

要注意的是：

在「Lingmo」的「Xdg Autostart」機制的「`Exec=`」那個格式似乎有些限制，

因為「variety」自動產生的「~/.config/autostart/variety.desktop」

裡面的「`Exec=`」那一行的寫法，在「Lingmo」沒有作用。

所以我們要將它稍微修改簡化如下，才能在登入系統後，自動執行「variety」。

``` ini
Exec=variety
```

完整內容，請參考我修改後的「[~/.config/autostart/variety.desktop](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/tool-config/part/variety/asset/overlay/etc/skel/.config/autostart/variety.desktop#L6)」。




## 相關討論

* [在「Lingmo」環境，如何透過「Variety」設定桌面圖片](https://github.com/orgs/LingmoOS/discussions/20#discussioncomment-10852058)
