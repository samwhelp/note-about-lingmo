---
title: 視窗平鋪移動操作
nav_order: 5022
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 視窗平鋪移動操作

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)




## 主題

* [移動到側邊(side)](#移動到側邊side)




## 移動到側邊(side)

| 按鍵組合          | 功能           | 執行指令              |
| ----------------- | -------------- | ---------------------------- |
| `Win + Up` | 視窗更改大小，移動至北方(畫面上半部) | `Window Quick Tile Top=` |
| `Win + Down` | 視窗更改大小，移動至南方(畫面下半部)  | `Window Quick Tile Bottom=` |
| `Win + Left` | 視窗更改大小，移動至西方(畫面左半部) | `Window Quick Tile Left=`  |
| `Win + Right` | 視窗更改大小，移動至東方(畫面右半部) | `Window Quick Tile Right=` |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L143-L150)

``` sh
Window Quick Tile Top=Meta+Up,Meta+Up,Quick Tile Window to the Top

Window Quick Tile Bottom=Meta+Down,Meta+Down,Quick Tile Window to the Bottom

Window Quick Tile Left=Meta+Left,Meta+Left,Quick Tile Window to the Left

Window Quick Tile Right=Meta+Right,Meta+Right,Quick Tile Window to the Right
```
