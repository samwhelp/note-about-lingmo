---
title: 佈景主題來源「Fluent」
nav_order: 7040
has_children: false
parent: 佈景主題來源
grand_parent: 佈景主題
---


# 佈景主題來源「Fluent」




## 主題

* [佈景主題來源](#佈景主題來源)
* [外觀設定樣式](#外觀設定樣式)




## 佈景主題來源

| 佈景主題來源 | 如何安裝 |
| ---------- | ------- |
| vinceliuice / [Fluent-kde](https://github.com/vinceliuice/Fluent-kde) | [如何安裝](#如何安裝fluent-kde) |
| vinceliuice / [Fluent-gtk-theme](https://github.com/vinceliuice/Fluent-gtk-theme) | [如何安裝](#如何安裝fluent-gtk-theme) |
| vinceliuice / [Fluent-icon-theme](https://github.com/vinceliuice/Fluent-icon-theme) | |
| yeyushengfan258 / [Citrus-icon-theme](https://github.com/yeyushengfan258/Citrus-icon-theme) | [如何安裝](https://samwhelp.github.io/note-about-lingmo/read/subject/theme/source/Citrus.html#如何安裝citrus-icon-theme) |




## 外觀設定樣式

| 外觀設定樣式 |
| ---------- |
| [Fluent](https://samwhelp.github.io/note-about-lingmo/read/subject/style/recipe/Fluent.html) |




## 如何安裝「Fluent-kde」

執行下面指令，Clone「[Fluent-kde](https://github.com/vinceliuice/Fluent-kde)」

``` sh
git clone https://github.com/vinceliuice/Fluent-kde.git
```

執行下面指令，切換到「Fluent-kde」這個資料夾

``` sh
cd Fluent-kde
```

執行下面指令，觀看有那些參數可以下

``` sh
./install.sh -h
```

顯示

```
Usage: ./install.sh [OPTION]...

OPTIONS:
  -n, --name NAME         Specify theme name (Default: Fluent)
  -t, --theme VARIANT     Specify theme color variant(s) [default|purple|pink|red|orange|yellow|green|grey|teal|all] (Default: blue)
  -c, --color VARIANT     Specify color variant(s) [standard|light|dark] (Default: All variants)s)
  --round VARIANT         Specify round variant
  --solid VARIANT         Specify solid variant
  -h, --help              Show help
```

> 執行下面指令安裝

``` sh
./install.sh
```




## 如何安裝「Fluent-gtk-theme」

執行下面指令，Clone「[Fluent-gtk-theme](https://github.com/vinceliuice/Fluent-gtk-theme)」

``` sh
git clone https://github.com/vinceliuice/Fluent-gtk-theme.git
```

執行下面指令，切換到「Fluent-gtk-theme」這個資料夾

``` sh
cd Fluent-gtk-theme
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

  -n, --name NAME         Specify theme name (Default: Fluent)

  -t, --theme VARIANT     Specify theme color variant(s) [default|purple|pink|red|orange|yellow|green|teal|grey|all] (Default: blue)

  -c, --color VARIANT     Specify color variant(s) [standard|light|dark] (Default: All variants)s)

  -s, --size VARIANT      Specify size variant [standard|compact] (Default: All variants)

  -i, --icon VARIANT      Specify icon variant(s) for shell panel
                          [default|apple|simple|gnome|ubuntu|arch|manjaro|fedora|debian|void|opensuse|popos|mxlinux|zorin|endeavouros|tux|nixos]
                          (Default: Windows)

  -l, --libadwaita        Install link to gtk4 config for theming libadwaita

  -r, --remove
  -u, --uninstall         Uninstall/remove themes or link for libadwaita

  --tweaks                Specify versions for tweaks [solid|float|round|blur|noborder|square]
                          solid:    no transparency version
                          float:    floating panel
                          round:    rounded windows
                          blur:     blur version for 'Blur-Me'
                          noborder: windows and menu with no border
                          square:   square windows button

  -h, --help              Show help
```

> 執行下面指令，安裝「grey」這個色系

``` sh
./install.sh -t grey --tweaks float
```

> 或是執行下面指令，安裝「所有」色系

``` sh
./install.sh -t all --tweaks float
```
