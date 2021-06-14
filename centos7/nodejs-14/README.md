# docker-nodejs-14-centos7
This image provides CentOS 7 with Node.js 14.x.x, NPM, [the build tools](https://access.redhat.com/documentation/en-us/red_hat_developer_toolset/7/html/user_guide/chap-red_hat_developer_toolset) and Python 3 installed.

# Tags
This image has no specific tag except `latest`.

# Supported architectures
Typical x86 systems and Apple Silicon Macs:

- `amd64`
- `arm64`

[More info](https://github.com/docker-library/official-images#architectures-other-than-amd64).

# Multi architecture build
```shell
# typical x86 systems and Apple Silicon Macs
docker buildx build --platform linux/amd64,linux/arm64 --push -t adrienv1520/nodejs-14-centos7 .
```

Having issues building with buildx on Apple M1:
1. Configure automated builds on Docker Hub and use tag `amd64`, example:
![Docker automated build example](../../docs/docker-automated-build.png "Docker automated build example")
2. Build and push image locally for `arm64` arch on a Apple M1:
```shell
docker build -t adrienv1520/nodejs-14-centos7:arm64 .
docker push adrienv1520/nodejs-14-centos7:arm64
```
3. Create manifest
```shell
docker manifest create adrienv1520/nodejs-14-centos7:latest adrienv1520/nodejs-14-centos7:amd64 adrienv1520/nodejs-14-centos7:arm64
docker manifest push --purge adrienv1520/nodejs-14-centos7:latest
```

# Usage
You can use this image as a base for other Docker images, by using `FROM adrienv1520/nodejs-14-centos7` in your Dockerfile.

Otherwise, you can also use this image as stand-alone. For example, if you run:
```shell
docker run --rm --name nodejs14c7 -it adrienv1520/nodejs-14-centos7 /bin/bash
```

You'll have a bash terminal opened in a container with CentOS 7, Node.js 14.x.x, NPM, build tools and Python 3.

# Additional information
Node.js and NPM have been installed using the procedure described at: [NodeSource Node.js Binary Distributions](https://github.com/nodesource/distributions#rpminstall).
