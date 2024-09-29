---
title: 開啟應用程式 (Terminal)
nav_order: 5010
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 開啟應用程式 (Terminal)

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)


## 一般

* [設定片段 / konsole](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L207-L211)

| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------- | --------------------------- |
| `Alt + Enter`     | 開啟 Terminal | `konsole`                 |
| `Alt + Shift + a` | 開啟 Terminal | `konsole`                 |
| `Alt + Shift + t` | 開啟 Terminal | `konsole`                 |


* [設定片段 / sakura](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L300-L302)

| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------- | --------------------------- |
| `Alt + Ctrl + a`  | 開啟 Terminal | `sakura`                 |
| `Alt + Ctrl + t`  | 開啟 Terminal | `sakura`                 |


## 下拉式

* [設定片段 / yakuake](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L236-L238)

| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------------------- | ---------------------------- |
| `Win + F2` | 開啟 Terminal (Drop Down) | `yakuake` |
| `Alt + Shift + y` | 開啟 Terminal (Drop Down) | `yakuake` |

> 這個綁定，即使「yakuake」沒有常駐，也能觸發。


* [設定片段 / yakuake](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L324-L326)

| 按鍵組合          | 功能         | 執行指令                     |
| ----------------- | ------------------------- | ---------------------------- |
| `F12` | 開啟 Terminal (Drop Down) | `yakuake` |

> 這個綁定，需要「yakuake」已經常駐，才能觸發。
