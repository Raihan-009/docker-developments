FROM docker:dind

RUN apk add --no-cache openssh shadow

EXPOSE 22

RUN ssh-keygen -A

RUN echo "root:1809009" | chpasswd

RUN useradd -m -G wheel -s /bin/bash lightyagami \
    && echo "lightyagami:1809009" | chpasswd

CMD ["/usr/sbin/sshd", "-D"]
