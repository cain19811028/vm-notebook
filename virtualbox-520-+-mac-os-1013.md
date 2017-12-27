# Windows 10 + VirtualBox 5.2.0 + Mac OS High Sierra 10.13

作業系統：Windows 10

處理器：i5-3470 3.20GHz

記憶體：32GB

VirtualBox 版本：5.2.0（[官網下載路徑](https://www.virtualbox.org/wiki/Downloads)）

Mac OS version：Mac OS High Sierra 10.13

## 安裝步驟

1. 載入下載好的 macOS High Sierra Final.vmdk
2. 設定 Base Memory =&gt; 4096、Processor =&gt; 2、Video Memory =&gt; 128
3. 用管理員身份開啟「命令提示字元（CMD）」
4. 輸入下列指令：
   * cd "c:\Program Files\Oracle\VirtualBox"
   * VBoxManage.exe modifyvm "MAC OS X" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff
   * VBoxManage setextradata "MAC OS X" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac11,3"
   * VBoxManage setextradata "MAC OS X" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"
   * VBoxManage setextradata "MAC OS X" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"
   * VBoxManage setextradata "MAC OS X" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal\(c\)AppleComputerInc"
   * VBoxManage setextradata "MAC OS X" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1
5. 啟動 VM



