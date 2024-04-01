---
title: 開啟應用程式 (Rofi)
nav_order: 5011
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 開啟應用程式 (Rofi)

> KDE Plasma Adjustment / [Keybind](https://github.com/samwhelp/note-about-kubuntu/tree/gh-pages/_demo/prototype/de/kde-plasma/part/keybind/kde-plasma-keybind-main)


# Rofi

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L288-L298)


| 按鍵組合          | 功能                           | 執行指令                        | Desktop entries |
| ----------------- | ------------------------------ | ------------------------------- | --- |
| `Alt + Shift + d` | 開啟 Rofi (可用應用程式列表)   | `rofi -show drun -show-icons`   | [rofi-show-drun.desktop](https://github.com/samwhelp/note-about-kubuntu/blob/gh-pages/_demo/prototype/de/kde-plasma/part/keybind/kde-plasma-keybind-main/config/rofi/applications/rofi-show-drun.desktop#L3) |
| `Alt + Shift + w` | 開啟 Rofi (已經開啟的視窗列表) | `rofi -show window -show-icons` | [rofi-show-window.desktop](https://github.com/samwhelp/note-about-kubuntu/blob/gh-pages/_demo/prototype/de/kde-plasma/part/keybind/kde-plasma-keybind-main/config/rofi/applications/rofi-show-window.desktop#L3) |
| `Alt + Shift + r` | 開啟 Rofi (可用指令列表)       | `rofi -show run`                | [rofi-show-run.desktop](https://github.com/samwhelp/note-about-kubuntu/blob/gh-pages/_demo/prototype/de/kde-plasma/part/keybind/kde-plasma-keybind-main/config/rofi/applications/rofi-show-run.desktop#L3) |
