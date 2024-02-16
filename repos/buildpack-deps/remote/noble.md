## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:fd07370a10295a60b64da2eaa13ee896d45cc3eaf8573884c54ca736078163fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:333917f6aa55aaa103d0b78bbb3743bda393e7d317bbcd3b1deb0f8b72031234
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323857558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01879effe0ec199729157e81f7d45cd0a74546be873c66d59fa0a688098b10f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b23ce13f84812ac6df1bc6603b609b4098273dd0ead57baadb72855d6221e`  
		Last Modified: Fri, 16 Feb 2024 03:41:09 GMT  
		Size: 231.6 MB (231608416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b6cc8af1549794c8486e4fd41dc40e9c7f2c0e20e9ee9530396e179f7d30e93e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278478732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500a6696aa4b58f2dcb0d85b29b97d91225b9a56cc350a1fd5a8ebfcb8b8f6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:59 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:59 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:53:02 GMT
ADD file:678218a331e2b831edef68fd454337cb55ed29bb64454ff990a67583493e06fa in / 
# Mon, 12 Feb 2024 04:53:02 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d82b6d605223cf339149712324b60bc99eb59175bb4d477ffb0fcc34cc97d78`  
		Last Modified: Fri, 16 Feb 2024 07:38:30 GMT  
		Size: 27.6 MB (27566827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860140fea4cdc3e53205a34786b066013a5e82411569c57836e8dcf0f8cfefcf`  
		Last Modified: Fri, 16 Feb 2024 07:38:28 GMT  
		Size: 13.0 MB (13049001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64741559589b095771e88f70854d70be6825c7f473f1a258bc60d13f07019e42`  
		Last Modified: Fri, 16 Feb 2024 07:38:47 GMT  
		Size: 51.9 MB (51929677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a5a4878eac06b9e698ee6a3250da6d8ed573d6e14fb144618d9daf1ff9bc7d`  
		Last Modified: Fri, 16 Feb 2024 07:39:23 GMT  
		Size: 185.9 MB (185933227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3eb16e62a071ad7d3fbfb73ff07a3b096b1c2c571d070f55b85d58845aab17e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310487016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7904e60519f5b1814dc03ad696849afbcf4f3d3f4067def614e910e5d0c0ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:48:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ddf3e3c3a3f4a7084396c5fea9e867258a287407252e406f4a47f9c57c7e768`  
		Last Modified: Fri, 16 Feb 2024 04:50:22 GMT  
		Size: 29.6 MB (29634636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a510494515f4fe176171eb81a58eb13a7d968c4fd55af5da54ea2b1236d850`  
		Last Modified: Fri, 16 Feb 2024 04:50:20 GMT  
		Size: 13.5 MB (13520137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e7554008f9b077a355c6245831eea73ea7b69335b673b117960e3985c652e`  
		Last Modified: Fri, 16 Feb 2024 04:50:36 GMT  
		Size: 48.2 MB (48184820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f65f1329b9a04f2040322eb6419b9f931ac6ee4a673b814acd7de474c173abf`  
		Last Modified: Fri, 16 Feb 2024 04:51:08 GMT  
		Size: 219.1 MB (219147423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:09a3d9ffff8cb8fdd1181b970e6046cca6735a0d5b0933ab4d6045e0c2af885c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340724194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83974ad154d44a698b0ba4385d07ef05492680f6befddac8e570e401d04c518c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:05:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:11:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f99e65953eb4c26f66aa6a038cad2127b130e0857531898f0345de4a7c7c967`  
		Last Modified: Fri, 16 Feb 2024 04:14:18 GMT  
		Size: 35.2 MB (35220719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85838c27b62b5d20ff7b908b2b786d1db23180ebd001f5af468413763f01c9c0`  
		Last Modified: Fri, 16 Feb 2024 04:14:12 GMT  
		Size: 16.0 MB (16037692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5962258c49518f24fa86ea6b63115900e0009f9793322227c39a561cacb6ace3`  
		Last Modified: Fri, 16 Feb 2024 04:14:38 GMT  
		Size: 53.6 MB (53572182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760e1a5aaa7d979936307c88cefa9024fdd1430b8041cf9ce8e9725e565fdac0`  
		Last Modified: Fri, 16 Feb 2024 04:15:24 GMT  
		Size: 235.9 MB (235893601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a48c64715451231c8f1a80ea6141dfde0c6839f220820139adcf2f675682e3e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305732967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3930ec12b77f5751f083122cae0faeb0b275c7bfabf5243027c90c511404b2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:31:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404889b91c64925706ad61665db8c07a99ed919566a735134342d7542d1607f2`  
		Last Modified: Fri, 16 Feb 2024 06:34:34 GMT  
		Size: 50.0 MB (49965092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cab934ab958cb8b6e6182f8598bbb4129e6c25c3c8e15805979f7c2026fa6e`  
		Last Modified: Fri, 16 Feb 2024 06:35:04 GMT  
		Size: 210.5 MB (210466296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
