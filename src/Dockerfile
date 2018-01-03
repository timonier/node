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
    # Install timonier/dumb-entrypoint
\
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
\
    # Clean
\
    && rm -f -r \
           /tmp/* \
           /var/lib/apt/lists/*

ENTRYPOINT [ "dumb-entrypoint" ]
