---
title: 視窗聚焦切換
nav_order: 5025
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 視窗聚焦切換

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)




## 主題

* [前後聚焦切換](#前後聚焦切換)
* [前後聚焦切換 (Alternative)](#前後聚焦切換-alternative)




## 前後聚焦切換

| 按鍵組合    | 功能                    | 執行指令                           |
| ----------- | ----------------------- | ---------------------------------- |
| `Win + a`   | 聚焦切換到前面一個視窗  | `Walk Through Windows (Reverse)=`  |
| `Win + s`   | 聚焦切換到後面一個視窗  | `Walk Through Windows=`            |


> 關於「`Win + s`」就是知名「`Alt + Tab`」的功能。


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L111-L112)

``` sh
Walk Through Windows=Meta+S,Alt+Tab,Walk Through Windows
Walk Through Windows (Reverse)=Meta+A,Alt+Shift+Backtab,Walk Through Windows (Reverse)
```


> 目前這組切換的顯示效果，是設定採用「`ling_thumbnail`」

> 關於「`ling_thumbnail`」是放在「[/usr/share/kwin/tabbox/ling_thumbnail](https://github.com/LingmoOS/lingmo-kwin-plugins/tree/main/tabbox/ling_thumbnail)」這個資料夾。


* [設定片段: ~/.config/kwinrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kwinrc#L59-L60)

``` ini
[TabBox]
LayoutName=ling_thumbnail
```




## 前後聚焦切換 (Alternative)

| 按鍵組合     | 功能                    | 執行指令                                       |
| ------------ | ----------------------- | ---------------------------------------------- |
| `Win + Esc`  | 聚焦切換到前面一個視窗  | `Walk Through Windows Alternative=`            |
| `Alt + Esc`  | 聚焦切換到後面一個視窗  | `Walk Through Windows Alternative (Reverse)=`  |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L113-L114)

``` sh
Walk Through Windows Alternative=Meta+Esc,none,Walk Through Windows Alternative
Walk Through Windows Alternative (Reverse)=Alt+Esc,none,Walk Through Windows Alternative (Reverse)
```


> 目前這組切換的顯示效果，是設定採用「`present_windows`」


* [設定片段: ~/.config/kwinrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kwinrc#L62-L63)

``` ini
[TabBoxAlternative]
LayoutName=present_windows
```




## 用法對照

* [工作空間切換](https://samwhelp.github.io/note-about-lingmo/read/config/keybind/workspace-switch.html)
