FROM ubuntu:20.04
RUN apt update && apt -y upgrade
RUN apt install -y openssh-server
EXPOSE 22

COPY ./sshd_config /etc/ssh/sshd_config

COPY ./docker_entrypoint.sh /tmp/docker_entrypoint.sh
RUN chmod +x /tmp/docker_entrypoint.sh

RUN useradd -ms /bin/bash user

ENTRYPOINT ["/tmp/docker_entrypoint.sh"]

