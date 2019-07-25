# 200-series-hackintosh-mojave

##### 作者：**Genius-lbesT**    黑苹果Genius

本教程制作为**7代hd630**核显台式机CPU通用的安装及完善驱动.

[**下载本教程的附件**](https://github.com/Lubibest/200-series-hackintosh-mojave/archive/master.zip)



## 正文

**AMD / NVDIA / INTEL均可通过EFI-for-install.zip安装到机器上.**

EFI蓝本为黑果小兵daliansky博客 blog.daliansky.net 的镜像with clover 4928（nvdia)/clover 4928(AMD+INTEL)提取.

**NVDIA支持10.13.6/AMD+INTEL支持最新版本mojave10.14.5**

感谢黑果小兵daliansky

#### AMD+INTEL-Mojave 10.14.6          [镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.6-18G84-Release-version-with-Clover-5027-original-image.html)

#### AMD+INTEL-Mojave 10.14.5           [镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.5-18F132-official-version-with-Clover-4928-original-image.html)

#### AMD+INTEL-Mojave 10.14.4           [镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.4-18E226-official-version-with-Clover-4903-original-image.html)

#### Nvdia-High Sierra 10.13.6               [镜像下载](https://blog.daliansky.net/macOS-High-Sierra-10.13.6-17G65-Release-Version-with-Clover-4596-original-mirror.html)

### 一、安装教程

[How-to-install-a-Hackintosh](https://github.com/Lubibest/How-to-install-a-Hackintosh)

### 二、安装

## 20190726 update

上传附件[**200-series-hackintosh-mojave-10.14.6-AMD.zip**](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/200-series-hackintosh-mojave-10.14.6-AMD.zip)，支持7代CPU配备AMD显卡的台式机在线升级10.14.6，请自行测试。

有问题请加群问。

#### 1.AMD显卡

AMD免驱显卡推荐安装mojave10.14.5，[镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.5-18F132-official-version-with-Clover-4928-original-image.html)

使用[**EFI-for-install**](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/EFI-for-install.zip)进行安装系统

安装完成后，用「**clover configurator**」替换硬盘的**ESP分区**的EFI文件为[**EFI-for-after install-AMD.zip**](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/EFI-for-after%20install-AMD.zip)

重启生效

AMD显卡的机器将持续得到clover升级的支持

### 2.intel

Intel HD630 核显推荐安装mojave10.14.5，[镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.5-18F132-official-version-with-Clover-4928-original-image.html)

使用[**EFI-for-install**](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/EFI-for-install.zip)进行安装系统

用「**clover configurator**」替换硬盘的ESP分区的EFI文件为[**EFI-for-after install-intel.zip**](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/EFI-for-after%20install-intel.zip)

PS：intel注入为`0X12345678`,请查阅核显ID列表查找并尝试驱动或通过Hackintool注入补丁，本教程为对核显机器完善驱动。

intel的机器将会持续得到clover升级的支持

#### 3.NVDIA显卡的机器

nvdia显卡推荐安装10.13.6（17G65)，[镜像下载](https://blog.daliansky.net/macOS-High-Sierra-10.13.6-17G65-Release-Version-with-Clover-4596-original-mirror.html)

使用[**EFI-for-install**](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/EFI-for-install.zip)进行安装系统

请在安装完成后使用终端运行下面的命令，并用「**clover configurator**」替换硬盘的ESP分区的EFI文件为[EFI-for-after install-nvdia.zip](https://github.com/Lubibest/200-series-hackintosh-mojave/raw/master/EFI-for-after%20install-nvdia.zip)

`bash <(curl -s https://raw.githubusercontent.com/Benjamin-Dobell/nvidia-update/master/nvidia-update.sh)`

重启生效

由于nvdia显卡无法更新os版本，我将不再为nvdia显卡的机器更新clover

### 三、.本教程中已放入applealc.kext，请根据自己的声卡型号尝试注入声卡ID，声卡ID请查阅下面这篇教程：

[AppleALC支持的Codecs列表及AppleALC的使用](https://blog.daliansky.net/AppleALC-Supported-codecs.html)

常用ALC：

alc 887  注入 5/7

alc 892  注入 1/2

a1220    注入 1/2

s1220a   注入 1/2

注入位置：

「**clover configurator**」

Devices/Audio/inject(手动输入）

![](https://github.com/Lubibest/300-series-hackintosh-mojave/blob/master/appleALC.png)

### 四、注意事项：

安装过程如果遇到任何问题，请查阅黑果小兵的两篇教程,如下：

[macOS Mojave 10.14安装中常见的问题及解决方法](https://blog.daliansky.net/Common-problems-and-solutions-in-macOS-Mojave-10.14-installation.html)

[macOS 10.13安装中常见的问题及解决方法](https://blog.daliansky.net/macOS-10.13-installation-of-common-problems-and-solutions.html)

### 五、.本教程适用的搭载7代CPU（HD630）主板安装黑苹果，主板包括

微星B250,微星Z270（微星H110,微星b150,微星Z170）

技嘉B250,技嘉Z270（技嘉H110,技嘉B150,技嘉Z170）

华硕B250,华硕Z270（华硕H110,华硕B150,华硕Z170）

或

B250,Z270,H110,B150,Z170芯片组的台式机电脑

具体请自行测试。

### 六、AMD显卡的EFI将在后续的os版本升级中得到更新

### 七、其他

#### 适用于HD530的100系主板的请阅读：

[100-series-hackintosh-mojave](https://github.com/Lubibest/100-series-hackintosh-mojave)

#### 适用于uhd630的300系主板的请阅读：

[300-series-hackintosh-mojave](https://github.com/Lubibest/300-series-hackintosh-mojave)

### 八、本教程EFI

由

**垃圾帮主**修改制作

**Genius lbesT**发布

作者：**Genius-lbesT**

qq群：724096369

![](https://github.com/Lubibest/Hackintosh/blob/master/JPG/QQ.png)

 **黑苹果Genius**   [打赏](https://github.com/Lubibest/About-Genius-lbesT)
