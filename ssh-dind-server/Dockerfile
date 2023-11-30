FROM docker:dind

RUN apk add --no-cache openssh shadow

EXPOSE 22

RUN ssh-keygen -A

RUN useradd -m -G wheel -s /bin/bash lightyagami 

RUN echo "lightyagami:1809009" | chpasswd

RUN service ssh start

CMD ["/usr/sbin/sshd", "-D"]
