FROM alpine:3.7
LABEL APP="mongodb"
LABEL APP_VERSION="3.4.10-r0"
LABEL APP_REPOSITORY="https://pkgs.alpinelinux.org/package/edge/community/x86_64/mongodb"

# Installing dependencies
RUN apk add --no-cache mongodb su-exec
RUN mkdir -p /data/db

WORKDIR /scripts

COPY ./scripts/start.sh start.sh

VOLUME [ "/data/db" ]

EXPOSE 27017 28017

ENTRYPOINT [ "./start.sh" ]