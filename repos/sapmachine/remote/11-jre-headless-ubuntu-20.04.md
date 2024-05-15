## `sapmachine:11-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:800beca634d90f7db50de2aad419934194890aa5fbbbb0f15838cb2df1657117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b64819d9b73b8088fc7112c19907c626bf14ea52e8102ec1feb58a1fc3c19808
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76871572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834c21e3ccd50d2d87a6b9912799f244ccb839e5cc9b6810f31a89b3aa2f4417`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Wed, 15 May 2024 22:34:36 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 15 May 2024 22:34:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 15 May 2024 22:34:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51f212446d572edb057a530f545332274c661a87cd398bfa000ce0028dea3c`  
		Last Modified: Wed, 15 May 2024 22:40:21 GMT  
		Size: 48.3 MB (48287273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a909db83dbad6494fae629aacbbab605d22ac3054f2040eefcdcbf1164dc04be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74819644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fd30537b3dd47cee2aeb33874725b753130426a288178ade5379f07dbb0eb`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Wed, 15 May 2024 22:57:10 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 15 May 2024 22:57:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 15 May 2024 22:57:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a236a1a1692898d46bc7a98a0a1de3397537682386f8ce077a9052d6eba084ee`  
		Last Modified: Wed, 15 May 2024 23:03:06 GMT  
		Size: 47.6 MB (47613499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7e83fef3465e0d01b6ac661b87fa38589c2fb67978896d68f687e1ef0611cfb4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79687961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1942253fa28cd33d7e2bd22d69c5ff21e7215eb7637909a9dc42c0ded25e97`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:02 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:06 GMT
ADD file:de463dcd7b30faec6d782106816b443697c99747238015d4d992786da4888987 in / 
# Sat, 27 Apr 2024 13:33:06 GMT
CMD ["/bin/bash"]
# Wed, 15 May 2024 22:27:53 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 15 May 2024 22:27:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 15 May 2024 22:27:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842f501e2541cf3af2b2c183cb8bc0e8ee178240b7a31e44ca04a5741c69410b`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 33.3 MB (33316011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7e7787e7972da55c69ec7192a7ef6ff09b49cd324b9653f5b7f8c42d6418df`  
		Last Modified: Wed, 15 May 2024 22:33:13 GMT  
		Size: 46.4 MB (46371950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
