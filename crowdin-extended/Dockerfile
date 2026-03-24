FROM crowdin/cli:latest

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/main" >> /etc/apk/repositories && \
    echo "http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories && \
    echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories && \
    echo "perl-file-rename * edge" >> /etc/apk/pin.conf && \
    apk add --no-cache unzip zip bash perl-file-rename

CMD [ "/usr/bin/bash", "-c", "echo Provide your own executable to run!" ]
