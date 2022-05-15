```bash
sudo apt update
sudo apt install v4l-utils
sudo apt install fswebcam 


sudo armbian-add-overlay overlay_csi_orangepipc.dts
sudo reboot


v4l2-ctl --list-devices
media-ctl --device /dev/media1 -p
media-ctl -d /dev/media1 --set-v4l2 '"ov5640 0-003c":0[fmt:UYVY8_2X8/1280x720]'
media-ctl --device /dev/media1 -p

fswebcam --device=/dev/video1 -r 1280x720 -p UYVY -S 10 filename.jpg
```

