---
title: 開啟應用程式 (Terminal)
nav_order: 5010
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 開啟應用程式 (Terminal)

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)




## 主題

* [一般終端機](#一般終端機)
* [相關議題](#相關議題)




## 一般終端機

| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------- | --------------------------- |
| `Alt + Enter`     | 開啟 Terminal | `lingmo-terminal`           |


| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------- | --------------------------- |
| `Alt + Shift + a` | 開啟 Terminal | `lingmo-terminal`           |
| `Alt + Ctrl + a`  | 開啟 Terminal | `sakura`                    |


| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------- | --------------------------- |
| `Alt + Shift + t` | 開啟 Terminal | `xfce4-terminal`            |
| `Alt + Ctrl + t`  | 開啟 Terminal | `qterminal`                 |


* [設定片段: ~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc#L18-L36)

``` ini
[Alt%2BShift%2BT]
Comment=Terminal
Exec=xfce4-terminal

[Alt%2BCtrl%2BT]
Comment=Terminal
Exec=qterminal

[Alt%2BReturn]
Comment=Terminal
Exec=lingmo-terminal

[Alt%2BShift%2BA]
Comment=Terminal
Exec=lingmo-terminal

[Alt%2BCtrl%2BA]
Comment=Terminal
Exec=sakura
```




## 相關議題

* [鍵盤按鍵綁定 / 開啟常用的應用程式](https://samwhelp.github.io/note-about-lingmo/read/config/keybind/application-launch-favorite.html)
