## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:2792cfe4f9d542bf405b9fd2716ca6f552508a5972c82aee7cf0960bb1a8b978
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
$ docker pull buildpack-deps@sha256:f8529b819594915ae9cc3b188c5c9304030d4597f1b2114f5e219c3608b86c7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312370278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac0d21d6f883870fe036d37de4501537470cf4e4157da6c015e21635bc7b35e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 08:48:30 GMT
ARG RELEASE
# Mon, 15 Jan 2024 08:48:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 08:48:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 08:48:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 08:48:31 GMT
ADD file:e5e7262b8cac5f725d4433779ecfbcadb4025759c5973a276b344033d087bfb3 in / 
# Mon, 15 Jan 2024 08:48:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:59:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc35f4f5ecaa073076bdb6773257cebc5c5f2ad32bf5f3c21b5f0f462cc825ab`  
		Last Modified: Wed, 17 Jan 2024 07:40:47 GMT  
		Size: 30.3 MB (30313466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc63ab3c7470561d0ea5fde5977e2154db737dcd470c977cd0202fbe1cb86d`  
		Last Modified: Wed, 17 Jan 2024 08:04:45 GMT  
		Size: 13.7 MB (13724970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8810979dcac41741ad928f971345e01782c372a7de2b1cf7c4e123a2dd375`  
		Last Modified: Wed, 17 Jan 2024 08:05:12 GMT  
		Size: 45.4 MB (45393284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119bcd1a8c6a2afa20f35a01b9ab2c61cd4e8a1670502601ae11ec5564fec88a`  
		Last Modified: Wed, 17 Jan 2024 08:05:49 GMT  
		Size: 222.9 MB (222938558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e811ec208c2b8251790e1cbe760b3c02a6245d1c418bb0c50803036f4d442935
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270519637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b13f0aea87b2986b2d1a3c60aab7b35d205aa6cc900fd9b072427031229e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:17:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b1fdfccfb097e3ea8369bc634c0a794c7f5dfa00a944deeff4a97c9496acd7f`  
		Last Modified: Thu, 04 Jan 2024 20:24:32 GMT  
		Size: 25.8 MB (25769091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7239c158ae97251c79c79b045912b146acfff69748a2146ac66091ac11d3a817`  
		Last Modified: Thu, 04 Jan 2024 20:24:29 GMT  
		Size: 14.6 MB (14621580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b5a3653290438533a6e25c0661e212a2f6e7a8757b18df319541e20188a0e5`  
		Last Modified: Wed, 17 Jan 2024 02:29:11 GMT  
		Size: 50.1 MB (50091765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a163e6271ade96eb72f1f822e130bd6fd7a7f4034343757a8aeea0f1a5b4da9`  
		Last Modified: Wed, 17 Jan 2024 02:29:56 GMT  
		Size: 180.0 MB (180037201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:924bdc65c2c6a97c6f128e9e3da62b60757046cdf5e5a88a15b295789a623689
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296858531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9386d75771abb5081b93c7b767d2db2e33e87c7cec58884923a868a78090a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 09:01:27 GMT
ARG RELEASE
# Mon, 15 Jan 2024 09:01:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 09:01:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 09:01:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 09:01:37 GMT
ADD file:50cd35ee54b9e6bef21c07d3de865616eca5989c84802fb5387d3e67116b92ef in / 
# Mon, 15 Jan 2024 09:01:38 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:25:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:520813436ddf1775384a8b61d3beb75fb5c87ba7ba0ce3f9840941e56bb9e5a3`  
		Last Modified: Wed, 17 Jan 2024 07:27:29 GMT  
		Size: 27.4 MB (27403386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc92cb739627d08f68672a7bc2d006b5cee710ee782a771e88fe36a8eed57f28`  
		Last Modified: Wed, 17 Jan 2024 07:27:27 GMT  
		Size: 15.5 MB (15514859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93856390a3ee7c4b783e715271b23a12c6acf94aff70154cc3e8ace97f38337`  
		Last Modified: Wed, 17 Jan 2024 07:27:43 GMT  
		Size: 45.4 MB (45435819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939a2502ab78eea4bc733dac75b819adadf9349ed7725a7d30993516221ad516`  
		Last Modified: Wed, 17 Jan 2024 07:28:12 GMT  
		Size: 208.5 MB (208504467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:de6c6a69e428cac7c166e218d4e7b1fdd9d4956caef97888e53c829b75589edc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325802538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f70b30ab43d3b5800fd6a3d79629b6282ef74eaa572d940cd744a53c741db77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 08:51:02 GMT
ARG RELEASE
# Mon, 15 Jan 2024 08:51:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 08:51:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 08:51:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 08:51:05 GMT
ADD file:5fe12e290a829b7d5ff1eef600b9e7e81a107059fdfd6c8195467a8e2f0a0463 in / 
# Mon, 15 Jan 2024 08:51:05 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:49:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:50:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:56:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5d48a6050ca99416832e234804b8b3fb2aecfab55da73b3f44bf60caf56ec7`  
		Last Modified: Wed, 17 Jan 2024 07:58:48 GMT  
		Size: 32.4 MB (32381280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6cd7f36bfac4a5a101ecc849afd614052d279b532e79535e7042b63ca4cdef`  
		Last Modified: Wed, 17 Jan 2024 07:59:11 GMT  
		Size: 18.6 MB (18561203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e50ca5a098317b71eb0c9feae6c31c09796fa161e2d8fd6021a86e7e1ed0293`  
		Last Modified: Wed, 17 Jan 2024 07:59:28 GMT  
		Size: 50.5 MB (50483936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b0aa309d83b6dc588976eafb6db03f148162926a9f72379582cd1e5f5d6ca5`  
		Last Modified: Wed, 17 Jan 2024 08:00:10 GMT  
		Size: 224.4 MB (224376119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e005e4677bff5ee1112d0310428d64a4959f3f07746910eeb67c30f195c2c6d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291147667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c781042dc5ee40cc58449e3420a8f89882ea25c0e6c6e1754c388e91e564e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 04:01:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0eb0ee1ee32a505c711b23ae33e7ecc888899622d95c7e982ef82dbb529c5d8`  
		Last Modified: Thu, 04 Jan 2024 20:50:14 GMT  
		Size: 28.2 MB (28174524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02199b1c3761965bf141c9010678515a9c50e39cc89d2a830d1dd5d17aa25bc2`  
		Last Modified: Thu, 04 Jan 2024 20:50:13 GMT  
		Size: 16.6 MB (16609480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485bb0479022ae70b4d5d036ab8cd2a74bdb0cdf2ce41f139a8f33c3c3062fe1`  
		Last Modified: Wed, 17 Jan 2024 04:09:32 GMT  
		Size: 47.5 MB (47466650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a964a9c9929f0234620bf2dd4effe60e6d9f99cc5772e627b8e1a32f683e7b1`  
		Last Modified: Wed, 17 Jan 2024 04:10:03 GMT  
		Size: 198.9 MB (198897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
