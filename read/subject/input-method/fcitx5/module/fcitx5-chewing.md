---
title: 如何安裝「新酷音輸入法」
nav_order: 3101
has_children: false
parent: fcitx5
grand_parent: 輸入法
---


# 如何安裝「新酷音輸入法」

> 如何安裝「[fcitx5-chewing](https://packages.debian.org/stable/fcitx5-chewing)」




## 微調腳本

| 微調腳本 | 中文輸入法 |
| -------- | ---------- |
| [fcitx5-chewing 安裝設定腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/im-config/fcitx5/fcitx5-chewing) | 新酷音輸入法 |


## 指令安裝

執行下面指令，安裝「im-config」。

``` sh
sudo apt-get install im-config
```

執行下面指令，安裝「fcitx5」和「fcitx5-chewing」。

``` sh
sudo apt-get install fcitx5 fcitx5-chewing
```

執行下面指令，確保安裝支援「GTK」和「QT」環境所需要的「Package」。

``` sh
sudo apt-get install fcitx5-frontend-gtk2 fcitx5-frontend-gtk3 fcitx5-frontend-gtk4 fcitx5-frontend-qt5 fcitx5-frontend-qt6
```

執行下面指令，安裝「圖形設定介面」的「輔助工具」。

``` sh
sudo apt-get install fcitx5-config-qt
```

> 可以參考我的「[package-list.txt](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/im-config/fcitx5/fcitx5-chewing/package-list.txt)」

| Package |
| ------- |
| [im-config](https://packages.debian.org/stable/im-config) |
| [fcitx5](https://packages.debian.org/stable/fcitx5) |
| [fcitx5-chewing](https://packages.debian.org/stable/fcitx5-chewing) |
| [fcitx5-config-qt](https://packages.debian.org/stable/fcitx5-config-qt) |
| [fcitx5-frontend-gtk2](https://packages.debian.org/stable/fcitx5-frontend-gtk2) |
| [fcitx5-frontend-gtk3](https://packages.debian.org/stable/fcitx5-frontend-gtk3) |
| [fcitx5-frontend-gtk4](https://packages.debian.org/stable/fcitx5-frontend-gtk4) |
| [fcitx5-frontend-qt5](https://packages.debian.org/stable/fcitx5-frontend-qt5) |
| [fcitx5-frontend-qt6](https://packages.debian.org/stable/fcitx5-frontend-qt6) |

上面的安裝指令，可以合併在一起如下

``` sh
sudo apt-get install \
	im-config \
	fcitx5 \
	fcitx5-chewing \
	fcitx5-frontend-gtk2 \
	fcitx5-frontend-gtk3 \
	fcitx5-frontend-gtk4 \
	fcitx5-frontend-qt5 \
	fcitx5-frontend-qt6 \
	fcitx5-config-qt

```




## 切換輸入法架構

執行下面指令，將「輸入法架構」切換到「fcitx5」

``` sh
im-config -n fcitx5
```

> 重新登出，然後登入，就會生效


## 加入輸入法

透過「圖形操作介面程式(`fcitx5-configtool`)」，

加入「新酷音輸入法(`fcitx5-chewing`)」這個「輸入法」。




## 備註

### ~/.xinputrc

上面的步驟「`im-config -n fcitx5`」，會儲存在「~/.xinputrc」，這個檔案。

執行下面指令，觀看「~/.xinputrc」這個檔案的內容

``` sh
cat ~/.xinputrc
```

顯示

```
# im-config(8) generated on Tue, 24 May 2022 13:19:25 +0800
run_im fcitx5
# im-config signature: 1584e859fcc6846c2f86d354c758ca0e  -
```

主要是「`run_im fcitx5`」這一行。
