---
title: 使用情境 / 檔案管理器導向的操作
nav_order: 1030
has_children: false
parent: 工作流程
grand_parent: 概覽
---


# 檔案管理器導向的操作




## 主題

* [解說](#解說)
* [接下來](#接下來)
* [相關連結](#相關連結)




## 解說

延續之前提到的「[如何開啟開啟應用程式](https://samwhelp.github.io/note-about-lingmo/read/guide/workflow/launch-application.html)」。


我個人目前在電腦上的操作，大概是「編輯檔案」，所以流程上大致如下

* 開啟「檔案管理器」
* 找到「要編輯的檔案」
* 直接點選開啟，或是按下「滑鼠右鍵」，顯示「檔案操作選單」，選擇要操作的動作，或是要用什麼慣用的程式開啟。
* 按下「F4」，就會開啟「慣用的終端機」，並且「切換路徑」到「所在的資料夾」。


> 目前「`lingmo-filemanager`」，並沒有「按下快捷鍵，開啟終端機」的功能。所以要透過『按下「滑鼠右鍵」，顯示「檔案操作選單」，點選「Open Terminal Here」』這流程達成。


> 根據上面提到的操作導向，我有設定如下的「按鍵綁定」。

| 按鍵組合          | 功能           | 執行指令                        | 備註            |
| ----------------- | -------------- | ------------------------------- | --------------- |
| `Alt + Shift + f` | 開啟檔案管理器 | `lingmo-filemanager`            | 主要檔案管理器  |
| `Alt + Shift + g` | 開啟檔案管理器 | `pcmanfm-qt`                    | 備用檔案管理器  |




## 其他

> 我另外有寫了不同的微調腳本，根據不同的「檔案管理器為主」所作的「按鍵綁定」。

| 檔案管理器導向 | 設定檔 |
| ------------- | ----- |
| [keybind-mode-lingmo-filemanager](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/alternative-config/keybind/keybind-mode-lingmo-filemanager) | [~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/alternative-config/keybind/keybind-mode-lingmo-filemanager/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc#L42-L48) |
| [keybind-mode-pcmanfm-qt](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/alternative-config/keybind/keybind-mode-pcmanfm-qt) | [~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/alternative-config/keybind/keybind-mode-pcmanfm-qt/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc#L42-L48) |
| [keybind-mode-thunar](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/alternative-config/keybind/keybind-mode-thunar) | [~/.config/lingmoglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/alternative-config/keybind/keybind-mode-thunar/asset/overlay/etc/skel/.config/lingmoglobalshortcutsrc#L42-L48) |




## 接下來

> 接下來介紹「[常用的視窗操作](https://samwhelp.github.io/note-about-lingmo/read/guide/workflow/window-control.html)」。




## 相關連結

* [鍵盤按鍵綁定一覽表](https://samwhelp.github.io/note-about-lingmo/read/cheatsheet/keybind.html#開啟應用程式--常用的應用程式)
* 按鍵綁定　/ [顯示「應用程式啟動選單」](https://samwhelp.github.io/note-about-lingmo/read/config/keybind/system-menu.html#顯示應用程式啟動選單)
* 按鍵綁定　/ [開啟常用的應用程式](https://samwhelp.github.io/note-about-lingmo/read/config/keybind/application-launch-favorite.html)
