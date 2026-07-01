FROM        --platform=$TARGETOS/$TARGETARCH azul/zulu-openjdk:22

LABEL       author="Vlssu" maintainer="vlssu@vlssu.com"
ENV         DEBIAN_FRONTEND noninteractive

LABEL       org.opencontainers.image.source="https://github.com/pterodactyl-china/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN 		apt-get update -y \
            && apt-get install -y lsof curl ca-certificates openssl git tar sqlite3 fontconfig libfreetype6 tzdata iproute2 libstdc++6 locales \
            && useradd -m -d /home/container container \
            && locale-gen zh_CN.UTF-8

ENV         LC_ALL=zh_CN.UTF-8
ENV         LANG=zh_CN.UTF-8
ENV         LANGUAGE=zh_CN.UTF-8

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]
