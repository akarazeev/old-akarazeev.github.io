---
title: Preventing a volume from mounting at boot (macOS Catalina)
lang: ru
ref: preventmount250120
date: 2020-01-24 03:00:01 +03:00
tags:
- Catalina
- Mount
- Volume
- SSD
layout: post
header:
  teaser: ""
---

Here are the steps to prevent a volume from mounting at boot on macOS Catalina:

1. Launch "Disk Utility" application and open the info for volume of interest: <img src="/images/prevent-mount/checkuuid.jpg" width="70%">
2. Copy the UUID: <img src="/images/prevent-mount/uuid.jpg" width="70%">
3. In terminal type ```sudo vim /etc/fstab```: <img src="/images/prevent-mount/sudovimetcfstab.jpg" width="70%">
4. Paste the copied UUID and type additional arguments (more [info](https://wiki.archlinux.org/index.php/fstab)): <img src="/images/prevent-mount/sudovimetcfstabuuid.jpg" width="70%">
