# README

Node.js JavaScript runtime

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/node/raw/master/bin/installer" | sudo sh -s -- install
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

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a [merge request](https://docs.gitlab.com/ee/user/project/merge_requests/).

__Note 1__: [GitHub repository](https://github.com/timonier/node) is a mirror. [Merge request](https://docs.gitlab.com/ee/user/project/merge_requests/) has to be submitted to the [GitLab repository](https://gitlab.com/timonier/node).

__Note 2__: Use the script `bin/build-image` to test your modifications locally.

If you like / use this project, please let me known by adding a [★](https://help.github.com/articles/about-stars/) on the [GitHub repository](https://github.com/timonier/node) or on the [GitLab repository](https://gitlab.com/timonier/node).

## Links

* [angular/cli](https://github.com/angular/angular-cli)
* [api-platform/client-generator](https://github.com/api-platform/client-generator)
* [facebookincubator/create-react-app](https://github.com/facebookincubator/create-react-app)
* [image "timonier/node"](https://hub.docker.com/r/timonier/node/)
* [mounting nfs shares inside docker container](https://stackoverflow.com/questions/39922161/mounting-nfs-shares-inside-docker-container)
* [nodejs](https://nodejs.org)
* [set up docker for mac with native nfs](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc)
* [timonier/dumb-entrypoint](https://gitlab.com/timonier/dumb-entrypoint)
* [yarn](https://yarnpkg.com)
* [zeit/serve](https://github.com/zeit/serve)
