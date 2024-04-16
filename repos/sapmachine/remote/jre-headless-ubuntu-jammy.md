## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:9ecbfba2cae9cc41185448bb7ba32cb948148338b6c34a87f6ce06447428a523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:b0ec05819ca22770f2ffb28b2b0bbd8b3c10040c257073b5c625dfb8e3929070
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88530150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7d04ea85b4d34af5fe1b030af3855b28cfad7620a9f167d953f7a8050f0937`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 07:39:42 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 07:39:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 16 Apr 2024 07:39:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aeb9052420ea00ad308d3a7ffff701d8355b90e1516439a6fd4acd3d554e64`  
		Last Modified: Tue, 16 Apr 2024 07:49:23 GMT  
		Size: 58.1 MB (58090372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d49e145c8df2ede2dc519cd8011b5e6de083086c76e6cf1fb2ff85c74c7a51cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85483784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de753b286ee406aa361ca499f3c039ac31b2cd6ca7062086962eddeaa5ea20a5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:46:33 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:46:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 16 Apr 2024 03:46:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449d5a6d2fe74d64c949a898921d829e476b3cb9864b07dbb6ee0d57fba6316f`  
		Last Modified: Tue, 16 Apr 2024 03:55:04 GMT  
		Size: 57.1 MB (57083486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c4ed4ac6021c1b1146a5868ebfa7d2b31bde35b37257a71c81ca11e1e9f5294c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94922251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb610f92592112ce48db93a872605e1d1e95affd168a6722fae0f5f4f809fa1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:28:38 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:28:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 16 Apr 2024 04:28:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f5349559cfd0f65c12318a3fc94d97481d27f98ff86ca7708c008402a5805a`  
		Last Modified: Tue, 16 Apr 2024 04:41:26 GMT  
		Size: 59.3 MB (59335001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
