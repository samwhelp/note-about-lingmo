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
* [開始「視窗移動」](#開始視窗移動)
* [開始「視窗更改大小」](#開始視窗更改大小)
* [永遠在最上方](#永遠在最上方)
* [永遠在最下方](#永遠在最下方)
* [內容區塊收合](#內容區塊收合)
* [切換顯示隱藏視窗裝飾](#切換顯示隱藏視窗裝飾)
* [將下方視窗移上來](#將下方視窗移上來)
* [視窗移動至畫面中央部位](#視窗移動至畫面中央部位)
* [透明度](#透明度)




## 關閉視窗

| 按鍵組合   | 功能      | 執行指令         |
| ---------- | --------- | ---------------- |
| `Win + q`  | 關閉視窗  | `Window Close=`  |


> 一般是採用「`Alt + F4`」來「關閉視窗」。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L121)

``` sh
Window Close=Meta+Q,Alt+F4,Close Window
```




## 全螢幕

| 按鍵組合   | 功能        | 執行指令              |
| ---------- | ----------- | --------------------- |
| `Win + f`  | 視窗全螢幕  | `Window Fullscreen=`  |
| `F11`      | 視窗全螢幕  | `Window Fullscreen=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L122)

``` sh
Window Fullscreen=F11\tMeta+F,none,Make Window Fullscreen
```




## 最大化

| 按鍵組合   | 功能        | 執行指令            |
| ---------- | ----------- | ------------------- |
| `Win + w`  | 視窗最大化  | `Window Maximize=`  |


> 也可以在「標題列」，使用「滑鼠左鍵」，點選兩下，切換視窗最大化。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L126)

``` sh
Window Maximize=Meta+W\tMeta+PgUp,Meta+PgUp,Maximize Window
```




## 最小化

| 按鍵組合   | 功能        | 執行指令            |
| ---------- | ----------- | ------------------- |
| `Win + x`  | 視窗最小化  | `Window Minimize=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L129)

``` sh
Window Minimize=Meta+X\tMeta+PgDown,Meta+PgDown,Minimize Window
```




## 開始「視窗移動」

| 按鍵組合   | 功能              | 執行指令        |
| ---------- | ----------------- | --------------- |
| `Win + e`  | 開始「視窗移動」  | `Window Move=`  |


> 按「Escape」鍵，取消「開始視窗移動」。

> 我比較常用的是另一種方式，採用「`Win + [滑鼠左鍵按住拖曳]`」來「移動視窗」。

> 也可以在「視窗標題列」，採用「`[滑鼠左鍵按住拖曳]`」來「移動視窗」。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L130)

``` sh
Window Move=Meta+E,none,Move Window
```




## 開始「視窗更改大小」

| 按鍵組合   | 功能                  | 執行指令          |
| ---------- | --------------------- | ----------------- |
| `Win + r`  | 開始「視窗更改大小」  | `Window Resize=`  |


> 按「Escape」取消「開始視窗更改大小」。

> 我比較常用的是另一種方式，採用「`Win + [滑鼠右鍵按住拖曳]`」來「更改視窗大小」。

> 也可以在「視窗八方邊界」，採用「`[滑鼠左鍵按住拖曳]`」來「更改視窗大小」。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L152)

``` sh
Window Resize=Meta+R,none,Resize Window
```




## 永遠在最上方

| 按鍵組合   | 功能                  | 執行指令                       |
| ---------- | --------------------- | ------------------------------ |
| `Win + t`  | 視窗保持永遠在最上方  | `Window Above Other Windows=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L119)

``` sh
Window Above Other Windows=Meta+T,none,Keep Window Above Others
```




## 永遠在最下方

| 按鍵組合   | 功能                  | 執行指令                       |
| ---------- | --------------------- | ------------------------------ |
| `Win + b`  | 視窗保持永遠在最下方  | `Window Below Other Windows=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L120)

``` sh
Window Below Other Windows=Meta+B,none,Keep Window Below Others
```




## 內容區塊收合

| 按鍵組合   | 功能              | 執行指令         |
| ---------- | ----------------- | ---------------- |
| `Win + y`  | 視窗內容區塊收合  | `Window Shade=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L153)

``` sh
Window Shade=Meta+Y,none,Shade Window
```




## 切換顯示隱藏視窗裝飾

| 按鍵組合   | 功能                               | 執行指令             |
| ---------- | ---------------------------------- | -------------------- |
| `Win + n`  | 切換顯示隱藏視窗裝飾(Decorations)  | `Window No Border=`  |


> 視窗裝飾(Decorations)，最明顯的，就可以看到標題列隱藏或是顯示。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L132)

``` sh
Window No Border=Meta+N,none,Hide Window Border
```




## 將下方視窗移上來

| 按鍵組合   | 功能              | 執行指令                      |
| ---------- | ----------------- | ----------------------------- |
| `Win + z`  | 將下方視窗移上來  | `Toggle Window Raise/Lower=`  |


> 反覆按，就會形成在最上方兩個視窗做切換的效果。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L106)

``` sh
Toggle Window Raise/Lower=Meta+Z,none,Toggle Window Raise/Lower
```




## 視窗移動至畫面中央部位

| 按鍵組合   | 功能                    | 執行指令              |
| ---------- | ----------------------- | --------------------- |
| `Win + m`  | 視窗移動至畫面中央部位  | `Window Move Center`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L131)

``` sh
Window Move Center=Meta+M,none,Move Window to the Center
```




## 透明度

| 按鍵組合   | 功能          | 執行指令             |
| ---------- | ------------- | -------------------- |
| `Win + ;`  | 視窗更加透明  | `Decrease Opacity=`  |
| `Win + '`  | 視窗更不透明  | `Increase Opacity=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L47)

``` sh
Increase Opacity=Meta+',none,Increase Opacity of Active Window by 5 %
```


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L51)

``` sh
Decrease Opacity=Meta+;,none,Decrease Opacity of Active Window by 5 %
```
