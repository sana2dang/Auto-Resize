# Auto-Resize
raspberry pi first boot auto resize


- add line "/boot/cmdline.txt" 
| rootwait quiet init=/usr/lib/raspi-config/init_resize.sh

| sudo wget -qO /etc/init.d/resize2fs_once https://github.com/RPi-Distro/pi-gen/raw/dev/stage2/01-sys-tweaks/files/resize2fs_once
| sudo chmod +x /etc/init.d/resize2fs_once
| sudo systemctl enable resize2fs_once

