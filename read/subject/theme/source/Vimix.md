---
title: 佈景主題來源「Vimix」
nav_order: 7030
has_children: false
parent: 佈景主題來源
grand_parent: 佈景主題
---


# 佈景主題來源「Vimix」




## 主題

* [佈景主題來源](#佈景主題來源)
* [外觀設定樣式](#外觀設定樣式)




## 佈景主題來源

| 佈景主題來源 | 如何安裝 |
| ---------- | ------- |
| vinceliuice / [Vimix-kde](https://github.com/vinceliuice/Vimix-kde) | [如何安裝](#如何安裝vimix-kde) |
| vinceliuice / [Vimix-gtk-themes](https://github.com/vinceliuice/Vimix-gtk-themes) | [如何安裝](#如何安裝vimix-gtk-themes) |
| vinceliuice / [Vimix-icon-theme](https://github.com/vinceliuice/Vimix-icon-theme) | |
| vinceliuice / [Vimix-cursors](https://github.com/vinceliuice/Vimix-cursors) | |
| yeyushengfan258 / [Citrus-icon-theme](https://github.com/yeyushengfan258/Citrus-icon-theme) | [如何安裝](https://samwhelp.github.io/note-about-lingmo/read/subject/theme/source/Citrus.html#如何安裝citrus-icon-theme) |




## 外觀設定樣式

| 外觀設定樣式 |
| ---------- |
| [Vimix](https://samwhelp.github.io/note-about-lingmo/read/subject/style/recipe/Vimix.html) |




## 如何安裝「Vimix-kde」

執行下面指令，Clone「[Vimix-kde](https://github.com/vinceliuice/Vimix-kde)」

``` sh
git clone https://github.com/vinceliuice/Vimix-kde.git
```

執行下面指令，切換到「Vimix-kde」這個資料夾

``` sh
cd Vimix-kde
```

執行下面指令，觀看有那些參數可以下

``` sh
./install.sh -h
```

顯示

```
Usage: ./install.sh [OPTIONS...]

OPTIONS:
  -d, --dest DIR           Specify theme destination directory (Default: )
  -n, --name NAME          Specify theme name (Default: Vimix)
  -t, --theme VARIANTS     Specify hue theme variant(s) [standard|doder|beryl|ruby|amethyst|jade] (Default: All variants)
  -b, --blur               Specify blur theme variants
  -h, --help               Show this help
```

> 執行下面指令安裝

``` sh
./install.sh
```




## 如何安裝「Vimix-gtk-themes」

執行下面指令，Clone「[Vimix-gtk-themes](https://github.com/vinceliuice/Vimix-gtk-themes)」

``` sh
git clone https://github.com/vinceliuice/Vimix-gtk-themes.git
```

執行下面指令，切換到「Vimix-gtk-themes」這個資料夾

``` sh
cd Vimix-gtk-themes
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
  -n, --name NAME         Specify theme name (Default: Vimix)
  -t, --theme VARIANT     Specify theme color variant(s) [doder|beryl|ruby|amethyst|jade|grey|all] (Default: doder(blue))
  -c, --color VARIANT     Specify color variant(s) [standard|light|dark] (Default: All variants)
  -s, --size  VARIANT     Specify size variant [standard|compact|all] (Default: standard variant)

  -l, --libadwaita        Link installed gtk-4.0 theme to config folder for all libadwaita app use this theme

  -r, --remove,
  -u, --uninstall         Uninstall/Remove installed themes

  -tweaks, --tweaks       Specify versions for tweaks [flat|grey|mix|translucent] (only nord and dracula can not mix use with!)
                          1. flat         Flat and normal button style for windows control buttons
                          2. grey         Use grey windows control buttons in grey accent color variants
                          3. mix          Mix theme color and dark grey color for background color in darkmode variants
                          4. translucent  Translucent panel version

  -h, --help              Show help
```

> 執行下面指令安裝

``` sh
./install.sh -t all --tweaks flat grey mix translucent
```
