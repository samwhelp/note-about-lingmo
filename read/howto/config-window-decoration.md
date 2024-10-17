---
title: 設定「Window Decoration」
nav_order: 7040
has_children: false
parent: 如何
---


# 設定「Window Decoration」

> **目前在「Lingmo OS」無法切換「Window Decoration」。**




## 主題

* [說明](#說明)
* [相關連結](#相關連結)




## 說明

> 因為「Lingmo OS」是透過「`lingmo-session`」啟動，然後「`lingmo-session`」會設定「[~/.config/kwinrc](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/lingmo-config/locale/en_us/Lingmo-Dark/asset/overlay/etc/skel/.config/kwinrc#L72-L77)」，設定片段如下

``` ini
[org.kde.kdecoration2]
BorderSize=Normal
ButtonsOnLeft=
ButtonsOnRight=HIAX
library=org.lingmo.decoration
theme=
```

> 相關的實作，可以參考如下的程式碼片段： lingmo-core / session / [application.cpp](https://github.com/LingmoOS/lingmo-core/blob/main/session/application.cpp#L318-L324)

``` cpp
    settings.beginGroup("org.kde.kdecoration2");
    settings.setValue("BorderSize", "Normal");
    settings.setValue("ButtonsOnLeft", "");
    settings.setValue("ButtonsOnRight", "HIAX");
    settings.setValue("library", "org.lingmo.decoration");
    settings.setValue("theme", "");
    settings.endGroup();
```

> 所以即使當我們手動修改「~/.config/kwinrc」，重新登入，最終還是變回原本的設定，因此目前在「Lingmo OS」無法切換「Window Decoration」。

> 根據上面的設定「`library=org.lingmo.decoration`」，了解到在「Lingmo OS」的「Window Decoration」是固定採用「`org.lingmo.decoration`」

執行

``` sh
dpkg -L lingmo-kwin-plugins | grep kdecoration
```

顯示

```
/usr/lib/x86_64-linux-gnu/qt5/plugins/org.kde.kdecoration2
/usr/lib/x86_64-linux-gnu/qt5/plugins/org.kde.kdecoration2/liblingdecoration.so
```

> 關於「`org.lingmo.decoration`」實作的程式碼，可以在「lingmo-kwin-plugins / plugins / [decoration](https://github.com/LingmoOS/lingmo-kwin-plugins/tree/main/plugins/decoration)」找到。




## 相關連結

| 相關連結 |
| ------- |
| Kubuntu 探索筆記 / [設定「Window Decoration」](https://samwhelp.github.io/note-about-kubuntu/read/howto/config-window-decoration.html) |

> 關於在「kwin」，如何透過修改「~/.config/kwinrc」，來設定「Window Decoration」，可以參考我上面這篇紀錄。
