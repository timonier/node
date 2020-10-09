FROM node:alpine

LABEL \
    maintainer="Morgan AUCHEDE <morgan.auchede@gmail.com>"

ENV \
    CHOKIDAR_USEPOLLING=true

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress bash binutils ca-certificates curl g++ git gpgme make openssh-client python tzdata \
\
    # Install create-react-app
\
    && yarn global add create-react-app \
\
    # Install generate-api-platform-client
\
    && yarn global add @api-platform/client-generator \
\
    # Install glibc
\
    && curl --location --output /etc/apk/keys/sgerrand.rsa.pub "https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub" \
    && curl --location --output /tmp/glibc.apk "https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.32-r0/glibc-2.32-r0.apk" \
    && curl --location --output /tmp/glibc-bin.apk "https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.32-r0/glibc-bin-2.32-r0.apk" \
    && apk add --no-cache --no-progress /tmp/glibc.apk /tmp/glibc-bin.apk \
\
    # Install ng
\
    && yarn global add @angular/cli \
\
    # Install prettier
\
    && yarn global add prettier \
\
    # Install serve
\
    && yarn global add serve \
\
    # Clean
\
    && rm -f -r /tmp/* "$(yarn cache dir)"/*
