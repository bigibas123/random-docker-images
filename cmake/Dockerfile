FROM debian:trixie-slim

SHELL  ["/usr/bin/bash", "-c"]
HEALTHCHECK NONE

ENV DEBIAN_FRONTEND="noninteractive"

RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list && \
    apt-get update && apt-get install --no-install-recommends -y bash curl wget git cmake build-essential ninja-build ca-certificates && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

CMD [ "/usr/bin/bash", "-c", "echo Provide your own executable to run!" ]
