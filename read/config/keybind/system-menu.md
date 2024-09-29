---
title: 系統選單
nav_order: 5002
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 系統選單

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)


## 顯示「視窗操作選單」

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L144)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Alt + F3`  | 顯示「視窗操作選單」 | `Window Operations Menu=` |
| `Alt + Space`  | 顯示「視窗操作選單」 | `Window Operations Menu=` |

> 也可以在「視窗標題列」使用「滑鼠右鍵」，就會顯示「視窗操作選單」。


## 顯示「開始功能表」

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L265)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Alt + F1`  | 顯示「桌面操作選單」 | `activate widget 3=` |
| `Win + Space`  | 顯示「桌面操作選單」 | `activate widget 3=` |


> 使用「Win鍵」顯示「開始功能表」的功能被我停用了。

> 請參考『[停用「Win鍵」開啟「開始功能表」](https://samwhelp.github.io/note-about-kubuntu/read/howto/disable-opening-application-launcher-with-super-key.html)』


## 顯示「顯示所有開啟視窗」

* [設定片段](https://github.com/samwhelp/note-about-mabox/tree/gh-pages/_demo/project/mabox-adjustment/asset/overlay/etc/skel/.config/openbox/share/gen/openbox-gen-rc/Section/Keybind/MenuClientList.php#L55)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Win + c`  | Toggle Present Windows (All desktops) | `ExposeAll=` |


## krunner

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L213-L216)


| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Alt + F2`  | 執行 krunner | `krunner` |


## System Activity

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L26)


| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Ctrl + Esc`  | Show System Activity | `Show System Activity=` |


