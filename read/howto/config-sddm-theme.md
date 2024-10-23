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
* [設定範例](#設定範例)
* [「SDDM」自帶的「Theme」](#sddm自帶的theme)




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

> 可以執行「[sddm --example-config](https://samwhelp.github.io/note-about-sddm/read/command/sddm.html#example-config)」來了解所有的參數和預設值。




## 說明

> 以下以[內建](https://github.com/sddm/sddm/tree/develop/data/themes)的「[sddm-theme-maldives](https://packages.debian.org/stable/sddm-theme-maldives)」為例來說明。


* [安裝「sddm-theme-maldives」](#安裝sddm-theme-maldives)
* [設定採用「sddm-theme-maldives」](#設定採用sddm-theme-maldives)
* [設定「sddm-theme-maldives」的「背景圖」](#設定sddm-theme-maldives的背景圖)
* [如何預覽](#如何預覽)




## 安裝「sddm-theme-maldives」

> 執行下面指令，安裝「[sddm-theme-maldives](https://packages.debian.org/stable/sddm-theme-maldives)」

``` sh
sudo apt-get install sddm-theme-maldives
```

執行

``` sh
dpkg -L sddm-theme-maldives
```

顯示

```
/.
/usr
/usr/share
/usr/share/doc
/usr/share/doc/sddm-theme-maldives
/usr/share/doc/sddm-theme-maldives/README
/usr/share/doc/sddm-theme-maldives/changelog.Debian.gz
/usr/share/doc/sddm-theme-maldives/changelog.gz
/usr/share/doc/sddm-theme-maldives/copyright
/usr/share/sddm
/usr/share/sddm/themes
/usr/share/sddm/themes/maldives
/usr/share/sddm/themes/maldives/Main.qml
/usr/share/sddm/themes/maldives/angle-down.png
/usr/share/sddm/themes/maldives/background.jpg
/usr/share/sddm/themes/maldives/maldives.jpg
/usr/share/sddm/themes/maldives/metadata.desktop
/usr/share/sddm/themes/maldives/rectangle.png
/usr/share/sddm/themes/maldives/theme.conf
```

> 主要的資料夾在「[/usr/share/sddm/themes/maldives](https://github.com/sddm/sddm/tree/develop/data/themes/maldives)」




## 設定採用「sddm-theme-maldives」

> 編輯「`/etc/sddm.conf`」，設定片段修改成如下

``` ini
[Theme]
Current=maldives
```

> 登出就可以看到效果。




## 設定「sddm-theme-maldives」的「背景圖」

執行下面指令，觀看「[/usr/share/sddm/themes/maldives/theme.conf](https://github.com/sddm/sddm/blob/develop/data/themes/maldives/theme.conf)」的內容

``` sh
cat /usr/share/sddm/themes/maldives/theme.conf
```

顯示

``` ini
[General]
background=background.jpg
```

> 我們可以產生一個新的檔案「[/usr/share/sddm/themes/maldives/theme.conf.user](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/sddm-config/by-theme/main/profile/Maldives/asset/overlay/usr/share/sddm/themes/maldives/theme.conf.user)」，內容如下

``` ini
[General]
background=/usr/share/backgrounds/lingmoos/Origin.jpg
```

> 登出就可以看到效果。




## 如何預覽

若是要預覽某個「SDDM 佈景主題」，

舉例要預覽「`/usr/share/sddm/themes/maldives`」，可以執行下面指令

``` sh
sddm-greeter --test-mode --theme /usr/share/sddm/themes/maldives
```




## 設定範例

| 設定範例 |
| ------- |
| [Lingmo](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/sddm-config/by-theme/main/profile/Lingmo) |
| [Elarun](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/sddm-config/by-theme/main/profile/Elarun) |
| [Maldives](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/sddm-config/by-theme/main/profile/Maldives) |
| [Maya](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/sddm-config/by-theme/main/profile/Maya) |
| [Maui](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/sddm-config/by-theme/main/profile/Maui) |




## 「SDDM」自帶的「Theme」

| SDDM Theme | Debian Package |
| ---------- | -------------- |
| [elarun](https://github.com/sddm/sddm/tree/develop/data/themes/elarun) | [sddm-theme-elarun](https://packages.debian.org/stable/sddm-theme-elarun) |
| [maldives](https://github.com/sddm/sddm/tree/develop/data/themes/maldives) | [sddm-theme-maldives](https://packages.debian.org/stable/sddm-theme-maldives) |
| [maya](https://github.com/sddm/sddm/tree/develop/data/themes/maya) | [sddm-theme-maya](https://packages.debian.org/stable/sddm-theme-maya) |
