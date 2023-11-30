FROM docker:dind

RUN apk --update add openssh-server sudo

RUN adduser -D -u 1000 ryuzaki && \
    echo 'ryuzaki:1809009' | chpasswd && \
    addgroup ryuzaki wheel

RUN /etc/init.d/sshd start

EXPOSE 22

CMD ["sh", "-c", "/usr/sbin/sshd -D"]
