---
title: 鍵盤按鍵綁定一覽表
nav_order: 9010
has_children: false
parent: 一覽表
---


# 鍵盤按鍵綁定一覽表




## 主題

* [設定檔](#設定檔)
* [系統操作](#系統操作)
* [開啟應用程式](#開啟應用程式)
* [視窗操作](#視窗操作)
* [工作空間](#工作空間)
* [音量控制](#音量控制)
* [螢幕亮度控制](#螢幕亮度控制)
* [螢幕截圖](#螢幕截圖)
* [相關連結](#相關連結)




## 設定檔

> 關於「按鍵綁定」的設定檔，有兩個如下

| Config File |
| ----------- |
| [~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc) |
| [~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc) |




## 系統操作

| 按鍵組合           | 功能                                    | 執行指令                   |
| ------------------ | --------------------------------------- | -------------------------- |
| `Alt + Shift + x`  | 顯示「離開系統選單」                    | `lingmo-shutdown`          |
| `Alt + Shift + l`  | 鎖住螢幕                                | `lingmo-screenlocker`      |
| `Win + d`          | 切換「顯示桌面」                        | `Show Desktop=`            |
| `Win + grave`      | 顯示「工作空間選單」                    | `ShowDesktopGrid=`         |
| `Win + Tab`        | 切換「顯示目前工作空間的所有視窗預覽」  | `Expose=`                  |
| `Alt + F1`         | 顯示「應用程式啟動選單」                | `lingmo-launcher`          |
| `Win + Space`      | 顯示「應用程式啟動選單」                | `lingmo-launcher`          |
| `Alt + F3`         | 顯示「視窗操作選單」                    | `Window Operations Menu=`  |
| `Alt + Space`      | 顯示「視窗操作選單」                    | `Window Operations Menu=`  |
| `Win + c`          | 顯示「所有開啟視窗預覽」                | `ExposeAll=`               |
| `Alt + F2`         | 執行 krunner                            | `krunner`                  |




## 開啟應用程式

> 可以按下「`Alt + F1`」執行「`lingmo-launcher`」，就可以找到其他的「應用程式」來執行




## 開啟應用程式 / Terminal

| 按鍵組合           | 功能           | 執行指令           |
| ------------------ | -------------- | ------------------ |
| `Alt + Enter`      | 開啟 Terminal  | `lingmo-terminal`  |
| `Alt + Shift + a`  | 開啟 Terminal  | `lingmo-terminal`  |
| `Alt + Ctrl + a`   | 開啟 Terminal  | `sakura`           |
| `Alt + Shift + t`  | 開啟 Terminal  | `xfce4-terminal`   |
| `Alt + Ctrl + t`   | 開啟 Terminal  | `qterminal`        |




## 開啟應用程式 / 常用的應用程式

| 按鍵組合           | 功能            | 執行指令                         |
| ------------------ | --------------- | -------------------------------- |
| `Alt + Shift + f`  | 開啟檔案管理器  | `lingmo-filemanager`             |
| `Alt + Shift + g`  | 開啟檔案管理器  | `pcmanfm-qt`                     |
| `Alt + Shift + e`  | 開啟文字編輯器  | `lingmo-texteditor`              |
| `Alt + Shift + b`  | 開啟網頁瀏覽器  | `firefox --new-tab about:blank`  |




## 相關連結

| 相關連結 |
| ------- |
| [鍵盤按鍵綁定](https://samwhelp.github.io/note-about-lingmo/read/config/keybind.html) |
