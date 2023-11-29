FROM ubuntu:latest

RUN apt update && apt install  openssh-server sudo -y

RUN useradd -rm -d /home/ryuzaki -s /bin/bash -g root -G sudo -u 1000 ryuzaki 

RUN  echo 'ryuzaki:1809009' | chpasswd

RUN service ssh start

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]
