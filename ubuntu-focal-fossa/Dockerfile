FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
       python3 sudo bash ca-certificates \
       systemd systemd-sysv gpg rsync \
       aptitude locales udev iproute2 \ 
    && apt-get clean
RUN ln -s /usr/bin/python3 /usr/bin/python
RUN sed -e '/path-exclude=\/usr\/share\/doc\/*/ s/^#*/#/' -i /etc/dpkg/dpkg.cfg.d/excludes
