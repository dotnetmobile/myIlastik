# myilastik
Dockerized version of iLastik, tool for image segmentation

  by dotnetmobile@gmail.com
---

This Docker image facilate the usage of [ilastik](https://www.ilastik.org), the interactive image annotation tool.

Prerequisits for MacOS: install [XQuartz](https://www.xquartz.org)

Instruction to build and run the image: <br>
```
open -a XQuartz
IP=$(ifconfig en0 | grep inet | awk '$1=="inet" {print $2}')
echo $IP
sudo xhost + $IP

# ilastik /home used for reading and writing outcomes is mounted with the host path /path_to_your_folder

sudo docker run --rm -e DISPLAY=$IP:0 -v /tmp/.X11-unix:/tmp/.X11-unix \
--mount type=bind,source=/path_to_your_folder,target=/home/ \
myilastik

```
