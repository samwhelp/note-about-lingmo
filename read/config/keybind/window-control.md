---
title: 視窗基本操作
nav_order: 5020
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 視窗基本操作

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)


## 主題

* [關閉視窗](#關閉視窗)
* [全螢幕](#全螢幕)
* [最大化](#最大化)
* [最小化](#最小化)
* [開始視窗移動](#開始視窗移動)
* [開始視窗更改大小](#開始視窗更改大小)
* [永遠在最上方](#永遠在最上方)
* [永遠在最下方](#永遠在最下方)
* [內容區塊收合](#內容區塊收合)
* [切換顯示隱藏視窗裝飾](#切換顯示隱藏視窗裝飾)
* [將下方視窗移上來](#將下方視窗移上來)
* [視窗移動至畫面中央部位](#視窗移動至畫面中央部位)
* [透明度](#透明度)


## 關閉視窗

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L127)

| 按鍵組合          | 功能     | 執行指令         |
| ----------------- | -------- | ---------------- |
| `Win + q`         | 關閉視窗 | `Window Close=` |
| `Alt + F4`         | 關閉視窗 | `Window Close=` |


## 全螢幕

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L128)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + f` | 視窗全螢幕 | `Window Fullscreen=` |
| `F11` | 視窗全螢幕 | `Window Fullscreen=` |


## 最大化

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L132)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + w` | 視窗最大化 | `Window Maximize=` |
| `Win + PgUp` | 視窗最大化 | `Window Maximize=` |

> 也可以在「標題列」，使用「滑鼠左鍵」，點選兩下，切換視窗最大化。


## 最小化

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L135)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + x` | 視窗最小化 | `Window Minimize=` |
| `Win + PgDown` | 視窗最小化 | `Window Minimize=` |


## 開始視窗移動

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L136)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + e` | 開始視窗移動 | `Window Move=` |

> 按「Escape」鍵，取消「開始視窗移動」。


## 開始視窗更改大小

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L158)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + r` | 開始視窗更改大小 | `Window Resize=` |

> 按「Escape」取消「開始視窗更改大小」。


## 永遠在最上方

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L125)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + t` | 視窗保持永遠在最上方 | `Window Above Other Windows=` |


## 永遠在最下方

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L126)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + b` | 視窗保持永遠在最下方 | `Window Below Other Windows=` |


## 內容區塊收合

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L159)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + y` | 視窗內容區塊收合 | `Window Shade=` |


## 切換顯示隱藏視窗裝飾

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L138)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + n` | 切換顯示隱藏視窗裝飾(Decorations) | `Window No Border=` |

> 視窗裝飾(Decorations)，最明顯的，就可以看到標題列隱藏或是顯示。


## 將下方視窗移上來

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L112)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + z` | 將下方視窗移上來 | `Toggle Window Raise/Lower=` |


## 視窗移動至畫面中央部位

* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L137)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + m` | 視窗移動至畫面中央部位 | `Window Move Center` |


## 透明度


* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L53)
* [設定片段](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L57)

| 按鍵組合          | 功能     | 執行指令         |
| --------- | ---------- | ----------------------------- |
| `Win + ;` | 視窗更加透明 | `Decrease Opacity=` |
| `Win + '` | 視窗更不透明 | `Increase Opacity=` |
