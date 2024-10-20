---
title: Download ISO
nav_order: 1000
has_children: false
parent: ISO
---


# Download ISO




## Lingmo OS 2.0 Hydrogen

* [https://github.com/orgs/LingmoOS/discussions/20](https://github.com/orgs/LingmoOS/discussions/20)
* [https://github.com/orgs/LingmoOS/discussions/19](https://github.com/orgs/LingmoOS/discussions/19)




## 下載腳本

* [下載腳本](https://github.com/samwhelp/lingmo-adjustment/tree/main/core/iso/boot-iso/boot-iso-by-grub/demo-boot-lingmo-hydrogen-iso)




## 下載點

> [https://www.lingmo.org/en/downloads](https://www.lingmo.org/en/downloads)

> 可以到「SourceForge / Lingmo OS / [Files](https://sourceforge.net/projects/lingmo-os/files/)」找到下載點。

> 例如可以找到「[https://sourceforge.net/projects/lingmo-os/files/release/iso/hydrogen/stable/](https://sourceforge.net/projects/lingmo-os/files/release/iso/hydrogen/stable/)」。




## 下載方式

執行下面的指令，就會下載「[lingmo-os-2.0-hydrogen-release-desktop-amd64.iso](https://sourceforge.net/projects/lingmo-os/files/release/iso/hydrogen/stable/lingmo-os-2.0-hydrogen-release-desktop-amd64.iso/download)」裡面所列的檔案

``` sh
wget -c https://sourceforge.net/projects/lingmo-os/files/release/iso/hydrogen/stable/lingmo-os-2.0-hydrogen-release-desktop-amd64.iso
```

> 關於「-c」指的是續傳




## Boot ISO

> 簡單「[驗證](#驗證)」過「下載完成的ISO檔案」，接下來可以選擇不同的「[Boot ISO](https://samwhelp.github.io/note-about-debian/read/core/iso/boot-iso.html)」方式。




## 驗證


### sha256sum

* [man sha256sum](https://manpages.debian.org/bookworm/coreutils/sha256sum.1.en.html)

執行

``` sh
wget -c https://sourceforge.net/projects/lingmo-os/files/release/iso/hydrogen/stable/sha256sum.txt

sha256sum -c sha256sum.txt
```

會看到類似如下的內容

```
lingmo-os-2.0-hydrogen-release-desktop-amd64.iso: OK
```
