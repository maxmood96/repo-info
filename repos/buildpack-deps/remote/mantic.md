## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:e0c64e997e1adf8a9bae9e56d7b1a5ab369d8345ceed4f05bffdecd010db3a71
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
$ docker pull buildpack-deps@sha256:f3e24648ef154885cea361d8b52c2e1985772d844acee52834f53a7b890a660b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279847530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804500f8c179d8acd90b7a8ac182045dd16d1a2a8852e33f39f2ca8d75bb8a07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:02:03 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:02:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:02:05 GMT
ADD file:870c43eadc01423c5bc11fc4422ee10b05cae0f50c997f8e380e0ed25c6c0b11 in / 
# Mon, 29 Apr 2024 16:02:05 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:06:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8496cd0ea1eee2817b0144b138e4851ca29d675473addef86c4d5838b98b10e0`  
		Last Modified: Tue, 30 Apr 2024 03:34:40 GMT  
		Size: 28.0 MB (28037242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90001033f98f32d73d26d33545975169f4a8186beac4819ea4fde58f38f27815`  
		Last Modified: Thu, 02 May 2024 02:13:27 GMT  
		Size: 9.9 MB (9911781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d673a81eea47677f1c20cd613c42d148d058da96220692d2550e23112c34d7`  
		Last Modified: Thu, 02 May 2024 02:13:44 GMT  
		Size: 44.8 MB (44768343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4707b0e737051f716e2f28a20fb735b02d0039f7410b285382c64f5768e886`  
		Last Modified: Thu, 02 May 2024 02:14:17 GMT  
		Size: 197.1 MB (197130164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ca3e5113b7e6f0f04020de4f7a6a18a7582b7a2960af44497fea12115bb5cc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246510618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb15e530f5c107eee84dc5eedaeed5c20c33d943d7eae04e81da24a4f37505a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:05:53 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:05:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:05:59 GMT
ADD file:36a9fb96170feb2e8bb6dfda0793b5f7069593502c61024a6ed3d84eb01afdaf in / 
# Mon, 29 Apr 2024 16:05:59 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:57:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:58:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:02:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c14f7cb79524b2adc26e658f09be736a2820a009c0cf783b8204bd8f44ff6dd1`  
		Last Modified: Thu, 02 May 2024 02:11:20 GMT  
		Size: 25.7 MB (25687736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891e062e56c3529de217cc9c1b86c28a85a8a887411ef56e0566d3b280203ff0`  
		Last Modified: Thu, 02 May 2024 02:11:17 GMT  
		Size: 9.2 MB (9152040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922394cec4336bec66ccf4cdc7027a9c41f90dcc87336a1ea3fae1ca7dd15295`  
		Last Modified: Thu, 02 May 2024 02:11:36 GMT  
		Size: 49.0 MB (48950463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aec45b68680584fce0c0c2f6a272f6d1cb44d067216db665c61cc1983905e8a`  
		Last Modified: Thu, 02 May 2024 02:12:06 GMT  
		Size: 162.7 MB (162720379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a3640231d503821e2c6a5da0188ac7bf1cf3007bd824ab909aaccdd8773e222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278033925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59229c4f31385dbdb1ebd95e2d43a2a346c2a4357ac6299ffc4564aa484be29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:32 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:36 GMT
ADD file:2a859c5d715743469a5a33d7b6038db94be34745cff1d5f681ed1d3d0e5931a6 in / 
# Tue, 16 Apr 2024 12:36:36 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:33:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9f940a958fa1db38437a7b5c1c0ed37e0c5942712bdd8f2b76b3389807d1ffd6`  
		Last Modified: Thu, 25 Apr 2024 13:46:30 GMT  
		Size: 27.4 MB (27379628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d18d62fa954ee78994d922bbd009c6e5a86cf5622f267d40eff6d0e20d7a5`  
		Last Modified: Thu, 25 Apr 2024 21:46:46 GMT  
		Size: 9.7 MB (9664678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bee0d85689fcb88d4edc1a4a568dd0c83256cd6df41453994ed58fa7b4e17f`  
		Last Modified: Thu, 25 Apr 2024 21:47:00 GMT  
		Size: 44.7 MB (44677946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f80c1f8fb52f7ab333456e3bb0485fecad800cfff0082408b4424cca4b0a3dd`  
		Last Modified: Thu, 25 Apr 2024 21:47:27 GMT  
		Size: 196.3 MB (196311673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd4fadf1be30331d776e1c0bca51d8f3eb84c269e05f8482b29332931e8b7c97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a29d9971d8be44fb65d9fc57e243af484322b74bc313188a441b0381015ecd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:42 GMT
ADD file:d101590827db35fb306467a12041319349f48362c5708f20a992cacfa084f678 in / 
# Tue, 16 Apr 2024 12:36:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:40:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:50:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48003274bf9d81034d8159e3fecf795a0d28af11431c0dac90ec318b737dba7f`  
		Last Modified: Thu, 25 Apr 2024 22:06:33 GMT  
		Size: 32.4 MB (32350551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a96571a4483e69c613086a3247b75c7f4157a94d51eaa2b35b852337ec5cba3`  
		Last Modified: Thu, 25 Apr 2024 22:06:27 GMT  
		Size: 11.6 MB (11585701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03369684bdfa11e2d1e5cd9d25cdda8608261828650129c36480834337b220`  
		Last Modified: Thu, 25 Apr 2024 22:06:50 GMT  
		Size: 49.6 MB (49561538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b527830ba02a4c6f389d5507ef2b815ae774ee62ff3aa25d06fa2a03bf7d2a`  
		Last Modified: Thu, 25 Apr 2024 22:07:30 GMT  
		Size: 207.4 MB (207361126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9b7495b48b0d48025f09d498d616d85a6d2444f43496ceb97d60ecb548ed7aa0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258360349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75f1763aee9261cfb542daaa68c084826f2379c33264c46bb2480565a3586b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:49:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:49:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:49:37 GMT
ADD file:76b6235c926b9bd628f27161f73913d479e584c2035eb7185806b814f4e96e14 in / 
# Mon, 29 Apr 2024 15:49:38 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:24:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:27:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae85e9169f00cfaac0525494fb8251c5f790089a9748fdbd34e5fec105e50fbe`  
		Last Modified: Thu, 02 May 2024 01:34:50 GMT  
		Size: 27.9 MB (27890933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e372ff38d547ce6c08db910602c662578b312dc24c86593738f583360e0613`  
		Last Modified: Thu, 02 May 2024 01:34:48 GMT  
		Size: 9.8 MB (9759011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f4cdf7791a613f05e9e4b51edd04a313f26fbe67c95bfbe74d9d933253a492`  
		Last Modified: Thu, 02 May 2024 01:35:03 GMT  
		Size: 45.3 MB (45254411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f70a60cda378edc68ae96c3a26b34f3237057c5fb7ff7d927208ad251cb0`  
		Last Modified: Thu, 02 May 2024 01:35:30 GMT  
		Size: 175.5 MB (175455994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
