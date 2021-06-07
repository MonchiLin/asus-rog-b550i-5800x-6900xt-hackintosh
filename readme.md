# Ryzen Hackintosh

## 我的配置如下

主板：Asus-Rog-B550I-Gaming

CPU：AMD Ryzen 5800X

显卡：AMD Radeon RX 6900XT

内存：芝奇幻光戟 8G*2 

机箱：爱国者 S1

电源：长城 TF850

散热：九州风神堡垒 240ex

**注意：该配置并非购买推荐，它仅仅是我利用现有的现有硬件组装的**

------

这份 EFI 遵守 https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html 构建，并且进行了一些修改，见 `tips.md`，我在构建时也尝试根据中文世界的一些教程构建（主要原因是已经过时），但是无一例外都失败了，
最后还是硬着头皮啃完了 OpenCore 的官方 AMD 构建教程，最终结果也没有让我失望，成功安装和启动。

我不建议你直接使用我的 EFI，而是自己通过 opencore 官方教程构建，如果你与我配置差不多，我建议你去看 `tips.md` 文件，里面列出了我遇到的一些问题。

## 可用

* WIFI 和 Bluetooth 可用

## 已知问题

[] 开机缓慢，在选择系统启动后黑屏很长时间才进入系统

[] 没有开机声音

[] 无法使用网线

## 更新记录

### 2021/06/07
更新 opencore 到 0.7 release 版本 

经过了一天的测试，基本上可以断定，启动慢的原因是因为之前使用了调试版本的 opencore ，不过在选择系统启动后仍然黑屏很长时间才进入系统

### 2021/06/06
增加 RestrictEvents，可以在系统信息中正确的显示 CPU


### 2021/06/06
完成了安装和启动，目前 opencore 还是调试版本


