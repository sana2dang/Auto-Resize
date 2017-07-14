# Auto-Resize
raspberry pi first boot auto resize


- add line "/boot/cmdline.txt" 
rootwait quiet init=/usr/lib/raspi-config/init_resize.sh
