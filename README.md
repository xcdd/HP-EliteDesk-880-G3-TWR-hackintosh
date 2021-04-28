使用opencore0.6.8构建
![](https://github.com/xcdd/HP-EliteDesk-880-G3-TWR-hackintosh/blob/main/picture/%E6%88%AA%E5%B1%8F2021-04-28%20%E4%B8%8B%E5%8D%888.17.21.png)

**U** 盘安装的同学，请使用 ****USB2.0**** 完成安装，别着急联网，先用 ****OpenCore Configurator**** （或者别的工具也行）刷新三码，不刷新就联网的后果自负 ...

（机型选择imac17，1)

## **本机配置**

请参考惠普官方信息：https://www8.hp.com/h20195/v2/getpdf.aspx/4AA6-9266EEAP.pdf

- CPU：i7-7700
- 内存：8+8=16GB
- 主硬盘：HP SSD EX900 256GB
- 核心显卡：HD630
- 独立显卡：无
- 有线网卡：Intel® I219LM Gigabit Network Connection
- 声卡：官网写的是ALC221，但我这台是CX20632 （Layoutid=23）
- 备注：已加入核显PCI信息，使用非HD630/独显的请自行删除掉

![](https://github.com/xcdd/HP-EliteDesk-880-G3-TWR-hackintosh/blob/main/picture/%E6%88%AA%E5%B1%8F2021-04-28%20%E4%B8%8B%E5%8D%888.15.53.png)

提示：

1. 本机器的主板非常木头（stupid)，表现为在安装macos后，如果把windows启动项放到第一位，很容易在按F9（快速引导）时看不到启动选项，请按F10进去BIOS里面改
> 所以建议把opencore启动项放到第一位，以后开机时按F9即可切换双系统
2. 为修补RTC问题，目前可能无法使用OpenCore启动windows
 
## BIOS 配置
请参考：https://github.com/sakoula/HP-EliteDesk-800-G2-6700#bios-setup
本机无需解锁CFG LOCK，根据指南配置好BIOS选项就行
> 我解锁以后就跟没解一样，可能是bios版本跟这个项目的有所区别

## **目前工作情况**
测试在catalina 10.15.7、big sur 11.3/11.2.3正常运行

CPU变频正常 核心显卡可以硬解

暂未完善休眠
