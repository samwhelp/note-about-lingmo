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

> 設定「Qt Style」採用「kvantum」，可以產生一個檔案「/etc/profile.d/qt-style.sh」，內容如下

``` sh
export QT_STYLE_OVERRIDE=kvantum
```

> 執行「`kvantummanager`」來設定採用「Kvantum Theme」，設定值會儲存在「~/.config/Kvantum/kvantum.kvconfig」這個檔案，內容類似如下

``` ini
[General]
theme=KvArcDark
```

重新開機後，再次登入系統，就可以看到效果。

可以執行「pcmanfm-qt」來觀看效果。

| Debian Package |
| -------------- |
| [qt5-style-kvantum](https://packages.debian.org/stable/qt5-style-kvantum) |
| [qt5-style-kvantum-l10n](https://packages.debian.org/stable/qt5-style-kvantum-l10n) |
| [qt5-style-kvantum-themes](https://packages.debian.org/stable/qt5-style-kvantum-themes) |




## 設定「Qt Style」採用「gtk2」
