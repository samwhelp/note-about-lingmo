---
title: Download ISO
nav_order: 1000
has_children: false
parent: ISO
---


# Download ISO




## Lingmo OS 2.1 Hydrogen

* [Lingmo OS 2.1 Hydrogen Released!](https://github.com/orgs/LingmoOS/discussions/34)




## Lingmo OS 2.0 Hydrogen

* [Lingmo OS 2.0 Hydrogen Released!](https://github.com/orgs/LingmoOS/discussions/19)
* [靈墨 OS 2.0 Hydrogen 發佈啦！](https://github.com/orgs/LingmoOS/discussions/20)





## 下載腳本

* [下載腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/core/iso/boot-iso/boot-iso-by-grub/demo-boot-lingmo-iso)




## 下載點

> [https://releases.lingmo.org.cn/releases/2.1/](https://releases.lingmo.org.cn/releases/2.1/)




## 下載方式

執行下面的指令，就會下載「[lingmo-os-2.1-hydrogen-release-desktop-amd64.iso](https://releases.lingmo.org.cn/d/releases/2.1/amd64/lingmo-os-2.1-hydrogen-release-desktop-amd64.iso)」裡面所列的檔案

``` sh
wget -c 'https://releases.lingmo.org.cn/d/releases/2.1/amd64/lingmo-os-2.1-hydrogen-release-desktop-amd64.iso'
```

> 關於「-c」指的是續傳




## Boot ISO

> 簡單「[驗證](#驗證)」過「下載完成的ISO檔案」，接下來可以選擇不同的方式「[Boot ISO](https://samwhelp.github.io/note-about-debian/read/core/iso/boot-iso.html)」。




## 驗證


### sha256sum

* [man sha256sum](https://manpages.debian.org/stable/coreutils/sha256sum.1.en.html)

執行

``` sh
wget -c 'https://releases.lingmo.org.cn/d/releases/2.1/amd64/sha256.txt'

sha256sum -c sha256.txt
```

會看到類似如下的內容

```
lingmo-os-2.1-hydrogen-release-desktop-amd64.iso: OK
```
