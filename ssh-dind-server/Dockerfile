FROM docker:dind

RUN apk --update add openssh

RUN adduser -D -u 1000 ryuzaki && \
    echo 'ryuzaki:1809009' | chpasswd && \
    addgroup ryuzaki wheel

RUN /usr/sbin/sshd-keygen && /usr/sbin/sshd

EXPOSE 22

CMD ["sh", "-c", "/usr/sbin/sshd -D"]
