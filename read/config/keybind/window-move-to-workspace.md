---
title: 視窗移到指定工作空間
nav_order: 5041
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 視窗移到指定工作空間

> [Lingmo 微調腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark)





## 主題

* [視窗移到工作空間](視窗移到工作空間)




## 視窗移到工作空間

| 按鍵組合          | 功能     | 執行指令         |
| --------- | -------------------------------------------- | --------------------------------------------------- |
| `Alt + Shift + 1` | 「視窗」移到「工作空間 1 (File)」 | `Window to Desktop 1=` |
| `Alt + Shift + 2` | 「視窗」移到「工作空間 2 (Edit)」 | `Window to Desktop 2=` |
| `Alt + Shift + 3` | 「視窗」移到「工作空間 3 (Web) 」 | `Window to Desktop 3=` |
| `Alt + Shift + 4` | 「視窗」移到「工作空間 4 (Term)」 | `Window to Desktop 4=` |
| `Alt + Shift + 5` | 「視窗」移到「工作空間 5 (Misc)」 | `Window to Desktop 5=` |
| `Alt + Shift + 6` | 「視窗」移到「工作空間 6」        | `Window to Desktop 6=` |
| `Alt + Shift + 7` | 「視窗」移到「工作空間 7」        | `Window to Desktop 7=` |
| `Alt + Shift + 8` | 「視窗」移到「工作空間 8」        | `Window to Desktop 8=` |
| `Alt + Shift + 9` | 「視窗」移到「工作空間 9」        | `Window to Desktop 9=` |


* [設定片段: ~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L156-L175)


``` sh
Window to Desktop 1=Alt+!,none,Window to Desktop 1
Window to Desktop 2=Alt+@,none,Window to Desktop 2
Window to Desktop 3=Alt+#,none,Window to Desktop 3
Window to Desktop 4=Alt+$,none,Window to Desktop 4
Window to Desktop 5=Alt+%,none,Window to Desktop 5
Window to Desktop 6=Alt+^,none,Window to Desktop 6
Window to Desktop 7=Alt+&,none,Window to Desktop 7
Window to Desktop 8=Alt+*,none,Window to Desktop 8
Window to Desktop 9=Alt+(,none,Window to Desktop 9
```





## 用法對照

* [工作空間切換](https://samwhelp.github.io/note-about-kubuntu/read/config/keybind/workspace-switch.html)
* [應用程式切換 Tab Page](https://samwhelp.github.io/note-about-kubuntu/read/config/keybind/application-tab-page.html)
* 通用鍵盤組合鍵操作 / [使用「上排數字鍵」相關的操作](https://samwhelp.github.io/system-modeling/read/zh_tw/spec-keybind/with-number-key)
