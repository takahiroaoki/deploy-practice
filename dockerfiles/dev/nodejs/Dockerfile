FROM amazonlinux:2.0.20230504.1

WORKDIR /app

# install basic tools
RUN yum -y update && yum install -y \
    systemd \
    shadow-utils \
    tar \
    unzip \
    sudo

# install node.js
RUN curl -fsSL https://rpm.nodesource.com/setup_16.x | bash -
RUN yum install -y nodejs-16.20.0

# add user
## shadow-utils contains "useradd"
ARG USER_NAME=dev-user
RUN useradd -m $USER_NAME && echo "${USER_NAME} ALL=NOPASSWD: ALL" >> /etc/sudoers
USER $USER_NAME