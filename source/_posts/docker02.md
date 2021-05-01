title: Docker_02 Windows環境安裝&設定
author: Eddie Chang
tags: []
categories:
  - Docker
date: 2021-04-28 18:44:00
---
# Windows10如何安裝Docker

*windows子系統概念及wsl與docker之間的關聯*

<!--more-->

### Windows版本Docker系統模式

System mode

- WSL2 backend
- Hyper-V backend and Windows containers




### WSL1

WSL是Windows子系統(Windows Subsystem for Linux)

WSL1在Docker中使用leagacy Hyper-V backed，因此必須開啟windows hyper-v功能



### WSL1啟用條件

- Windows 10 64-bit(Pro)up
- 4GB RAM
- Windows版本(Build 17134)up
- HyperV and Container Windows feature enable

### WSL1安裝
1.Powershell系統管理員啟用Windows的WSL功能

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart 
``` 

### WSL2

WSL1使用仿真Linux技術

WSL2使用完整的linux內核技術在windows平台上

WSL2 Support Vmware 15.5up / VirtualBox 6up

### WSL2啟用條件

- Windows 10 64-bit 
- 4GB RAM
- Windows版本1903(Build 18362)up
- Enable Windows WSL2 Feature
- Download Linux kernel update package [->Download](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)


### WSL2安裝

[微軟官方文檔](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

1.Powershell系統管理員啟用Windows Virtual Machine Plateform功能

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

2.Powershell系統管理員將WSL預設版本改為2

```
wsl --set-default-version 2
```

3.安裝Linux，開啟微軟商店下載Ubuntu

![](ubuntu.png)

4.指定Linux distro integration Docker

![](docker.png)

### 確認WSL版本

檢查本機上安裝的Linux版本啟用WSL2

```
wsl -l -v
```
    
### 升級現有的Linux distro到WSL2

```
wsl.exe --set-version (distro name) 2
```

### 將未來安裝的Linux distro預設為WSL2

```
wsl.exe --set-default-version 2
```