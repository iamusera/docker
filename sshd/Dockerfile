FROM registry.cn-hangzhou.aliyuncs.com/image-anykey/python:3.8.10

ENV PROJECT_NAME=cjPython env=dev

RUN apt update && \
    apt-get install -y openssh-server vim wget && \
    mkdir /var/run/sshd  && \
    echo 'root:1' |chpasswd

CMD ["/usr/sbin/sshd", "-D"]