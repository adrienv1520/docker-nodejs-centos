# docker-nodejs-16-centos8
This image provides CentOS 8 with Node.js 16.x.x, NPM, [the build tools](https://linuxconfig.org/install-development-tools-on-redhat-8) and Python 3 installed.

# Tags
This image has no specific tag except `latest`.

# Building
```shell
docker build --tag=nodejs-16-centos8 .
```

# Usage
You can use this image as a base for other Docker images, by using `FROM adrienv1520/nodejs-16-centos8` in your Dockerfile.

Otherwise, you can also use this image as stand-alone. For example, if you run:
```shell
docker run --rm --name nodejs16 -it adrienv1520/nodejs-16-centos8 /bin/bash
```

You'll have a bash terminal opened in a container with CentOS 8, Node.js 16.x.x, NPM, build tools and Python 3.

# Additional information
Node.js and NPM have been installed using the procedure described at: [NodeSource Node.js Binary Distributions](https://github.com/nodesource/distributions#rpminstall).
