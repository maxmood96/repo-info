## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:be63c64ee3fd7e0fa9d9330932a9bd46435e015ec6a6f5c1a13715580abfff5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:95636449c78c5311c92bb5c04cb71ca71e321e62d9ba7f340496a3e8ea1b6613
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364424180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0886d8c654ee90cd57e0951a093439e8008935828f019928689ca1c412fd23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac0b2d691022b6e9d2a4261f3c3547b5863197743e9544f77779e589aa6a9`  
		Last Modified: Wed, 04 Sep 2024 23:03:29 GMT  
		Size: 66.2 MB (66214670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6946879d70176adc3ffb5837bbaa51b79bced4142aae63dfbde91e5c47b690`  
		Last Modified: Wed, 04 Sep 2024 23:04:03 GMT  
		Size: 224.5 MB (224549385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d01e97fce87eb39b36f37f8aa45312b5a11da5fe5cca14f145171bd8242a1cad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0658cfb7a474590e1994b4a562fa6dabef9db569cd315e4dc4af819218edc3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff253c8c9180c53a680ac594e0b90ace399416d9f322bef4f9a66e3d0fe0c5af`  
		Last Modified: Tue, 13 Aug 2024 01:32:17 GMT  
		Size: 63.7 MB (63717307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e89c01125ee82ab0aa0af47c3526f7864fc2f07adc19ebfe1e2b58061dbb7b`  
		Last Modified: Tue, 13 Aug 2024 01:32:53 GMT  
		Size: 201.3 MB (201294728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:37b6810fa3d1d732d30766846909d30dfab637c900f47d30c4ae3280dfd8c9db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314706112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb90709c7a5e58c2a0ebff4d085a2cfed0066899451050ce3039cd3c67da182`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:33:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b337ebc4882ba5bf1b4d0ef428653fa3a9963e209aefc6227386f1a76b3176`  
		Last Modified: Wed, 04 Sep 2024 22:38:28 GMT  
		Size: 61.1 MB (61148386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f918449aecbe1b94d67117d739aece3a6bc2dc9aea2eecff37a6d4a68cf059`  
		Last Modified: Wed, 04 Sep 2024 22:39:08 GMT  
		Size: 187.1 MB (187105286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e67fb06f6e500129e26b9720fda34f641d39d6830faaee85458a3f5ad6243ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358192533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1708ee9622d0dde1a503c07b7ed6ad4bb182e70bbb6bfd19eef2b2e5d6328b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:05:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ed4283c0e34c1b3349c61e47afaf58a71aecea82db8aee69f2c8a865f8c6e`  
		Last Modified: Wed, 04 Sep 2024 22:10:04 GMT  
		Size: 66.2 MB (66237648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef4fa35fa4ab50f808bb497d29332afec951c4bcb10c0dd0d72bbb720a7932a`  
		Last Modified: Wed, 04 Sep 2024 22:10:32 GMT  
		Size: 218.1 MB (218109327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04cd0e8012a7b0a927453540343a58c40ce7422329b38254cc3e2c0fa5709eb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.2 MB (370192161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a14e845327d478743cc97f4cad35b0845c843799f0201dcea0ab4a3d804b16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:11:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a203d729458242dda28f4795cf80bb88746084ccdc8cce21ba2acd7dcaefb3`  
		Last Modified: Tue, 13 Aug 2024 01:17:23 GMT  
		Size: 226.9 MB (226923306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3b99b1a614b2627c2ee392abf6cec24d6e709a64ff2660fa5dfcff701541b014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343104341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e38cadba3b728e3cc3d2698789e9a516b7fff066fe5de0170975495cb00f8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:21:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b82974da5a3d69a6ca94388b0a3f14e1fe28ce4d21ef9f4032d841f5325b32`  
		Last Modified: Tue, 13 Aug 2024 01:38:31 GMT  
		Size: 65.0 MB (64998376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b138f1bac27906feed7c16ced7bfda41230bd94f4e3fa7fa461b5d556cca85`  
		Last Modified: Tue, 13 Aug 2024 01:40:49 GMT  
		Size: 205.6 MB (205575439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad4b04250fc6a8dfb76563542cd67b13c68bb161c5ae1e30e1821818f90a5ef6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.8 MB (375834614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662c9bbbe195ec285293da4dbb7e93e9ede726496a2364e6f9523f561594b7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172a0ce16e36a34ff88a2732bbe6037759cb39c60616bd29dbc966d3bb79ec3`  
		Last Modified: Tue, 13 Aug 2024 01:37:28 GMT  
		Size: 71.4 MB (71359436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c40f2aa6297d7f1a7d0c5c01d5abdbc3208369127949982cb6b44835f9e6370`  
		Last Modified: Tue, 13 Aug 2024 01:38:08 GMT  
		Size: 224.6 MB (224601465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1f0fb710e4c77f45c369961d8f5ad1b5c3c2d6d6637879b7f0ee0cec7a11e1e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443858778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13763f9c3914a92f12e358871f27bfd1ee3de1d1a8f20a4e5a9c057826caed09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65deb42d9c749a528063c18ed3482c3235a8863523f7fc5d895330b910edd50a`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 65.5 MB (65455674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a959a2b7a253bddaf7fd68b258fe0255968fc0d4f52643281e2ac2de68e19e6`  
		Last Modified: Tue, 13 Aug 2024 00:53:51 GMT  
		Size: 307.3 MB (307284095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:82d3e113ccf2880c3912b85e42057ceef574bf3adbe52c37b776b906b69dd473
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342028696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984dfc489e1f8db6f7dc2248ab5d807b1457996661c87373f320a97a40a6e041`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:21:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c43737168f685110fa0a3c4ec68bd02aecf241fa770d30b263bb78a2ad0f70`  
		Last Modified: Tue, 13 Aug 2024 01:26:30 GMT  
		Size: 67.3 MB (67269243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9eb516daa4ac7451bd5504522258db8cda9841d72e9c32f295c166a2ea370d`  
		Last Modified: Tue, 13 Aug 2024 01:26:57 GMT  
		Size: 200.7 MB (200715920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
