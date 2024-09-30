---
title: 按鍵綁定
nav_order: 2000
has_children: true
parent: 設定
---


# 按鍵綁定

> [鍵盤按鍵綁定一覽表](https://samwhelp.github.io/note-about-lingmo/read/cheatsheet/keybind.html)




## 主題

* [設定檔](#設定檔)
* [系統操作](#系統操作)
* [開啟應用程式](#開啟應用程式)
* [視窗操作](#視窗操作)
* [工作空間](#工作空間)
* [音量控制](#音量控制)
* [螢幕亮度控制](#螢幕亮度控制)
* [螢幕截圖](#螢幕截圖)
* [統整對照](#統整對照)
* [圖形使用者介面程式](#圖形使用者介面程式)




## 設定檔

這裡設定的根據，是採用「[我慣用的設定](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)」，

請參考「[我的設定檔](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config)」。


> 關於「按鍵綁定」的設定檔，有兩個如下

| 設定檔 |
| ----- |
| [~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc) |
| [~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc) |


> 其實可以單獨使用「~/.config/kglobalshortcutsrc」就可以實作想要的「按鍵綁定」，可以參考「[另一個範例](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/KglobalshortcutOnly-Lingmo-Dark)」。

還有參考另一篇「[如何設定KDE按鍵綁定](https://samwhelp.github.io/note-about-kde/read/howto/config-keybind-by-command.html)」的說明。

> [按鍵操作快速上手指南](https://samwhelp.github.io/system-modeling/read/zh_tw/quick-start)




## 系統操作

| 主題 |
| --- |
| [系統操作](keybind/system-control) |
| [系統選單](keybind/system-menu) |




## 開啟應用程式

| 主題 |
| --- |
| [開啟 Terminal](keybind/application-launch-terminal) |
| [開啟常用的應用程式](keybind/application-launch-favorite) |




## 視窗操作

| 主題 |
| --- |
| [視窗基本操作](keybind/window-control) |
| [視窗聚焦切換](keybind/window-focus) |
| [視窗平鋪移動操作](keybind/window-tiling-move) |




## 工作空間

| 主題 |
| --- |
| [工作空間切換](keybind/workspace-switch) |
| [視窗移到指定工作空間](keybind/window-move-to-workspace) |
| [桌面操作](keybind/desktop-control) |
| [活動操作](keybind/activity-control) |




## 音量控制

| 主題 |
| --- |
| [音量控制](keybind/volume-control) |




## 螢幕亮度控制

| 主題 |
| --- |
| [螢幕亮度控制](keybind/monitor-brightness-control) |




## 螢幕截圖

| 主題 |
| --- |
| [螢幕截圖](keybind/screenshot-control) |




## 統整對照

* [鍵盤按鍵綁定一覽表](https://samwhelp.github.io/note-about-lingmo/read/cheatsheet/keybind.html)
* [按鍵操作快速上手指南](https://samwhelp.github.io/system-modeling/read/zh_tw/quick-start)
* [通用鍵盤組合鍵操作](https://samwhelp.github.io/system-modeling/read/zh_tw/spec-keybind-common)




## 圖形使用者介面程式

* /usr/share/applications/kcm_keys.desktop

``` sh
systemsettings kcm_keys
```
