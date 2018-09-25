# opencv-pi3-memo

In this memo, we describe the build of
Python3 + OpenCV using Berryconda (by jjhelmus).

1. Install Raspbian Stretch Lite to Raspberry Pi 3.

2. Update & Upgrade

(sudo su)
apt update
apt upgrade
reboot

3. Install Berryconda
(https://github.com/jjhelmus/berryconda)
wget https://github.com/jjhelmus/berryconda/releases/download/v2.0.0/Berryconda3-2.0.0-Linux-armv7l.sh
chmod 755 Berryconda3-2.0.0-Linux-armv7l.sh
./Berryconda3-2.0.0-Linux-armv7l.sh

4. Install OpenCV using conda

conda install opencv

5. Test
Run following code

import cv2
cam = cv2.VideoCapture(0)
retcod, frame = cam.read()
cv2.imwrite('sample.jpg', frame)
cam.release()
