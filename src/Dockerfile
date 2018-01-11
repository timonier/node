FROM node:alpine

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

RUN set -ex \
\
    # Install packages
\
    && apk add --no-cache --no-progress \
           ca-certificates \
           curl \
\
    # Install api-platform/client-generator \
\
    && yarn global add \
           @api-platform/client-generator \
\
    # Install facebookincubator/create-react-app
\
    && yarn global add \
           create-react-app \
\
    # Install sgerrand/alpine-pkg-glibc
\
    && export $(curl --location "https://github.com/timonier/version-lister/raw/generated/sgerrand/alpine-pkg-glibc/latest" | xargs) \
    && curl --location --output /etc/apk/keys/sgerrand.rsa.pub "https://github.com/sgerrand/alpine-pkg-glibc/raw/master/sgerrand.rsa.pub" \
    && curl --location --output /tmp/glibc.apk "https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${GLIBC_VERSION}/glibc-${GLIBC_VERSION}.apk" \
    && apk add /tmp/glibc.apk \
\
    # Install timonier/dumb-entrypoint
\
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
\
    # Clean
\
    && rm -f -r \
           /tmp/*

ENTRYPOINT [ "dumb-entrypoint" ]
