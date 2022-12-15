FROM python:3.8.10-slim

ENV TZ=Asia/Shanghai LD_LIBRARY_PATH=/opt/oracle/instantclient_21_8 LANG=C.UTF-8

ADD https://download.oracle.com/otn_software/linux/instantclient/218000/instantclient-basic-linux.x64-21.8.0.0.0dbru.zip /opt/oracle/

RUN echo 'deb http://mirrors.aliyun.com/debian/ buster main non-free contrib \n\
deb http://mirrors.aliyun.com/debian-security buster/updates main \n\
deb http://mirrors.aliyun.com/debian/ buster-updates main non-free contrib \n\
deb http://mirrors.aliyun.com/debian/ buster-backports main non-free contrib \n\
deb-src http://mirrors.aliyun.com/debian-security buster/updates main \n\
deb-src http://mirrors.aliyun.com/debian/ buster main non-free contrib \n\
deb-src http://mirrors.aliyun.com/debian/ buster-updates main non-free contrib \n\
deb-src http://mirrors.aliyun.com/debian/ buster-backports main non-free contrib' > /etc/apt/sources.list \
    && echo "${TZ}" > /etc/timezone \
    && ln -sf /usr/share/zoneinfo/${TZ} /etc/localtime \
    && apt-get update  && apt-get install -y \
    tzdata \
    gcc \
    gcc+ \
    g++ \
    unzip \
    build-essential \
    python-dev \
    postgresql \
    libaio1 \
    libaio-dev \
    libsasl2-dev \
    libldap2-dev \
    libpq-dev \
    libffi-dev \
    openssl \
    libssl-dev \
    && ls /opt/oracle/*.zip | xargs -n1 unzip -d /opt/oracle/ \
    && apt clean \
    && apt autoremove --purge \
    && rm -rf /tmp/* \
    && rm /opt/oracle/*.zip \
    && rm -rf /var/lib/apt/lists/*

