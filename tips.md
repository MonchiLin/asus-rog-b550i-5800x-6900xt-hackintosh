## 遇到的问题和解决方案

### 卡在：eb|#log:exitbs:start

这是卡了我最长时间的问题，我重复了多次开试错，最后终于发现，需要禁用 BIOS 中的 **Above 4G decoding**，
一开始我遵循该教程配置 BIOS，https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html#amd-bios-settings，但是始终卡在了 *eb|#log:exitbs:start*，
最后我尝试禁止 **Above 4G decoding**，并且在引导参数中添加了 `npci=0x2000`，终于成功进行了引导。
 
### 卡在 rtc only single ram bank (128 bytes)

解决了 *eb|#log:exitbs:start* 之后，我就遇到了这个问题，但是实际上这个问题我并没有做什么，我将所有非必需的 `.kext` 和 `.efi` 文件全部删除掉，他就好了

### load root_image 之后黑屏

当时差不多是晚上 1 点了，前面遇到的问题几乎消耗了我所有的耐心，并且这个问题对我来说是在过于无解，在我准备放弃时，突然灵光一闪，会不会是 6900xt 不能被识别，于是我搜索到了 `agdpmod=pikera`，并且将它
加到了启动参数，然后奇迹发生了，终于亮起了 Apple 图标，并且成功进行了安装和启动。

### 网卡

在安装黑苹果之前，我已经做了一些预习找到了这个 `https://github.com/OpenIntelWireless/itlwm`，我以为只要加上了就可以直接使用 Wifi，但是实际上并不对，除了这个 `Kext` 之外
还需要只用配套的软件 `https://github.com/OpenIntelWireless/HeliPort`

## 安装黑苹果的一些经验

我推荐在调试 EFI 时使用 `DiskGenius`，一开始我使用黑果小兵的镜像写入了 U 盘，但是在 windows 下我想修改 EFI 文件，却提示我一些安全问题，最后我将 EFI 盘格式化并且调整盘符后，终于可以自由修改文件了，但是
此时又产生了一个新的问题，我的 EFI 分区无法被引导，后来我发现 `DiskGenius` 提供了 UEFI 引导管理的功能，并且在里面发现，opencore.efi 并没有正确被识别，经过手动设置后才被正常识别。

除此之外`DiskGenius` 的 UEFI 引导管理的功能还可以指定电脑重启后从那个启动项引导。

