---
title: 設定字型查找順序
nav_order: 3101
has_children: false
parent: 字型設定
grand_parent: 字型
---


# 設定字型查找順序

* [設定腳本](#設定腳本)
* [設定檔路徑](#設定檔路徑)




## 設定腳本

| 設定腳本 |
| --- |
| [font-match-order](https://github.com/samwhelp/lingmo-adjustment/tree/main/prototype/main/font-config/font-match-order#usage) |




## 設定檔路徑

| 設定檔路徑 |
| --- |
| [~/.config/fontconfig/conf.d/99-x-lingmo.conf](https://github.com/samwhelp/lingmo-adjustment/blob/main/prototype/main/font-config/font-match-order/asset/overlay/etc/skel/.config/fontconfig/conf.d/99-x-lingmo.conf) |


> 因為原本會有一個「`99-lingmo.conf`」，所以加了一個命名為「`99-x-lingmo.conf`」，就會排序在後，就會覆蓋前面的設定。
