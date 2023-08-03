## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:594df2f870c56c720a6d79560aaba368ccb7baddb107cf9f703919e1a2057640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bfffaa002e603f1746d4140734bcb11d31f11d46f49bd15c8c87658dbe2bbd92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268512898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62f01d447d75d9d7421d061d4f0060124ea4a4a5d099f94065d2d5f256cc11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:16:11 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:16:12 GMT
ADD file:3ff011e7c817c9b010391c2b2f74a111d8c37165e6fdff18e18ccfa67ff7667b in / 
# Mon, 31 Jul 2023 17:16:12 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:29:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:33:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b631a20f124dbf4ef89945623fa5c94460561f9c7b119e17fd3c1a4bb50ced01`  
		Last Modified: Thu, 03 Aug 2023 03:39:26 GMT  
		Size: 27.6 MB (27620888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da929c5e27c82b25b247dc649219b7fe3bf48f28e76bed18114af4abd4791a`  
		Last Modified: Thu, 03 Aug 2023 03:39:23 GMT  
		Size: 13.7 MB (13744580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7845fca4b254b8c361b6d30d8a0e5b9d6c5a8df43f1482a7c0ed841be440e66`  
		Last Modified: Thu, 03 Aug 2023 03:39:41 GMT  
		Size: 44.4 MB (44385831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13732bb59235c716d5feeb147388be0507a46221614c1bb12d7b021779e34d7`  
		Last Modified: Thu, 03 Aug 2023 03:40:12 GMT  
		Size: 182.8 MB (182761599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a565c3cb1f8cd41f245613f8957013b3a264838499c1bc2d8c580b5941160847
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232389301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3117034abfe05412e6279df4faaeedb6f2efe734b749483f02f70b23836ab7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:20:03 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:20:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:20:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:20:04 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:20:13 GMT
ADD file:3ec1cc20b36a86b78ff00125a182fab6d7ee8916dbdc6f52d40e182e2892dd06 in / 
# Mon, 31 Jul 2023 17:20:14 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:13:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:17:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c3febaf312f99233e7db5cc744fa3ec8c5db0830dcbc8c5125cfdd72aecf67`  
		Last Modified: Thu, 03 Aug 2023 01:25:14 GMT  
		Size: 25.4 MB (25435340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a700903f5f3ce05aabebc3211881ef254b83adf35f632c84c489992fa28ba`  
		Last Modified: Thu, 03 Aug 2023 01:25:11 GMT  
		Size: 12.7 MB (12664410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ac461f8a1743501ef6bb272d8425c3b410e894c911165311e282e36b180636`  
		Last Modified: Thu, 03 Aug 2023 01:25:30 GMT  
		Size: 48.7 MB (48671997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecfeb569a89541933b15e8f732b6d5ea530c3db7a69ec0ec203b7616765941f`  
		Last Modified: Thu, 03 Aug 2023 01:25:58 GMT  
		Size: 145.6 MB (145617554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:413452ef2b8b21174edae216d7d575c62f1a75680d16a91bd602faef3fb6cd18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258111819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15472ea9645030f627ea62abc62f9b1dc183a64c830d7ddb5f042130d5c7e063`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:39:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:43:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc3ebe95800c7b88cce17a04cb6a4e51211ef73656bd15c0885a6f96b173aeef`  
		Last Modified: Thu, 03 Aug 2023 00:50:53 GMT  
		Size: 27.0 MB (27031709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c53b82c57224a6aeb0716a4227436ebcf006fbd33ca9346c8875243d0ba942`  
		Last Modified: Thu, 03 Aug 2023 00:50:50 GMT  
		Size: 13.3 MB (13333570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf1c6caaac9b5afe5c21f87c81ea52cb2f170dc8014fc97564f9337986ac802`  
		Last Modified: Thu, 03 Aug 2023 00:51:07 GMT  
		Size: 44.2 MB (44235418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca7ab853d6afc315714a36136c799da5283745fc8dd554205eacc854b029685`  
		Last Modified: Thu, 03 Aug 2023 00:51:33 GMT  
		Size: 173.5 MB (173511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e3108463e296ffe459ea82aa555c65cc845d282c08c133cbc3c89b478efebeed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293045547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528798424c0d5cbae974a62b5d3633cb2e55806c2fc356882a9bb10757052d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:18:51 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:18:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:18:54 GMT
ADD file:98fe279e3c3239702ac2eef51540228e24a3e15e923342cb3e7cd7dd3684a090 in / 
# Mon, 31 Jul 2023 17:18:54 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:32:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:38:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c8f1d2c62b1aacc6f999b01ed9c6ef10bc5fd3a989af86649162cf5292934393`  
		Last Modified: Thu, 03 Aug 2023 03:51:49 GMT  
		Size: 32.0 MB (32013471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd1b07037748833f21cbeb83084ac8ff4a0ca93e61d3e0ac3914daf1beac24`  
		Last Modified: Thu, 03 Aug 2023 03:51:45 GMT  
		Size: 15.8 MB (15842395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e1c2370aa8951d8926c5924bcf24547ca74703904b0527c7f23e46740815f0`  
		Last Modified: Thu, 03 Aug 2023 03:52:13 GMT  
		Size: 49.1 MB (49086146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa281b8d2db730035bc9fca050c2d962532df63e59ee2bf70160dc162d8fc5e`  
		Last Modified: Thu, 03 Aug 2023 03:53:10 GMT  
		Size: 196.1 MB (196103535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:44b784789004e2fccc14b9636f8fa0730efb5f1930d11d54f7c14c56311fabc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240153847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adfad68a288281bc1389101040be477a39a459346be0ac42cacc62af7ed7d1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:12:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:13:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:15:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec64faa69090fa13dbf3419726044381d0c7137866daa46daa6a85f785a5389a`  
		Last Modified: Thu, 03 Aug 2023 00:21:59 GMT  
		Size: 26.2 MB (26244138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910656a90f2717882b9ec910b9f54fd6d237915853a5ffd4b160913158408a2`  
		Last Modified: Thu, 03 Aug 2023 00:21:57 GMT  
		Size: 14.0 MB (14005556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c57b46166fdc730877dcee11a4a6741fc625ecc917bc6560eedc5c318870915`  
		Last Modified: Thu, 03 Aug 2023 00:22:11 GMT  
		Size: 44.3 MB (44275485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b0c7ea3a3d1a46630eb9d54eec8f2d9242f0b9406342b50959c7ae76e87ce`  
		Last Modified: Thu, 03 Aug 2023 00:22:38 GMT  
		Size: 155.6 MB (155628668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
