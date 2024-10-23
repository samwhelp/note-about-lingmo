---
title: 設定「SDDM Theme」
nav_order: 7050
has_children: false
parent: 如何
---


# 設定「SDDM Theme」




## 主題

* [相關連結](#相關連結)
* [前提](#前提)
* [說明](#說明)




## 相關連結

| 相關連結 |
| ------- |
| [SDDM 設定目前採用的佈景主題](https://samwhelp.github.io/note-about-sddm/read/howto/config-current-theme.html) |
| [SDDM 更改某個佈景主題的背景圖片](https://samwhelp.github.io/note-about-sddm/read/howto/custom-theme-background.html) |
| Arch Wiki / SDDM / [Theme settings](https://wiki.archlinux.org/title/SDDM#Theme_settings) |
| SDDM Wiki / Theming / [Theme Configuration](https://github.com/sddm/sddm/wiki/Theming#theme-configuration) |
| Github / sddm / data / themes / maldives / [Main.qml](https://github.com/sddm/sddm/blob/develop/data/themes/maldives/Main.qml#L58-L68) |
| Github / sddm / data / themes / maldives / [theme.conf](https://github.com/sddm/sddm/blob/develop/data/themes/maldives/theme.conf#L1-L2) |
| Github / KDE / sddm-kcm / src / [themesmodel.cpp](https://github.com/KDE/sddm-kcm/blob/master/src/themesmodel.cpp#L183-L195) |




## 前提

> 在「Lingmo OS」預設採用的「SDDM Theme」是「[lingmo-sddm-theme](https://github.com/LingmoOS/lingmo-sddm-theme)」。

> 設定採用的設定檔是「[/etc/sddm.conf](https://github.com/LingmoOS/lingmo-sddm-theme/blob/main/sddm.conf)」，設定片段如下

``` ini
[Theme]
Current=lingmo
```




## 說明
