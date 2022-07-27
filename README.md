# VPS_OpenWrt
![GitHub Stars](https://img.shields.io/github/stars/esirplayground/VPS_OpenWrt.svg?style=flat&logo=appveyor&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/esirplayground/VPS_OpenWrt.svg?style=flat&logo=appveyor&label=Forks&logo=github)
![GitHub last commit](https://img.shields.io/github/last-commit/esirplayground/VPS_OpenWrt?label=Latest%20Commit&logo=github)

这个 repo 有助于将 OpenWrt 部署到您的 VPS 上。<br>
在此感谢 `ptpt52` 出色的项目: https://github.com/x-wrt<br>
在此感谢 `eSir` 出色的项目: https://github.com/esirplayground/VPS_OpenWrt<br>

**Tutorial**<br>

Youtube Video [in Mandarin]: 📺https://youtu.be/iXhd-h4aVW8

**Prerequisite**
 - **`Ubuntu`** or **`Debian`** (CentOS/Arch Based Not tested)
 - **`wget`** installed<br>
   probably you don't need this, but if you do, you could run command below to install `wget`:<br>
    ```Bash
    apt update && apt install -y wget 
    ```
**Steps**

1.  上传 OpenWrt 固件（WinSCP 或其他工具），将其重命名为 `op.img.gz`

2.  上传 本项目中 `wrt_kernel.bin`或取消 63行`#wget --no-check-certificate https://raw.githubusercontent.com/esirplayground/VPS_OpenWrt/main/$wrt_kernel`的注释

3.  运行下面的命令行:
    ```Bash
    bash -c "$(wget -O- https://raw.githubusercontent.com/aheig/OpenWrt-for-VPS/main/vps_deploy.sh)"
    ```
    如果提示 https 证书有异常，请尝试此操作:

    ```Bash
    wget --no-check-certificate -O- https://raw.githubusercontent.com/aheig/OpenWrt-for-VPS/main/vps_deploy.sh|bash
    ```
**支持平台 :**
- Google Cloud
- Azure
- Vultr
- Virmach
- Racknerd
- Hostdare
- Ali Cloud (Domestic)
- hostEONS
- ...

**`NOT` Support Platform :**
- Oracle
