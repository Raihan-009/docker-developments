FROM docker:dind

RUN apk add --no-cache openssh shadow

EXPOSE 22

RUN ssh-keygen -A

RUN echo "root:1809009" | chpasswd
RUN useradd -m -G wheel -s /bin/bash ryuzaki \
    && echo "ryuzaki:1809009" | chpasswd

RUN echo "ryuzaki ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ryuzaki

CMD ["/usr/sbin/sshd", "-D"]
