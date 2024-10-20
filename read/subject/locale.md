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


| Fedora Docs |
| ---------- |
| [System Locale and Keyboard Configuration](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/basic-system-configuration/System_Locale_and_Keyboard_Configuration/) |




## 說明


## 說明 / 起始環境語系

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

> 注意「[/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.conf)」，是安裝程式「[calamares](https://github.com/calamares/calamares)」在安裝過程所產生的，它會填寫很多行。但一般實務上只需要第一行「`LANG=en_US.UTF-8`」就可以了。




## 說明 / 切換語系

以下說明，以切換成「[zh_TW](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/locale-config/locale/locale-zh_TW)」為例。




## 說明 / 切換語系 / 修改「/etc/locale.gen」

> 原本的「[/etc/locale.gen](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.gen#L517-L520)」其中有一段類似如下


```
###
#
# Locales enabled by Calamares
en_US.UTF-8 UTF-8
```

> 我們可以多加入一行「`zh_TW.UTF-8 UTF-8`」

> 修改後的「[/etc/locale.gen](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/locale/locale-zh_TW/asset/overlay/etc/locale.gen#L520-L521)」其中有一段如下

```
###
#
# Locales enabled by Calamares
en_US.UTF-8 UTF-8
zh_TW.UTF-8 UTF-8
```

> 修改「`/etc/locale.gen`」後，要執行下面指令

``` sh
sudo locale-gen
```

顯示

```
Generating locales (this might take a while)...
  en_US.UTF-8... done
  zh_TW.UTF-8... done
Generation complete.
```

執行下面指令，確認

``` sh
locale -a
```

顯示

```
C
C.utf8
en_US.utf8
POSIX
zh_TW.utf8
```



## 說明 / 切換語系 / 修改「/etc/locale.conf」

執行

``` sh
file /etc/default/locale
```

顯示

```
/etc/default/locale: symbolic link to ../locale.conf
```

所以我們只要修改「`/etc/locale.conf`」就可以了。


> 原本的「[/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.conf)」內容如下


```
LANG=en_US.UTF-8
LC_ADDRESS=en_US.UTF-8
LC_IDENTIFICATION=en_US.UTF-8
LC_MEASUREMENT=en_US.UTF-8
LC_MONETARY=en_US.UTF-8
LC_NAME=en_US.UTF-8
LC_NUMERIC=en_US.UTF-8
LC_PAPER=en_US.UTF-8
LC_TELEPHONE=en_US.UTF-8
LC_TIME=en_US.UTF-8
```

> 注意「[/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/locale.conf)」，是安裝程式「[calamares](https://github.com/calamares/calamares)」在安裝過程所產生的，它會填寫很多行。但一般實務上只需要第一行「`LANG=en_US.UTF-8`」就可以了。

> 修改後的「[/etc/locale.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/locale/locale-zh_TW/asset/overlay/etc/locale.conf)」內容如下

```
LANG=zh_TW.UTF-8
```

> 修改「`/etc/locale.conf`」後，重新開機後，再執行下面指令確認

``` sh
locale
```

顯示

```
LANG=zh_TW.UTF-8
LANGUAGE=zh_TW
LC_CTYPE=zh_TW.UTF-8
LC_NUMERIC=zh_TW.UTF-8
LC_TIME=zh_TW.UTF-8
LC_COLLATE=zh_TW.UTF-8
LC_MONETARY=zh_TW.UTF-8
LC_MESSAGES="zh_TW.UTF-8"
LC_PAPER="zh_TW.UTF-8"
LC_NAME="zh_TW.UTF-8"
LC_ADDRESS="zh_TW.UTF-8"
LC_TELEPHONE="zh_TW.UTF-8"
LC_MEASUREMENT=zh_TW.UTF-8
LC_IDENTIFICATION="zh_TW.UTF-8"
LC_ALL=
```

> 上面兩個步驟，應該在大部分的Linux發行版通用。

> 在「Lingmo」這個「桌面環境」，則是還有一個設定檔「`~/.config/lingmoos/language.conf`」需要設定。




## 說明 / 切換語系 / 修改「~/.config/lingmoos/language.conf」


> 原本的「[~/.config/lingmoos/language.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/sample/en_US/language.conf)」內容如下

``` ini
[General]
language=en_US
```


> 修改後的「[~/.config/lingmoos/language.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/locale-config/locale/locale-zh_TW/asset/overlay/etc/skel/.config/lingmoos/language.conf)」內容如下

```
[General]
language=zh_TW
```

> 修改「`~/.config/lingmoos/language.conf`」後，登出系統，再登入，就可以看到「圖形程式介面」會出現「繁體中文」。


## 圖形介面程式

在「Lingmo」也有提供「`lingmo-settings -m language`」這個「圖形介面程式」來操作切換「語系」。
