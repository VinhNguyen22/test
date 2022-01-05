FROM ubuntu:18.04

#RUN echo "resolvconf resolvconf/linkify-resolvconf boolean false" | debconf-set-selections

RUN apt-get update && apt-get -y install \
  wget \
  dialog \
  #openssh-client \
  software-properties-common \
  #dnsmasq \
  #dnsutils \
  net-tools \
  sudo \
  rsyslog \
  unzip

VOLUME ["/opt/zimbra-install"]

EXPOSE 22 25 465 587 110 143 993 995 80 443 8080 8443 7071

COPY opt /opt/

COPY etc /etc/

CMD ["/bin/bash", "/opt/start.sh", "-d"]
