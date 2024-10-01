---
title: 桌面操作
nav_order: 5045
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 桌面操作

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)




## 主題

* [桌面放大或縮小](#桌面放大或縮小)




## 桌面放大或縮小

| 按鍵組合   | 功能              | 執行指令             |
| ---------- | ----------------- | -------------------- |
| `Win + 0`  | 桌面恢復原來大小  | `view_actual_size=`  |
| `Win + -`  | 桌面縮小          | `view_zoom_out=`     |
| `Win + =`  | 桌面放大          | `view_zoom_in=`      |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L189-L191)

``` sh
view_actual_size=Meta+0,Meta+0,Zoom to Actual Size
view_zoom_in=Meta++\tMeta+=,Meta++,Zoom In
view_zoom_out=Meta+-,Meta+-,Zoom Out
```
