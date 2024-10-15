---
title: 透過「Dbus」設定桌面圖片
nav_order: 7010
has_children: false
parent: 如何
---


# 透過「Dbus」設定桌面圖片




## 主題

* [探索](#探索)
* [Debian Package](#debian-package)
* [安裝「qdbus」](#安裝qdbus)
* [Help](#help)
* [參考指令](#參考指令)
* [接下來](#接下來)
* [相關連結](#相關連結)




## 探索

| Link |
| ---- |
| [lingmo-core](https://github.com/LingmoOS/lingmo-core/blob/main/settings-daemon/theme/thememanager.cpp#L301-L319) |
| [lingmo-settings](https://github.com/LingmoOS/lingmo-settings/blob/main/src/background.cpp#L16-L21) |

稍微探索了上面兩個專案，了解到，

除了可以透過「`lingmo-settings -m background`」這個「圖形介面程式」來設定「Lingmo」的「桌面圖片」。

在「Lingmo」也有提供「Dbus」的介面，

讓我們也可以透過「指令」的方式，來設定「Lingmo」的「桌面圖片」。

以下我們以「`qdbus`」為例，因為我個人的經驗，覺得這個比較容易上手。




## Debian Package

| Debian Package |
| -------------- |
| [qdbus-qt5](https://packages.debian.org/stable/qdbus-qt5) |
| [qdbus-qt6](https://packages.debian.org/stable/qdbus-qt6) |




## 安裝「qdbus」

執行下面指令，安裝「[qdbus-qt5](https://packages.debian.org/stable/qdbus-qt5)」這個「Debian Package」。

``` sh
sudo apt-get install qdbus-qt5
```




## Help

執行

``` sh
qdbus --help
```

顯示

```
Usage: qdbus [--system] [--bus busaddress] [--literal] [servicename] [path] [method] [args]

  servicename       the service to connect to (e.g., org.freedesktop.DBus)
  path              the path to the object (e.g., /)
  method            the method to call, with or without the interface
  args              arguments to pass to the call
With 0 arguments, qdbus will list the services available on the bus
With just the servicename, qdbus will list the object paths available on the service
With service name and object path, qdbus will list the methods, signals and properties available on the object

Options:
  --system          connect to the system bus
  --bus busaddress  connect to a custom bus
  --literal         print replies literally
```




## 參考指令

## Wallpaper / set

執行下面指令，將「Lingmo」的「桌面圖片」設定為「/usr/share/backgrounds/lingmoos/grass1.jpg」。

``` sh
qdbus com.lingmo.Settings /Theme com.lingmo.Theme.setWallpaper "/usr/share/backgrounds/lingmoos/grass1.jpg"
```




## Wallpaper / get

執行下面指令，獲得「Lingmo」目前設定的「桌面圖片路徑」。

``` sh
qdbus com.lingmo.Settings /Theme com.lingmo.Theme.wallpaper
```

顯示

```
/usr/share/backgrounds/lingmoos/grass1.jpg
```




## 接下來

接著我們來了解，在「Lingmo」，如何[透過「Variety」設定桌面圖片](https://samwhelp.github.io/note-about-lingmo/read/howto/set-wallpaper-by-variety.html)。




## 相關連結

* [外觀設定介面](https://samwhelp.github.io/note-about-lingmo/read/subject/style/config.html)
