## `buildpack-deps:kinetic`

```console
$ docker pull buildpack-deps@sha256:182fb8ceb3807f758a32071040ff65080b648df4381c4519bb9bfb6677f97f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:317a299df2865d274ead2d23902df2210363380f4a2eaf0d3d78788075005429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258652746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8608a0b7fdb185cc6b1ff665bd7a561642e0af7fb7b2526377aac43b0fb192ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:42:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:45:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00919c8a5cf1930144d6fd110c137244137a98d7a72e6a12685a879091389d23`  
		Last Modified: Tue, 25 Oct 2022 09:53:54 GMT  
		Size: 6.8 MB (6779535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895cb5b3ae5f27255eda4cb39e4ed45bad1d38cab7a215c9e80ea9d4fcb23d67`  
		Last Modified: Tue, 25 Oct 2022 09:53:53 GMT  
		Size: 3.6 MB (3633931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e075966acfa5f4b1c6e4d9187fbcd089b5234559942b4917aca46f88f5e2dbea`  
		Last Modified: Tue, 25 Oct 2022 09:54:09 GMT  
		Size: 39.7 MB (39713932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec68da96895d936fa54f0ac2f34a2afdfcc69260dc0dac410281882801ba10`  
		Last Modified: Tue, 25 Oct 2022 09:54:44 GMT  
		Size: 181.1 MB (181067766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bdb75dfe011d97a4fd170763dedfdb3b2da5ee4b38a037556dac8110f28415f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221827551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3d29dd096a97db03ae22dda02181c623413bdd9d4d02a8baaf6e31c1383e1a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 17:59:05 GMT
ADD file:75349a3eb1b6088d6273239255c38f1b06092238dc4f33150465f79c3dfb0d2a in / 
# Wed, 02 Nov 2022 17:59:06 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:24:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Nov 2022 18:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:27:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceab7032a4972ceafece338b0f5e3ebbc81d48d712647ff011a102e03e71d244`  
		Last Modified: Wed, 02 Nov 2022 18:00:51 GMT  
		Size: 25.9 MB (25871361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5cde5881687bfd0f5c7814e306e45ba740d0b7a55578dedc1cf6e332748645`  
		Last Modified: Wed, 02 Nov 2022 18:32:30 GMT  
		Size: 6.0 MB (5954638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbbfc114f5fb1e6d3ab4d8d42d3252c89f60f18670e7e7047271d69bcb04024`  
		Last Modified: Wed, 02 Nov 2022 18:32:30 GMT  
		Size: 3.8 MB (3801131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f1b183c0c9f5adcb88fbfadc25ae36a85eeeb5ea63c41e4794985065cff58`  
		Last Modified: Wed, 02 Nov 2022 18:32:51 GMT  
		Size: 42.6 MB (42594218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db49b9e30965d86644977bf58c058bed9c3f064a76d90cdcee1ced7641b2d64`  
		Last Modified: Wed, 02 Nov 2022 18:33:27 GMT  
		Size: 143.6 MB (143606203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7f591bb67e4190e35105756af84f44d4bdd7c020d451632335a530a83e8e299a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246644046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c243a099dd8aadaf491de0633949554b9e17b02bb3dbecaeba22314be0c60`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:06 GMT
ADD file:30361063c284df6e20a85ff95b9c7b93648fe9e04ac935c9ff888e5c5f3af7ea in / 
# Tue, 25 Oct 2022 05:55:06 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:19:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:19:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 08:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:23:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a2e58a4bc1e52e3ab8904706a68a79146364ec32d8caf1bd106c3c9966a38fc`  
		Last Modified: Tue, 25 Oct 2022 05:56:30 GMT  
		Size: 26.7 MB (26676995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c8913a9c66f64a1f5ca1349c8a8b9923f9eb9c8aed25bf3ec160a33e5a796`  
		Last Modified: Tue, 25 Oct 2022 08:36:03 GMT  
		Size: 6.6 MB (6607031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491d7cc7a42af61771e26652e91532db813e380fa19339f7279420206df0290`  
		Last Modified: Tue, 25 Oct 2022 08:36:03 GMT  
		Size: 3.6 MB (3602476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2cf60ff33717c4a17f0ca2f77473b69d8d357e4dc81ef8bb8a5e24382aa106`  
		Last Modified: Tue, 25 Oct 2022 08:36:17 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297c22e5e80de066ab641f5f47a060831dda9dbda728c9ffc0333ffd65aec38`  
		Last Modified: Tue, 25 Oct 2022 08:36:45 GMT  
		Size: 170.3 MB (170270976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:51996e24b6a2b38c48ebbd6d72b55d93305c4704db27dca5c5777654d1ae0ea1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281267737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe8d36a0b8581f15462dbc087c53d2937d29753b017aa4a2cc843d2dbf347b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:47 GMT
ADD file:02ef6cd7544bbd78972e9193da5adf058ae660c0dfbdba6a01c6dd53ca0dd4dd in / 
# Wed, 02 Nov 2022 18:17:49 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:44:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Nov 2022 18:45:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:48:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:345382392ac82767fe9071a0db9ec45e49ca5810d51499caf1f2e1f9a5219733`  
		Last Modified: Wed, 02 Nov 2022 18:19:26 GMT  
		Size: 32.1 MB (32099850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a66230aa93af28fd2ae7105d7436076c43a6e62ef4e40dfbd05bad90cd6d6b2`  
		Last Modified: Wed, 02 Nov 2022 18:53:26 GMT  
		Size: 7.8 MB (7752358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d5e0c03ca131a3450680ae21ae96995663400861d73240ceb2a708f69c803`  
		Last Modified: Wed, 02 Nov 2022 18:53:25 GMT  
		Size: 4.4 MB (4362075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6009aba2d0a4482f73548f83e57bec8012daa0911a5c2d15a377d91a0649fce6`  
		Last Modified: Wed, 02 Nov 2022 18:53:50 GMT  
		Size: 44.1 MB (44121294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27b57fa0dff9bed60a02739d356abd59149ae9c21623ec01c320727bd475d2d`  
		Last Modified: Wed, 02 Nov 2022 18:54:49 GMT  
		Size: 192.9 MB (192932160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:da200837021c8150a6881fc97da46cfaa00058731aa3e085897be5d223bec963
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279896593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56909c75d3581e4baf56c47a6f9e0da34b49385de990c11af9ae452fc4904e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:25:56 GMT
ADD file:8b523a4459cfcef333ade98289072a047a1f716565672fbba2b99fa0b7595bff in / 
# Tue, 25 Oct 2022 04:25:58 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:59:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 10:02:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 10:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f4447a9c12287b9486384fdda13ff5d2394a84fa81f944b1df82a6c65cacc889`  
		Last Modified: Tue, 25 Oct 2022 04:42:49 GMT  
		Size: 25.6 MB (25621218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc55b17f01e8499ec0532021df7869d72331bb1a3894bd93e3d212b1498e245`  
		Last Modified: Tue, 25 Oct 2022 10:37:50 GMT  
		Size: 5.9 MB (5936166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edee1f55b908e16aef18d4f96c19a0fa263eb259b672dc0e87b32f06e8d90562`  
		Last Modified: Tue, 25 Oct 2022 10:37:46 GMT  
		Size: 3.9 MB (3881286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0135afedddf116d7f21e74c1d02601f444604a7e6d608d4cb1245f6637cac4e`  
		Last Modified: Tue, 25 Oct 2022 10:40:10 GMT  
		Size: 42.8 MB (42832911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d2cbfeab48c839a5768440d0ce7acc79a0231a83e4a35b574f90142254ab1f`  
		Last Modified: Tue, 25 Oct 2022 10:47:14 GMT  
		Size: 201.6 MB (201625012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c77c3e8413804ee18565ed6fffe5e8a142091588980dd807b1308f724361cc02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228557086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ea76c6eabe8897a743624ab28ee73dd7666687bb9b600d6c8eaa39618025f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:49 GMT
ADD file:09ee4d9832dd5806eff549d8fa985f38ec5204ca80ef0fe5c5e614802cfa064b in / 
# Wed, 02 Nov 2022 18:42:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:06:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:06:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Nov 2022 19:07:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:10:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b34514224fe768d909b05dcd6ac27c44f4e63bef04be0728f33433ca9a7798ab`  
		Last Modified: Wed, 02 Nov 2022 18:44:17 GMT  
		Size: 26.0 MB (26022224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d108ef6171fca3acbbf9623da81c6b8d324702f4cc40d243121893096d6041`  
		Last Modified: Wed, 02 Nov 2022 19:14:38 GMT  
		Size: 6.5 MB (6474315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88c2b98692a0e66d0c62cd87407d4b34cdea4894b835f55ecad111c89a807a5`  
		Last Modified: Wed, 02 Nov 2022 19:14:38 GMT  
		Size: 3.6 MB (3624898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf023a124a1777c45ce37d17a90e27bcd8cacb72f7c53ea24f503335924324ce`  
		Last Modified: Wed, 02 Nov 2022 19:14:53 GMT  
		Size: 39.5 MB (39548814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707c85d4be6998504c5f89ac6899cef3b6c77a34c7ffe5a0700ee5ab6cba9164`  
		Last Modified: Wed, 02 Nov 2022 19:15:26 GMT  
		Size: 152.9 MB (152886835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
