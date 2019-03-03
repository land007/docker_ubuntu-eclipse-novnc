# docker_ubuntu-eclipse-novnc

The porter uses Ubuntu's original desktop, installs ecliipse+ chrome, and supports Chinese


```bash
sudo docker run -itd -p 6080:6080 -e PASSWORD=1 -e SUDO=yes –name zc004 land007/ubuntu-eclipse-novnc:latest
```

http://localhost:6080/vnc.html

After booting, you can remotely display the following address. The password is 1. This 1 is the VNC connection 1 and the root password.


```bash
#Start
sudo docker pull land007/ubuntu-eclipse-novnc ; sudo docker stop ubuntu-eclipse-novnc ; sudo docker rm ubuntu-eclipse-novnc ; docker run -it -p 5901:5901 -p 6080:6080 -p 4040:4040 --privileged --name ubuntu-eclipse-novnc land007/ubuntu-eclipse-novnc:latest
#Persistent eclipse
sudo docker pull land007/ubuntu-eclipse-novnc ; sudo docker stop ubuntu-eclipse-novnc ; sudo docker rm ubuntu-eclipse-novnc ; docker run -it -v ~/docker/eclipse-workspace:/eclipse-workspace -v ~/docker/eclipse:/usr/local/eclipse -p 5901:5901 -p 6080:6080 -p 4040:4040 --privileged --name ubuntu-eclipse-novnc land007/ubuntu-eclipse-novnc:latest
#Persistent eclipse
sudo docker pull land007/ubuntu-eclipse-novnc ; sudo docker stop ubuntu-eclipse-novnc ; sudo docker rm ubuntu-eclipse-novnc ; docker run -it -v ~/docker/chrome_default:/home/ubuntu/.config/google-chrome/Default -v ~/docker/eclipse-workspace:/eclipse-workspace -v ~/docker/eclipse:/usr/local/eclipse -p 5901:5901 -p 6080:6080 -p 4040:4040 -p 2020:20022 --privileged --name ubuntu-eclipse-novnc land007/ubuntu-eclipse-novnc:latest
#View password
sudo docker exec $CONTAINER_ID cat /home/ubuntu/password.txt
```

![image](https://github.com/land007/docker_ubuntu-eclipse-novnc/raw/master/WechatIMG543.jpeg)

