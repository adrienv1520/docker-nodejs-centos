# docker-nodejs-14-centos8-slim
This image provides CentOS 8 with Node.js 14.x.x and NPM installed.

# Tags
This image has no specific tag except `latest`.

# Building
```shell
docker build --tag=nodejs-14-centos8-slim .
```

# Usage
You can use this image as a base for other Docker images, by using `FROM adrienv1520/nodejs-14-centos8-slim` in your Dockerfile.

Otherwise, you can also use this image as stand-alone. For example, if you run:
```shell
docker run --rm --name nodejs14 -it adrienv1520/nodejs-14-centos8-slim /bin/bash
```

You'll have a bash terminal opened in a container with CentOS 8, Node.js 14.x.x and NPM.

# Additional information
Node.js and NPM have been installed using the procedure described at: [NodeSource Node.js Binary Distributions](https://github.com/nodesource/distributions#rpminstall).
