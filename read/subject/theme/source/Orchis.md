---
title: 佈景主題來源「Orchis」
nav_order: 7010
has_children: false
parent: 佈景主題來源
grand_parent: 佈景主題
---


# 佈景主題來源「Orchis」




## 主題

* [佈景主題來源](#佈景主題來源)
* [外觀設定樣式](#外觀設定樣式)




## 佈景主題來源

| 佈景主題來源 | 如何安裝 |
| ---------- | ------- |
| vinceliuice / [Orchis-kde](https://github.com/vinceliuice/Orchis-kde) | [如何安裝](#如何安裝orchis-kde) |
| vinceliuice / [Orchis-theme](https://github.com/vinceliuice/Orchis-theme) | [如何安裝](#如何安裝orchis-theme) |
| yeyushengfan258 / [Citrus-icon-theme](https://github.com/yeyushengfan258/Citrus-icon-theme) | [如何安裝](https://samwhelp.github.io/note-about-lingmo/read/subject/theme/source/Citrus.html#如何安裝citrus-icon-theme) |




## 外觀設定樣式

| 外觀設定樣式 |
| ---------- |
| [Orchis](https://samwhelp.github.io/note-about-lingmo/read/subject/style/recipe/Orchis.html) |




## 如何安裝「Orchis-kde」

執行下面指令，Clone「[Orchis-kde](https://github.com/vinceliuice/Orchis-kde)」

``` sh
git clone https://github.com/vinceliuice/Orchis-kde.git
```

執行下面指令，切換到「Orchis-kde」這個資料夾

``` sh
cd Orchis-kde
```

> 執行下面指令安裝

``` sh
./install.sh
```




## 如何安裝「Orchis-theme」

執行下面指令，Clone「[Orchis-theme](https://github.com/vinceliuice/Orchis-theme)」

``` sh
git clone https://github.com/vinceliuice/Orchis-theme.git
```

執行下面指令，切換到「Orchis-theme」這個資料夾

``` sh
cd Orchis-theme
```

執行下面指令，觀看有那些參數可以下

``` sh
./install.sh -h
```

顯示

```
Usage: ./install.sh [OPTION]...

OPTIONS:
  -d, --dest DIR          Specify destination directory (Default: ~/.local/share/themes)
  -n, --name NAME         Specify theme name (Default: Orchis)

  -t, --theme VARIANT     Specify theme color variant(s) [default|purple|pink|red|orange|yellow|green|teal|grey|all] (Default: blue)
  -c, --color VARIANT     Specify color variant(s) [standard|light|dark] (Default: All variants)s)
  -s, --size VARIANT      Specify size variant [standard|compact] (Default: All variants)

  -i, --icon VARIANT      Specify icon variant(s) for shell panel activities button
                          [default|apple|simple|gnome|ubuntu|arch|manjaro|fedora|debian|void|opensuse|popos|mxlinux|zorin|endeavouros|tux|nixos|gentoo|budgie]
                          (Default: ChromeOS style)

  -l, --libadwaita        Link installed Orchis gtk-4.0 theme to config folder for all libadwaita app use Orchis theme

  --tweaks                Specify versions for tweaks [solid|compact|black|primary|macos|submenu|(nord/dracula)] (Options can mix)
                          1. solid              No transparency panel variant
                          2. compact            No floating panel variant
                          3. black              Full black variant
                          4. primary            Change radio icon checked color to primary theme color (Default is Green)
                          5. macos              Change window buttons to MacOS style
                          6. submenu            Set normal submenus color contrast (dark submenu style on dark version)
                          7. [nord|dracula]     Nord/dracula colorscheme themes (nord and dracula can not mix use!)
                          8. dock               Fix style for 'dash-to-dock' or 'ubuntu-dock' extension

  --round                 Change theme round corner border-radius [Input the px value you want] (Suggested: 2px < value < 16px)
                          1. 3px
                          2. 4px
                          3. 5px
                          ...
                          13. 15px

  --shell                 install gnome-shell version [38|40|42|44|46] (Without this option script will detect shell version and install the right theme)
                          1. 38                 Gnome-shell version <= 38.0
                          2. 40                 Gnome-shell version = 40.0
                          3. 42                 Gnome-shell version = 42.0
                          4. 44                 Gnome-shell version = 44.0
                          4. 46                 Gnome-shell version = 46.0

  -r, --remove,
  -u, --uninstall         Uninstall/Remove installed themes

  -h, --help              Show help
```

> 執行下面指令安裝

``` sh
./install.sh -t all
```
