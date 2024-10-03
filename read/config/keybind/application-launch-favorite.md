---
title: 開啟應用程式 (常用的)
nav_order: 5013
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 開啟應用程式 (常用的)

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)




## 主題

* [常用的應用程式](#常用的應用程式)
* [其他](#其他)
* [相關議題](#相關議題)



## 常用的應用程式

| 按鍵組合           | 功能            | 執行指令                         |
| ------------------ | --------------- | -------------------------------- |
| `Alt + Shift + f`  | 開啟檔案管理器  | `lingmo-filemanager`             |
| `Alt + Shift + g`  | 開啟檔案管理器  | `pcmanfm-qt`                     |
| `Alt + Shift + e`  | 開啟文字編輯器  | `lingmo-texteditor`              |
| `Alt + Shift + b`  | 開啟網頁瀏覽器  | `firefox --new-tab about:blank`  |
| `Alt + Shift + s`  | 開啟系統設定    | `lingmo-settings`                |


* [設定片段: ~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc#L42-L56)

``` ini
[Alt%2BShift%2BF]
Comment=File Manager
Exec=lingmo-filemanager

[Alt%2BShift%2BG]
Comment=File Manager
Exec=pcmanfm-qt

[Alt%2BShift%2BE]
Comment=Text Editor
Exec=lingmo-texteditor

[Alt%2BShift%2BB]
Comment=Web Browser
Exec=firefox --new-tab about:blank
```


``` ini
[Alt%2BShift%2BS]
Comment=System Settings
Exec=lingmo-settings
```




## 其他

> 可以按下「`Alt + F1`」執行「`lingmo-launcher`」，就可以找到其他的「應用程式」來執行




## 相關議題

* [鍵盤按鍵綁定 / 開啟終端機](https://samwhelp.github.io/note-about-lingmo/read/config/keybind/application-launch-terminal.html)
