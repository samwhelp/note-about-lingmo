---
title: 佈景主題來源「Graphite」
nav_order: 7020
has_children: false
parent: 佈景主題來源
grand_parent: 佈景主題
---


# 佈景主題來源「Graphite」




## 主題

* [佈景主題來源](#佈景主題來源)
* [外觀設定樣式](#外觀設定樣式)




## 佈景主題來源

| 佈景主題來源 | 如何安裝 |
| ---------- | ------- |
| vinceliuice / [Graphite-kde-theme](https://github.com/vinceliuice/Graphite-kde-theme) | [如何安裝](#如何安裝graphite-kde-theme) |
| vinceliuice / [Graphite-gtk-theme](https://github.com/vinceliuice/Graphite-gtk-theme) | [如何安裝](#如何安裝graphite-gtk-theme) |
| yeyushengfan258 / [Citrus-icon-theme](https://github.com/yeyushengfan258/Citrus-icon-theme) | [如何安裝](https://samwhelp.github.io/note-about-lingmo/read/subject/theme/source/Citrus.html#如何安裝citrus-icon-theme) |


> 搜尋：「[graphite](https://github.com/vinceliuice?tab=repositories&q=graphite)」




## 外觀設定樣式

| 外觀設定樣式 |
| ---------- |
| [Graphite](https://samwhelp.github.io/note-about-lingmo/read/subject/style/recipe/Graphite.html) |




## 如何安裝「Graphite-kde-theme」

執行下面指令，Clone「[Graphite-kde-theme](https://github.com/vinceliuice/Graphite-kde-theme)」

``` sh
git clone https://github.com/vinceliuice/Graphite-kde-theme.git
```

執行下面指令，切換到「Graphite-kde-theme」這個資料夾

``` sh
cd Graphite-kde-theme
```

執行下面指令，觀看有那些參數可以下

``` sh
./install.sh -h
```

顯示

```
Usage: ./install.sh [OPTION]...

OPTIONS:
  -n, --name NAME         Specify theme name (Default: Graphite)
  -t, --theme VARIANT     Specify theme color variant(s) [default|nord] (Default: All variants)s)
  -c, --color VARIANT     Specify color variant(s) [standard|light|dark] (Default: All variants)s)
  --rimless VARIANT       Specify rimless variant

  -h, --help              Show help
```

> 執行下面指令安裝

``` sh
./install.sh
```




## 如何安裝「Graphite-gtk-theme」

執行下面指令，Clone「[Graphite-gtk-theme](https://github.com/vinceliuice/Graphite-gtk-theme)」

``` sh
git clone https://github.com/vinceliuice/Graphite-gtk-theme.git
```

執行下面指令，切換到「Graphite-gtk-theme」這個資料夾

``` sh
cd Graphite-gtk-theme
```

執行下面指令，觀看有那些參數可以下

``` sh
./install.sh -h
```

顯示

```
'gnome-shell' not found, using styles for last gnome-shell version available.
Usage: ./install.sh [OPTION]...

OPTIONS:
  -d, --dest DIR          Specify destination directory (Default: ~/.local/share/themes)

  -n, --name NAME         Specify theme name (Default: Graphite)

  -t, --theme VARIANT     Specify theme color variant(s) [default|purple|pink|red|orange|yellow|green|teal|blue|all] (Default: grey)

  -c, --color VARIANT     Specify color variant(s) [standard|light|dark] (Default: All variants)s)

  -s, --size VARIANT      Specify size variant [standard|compact] (Default: standard variants)

  -g, --gdm               Install GDM theme

  -l, --libadwaita        Install link to gtk4 config for theming libadwaita

  -u, --uninstall
  -r, --remove            Uninstall/Remove themes or link for libadwaita

  --tweaks                Specify versions for tweaks [nord|black|darker|rimless|normal]
                          (WORRING: 'nord' and 'darker' can not mix use with 'black'!)
                          1. nord       Nord colorscheme version
                          2. black      Blackness colorscheme version
                          3. darker     Darker (default|nord) color version (black option can not be darker)
                          4. rimless    Remove the 2px outline about windows and menus
                          5. normal     Normal sidebar style (Nautilus)
                          6. float      Float gnome-shell panel style
                          7. colorful   Colorful gnome-shell panel style

  -h, --help              Show help
```

> 執行下面指令安裝

``` sh
./install.sh -t all
```
