---
title: 開發技巧 / 如何從「Lingmo 原始碼專案」編譯成「Debian Package」
nav_order: 8010
has_children: false
parent: 技巧
grand_parent: 開發
---


# 開發技巧 / 如何從「Lingmo 原始碼專案」編譯成「Debian Package」




## 主題

* [緣起](#緣起)
* [說明](#說明)
* [Manpage](#manpage)




## 緣起

> 從「LingmoOS / [lingmo-build](https://github.com/LingmoOS/lingmo-build)」這個專案，學到下面三個指令。

> 主要是探索「LingmoOS / lingmo-build / Modules / [BuildUtils.psm1](https://github.com/LingmoOS/lingmo-build/blob/main/Modules/BuildUtils.psm1)」這個檔案。

``` sh

##
## ## Link
##
## * https://github.com/LingmoOS/lingmo-build
## * https://github.com/LingmoOS/lingmo-build/blob/main/Modules/BuildUtils.psm1
## 
##


##
## ## Install-GlobalDepends
##

sudo apt-get --yes install git devscripts equivs




##
## ## Install-RepoDepends
##

sudo mk-build-deps -i -t "apt-get -y" -r


##
## ## Start-CompileDeb
##


dpkg-buildpackage -b -uc -us -tc -j$(nproc)

```




## 說明

> 以下以「LingmoOS / [lingmo-core](https://github.com/LingmoOS/lingmo-core)」這個專案，當作案例說明



## 安裝打包過程所需的「Package」

> 執行下面指令，安裝打包過程所需的「Package」

``` sh
sudo apt-get --yes install git devscripts equivs
```




## 準備工作資料夾

執行下面指令，產生工作資料夾「~/Documents/lingmo/source」

``` sh
mkdir -p ~/Documents/lingmo/source
```

執行下面指令，切換到工作資料夾「~/Documents/lingmo/source」

``` sh
cd ~/Documents/lingmo/source
```




## Clone

執行下面指令，clone「[lingmo-core](https://github.com/LingmoOS/lingmo-core)」這個專案。

``` sh
git clone https://github.com/LingmoOS/lingmo-core.git
```

執行下面指令，切換到「lingmo-core」這個資料夾

``` sh
cd lingmo-core
```




## 安裝編譯專案所需的「Package」

> 執行下面指令，安裝編譯專案所需的「Package」

``` sh
sudo mk-build-deps -i -t "apt-get -y" -r
```




## 編譯打包

> 執行下面指令，編譯打包

``` sh
dpkg-buildpackage -b -uc -us -tc -j$(nproc)
```

打包完成的檔案，會放在上層資料夾

``` sh
ls -1 ../lingmo-core*.*
```

顯示

```
../lingmo-core_2.0.2_amd64.buildinfo
../lingmo-core_2.0.2_amd64.changes
../lingmo-core_2.0.2_amd64.deb
../lingmo-core-dbgsym_2.0.2_amd64.deb
```




## Manpage

* [man mk-build-deps](https://manpages.debian.org/stable/devscripts/mk-build-deps.1.en.html)
* [man dpkg-buildpackage](https://manpages.debian.org/stable/dpkg-dev/dpkg-buildpackage.1.en.html)




## 其他「clone」的參考指令

> clone recursive

``` sh
git clone --recursive "https://github.com/LingmoOS/lingmo-core.git" "lingmo-core"
```

> clone tag 2.0.1

``` sh
git clone --recursive -b "2.0.1" "https://github.com/LingmoOS/lingmo-core.git" "lingmo-core"
```
