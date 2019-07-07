FROM ubuntu:bionic

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
       python sudo bash ca-certificates \
       systemd systemd-sysv gpg rsync \
       aptitude locales ifupdown \ 
    && apt-get clean

RUN sed -e '/path-exclude=\/usr\/share\/doc\/*/ s/^#*/#/' -i /etc/dpkg/dpkg.cfg.d/excludes
