# Auto-Resize
raspberry pi first boot auto resize


add line "/boot/cmdline.txt" 
- rootwait quiet init=/usr/lib/raspi-config/init_resize.sh

/boot/cmdline.txt 에서
rootwait 뒤에 quiet init=/usr/lib/raspi-config/init_resize.sh 을 적어준다.

putty 실행 or ssh 에서 아래 명령어를 차례대로 실행
* sudo wget -qO /etc/init.d/resize2fs_once https://github.com/RPi-Distro/pi-gen/raw/dev/stage2/01-sys-tweaks/files/resize2fs_once
* sudo chmod +x /etc/init.d/resize2fs_once
* sudo systemctl enable resize2fs_once

shutdown 하고 이미지를 만들어라
