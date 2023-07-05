<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.19`](#sapmachine11019)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.7`](#sapmachine1707)
-	[`sapmachine:20`](#sapmachine20)
-	[`sapmachine:20.0.1`](#sapmachine2001)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:20c94d09edb15eafbdf0ef02a04f6c6a45ec45a42995a7cc29a8a041add46b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:ba49b54f3626693e4c97b32fa626d57c3fe25868a17e0704af1da48ddb0721d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234262250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ae39c9657ddb2af998520fd96cfe7dd7bcc2900f6e708588a34de9496801b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:45:42 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:45:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 04 Jul 2023 18:45:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d6a4c8d18ed295c9b30d1e7dcb1091773f39694542bd5b34d1349d5b49c0e`  
		Last Modified: Tue, 04 Jul 2023 18:47:15 GMT  
		Size: 199.2 MB (199216717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f757652d3928258fe5b9245663303f54a79b63525121c9ba383f2a4aef16f7e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230597181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed68e6da2182086d66ef644f58265d2b3d090c3b14f910430a7acca0264f2db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:16 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 04 Jul 2023 15:09:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca92fb4966f21c1a5e4e8540c3ecf526ad5f43b6badbf16b2799abb03a2f2db`  
		Last Modified: Tue, 04 Jul 2023 15:10:45 GMT  
		Size: 197.6 MB (197640145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5c767448712c70329a763b9f2e9065ab9f505832b782df51b51f403a3f6ca358
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226745663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de730464e414d5128d2651843a05c53f3a0791f740535449e8248206ccb5503`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:27:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:28:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 05 Jul 2023 01:28:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae01662217c8013a73bf0d838ff28d286356c9c875cebeaed6c1f8d1a67b0fe`  
		Last Modified: Wed, 05 Jul 2023 01:32:46 GMT  
		Size: 185.7 MB (185652520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.19`

```console
$ docker pull sapmachine@sha256:20c94d09edb15eafbdf0ef02a04f6c6a45ec45a42995a7cc29a8a041add46b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11.0.19` - linux; amd64

```console
$ docker pull sapmachine@sha256:ba49b54f3626693e4c97b32fa626d57c3fe25868a17e0704af1da48ddb0721d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234262250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ae39c9657ddb2af998520fd96cfe7dd7bcc2900f6e708588a34de9496801b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:45:42 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:45:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 04 Jul 2023 18:45:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d6a4c8d18ed295c9b30d1e7dcb1091773f39694542bd5b34d1349d5b49c0e`  
		Last Modified: Tue, 04 Jul 2023 18:47:15 GMT  
		Size: 199.2 MB (199216717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11.0.19` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f757652d3928258fe5b9245663303f54a79b63525121c9ba383f2a4aef16f7e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230597181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed68e6da2182086d66ef644f58265d2b3d090c3b14f910430a7acca0264f2db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:16 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 04 Jul 2023 15:09:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca92fb4966f21c1a5e4e8540c3ecf526ad5f43b6badbf16b2799abb03a2f2db`  
		Last Modified: Tue, 04 Jul 2023 15:10:45 GMT  
		Size: 197.6 MB (197640145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11.0.19` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5c767448712c70329a763b9f2e9065ab9f505832b782df51b51f403a3f6ca358
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226745663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de730464e414d5128d2651843a05c53f3a0791f740535449e8248206ccb5503`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:27:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:28:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 05 Jul 2023 01:28:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae01662217c8013a73bf0d838ff28d286356c9c875cebeaed6c1f8d1a67b0fe`  
		Last Modified: Wed, 05 Jul 2023 01:32:46 GMT  
		Size: 185.7 MB (185652520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:bdcede44bb906fa2d29c3f7cf61dc4d65aaf5013349b4c60d424827df23ea3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ccc42cd4233ee6006569d4c77aae0f3f125a6550147bfa37608710ce976242e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32ea279f46a5075ece209459e0679b196448923a72291b3e37c1c1ef14539cc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 18:46:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281360c02a410a2442426f6cd9cb72939a639eeb225e9b9e39c71940b8d15e`  
		Last Modified: Tue, 04 Jul 2023 18:47:41 GMT  
		Size: 198.5 MB (198529038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2f0f6a1aee75ef1675bf60136c377432a29a2701ac945e83167b5741dde45c0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230091366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18c74b0ad42d22fd8228e6046da6b34ce83c1618bb5f58c3b102295b66b8537`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:46 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 15:09:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef3fb831ee6d2d3ce1723d07c70f13a5553b1c127538e2a4932ab3489ab7c3`  
		Last Modified: Tue, 04 Jul 2023 15:11:04 GMT  
		Size: 197.1 MB (197134330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0984a0cc2cafd7fb770f9244fb048cd8a58abdfd1c09c3356963b473ea7246ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240578188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d1d922cb8d7e536911bfccb5637262ccaf7e305ea3a19cf4eac0b82edc482`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:29:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Jul 2023 01:30:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e203a18bba3f1a361fb7a304bede6e6369bb96037e9fbe0dff8c790b86a5a88e`  
		Last Modified: Wed, 05 Jul 2023 01:33:21 GMT  
		Size: 199.5 MB (199485045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.7`

```console
$ docker pull sapmachine@sha256:bdcede44bb906fa2d29c3f7cf61dc4d65aaf5013349b4c60d424827df23ea3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17.0.7` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ccc42cd4233ee6006569d4c77aae0f3f125a6550147bfa37608710ce976242e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32ea279f46a5075ece209459e0679b196448923a72291b3e37c1c1ef14539cc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 18:46:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281360c02a410a2442426f6cd9cb72939a639eeb225e9b9e39c71940b8d15e`  
		Last Modified: Tue, 04 Jul 2023 18:47:41 GMT  
		Size: 198.5 MB (198529038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17.0.7` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2f0f6a1aee75ef1675bf60136c377432a29a2701ac945e83167b5741dde45c0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230091366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18c74b0ad42d22fd8228e6046da6b34ce83c1618bb5f58c3b102295b66b8537`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:46 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 15:09:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef3fb831ee6d2d3ce1723d07c70f13a5553b1c127538e2a4932ab3489ab7c3`  
		Last Modified: Tue, 04 Jul 2023 15:11:04 GMT  
		Size: 197.1 MB (197134330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17.0.7` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0984a0cc2cafd7fb770f9244fb048cd8a58abdfd1c09c3356963b473ea7246ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240578188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d1d922cb8d7e536911bfccb5637262ccaf7e305ea3a19cf4eac0b82edc482`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:29:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Jul 2023 01:30:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e203a18bba3f1a361fb7a304bede6e6369bb96037e9fbe0dff8c790b86a5a88e`  
		Last Modified: Wed, 05 Jul 2023 01:33:21 GMT  
		Size: 199.5 MB (199485045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:20`

```console
$ docker pull sapmachine@sha256:ebff0955567dd8fab2306a5ef4609a6fe6d4933d59a8ae5f518300fb1907c3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:20` - linux; amd64

```console
$ docker pull sapmachine@sha256:f793221a79add4750dbe7bc1b0d64d1b2111fae7b32610f467f29373cd4e8da7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243225007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb26825a2cf8b7d85a5680d4589220f67b66b01a0461e66092b430b1378c4e52`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 18:46:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6250cab60d630fb90303abb73f528c037c23c725e57dce7ae39f5a271bf8de`  
		Last Modified: Tue, 04 Jul 2023 18:48:06 GMT  
		Size: 208.2 MB (208179474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:20` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:089d0731d89d4e375fb569e7093c6fcb7201d9d2364015c232d602c9ffb4d723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239407111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d512b6e06b04ac4a9d06e38886610b3aea9ba598f43a672a6ecc7738a7774c76`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:17 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 15:10:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce2a52a21f2e3597ed1d349ac03b32d0606d2a6d9083b5d907a7c197b786d2`  
		Last Modified: Tue, 04 Jul 2023 15:11:25 GMT  
		Size: 206.5 MB (206450075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:20` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:09ad6edf92f53d8c22563cae269000748171bf61ad573f9970463541e986f0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70cce5b1125ae64be0b7cd6eaa0048cf5b27aedd385d544b82d894717efee5d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:31:51 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:31:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Wed, 05 Jul 2023 01:31:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d3252a81af14d53cf2488077b55aed61f79dd96adabf36c770e183bfcc3117`  
		Last Modified: Wed, 05 Jul 2023 01:34:01 GMT  
		Size: 209.4 MB (209367400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:20.0.1`

```console
$ docker pull sapmachine@sha256:ebff0955567dd8fab2306a5ef4609a6fe6d4933d59a8ae5f518300fb1907c3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:20.0.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:f793221a79add4750dbe7bc1b0d64d1b2111fae7b32610f467f29373cd4e8da7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243225007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb26825a2cf8b7d85a5680d4589220f67b66b01a0461e66092b430b1378c4e52`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 18:46:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6250cab60d630fb90303abb73f528c037c23c725e57dce7ae39f5a271bf8de`  
		Last Modified: Tue, 04 Jul 2023 18:48:06 GMT  
		Size: 208.2 MB (208179474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:20.0.1` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:089d0731d89d4e375fb569e7093c6fcb7201d9d2364015c232d602c9ffb4d723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239407111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d512b6e06b04ac4a9d06e38886610b3aea9ba598f43a672a6ecc7738a7774c76`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:17 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 15:10:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce2a52a21f2e3597ed1d349ac03b32d0606d2a6d9083b5d907a7c197b786d2`  
		Last Modified: Tue, 04 Jul 2023 15:11:25 GMT  
		Size: 206.5 MB (206450075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:20.0.1` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:09ad6edf92f53d8c22563cae269000748171bf61ad573f9970463541e986f0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70cce5b1125ae64be0b7cd6eaa0048cf5b27aedd385d544b82d894717efee5d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:31:51 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:31:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Wed, 05 Jul 2023 01:31:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d3252a81af14d53cf2488077b55aed61f79dd96adabf36c770e183bfcc3117`  
		Last Modified: Wed, 05 Jul 2023 01:34:01 GMT  
		Size: 209.4 MB (209367400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:ebff0955567dd8fab2306a5ef4609a6fe6d4933d59a8ae5f518300fb1907c3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:f793221a79add4750dbe7bc1b0d64d1b2111fae7b32610f467f29373cd4e8da7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243225007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb26825a2cf8b7d85a5680d4589220f67b66b01a0461e66092b430b1378c4e52`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 18:46:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6250cab60d630fb90303abb73f528c037c23c725e57dce7ae39f5a271bf8de`  
		Last Modified: Tue, 04 Jul 2023 18:48:06 GMT  
		Size: 208.2 MB (208179474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:089d0731d89d4e375fb569e7093c6fcb7201d9d2364015c232d602c9ffb4d723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239407111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d512b6e06b04ac4a9d06e38886610b3aea9ba598f43a672a6ecc7738a7774c76`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:17 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 15:10:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce2a52a21f2e3597ed1d349ac03b32d0606d2a6d9083b5d907a7c197b786d2`  
		Last Modified: Tue, 04 Jul 2023 15:11:25 GMT  
		Size: 206.5 MB (206450075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:09ad6edf92f53d8c22563cae269000748171bf61ad573f9970463541e986f0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70cce5b1125ae64be0b7cd6eaa0048cf5b27aedd385d544b82d894717efee5d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:31:51 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:31:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Wed, 05 Jul 2023 01:31:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d3252a81af14d53cf2488077b55aed61f79dd96adabf36c770e183bfcc3117`  
		Last Modified: Wed, 05 Jul 2023 01:34:01 GMT  
		Size: 209.4 MB (209367400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:bdcede44bb906fa2d29c3f7cf61dc4d65aaf5013349b4c60d424827df23ea3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ccc42cd4233ee6006569d4c77aae0f3f125a6550147bfa37608710ce976242e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32ea279f46a5075ece209459e0679b196448923a72291b3e37c1c1ef14539cc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 18:46:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281360c02a410a2442426f6cd9cb72939a639eeb225e9b9e39c71940b8d15e`  
		Last Modified: Tue, 04 Jul 2023 18:47:41 GMT  
		Size: 198.5 MB (198529038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2f0f6a1aee75ef1675bf60136c377432a29a2701ac945e83167b5741dde45c0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230091366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18c74b0ad42d22fd8228e6046da6b34ce83c1618bb5f58c3b102295b66b8537`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:46 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 15:09:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef3fb831ee6d2d3ce1723d07c70f13a5553b1c127538e2a4932ab3489ab7c3`  
		Last Modified: Tue, 04 Jul 2023 15:11:04 GMT  
		Size: 197.1 MB (197134330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0984a0cc2cafd7fb770f9244fb048cd8a58abdfd1c09c3356963b473ea7246ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240578188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d1d922cb8d7e536911bfccb5637262ccaf7e305ea3a19cf4eac0b82edc482`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:29:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Jul 2023 01:30:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e203a18bba3f1a361fb7a304bede6e6369bb96037e9fbe0dff8c790b86a5a88e`  
		Last Modified: Wed, 05 Jul 2023 01:33:21 GMT  
		Size: 199.5 MB (199485045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
