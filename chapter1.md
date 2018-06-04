# Windows 10 + VirtualBox 5.2.12 + Debian 9.4.0

作業系統：Windows 10

處理器：i5-3470 3.20GHz

記憶體：32GB

VirtualBox 版本：5.2.12（[官網下載路徑](https://www.virtualbox.org/wiki/Downloads)）

Debian Linux Image：9.4.0（[torrent](https://cdimage.debian.org/debian-cd/current/amd64/bt-dvd/debian-9.4.0-amd64-DVD-1.iso.torrent "Debian 9.4.0")）

## 解決 VirtualBox 無法顯示 1920 \* 1080 解析度的問題

１、開啟 terminal 並且切換成 root 身份

```
su
```

２、更新 debian 套件

```
apt-get update
apt-get upgrade
```

３、安裝必要的套件

```
apt-get install build-essential module-assistant
```

４、為了建立 kernel modules 而設定系統

```
m-a prepare
```

５、下載 Guest Additions ISO 並且掛載至 VirtualBox

Link：[https://tracker.debian.org/pkg/virtualbox-guest-additions-iso](https://tracker.debian.org/pkg/virtualbox-guest-additions-iso)

６、如果沒有正常掛載則另外執行

```
mount /media/cdrom
```

７、執行下列指令

```
sh /media/cdrom/VBoxLinuxAdditions.run
```

８、重啟系統

```
reboot
```



