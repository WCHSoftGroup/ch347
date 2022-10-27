# 简介

​	   高速USB转接芯片CH347是一款集成480Mbps高速USB接口、JTAG接口、SPI接口、I2C接口、异步[UART](https://so.csdn.net/so/search?q=UART&spm=1001.2101.3001.7020)串口、GPIO接口等多种硬件接口的转换芯片。

接口示意图：

![image-20221027192242216](README.assets/image-20221027192242216.png)

应用示意图：

![image-20221027192258872](README.assets/image-20221027192258872.png)

## JTAG接口特点

- 工作在 Host/Master主机模式；
- 硬件信号：TMS、TCK、TDI、TDO和TRST；
- 支持自定义协议的快速模式和bit-bang模式，传输速率可达30Mbit/S；
- 提供计算机端驱动程序和USB转JTAG TAP函数库，支持二次开发；

## SPI接口特点

- 工作在 Host/Master主机模式；
- 内置硬件DMA，支持批量数据的快速发送和读取；
- 硬件信号：SCS0、SCS1、SCK、MISO和MOSI；
- 工作模式：SPI模式0/SPI模式1/SPI模式2/SPI模式3；
- 传输位序：MSB/LSB；
- 数据结构：8位/16位传输；
- 提供计算机端驱动程序和USB转SPI函数库，支持二次开发；

## I2C接口特点

- 工作在 Host/Master主机模式；
- 硬件信号：SCL、SDA；
- 支持4种传输速度：低速20KHz、标准100KHz、快速400KHz、高速750KHz；
- 支持I2C时序参数调节；
- 提供计算机端驱动程序和USB转I2C函数库，支持二次开发；

## UART接口特点

- 硬件信号：TXD、RXD、Modem信号；
- 支持串口波特率：1200bps~9Mbps；
- 支持串口数据格式：8个数据位、1/2个停止位、奇/偶/无校验；
- 支持RS485方向自动切换；
- 支持串口自动硬件流控；
- 提供VCP串口驱动方式/HID免驱应用方式；
- 支持标准串口/厂商CH347动态库/HID接口形式访问串口；

# 项目说明

​    本项目将基于CH347的接口特性，逐渐增添对应的接口应用，当前已加入：

​	1、添加CH347-JTAG接口的Openocd可执行环境

​	2、依托于1中openocd编写的FPGA下载工具CH347FPGADownloader，当前可实现XILINX部分FPGA的程序烧写。