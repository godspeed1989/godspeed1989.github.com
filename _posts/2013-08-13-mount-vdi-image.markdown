---
layout: page
title : Mount VirtualBox vdi file
categories : [mount]
tagline: mount vdi disk image file
---

*   Mount   
   
	echo 'insert ndb model'   
	sudo insmod /lib/modules/`uname -r`/kernel/drivers/block/nbd.ko   
   
	echo 'make the nbd device'   
	sudo qemu-nbd -c /dev/nbd{1-9} $1   
   
	echo 'wait for nbd9 available'   
	sleep 3   
   
	echo 'mount partition 1'   
	sudo mount /dev/nbd9p1 /your/mount/point   
   

*   Unmount   
   
	sync   

	echo 'umount partition 1'   
	sudo umount /your/mount/point   
   
	echo 'remove the nbd device'   
	sudo qemu-nbd -d /dev/nbd{1-9}   
   
	echo 'remove module'   
	sudo rmmod nbd   

