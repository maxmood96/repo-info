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
$ docker pull sapmachine@sha256:fc95b20ad46ff237cd7663c707ea672f9b73c3b536e6a9190e378cdd83c6be1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:f87ede6e2176f403cd13e3a21489ffa12d942288da595cecde86b7da261c1124
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234261920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa21a6fa1c94419e83fc4643dcea9f156f1ff4459022e5f5616140201f9c05`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:11:41 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Jun 2023 04:11:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ac4645da9a9a399a9bdf7854abd92d9770f58ee94e42337d6752541603fda`  
		Last Modified: Fri, 16 Jun 2023 04:13:21 GMT  
		Size: 199.2 MB (199216668 bytes)  
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
$ docker pull sapmachine@sha256:92574ca8de30ed9da245e7493b0a51680c5e2341a7e7192db90aa7ff26ab392e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226745317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543cee7bce741ff5e4ec7199477c85ca1195e12c21e998603642d113ca367a5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:41:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:41:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Jun 2023 00:41:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc3b99e16fc6bdd4239e3db1dbc19d2c87041f31dca79cff18809d80b69f345`  
		Last Modified: Fri, 16 Jun 2023 00:45:23 GMT  
		Size: 185.7 MB (185652374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.19`

```console
$ docker pull sapmachine@sha256:fc95b20ad46ff237cd7663c707ea672f9b73c3b536e6a9190e378cdd83c6be1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11.0.19` - linux; amd64

```console
$ docker pull sapmachine@sha256:f87ede6e2176f403cd13e3a21489ffa12d942288da595cecde86b7da261c1124
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234261920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa21a6fa1c94419e83fc4643dcea9f156f1ff4459022e5f5616140201f9c05`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:11:41 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Jun 2023 04:11:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ac4645da9a9a399a9bdf7854abd92d9770f58ee94e42337d6752541603fda`  
		Last Modified: Fri, 16 Jun 2023 04:13:21 GMT  
		Size: 199.2 MB (199216668 bytes)  
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
$ docker pull sapmachine@sha256:92574ca8de30ed9da245e7493b0a51680c5e2341a7e7192db90aa7ff26ab392e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226745317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543cee7bce741ff5e4ec7199477c85ca1195e12c21e998603642d113ca367a5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:41:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.19     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:41:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Jun 2023 00:41:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc3b99e16fc6bdd4239e3db1dbc19d2c87041f31dca79cff18809d80b69f345`  
		Last Modified: Fri, 16 Jun 2023 00:45:23 GMT  
		Size: 185.7 MB (185652374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:2d52265a01e18fc6716212674774358739142b10378390d3c4d217c410ade600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:b93c0b8a2053b8b577fe6e5f38020046339ce2677080de46aa9ae3c90987cca7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822008d89bbd286032075a91a310d196c3eef40486c2389e34bfa5c987f9a4e9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 04:12:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4a1e74fee3694e6add3872cc34fdfbfd2d9ce9f1c1fa6ecc5dba07b4e0cad`  
		Last Modified: Fri, 16 Jun 2023 04:13:43 GMT  
		Size: 198.5 MB (198528900 bytes)  
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
$ docker pull sapmachine@sha256:f80980074b0b323de300ec5a422ffa7065478716ec781fd1aa10b6f9ee708ec1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240577979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e44e9860e35d21a5285d4c61b6ffb95e6d46b544a403c839a74c613da9355`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 00:42:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f39c886a3a370de9fca788de47f96fe5076c5868d55898b6263b63a3400fd6`  
		Last Modified: Fri, 16 Jun 2023 00:45:57 GMT  
		Size: 199.5 MB (199485036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.7`

```console
$ docker pull sapmachine@sha256:2d52265a01e18fc6716212674774358739142b10378390d3c4d217c410ade600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17.0.7` - linux; amd64

```console
$ docker pull sapmachine@sha256:b93c0b8a2053b8b577fe6e5f38020046339ce2677080de46aa9ae3c90987cca7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822008d89bbd286032075a91a310d196c3eef40486c2389e34bfa5c987f9a4e9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 04:12:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4a1e74fee3694e6add3872cc34fdfbfd2d9ce9f1c1fa6ecc5dba07b4e0cad`  
		Last Modified: Fri, 16 Jun 2023 04:13:43 GMT  
		Size: 198.5 MB (198528900 bytes)  
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
$ docker pull sapmachine@sha256:f80980074b0b323de300ec5a422ffa7065478716ec781fd1aa10b6f9ee708ec1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240577979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e44e9860e35d21a5285d4c61b6ffb95e6d46b544a403c839a74c613da9355`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 00:42:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f39c886a3a370de9fca788de47f96fe5076c5868d55898b6263b63a3400fd6`  
		Last Modified: Fri, 16 Jun 2023 00:45:57 GMT  
		Size: 199.5 MB (199485036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:20`

```console
$ docker pull sapmachine@sha256:1ab5e29b8afd84abae9690722476acf11cb1a7bf57d8134e144eb8c5cac1a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:20` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d7690f66016cd5970d3a380c7efe2637dfc73cc93c8d8c3fec62832506976e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243224748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cace1dd9cf5b16e0221c5e29f1dd8f11f63cd06e177052a6377070969a9091`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 04:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c332f40b32439b131d434ea8fcdd7b6e4822a2709441b2d7fdc45c54b01eb`  
		Last Modified: Fri, 16 Jun 2023 04:14:07 GMT  
		Size: 208.2 MB (208179496 bytes)  
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
$ docker pull sapmachine@sha256:7048a59aedff017dd2ac831d5f2fa807a656a4a5086c5d34b183de305fbcc3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c39d18a732192c330e58064b153ec3052a8e37cdf85a138887b754a564b893f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:33 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 00:44:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c669e2fd2913360cb59c8c4e1880f89bad52febcf63d016452c264375b1139`  
		Last Modified: Fri, 16 Jun 2023 00:46:34 GMT  
		Size: 209.4 MB (209367124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:20.0.1`

```console
$ docker pull sapmachine@sha256:1ab5e29b8afd84abae9690722476acf11cb1a7bf57d8134e144eb8c5cac1a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:20.0.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d7690f66016cd5970d3a380c7efe2637dfc73cc93c8d8c3fec62832506976e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243224748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cace1dd9cf5b16e0221c5e29f1dd8f11f63cd06e177052a6377070969a9091`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 04:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c332f40b32439b131d434ea8fcdd7b6e4822a2709441b2d7fdc45c54b01eb`  
		Last Modified: Fri, 16 Jun 2023 04:14:07 GMT  
		Size: 208.2 MB (208179496 bytes)  
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
$ docker pull sapmachine@sha256:7048a59aedff017dd2ac831d5f2fa807a656a4a5086c5d34b183de305fbcc3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c39d18a732192c330e58064b153ec3052a8e37cdf85a138887b754a564b893f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:33 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 00:44:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c669e2fd2913360cb59c8c4e1880f89bad52febcf63d016452c264375b1139`  
		Last Modified: Fri, 16 Jun 2023 00:46:34 GMT  
		Size: 209.4 MB (209367124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:1ab5e29b8afd84abae9690722476acf11cb1a7bf57d8134e144eb8c5cac1a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d7690f66016cd5970d3a380c7efe2637dfc73cc93c8d8c3fec62832506976e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243224748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cace1dd9cf5b16e0221c5e29f1dd8f11f63cd06e177052a6377070969a9091`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 04:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c332f40b32439b131d434ea8fcdd7b6e4822a2709441b2d7fdc45c54b01eb`  
		Last Modified: Fri, 16 Jun 2023 04:14:07 GMT  
		Size: 208.2 MB (208179496 bytes)  
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
$ docker pull sapmachine@sha256:7048a59aedff017dd2ac831d5f2fa807a656a4a5086c5d34b183de305fbcc3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c39d18a732192c330e58064b153ec3052a8e37cdf85a138887b754a564b893f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:33 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 00:44:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c669e2fd2913360cb59c8c4e1880f89bad52febcf63d016452c264375b1139`  
		Last Modified: Fri, 16 Jun 2023 00:46:34 GMT  
		Size: 209.4 MB (209367124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:2d52265a01e18fc6716212674774358739142b10378390d3c4d217c410ade600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:b93c0b8a2053b8b577fe6e5f38020046339ce2677080de46aa9ae3c90987cca7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822008d89bbd286032075a91a310d196c3eef40486c2389e34bfa5c987f9a4e9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 04:12:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4a1e74fee3694e6add3872cc34fdfbfd2d9ce9f1c1fa6ecc5dba07b4e0cad`  
		Last Modified: Fri, 16 Jun 2023 04:13:43 GMT  
		Size: 198.5 MB (198528900 bytes)  
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
$ docker pull sapmachine@sha256:f80980074b0b323de300ec5a422ffa7065478716ec781fd1aa10b6f9ee708ec1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240577979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e44e9860e35d21a5285d4c61b6ffb95e6d46b544a403c839a74c613da9355`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 00:42:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f39c886a3a370de9fca788de47f96fe5076c5868d55898b6263b63a3400fd6`  
		Last Modified: Fri, 16 Jun 2023 00:45:57 GMT  
		Size: 199.5 MB (199485036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
