FROM        --platform=$TARGETOS/$TARGETARCH node:16-bullseye-slim

LABEL       author="answ3r" maintainer="peterhub31@gmail.com"

LABEL       org.opencontainers.image.source="https://github.com/answ3r-xyz/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apt-get -y update
RUN         apt-get -y install curl jo ca-certificates openssl ffmpeg git tar python3 build-essential iproute2 sqlite3
RUN			useradd -d /home/container -m container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]
