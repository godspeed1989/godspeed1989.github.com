---
layout: page
title : Linux安装ISE USB cable driver
categories : [fpga]
tagline: usb cable driver install under linux
---
##Linux下安装ISE下载线驱动
最近在使用zedboard开发，需要在Linux使用ISE编程和下载调试。   
这里纪录一下Linux的下USB cable driver的安装。

*   安装libusb驱动   
	
	git clone git://git.zerfleddert.de/usb-driver
	make
	sudo ./setup_pcusb

    引入环境变量

	export LD_PRELOAD=/usr/local/lib/libusb-driver.so

*   安装Digilent驱动

	cd $ISE_DIR/14.4/ISE_DS/common/bin/lin/digilent
	./install_digilent.sh

*   加入udev规则

    创建文件/etc/udev/rules.d/xilinx.rules

	SUBSYSTEM=="usb", ACTION=="add", ATTRS{idVendor}=="0403", ATTRS{idProduct}=="6014", GROUP="user", MODE="0777"
	SUBSYSTEM=="usb", ACTION=="add", ATTRS{idVendor}=="04b4", ATTRS{idProduct}=="0008", GROUP="user", MODE="0777"

    这一步是zedboard特有的，因为zedboard的JTAG比较特殊，通过lsusb看到：

	ID 0403:6014 Future Technology Devices International, Ltd FT232H Single HS USB-UART/FIFO IC

    通过加入udev规则可以让impact有权限访问设备。

最后，重启udev

	#service udev restart
