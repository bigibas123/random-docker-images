FROM debian:trixie-slim

SHELL  ["/usr/bin/bash", "-c"]
HEALTHCHECK NONE

LABEL org.opencontainers.image.title="Debian CMake image"
LABEL org.opencontainers.image.description="A minimal debian Docker image with CMake and some other common tools installed"
LABEL org.opencontainers.image.base.name="debian:trixie-slim"
LABEL org.opencontainers.image.licenses="MIT-0"

LABEL org.opencontainers.image.vendor="bigibas123"
LABEL org.opencontainers.image.authors="bigibas123"
LABEL org.opencontainers.image.url="https://github.com/bigibas123/random-docker-images/"
LABEL org.opencontainers.image.documentation="https://github.com/bigibas123/random-docker-images/"
LABEL org.opencontainers.image.source="https://github.com/bigibas123/random-docker-images/"


ENV DEBIAN_FRONTEND="noninteractive"

RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list && \
    apt-get update && apt-get install --no-install-recommends -y bash curl wget git cmake build-essential ninja-build ca-certificates && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

CMD [ "/usr/bin/bash", "-c", "echo Provide your own executable to run!" ]
