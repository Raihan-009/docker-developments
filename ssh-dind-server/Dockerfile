FROM docker:dind

RUN apk add --no-cache openssh shadow

EXPOSE 22

RUN ssh-keygen -A

RUN adduser -D -g '' lightyagami
RUN echo "lightyagami:1809009" | chpasswd

CMD ["/usr/sbin/sshd", "-D"]
