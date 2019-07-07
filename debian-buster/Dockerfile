FROM debian:buster

RUN apt-get update \
    && apt-get upgrade -y \ 
    && apt-get install -y \
       python sudo bash ca-certificates \
       systemd systemd-sysv gpg rsync \
       aptitude locales ifupdown \
    && apt-get clean
