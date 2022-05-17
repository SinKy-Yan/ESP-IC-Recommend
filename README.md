# ESP32 IC Recommend

因为ESP32是一个很好玩又很万金油的芯片，可以用在各种项目上，但是可能对其它配套芯片的选型不是很了解，所以在这里推荐一些方案和芯片

规则介绍：

1. 芯片名后有✨的都是比较推荐的

2. 每个芯片介绍里的电气参数不一定准确

---

[TOC]

## 充放电一体IC

### - [AXP209](https://item.szlcsc.com/81672.html)

挺猛的电源管理芯片，但是对应的配置项很多，甚至不能直接拿来用，需要先配置好寄存器再上板子

特便宜，我记得还有个AXP192也差不多，但是我都没搞成功过

QFN-48_6x6x04P

### - [IP5306](https://item.szlcsc.com/193089.html)✨

简单的充放电一体芯片，外围电路也简单，立创开源上有案例，M5Stack的Core1就用的这个芯片

ESOP-8

## LDO

### - [AMS1117-3.3](https://item.szlcsc.com/327652.html)

经典的线性稳压器，但是体积太大

**很多厂都有做，下面的电气参数不一定对**

I~OUT~=100mA时压降1V（文档是这么说的，离谱）

最大输入电压**18V**，最大输出电流**1A**

SOT-223

### - [ME6211C33M5G](https://item.szlcsc.com/84106.html)✨

从合宙的ESP32-C3板子上发现的，**带有一个EN脚**

I~OUT~=100mA时压降120mV

最大输入电压**6V**，最大输出电流**500mA**

SOT-23-5

### - [LP2985-33DBVR](https://item.szlcsc.com/96618.html)✨

好像是稚晖的一个板子上用过的

I~OUT~=150mA时压降120mV

最大输入电压**16V**，最大输出电流**150mA**

SOT-23-5

### - [XC6206P332MR](https://item.szlcsc.com/2973330.html)

立创开源平台看见的一个项目用的

I~OUT~=100mA时压降200mV

最大输入电压**16V**，最大输出电流**150mA**

SOT-23-3L

## USB2TTL

### - [CP2102-GMR](https://item.szlcsc.com/7033.html)

大了点，功能太多几乎用不到

波特率最高1Mbps

QFN-28_5x5x05P

### - [CP2104-F03-GMR](https://item.szlcsc.com/48747.html)✨

比CP2104小点，功能还是很多用不到的

波特率最高2Mbps

QFN-24_4x4x05P

### - [CH340E](https://item.szlcsc.com/100866.html)✨

相对好焊

波特率最高2Mbps

MSOP-10

### - [CH340G](https://item.szlcsc.com/14927.html)

有点大，但是是这些里面最好焊的，而且便宜

波特率最高2Mbps

SOP-16

### - [CH343P](https://item.szlcsc.com/3039795.html)✨

这些里面最小的，速率支持最快的，价格没有CP那俩贵

波特率最高6Mbps

QFN-16

## 三极管

### - [LMBT3904DW1T1G](https://item.szlcsc.com/143077.html)✨

是两个NPN的结合体，不用两个分开的S8050了

SOT-363

### - [S8050](https://item.szlcsc.com/3248265.html)

最常见的用于自动下载电路的三极管

SOT-23

## 传感器

### - BMP280

大气压强传感器，附带个温度传感器，用来校准大气压数据的

有**BMP280**和**BME280**两种传感器，**BME280**多了一个湿度传感

### - BH1750

照度传感器
