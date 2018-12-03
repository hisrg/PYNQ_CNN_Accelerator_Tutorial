中文：
    这个git记录了我使用PYNQ实现CNN lenet5 加速的整个过程，主要包括如何将PYNQ移植到自定义的ZYNQ板子上，如何编写PL端的硬件加速器代码，包括HLS版本和Verilog版本，以及PS端的控制代码，PS端的控制代码主要使用python编写。
    请大家继续关注，我会陆续更新这个git。
    
第一部分：移植PYNQ到Custom ZYNQ Board上
    1.自定义linux启动
       请参考PPT:ZYNQ 自定义硬件启动，该PPT简要介绍了移植过程，可以作为教程使用。
    2.基于petalinux 以太网驱动移植
       请参考PPT：Petalinux 以太网驱动芯片移植
