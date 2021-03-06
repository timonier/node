# README

Node.js JavaScript runtime

If you like / use this project, please let me known by adding a ★ on the [GitHub repository](https://github.com/timonier/node).

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://github.com/timonier/node/raw/master/bin/installer" | sudo sh -s -- install
```

__Note 1__: If you do not define `INSTALL_DIRECTORY`, `installer` will use in `/usr/local/bin`.

__Note 2__: `docker-for-mac` users have to configure [native NFS server](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc).

## Usage

### angular-cli

Run the command `angular-cli`:

```sh
# See all angular-cli options

ng --help

# Run angular-cli

ng new my-spa
```

### create-react-app

Run the command `create-react-app`:

```sh
# See all create-react-app options

create-react-app --help

# Run create-react-app

create-react-app admin
```

### generate-api-platform-client

Run the command `generate-api-platform-client`:

```sh
# See all generate-api-platform-client options

generate-api-platform-client --help

# Run generate-api-platform-client

generate-api-platform-client "http://127.0.0.1:8000" my-spa
```

### node

Run the command `node`:

```sh
# See all node options

node --help

# Run node-app

node -e 'console.log("Hello World");'
```

### npm

Run the command `npm`:

```sh
# See all npm options

npm help

# Run npm

npm install react
```

### serve

```sh
# See all serve options

serve --help

# Run serve

serve /home/morgan/Documents
```

### yarn

Run the command `yarn`:

```sh
# See all yarn options

yarn --help

# Run yarn

yarn add api-platform-admin
```

## Links

* [angular/cli](https://github.com/angular/angular-cli)
* [api-platform/client-generator](https://github.com/api-platform/client-generator)
* [facebookincubator/create-react-app](https://github.com/facebookincubator/create-react-app)
* [image "timonier/node"](https://hub.docker.com/r/timonier/node/)
* [mounting nfs shares inside docker container](https://stackoverflow.com/questions/39922161/mounting-nfs-shares-inside-docker-container)
* [nodejs](https://nodejs.org)
* [set up docker for mac with native nfs](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc)
* [timonier/node](https://github.com/timonier/node)
* [yarn](https://yarnpkg.com)
* [zeit/serve](https://github.com/zeit/serve)
