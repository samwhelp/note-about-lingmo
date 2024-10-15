---
title: 設定「Qt Style」
nav_order: 7030
has_children: false
parent: 如何
---


## 設定「Qt Style」




## 主題

* [環境變數](#環境變數)
* [設定環境變數「QT_STYLE_OVERRIDE」](#設定環境變數qt_style_override)
* [設定「Qt Style」採用「kvantum」](#設定qt-style採用kvantum)
* [設定「Qt Style」採用「gtk2」](#設定qt-style採用gtk2)
* [設定範例](#設定範例)
* [Source](#source)
* [相關連結](#相關連結)




## 環境變數

執行

``` sh
env | grep QT | sort -u
```

顯示

``` sh
QT_ACCESSIBILITY=1
QT_AUTO_SCREEN_SCALE_FACTOR=0
QT_IM_MODULE=fcitx
QT_LINUX_ACCESSIBILITY_ALWAYS_ON=1
QT_PLATFORM_PLUGIN=lingmo
QT_QPA_PLATFORMTHEME=lingmo
QT_QPA_PLATFORM=xcb
QT_QPA_UPDATE_IDLE_TIME=10
QT_SCREEN_SCALE_FACTORS=1
QTWEBENGINE_DICTIONARIES_PATH=/usr/share/hunspell-bdic/
```

在設定「Qt Style」這個議題，我們關注的是其中兩行如下

``` sh
QT_PLATFORM_PLUGIN=lingmo
QT_QPA_PLATFORMTHEME=lingmo
```

這兩個「環境變數」是在「`lingmo-session`」設定的

程式碼片段: [lingmo-core/session/application.cpp](https://github.com/LingmoOS/lingmo-core/blob/main/session/application.cpp#L183-L185)

``` cpp
    // Qt
    qputenv("QT_QPA_PLATFORMTHEME", "lingmo");
    qputenv("QT_PLATFORM_PLUGIN", "lingmo");
```

也就是設定「Qt Style」採用「lingmo」。

原始碼專案是「GitHub / LingmoOS / [lingmo-qt-plugins](https://github.com/LingmoOS/lingmo-qt-plugins)」。

然後「Debian Package」是「`lingmo-qt-plugins`」。

執行

``` sh
dpkg -L lingmo-qt-plugins
```

顯示

```
/.
/usr
/usr/lib
/usr/lib/x86_64-linux-gnu
/usr/lib/x86_64-linux-gnu/qt5
/usr/lib/x86_64-linux-gnu/qt5/plugins
/usr/lib/x86_64-linux-gnu/qt5/plugins/platformthemes
/usr/lib/x86_64-linux-gnu/qt5/plugins/platformthemes/liblingmoplatformtheme.so
/usr/lib/x86_64-linux-gnu/qt5/plugins/styles
/usr/lib/x86_64-linux-gnu/qt5/plugins/styles/liblingmostyle.so
/usr/share
/usr/share/doc
/usr/share/doc/lingmo-qt-plugins
/usr/share/doc/lingmo-qt-plugins/changelog.gz
/usr/share/doc/lingmo-qt-plugins/copyright
```



## 設定環境變數「QT_STYLE_OVERRIDE」

因為「`QT_QPA_PLATFORMTHEME`」已經被「`lingmo-session`」設定了，

> 所以我們可以透過另一個變數「`QT_STYLE_OVERRIDE`」來切換「Qt Style」。

舉例: 可以產生一個檔案「/etc/profile.d/qt-style.sh」，內容如下

``` sh
export QT_STYLE_OVERRIDE=kvantum
```




## 設定「Qt Style」採用「kvantum」

執行下面指令，安裝「[qt5-style-kvantum](https://packages.debian.org/stable/qt5-style-kvantum)」

``` sh
sudo apt-get install qt5-style-kvantum
```

執行

``` sh
dpkg -L qt5-style-kvantum | grep plugin
```

顯示

```
/usr/lib/x86_64-linux-gnu/qt5/plugins
/usr/lib/x86_64-linux-gnu/qt5/plugins/styles
/usr/lib/x86_64-linux-gnu/qt5/plugins/styles/libkvantum.so
```

> 設定「Qt Style」採用「`kvantum`」，可以產生一個檔案「/etc/profile.d/qt-style.sh」，內容如下

``` sh
export QT_STYLE_OVERRIDE=kvantum
```

> 執行「`kvantummanager`」來設定採用「Kvantum Theme」，設定值會儲存在「~/.config/Kvantum/kvantum.kvconfig」這個檔案，內容類似如下

``` ini
[General]
theme=KvArcDark
```

> 重新開機後，再次登入系統，就可以看到效果。

> 可以執行「pcmanfm-qt」來觀看效果。


| Debian Package |
| -------------- |
| [qt5-style-kvantum](https://packages.debian.org/stable/qt5-style-kvantum) |
| [qt5-style-kvantum-l10n](https://packages.debian.org/stable/qt5-style-kvantum-l10n) |
| [qt5-style-kvantum-themes](https://packages.debian.org/stable/qt5-style-kvantum-themes) |


> 更多採用「kvantum」的「[外觀設定樣式](https://samwhelp.github.io/note-about-lingmo/read/subject/style/recipe.html)」




## 設定「Qt Style」採用「gtk2」

以下步驟可以讓「Qt Style」跟隨「gtk2」的設定。

執行下面指令，安裝「[qt5-gtk2-platformtheme](https://packages.debian.org/stable/qt5-gtk2-platformtheme)」

``` sh
sudo apt-get install qt5-gtk2-platformtheme
```


執行

``` sh
dpkg -L qt5-style-kvantum | grep plugin
```

顯示

```
/usr/lib/x86_64-linux-gnu/qt5/plugins
/usr/lib/x86_64-linux-gnu/qt5/plugins/platformthemes
/usr/lib/x86_64-linux-gnu/qt5/plugins/platformthemes/libqgtk2.so
/usr/lib/x86_64-linux-gnu/qt5/plugins/styles
/usr/lib/x86_64-linux-gnu/qt5/plugins/styles/libqgtk2style.so
```

> 設定「Qt Style」採用「`gtk2`」，可以產生一個檔案「/etc/profile.d/qt-style.sh」，內容如下

``` sh
export QT_STYLE_OVERRIDE=gtk2
```

> 產生一個檔案「[~/.gtkrc-2.0](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.gtkrc-2.0#L8)」，內容類似如下

``` ini
gtk-theme-name="Lingmo-dark"
gtk-icon-theme-name="Crule-dark"
gtk-font-name="Sans 12"
gtk-cursor-theme-name="lingmo-dark"
gtk-cursor-theme-size=24
```

> 關於「`gtk-theme-name="Lingmo-dark"`」指的是「`/usr/share/themes/Lingmo-dark/gtk-2.0/`」。


> 關於「`gtk-icon-theme-name="Crule-dark"`」指的是「`/usr/share/icons/Crule-dark/`」。


> 關於「`gtk-cursor-theme-name="lingmo-dark"`」指的是「`/usr/share/icons/lingmo-dark/cursors/`」。


> 重新開機後，再次登入系統，就可以看到效果。

> 可以執行「pcmanfm-qt」來觀看效果。


| Debian Package |
| -------------- |
| [qt5-style-plugins](https://packages.debian.org/stable/qt5-style-plugins) |
| [qt5-gtk2-platformtheme](https://packages.debian.org/stable/qt5-gtk2-platformtheme) |
| [qt5-style-plugin-cleanlooks](https://packages.debian.org/stable/qt5-style-plugin-cleanlooks) |
| [qt5-style-plugin-motif](https://packages.debian.org/stable/qt5-style-plugin-motif) |
| [qt5-style-plugin-plastique](https://packages.debian.org/stable/qt5-style-plugin-plastique) |


> 關於「[qt5-style-plugins](https://packages.debian.org/stable/qt5-style-plugins)」是「[Debian Meta Package](https://wiki.debian.org/metapackage)」，可以直接安裝它，就會連帶安裝「qt5-gtk2-platformtheme」，「qt5-style-plugin-cleanlooks」，「qt5-style-plugin-motif」，「qt5-style-plugin-plastique」。




## 設定範例

| 設定範例 |
| ------- |
| [qt-style-follow-gtk2](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/qt-style-config/qt-style-follow-gtk2) |
| [qt-style-follow-kvantum](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/qt-style-config/qt-style-follow-kvantum) |
| [qt-style-follow-lingmo](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/qt-style-config/qt-style-follow-lingmo) |



## Source

| Source |
| ------ |
| GitHub / qt / [qtstyleplugins](https://github.com/qt/qtstyleplugins) |
| GitHub / tsujan / [Kvantum](https://github.com/tsujan/Kvantum) |
| GitHub / LingmoOS / [lingmo-qt-plugins](https://github.com/LingmoOS/lingmo-qt-plugins) |


| Source |
| ------ |
| GitHub / qt / [qtbase](https://github.com/qt/qtbase/blob/dev/src/gui/kernel/qplatformtheme.cpp#L36) |




## 相關連結

* [外觀設定樣式](https://samwhelp.github.io/note-about-lingmo/read/subject/style/recipe.html)
