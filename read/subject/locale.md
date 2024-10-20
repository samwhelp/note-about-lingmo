---
title: 語系
nav_order: 3010
has_children: true
---


# 語系


## 主題

* [相關議題](#相關議題)
* [設定範例](#設定範例)
* [設定檔](#設定檔)
* [相關文件](#相關文件)
* [說明](#說明)



## 相關議題

| 相關議題 |
| ------- |
| [字型](https://samwhelp.github.io/note-about-lubuntu/read/subject/font.html) |
| [輸入法](https://samwhelp.github.io/note-about-lubuntu/read/subject/input-method.html) |




## 設定範例

| 設定範例 |
| ------- |
| [locale-en_US](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/locale-config/locale/locale-en_US) |
| [locale-zh_TW](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/locale-config/locale/locale-zh_TW) |
| [locale-zh_CN](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/locale-config/locale/locale-zh_CN) |




## 設定檔

> 以「[locale-zh_TW](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/locale-config/locale/locale-zh_TW)」為例

| 設定檔 |
| ----- |
| [/etc/locale.gen](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/locale/locale-zh_TW/asset/overlay/etc/locale.gen#L520-L521) |
| [/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/locale/locale-zh_TW/asset/overlay/etc/locale.conf) |
| [~/.config/lingmoos/language.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/locale/locale-zh_TW/asset/overlay/etc/skel/.config/lingmoos/language.conf) |




## 相關文件

| Debian Wiki |
| ---------- |
| [Locale](https://wiki.debian.org/Locale) |


| Arch Wiki |
| ---------- |
| [Locale](https://wiki.archlinux.org/title/Locale) |
| [System time](https://wiki.archlinux.org/title/System_time) |




## 說明

### 起始環境

我個人習慣使用「英文介面」，

所以安裝時，

> 在「[Locale](https://calamares.io/docs/location/)」的設定，我會選擇「en_US」，
> 在「時區」的設定，我會選擇「`Asia/Taipei`」。

所以當安裝完成後，其中跟「Locale」相關的設定檔如下

| 設定檔 |
| ----- |
| [/etc/locale.gen](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.gen#L517-L520) |
| [/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.conf) |
| [~/.config/lingmoos/language.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/language.conf) |

執行

``` sh
file /etc/localtime
```

顯示

```
/etc/localtime: symbolic link to /usr/share/zoneinfo/Asia/Taipei
```




執行下面指令

``` sh
locale -a
```

顯示 (請對照「[/etc/locale.gen](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.gen#L517-L520)」)

```
C
C.utf8
en_US.utf8
POSIX
```




執行下面指令

``` sh
locale
```

顯示 (請對照「[/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.conf)」)

```
LANG=en_US.UTF-8
LANGUAGE=en_US
LC_CTYPE=en_US.UTF-8
LC_NUMERIC=en_US.UTF-8
LC_TIME=en_US.UTF-8
LC_COLLATE=en_US.UTF-8
LC_MONETARY=en_US.UTF-8
LC_MESSAGES="en_US.UTF-8"
LC_PAPER="en_US.UTF-8"
LC_NAME="en_US.UTF-8"
LC_ADDRESS="en_US.UTF-8"
LC_TELEPHONE="en_US.UTF-8"
LC_MEASUREMENT=en_US.UTF-8
LC_IDENTIFICATION="en_US.UTF-8"
LC_ALL=
```

> 注意「[/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.conf)」，是安裝程式「[calamares](https://github.com/calamares/calamares)」在安裝過程所產生的，它會填寫很多行。但一般實務上只需要第一行「`LANG=en_US.UTF-8`」。
