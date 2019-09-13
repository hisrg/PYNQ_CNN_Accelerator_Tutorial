中文：
    这个git记录了我使用PYNQ实现CNN lenet5 加速的整个过程，主要包括如何将PYNQ移植到自定义的ZYNQ板子上，如何编写PL端的硬件加速器代码，包括HLS版本和Verilog版本，以及PS端的控制代码，PS端的控制代码主要使用python编写。
    请大家继续关注，我会陆续更新这个git。
    
第一部分：移植PYNQ到Custom ZYNQ Board上
    1.自定义linux启动
       请参考PPT:ZYNQ 自定义硬件启动，该PPT简要介绍了移植过程，可以作为教程使用。
    2.基于petalinux 以太网驱动移植
       请参考PPT：Petalinux 以太网驱动芯片移植
    3.基于自定义ZYNQ 板子DMA驱动移植
       请参考PPT：基于自定义PYNQ板子的DMA移植
      
第二部分：基于PYNQ的HLS CNN 卷积神经网络硬件架构
     详见基于PYNQ的HLS 版本CNN 卷积神经网络硬件架构.pdf
     
剩下步骤可以参考：
https://github.com/mfarhadi/CNNIOT From MIT

常见问题总结：
1、linux 内核启动了，但进入不了pynq系统怎么办？(from zedboard)
注意：官方默认给的BSP包里面配置的启动模式为FLASH或QSPI启动模式，您需要重新配置uboot的启动模式，在peatlinux中进入启动配置选项菜单后，选择从
SD卡启动即可，然后重新编译并生成启动文件，按照教程后面的步骤进行即可。
2、如何将linux image 烧写到SD卡中，
可以参考https://pynq.readthedocs.io/en/latest/getting_started/pynq_image.html中描述的步骤将PYNQ image烧入到SD卡中。

