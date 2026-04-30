ARG GDAL_VERSION=ubuntu-small-latest
FROM ghcr.io/osgeo/gdal:${GDAL_VERSION}

SHELL  ["/usr/bin/bash", "-c"]
HEALTHCHECK NONE

ENV DEBIAN_FRONTEND="noninteractive"

RUN apt-get update && apt-get install --no-install-recommends -y build-essential cmake git && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

CMD [ "/usr/bin/bash", "-c", "echo Provide your own executable to run!" ]
