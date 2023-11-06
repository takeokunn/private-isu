FROM ubuntu:latest

RUN apt update \
    && apt install -y openssh-server

RUN mkdir /var/run/sshd

RUN echo 'root:P@assw0rd' | chpasswd
RUN sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config
