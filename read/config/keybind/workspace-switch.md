---
title: 工作空間切換
nav_order: 5040
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 工作空間切換

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)


## 我個人定義的個工作空間

| 工作空間 | 名稱  |
| -------- | ----- |
| 1        | File  |
| 2        | Edit  |
| 3        | Web   |
| 4        | Term  |
| 5        | Misc  |


## 指定切換

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L79-L98)

| 按鍵組合  | 功能                    | 執行指令                       |
| --------- | ----------------------- | ------------------------------ |
| `Alt + Ctrl + 1` | 切換到工作空間 1 (File) | `Switch to Desktop 1=` |
| `Alt + Ctrl + 2` | 切換到工作空間 2 (Edit) | `Switch to Desktop 2=` |
| `Alt + Ctrl + 3` | 切換到工作空間 3 (Web)  | `Switch to Desktop 3=` |
| `Alt + Ctrl + 4` | 切換到工作空間 4 (Term) | `Switch to Desktop 4=` |
| `Alt + Ctrl + 5` | 切換到工作空間 5 (Misc) | `Switch to Desktop 5=` |
| `Alt + Ctrl + 6` | 切換到工作空間 6        | `Switch to Desktop 6=` |
| `Alt + Ctrl + 7` | 切換到工作空間 7        | `Switch to Desktop 7=` |
| `Alt + Ctrl + 8` | 切換到工作空間 8        | `Switch to Desktop 8=` |
| `Alt + Ctrl + 9` | 切換到工作空間 9        | `Switch to Desktop 9=` |



## 循環切換

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L73-L74)


| 按鍵組合  | 功能                 | 執行指令                   |
| --------- | -------------------- | -------------------------- |
| `Alt + a` | 切換到上一個工作空間 | `Switch One Desktop to the Left=` |
| `Alt + s` | 切換到下一個工作空間 | `Switch One Desktop to the Right=` |


* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L113-L114)

| 按鍵組合  | 功能                 | 執行指令                   |
| --------- | -------------------- | -------------------------- |
| `Alt + h` | 切換到上一個工作空間 | `Walk Through Desktop List (Reverse)=` |
| `Alt + l` | 切換到下一個工作空間 | `Walk Through Desktop List=` |




## 用法對照

* [視窗移到指定工作空間](https://samwhelp.github.io/note-about-kubuntu/read/config/keybind/window-move-to-workspace.html)
* [應用程式切換 Tab Page](https://samwhelp.github.io/note-about-kubuntu/read/config/keybind/application-tab-page.html)
* [聚焦或開啟常用的應用程式](https://samwhelp.github.io/note-about-kubuntu/read/config/keybind/application-focus-or-launch-favorite.html)
* 通用鍵盤組合鍵操作 / [使用「上排數字鍵」相關的操作](https://samwhelp.github.io/system-modeling/read/zh_tw/spec-keybind/with-number-key)
