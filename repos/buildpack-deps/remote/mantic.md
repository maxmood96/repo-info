## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:2532dd818486455cb11fef974b48e581eb3ea03ac1e1344efbf8bea7f1bc10e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:34a853f264e3fe8f0c2529116ee3c8c56ca8f46c5f1d7f65d4e6065fbdc25917
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279844814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc1d5696421ccb22fe07e3326101cbe834d779b68ce4371c106e7a6820ffbdf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:08 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:10 GMT
ADD file:e20f41d92fb02981d800b49f0872a5a0bc05c8b9f7dc569390c26af4b8d41caa in / 
# Fri, 12 Apr 2024 15:51:10 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:44:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:47:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a809a3b753932b0561db172e7a73f6408ffe16d23e3e7798fcdedb745b9376b2`  
		Last Modified: Fri, 12 Apr 2024 20:25:07 GMT  
		Size: 28.0 MB (28037166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0f148be6cac6a23a4edb3900d79a7b45807ee8f1d08444ed868006929611c7`  
		Last Modified: Tue, 16 Apr 2024 03:54:34 GMT  
		Size: 9.9 MB (9911668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b954ac7a2fd0002e0527e63a72405a55ba14a8f00932b05ff344f64350354c`  
		Last Modified: Tue, 16 Apr 2024 03:54:50 GMT  
		Size: 44.8 MB (44766344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cb83b8b2d911dd664cce09dffb30cded5f2d52394f0aa2234518545e03a31d`  
		Last Modified: Tue, 16 Apr 2024 03:55:23 GMT  
		Size: 197.1 MB (197129636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a97774ff38574234ba642237f26b5a56686e120f35d52801cdfb568a4ca4c2f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246505970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812adf25fd2ecd0a7dda68ffae2633cd165b1bae908542bf1819ce1b2a368821`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:22:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:22:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:26:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d03784ef1a0f8fba0d5ba66aa649704c0738839e0e0b7a3edcf32e7e679e3284`  
		Last Modified: Tue, 16 Apr 2024 02:33:44 GMT  
		Size: 25.7 MB (25685475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7dffb31d254b552d12914e690e612e00d722122772f28e4f60878569a1faaa`  
		Last Modified: Tue, 16 Apr 2024 02:33:41 GMT  
		Size: 9.2 MB (9151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf231dd75ff3ba004a73cfe9bfe03f40adef2f17d2d7902e7670fd14d427bef`  
		Last Modified: Tue, 16 Apr 2024 02:34:00 GMT  
		Size: 48.9 MB (48949406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fc8494a8b56715167e1336f0a3a3ea6356430223da436ca909a7a5c7a02740`  
		Last Modified: Tue, 16 Apr 2024 02:34:30 GMT  
		Size: 162.7 MB (162719703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:731cd983d3ce69d4c3675d6785c277e077bdf72ddc5656a646c81f189e9e53df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271963020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd68da85d5538251384ff0fdc2aedec7071fa8ab5fc95818c5f5ab10f6720f7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:04:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14dec08930ea65c3dbde0e38ed54f079d9cc601f7e9429870443eb6f5c127ecd`  
		Last Modified: Tue, 16 Apr 2024 02:12:13 GMT  
		Size: 27.4 MB (27378355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48b671c7c275cde8e73a26074b9763487010e57526a55b3e22e3bc0da54ec6b`  
		Last Modified: Tue, 16 Apr 2024 02:12:10 GMT  
		Size: 9.7 MB (9664437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6855e3956a9a4d92d9a1298b6fe89998168da253af783ba53efa35c4403235bd`  
		Last Modified: Tue, 16 Apr 2024 02:12:26 GMT  
		Size: 44.7 MB (44677506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44488ca64d68e744c93e18124ae16efba2553d1b3bd7344de4f0650a80d0f2e`  
		Last Modified: Tue, 16 Apr 2024 02:12:53 GMT  
		Size: 190.2 MB (190242722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2349a0c18c312c216a6a5c409c70955e2eded56433b6d70ff4031a374779f571
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293760934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a188e7246d596045416d488cbf77dc346ddb5d7e690314aa2c81e69b867f7c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:38 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:42 GMT
ADD file:a8da603c55c74defd91d533f7d8ae1989fdabaffbd1dffc9bda21c86eb06e0dd in / 
# Fri, 12 Apr 2024 15:50:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:20:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5f150c6aafa2908189205a2f6135c61c644daafd16d4b9fbb420f2d36da7c9cd`  
		Last Modified: Tue, 16 Apr 2024 03:32:53 GMT  
		Size: 32.4 MB (32350225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894c0745c5416dd216b7c49826dc5ede395abbe248d05a9409af9af764903622`  
		Last Modified: Tue, 16 Apr 2024 03:32:44 GMT  
		Size: 11.6 MB (11585816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce7686d375a21db004d3e3fe2d769bd8323976cc6e1f10f243c874c374105b`  
		Last Modified: Tue, 16 Apr 2024 03:33:11 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae87e30b68ac7dd58704311624af22a6fffc7ee245c345cc359000d731d247e1`  
		Last Modified: Tue, 16 Apr 2024 03:33:50 GMT  
		Size: 200.3 MB (200263325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0bb4be8e9694b1643f291f8dc14c2ec77a94fe63e7c34d645270681d5056626
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258357386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51802e8a43b0c61410f61911274b3a306cb32543bb003147a42f0ad5989b3fce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:31:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c38167d4d3684f5f8ee90b7adc5372841c98bba0d9aa208819985d030733dcfe`  
		Last Modified: Tue, 16 Apr 2024 01:37:51 GMT  
		Size: 27.9 MB (27890477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15768582f995f80e1c5766c7d3c9f5c2a98ef818cd780593cc4ec8e4abebc68`  
		Last Modified: Tue, 16 Apr 2024 01:37:49 GMT  
		Size: 9.8 MB (9758725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8626ab716cf334ee2c2065efea9a5208a1ca02fec3d802f60e7c3307826539`  
		Last Modified: Tue, 16 Apr 2024 01:38:05 GMT  
		Size: 45.3 MB (45253789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56139bd19e7ca4356199686daeef8a1ff38afe98729b44ed774ab26bc8078c1`  
		Last Modified: Tue, 16 Apr 2024 01:38:33 GMT  
		Size: 175.5 MB (175454395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
