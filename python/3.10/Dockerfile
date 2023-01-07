FROM python:3.10-slim

LABEL author="Michael Parker" maintainer="parker@pterodactyl.io"

RUN apt update \
            && apt-get -y install git gcc g++ ca-certificates dnsutils curl iproute2 ffmpeg procps xvfb \
            && useradd -m -d /home/container container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

COPY ./../entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
