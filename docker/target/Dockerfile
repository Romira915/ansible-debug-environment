# Amazon EC2
FROM ubuntu:latest

RUN apt update && apt install -y openssh-server
RUN mkdir /var/run/sshd
RUN echo 'root:password' | chpasswd

RUN sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config

ENV NOTVISIBLE "in users profile"
RUN echo "export VISIBLE=now" >> /etc/profile

EXPOSE 22

# sshdを起動
ENTRYPOINT [ "/usr/sbin/sshd", "-D" ]