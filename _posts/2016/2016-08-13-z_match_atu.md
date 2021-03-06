---
layout: post
title: 制作 QRP Z-Match 天调
date: 2016-08-13 11:36:36 +0800
categories:
- 日志
tags:
- 无线电
- DIY
---

Z-Macth天调在国外已经流行很久了，最近看了Charlie Lofgren, W6JJZ 和 Lloxd Butler, VK5BR的关于Z-Match ATU论述，很有意思，计划仿制一个。    

Z-Match ATU的特点如下：    

Advantages of the Z-Match     
● Matches balanced loads without the use of lossy baluns.    
●Being a parallel resonant circuit, the Z-match can provide some band-pass filtering for your receiver and harmonic attenuation for your transmitter.    
●A well-designed Z-match tuner has a high Q and is more efficient (less lossy) than other types of tuners.    
●The fixed inductor simplifies construction (no taps or rollers needed).    
●Using a toroid inductor and some small poly film variable capacitors, the Z-match can be built into a very compact package. This sort of thing usually appeals to QRPers.    

Disadvantage      
●Tuning is usually very narrow and can be a bit touchy sometimes to tune up.    

网上图纸大概分三种，一种是W6JJZ最初的版本，还有两种是C2都接地但是抽头比例不同。我选择了W6JJZ的版本，其他两个版本也试验过，区别不大。 按照下图，目标是QRP，体积越小越好，电容使用收音机的270p双联可调电容，原来大都使用T130-2或者T130-6磁环（W6JJZ建议尽量使-6的磁环），我手里只有T50-6，所以重新计算了匝数。    
![](https://github.com/bh3nvn/bh3nvn.github.io/raw/master/image/2016/2016-08-12-01.jpg)     	

T1初级50匝，在12、25匝处抽头，次级24匝，以初级12匝抽头处为中心（GND）两边各绕12匝。    
![](https://github.com/bh3nvn/bh3nvn.github.io/raw/master/image/2016/2016-08-12-05.jpg)     

SWR检测部分的电阻使用2瓦以上，D2使用肖特基或者锗二极管。这个SWR桥在终端对地短路时候阻抗是25Ω，在终端开路时候阻抗是75Ω，能够比较好的保护发射机。受电阻功率限制，调谐功率不能高于5瓦，时间不能太长，否则电阻发热严重。工作的时候通过开关旁路SWR电路以较小损耗。    

制作完成之后的样子，三围80x60x35mm。左边的电容是LOAD，右边是TUNE。左边的钮子开关用于调谐，打到右边调谐两个电容至指示灯刚好熄灭，此时负载驻波最小，调谐完成后打到左边正常工作。右边的钮子开关打到右边是平衡输出，打到左边是不平衡输出。    ![](https://github.com/bh3nvn/bh3nvn.github.io/raw/master/image/2016/2016-08-12-00.jpg)     		  
如果调谐TUNE电容能有两个谐振点，那么选择电容较小的一个，效率会比较高。    
![](https://github.com/bh3nvn/bh3nvn.github.io/raw/master/image/2016/2016-08-12-02.jpg)     		


接上Ultimate3 0.5瓦发射，天调输出接10米长线，输出如下：    
![](https://github.com/bh3nvn/bh3nvn.github.io/raw/master/image/2016/2016-08-12-03.jpg)     		

经过对比，比端馈的LC匹配天调效率高很多。


