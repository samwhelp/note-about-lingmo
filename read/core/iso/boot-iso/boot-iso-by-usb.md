---
title: Boot ISO By USB
nav_order: 1020
has_children: false
parent: Boot ISO
grand_parent: ISO
---


# Boot ISO By USB




## Arch Wiki

* [USB flash installation medium](https://wiki.archlinux.org/title/USB_flash_installation_medium)




## 操作步驟


### 下載 ISO

先參考「[Download ISO](https://samwhelp.github.io/note-about-lingmo/read/core/iso/download-iso.html)」這篇提到的下載方式，下載「Lingmo OS 官方提供最新的ISO檔案」。

舉例執行下面指令

``` sh
wget -c https://sourceforge.net/projects/lingmo-os/files/release/iso/hydrogen/stable/lingmo-os-2.0-hydrogen-release-desktop-amd64.iso
```

就會下載一個檔案「lingmo-os-2.0-hydrogen-release-desktop-amd64.iso」。




### 尋找 Device 代號

先執行下面指令，找到「目標USB隨身碟」的「Device代號」

``` sh
lsblk
```

> 假設找到的「目標USB隨身碟」是「/dev/sdc」。




### 寫入隨身碟

接著執行下面指令，就會寫入「USB隨身碟」。

``` sh
sudo dd if=./lingmo-os-2.0-hydrogen-release-desktop-amd64.iso of=/dev/sdc bs=4M status=progress && sync
```

或是執行下面指令，就會寫入「USB隨身碟」。

``` sh
sudo dd if=./lingmo-os-2.0-hydrogen-release-desktop-amd64.iso of=/dev/sdc bs=4M status=progress conv=fsync oflag=direct
```

接著重新開機，在「BIOS」選擇使用「該USB隨身碟」開機。




## Link

* Lingmo Wiki / [Installation Guide](https://wiki.lingmo.org/wiki/installation-guide)
