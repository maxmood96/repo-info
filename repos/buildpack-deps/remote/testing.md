## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:7ff9dc62f50ec2fcb157a959cf1888a4afd274045b92875eb702d0c64890fbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2d5e989857d1e1f64ace65ec7af0794b7f990c3fcea51a62110360c9781ffc58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396707025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e4884de179770a56b2f4f6d82a82db6e330cdc21307212134f537fcd47c9ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:40:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86533899ea4c6a05c0bc99be1cf97d8c7b1864649d1d7b07f04486b15f07cb0`  
		Last Modified: Tue, 19 Dec 2023 04:45:40 GMT  
		Size: 66.1 MB (66061532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee84ae1998d47ab8aff67d6563bd2a6e54efb95c3d90f97ef91f104b052d9eb2`  
		Last Modified: Tue, 19 Dec 2023 04:46:20 GMT  
		Size: 254.6 MB (254641404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d803c828fa78e4048b6dd9f0819767f330151ea595818e1febed9c5afd3cb1a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364689828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733f23a4295ce61add3f84746d870e37e455f2f81532ea3486e741341710334`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:30:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0751a1e8acd62fd190d7c3bec2800497b26033c33f78f5fb4ac87c59dc9eff`  
		Last Modified: Tue, 19 Dec 2023 05:36:11 GMT  
		Size: 228.9 MB (228855857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b64f50a42a58644b6a568f9783fff2e135fe8c2f7b283704e1f0fe2a78f9ff49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341102455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f528d7742ac4e37cc0d437bcb2f37ecfb2cfb9802296553b579d0928463012`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:10:03 GMT
ADD file:3a9b07d7d2dd3958b5dd3f5e10d02d2e2f612023edc0a993b72001585b39fffb in / 
# Tue, 19 Dec 2023 02:10:04 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:05:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fdfd0725abb7810a629f5d363de8fc6e2d9dcb7251dbd35de649c96745cd052`  
		Last Modified: Tue, 19 Dec 2023 02:16:07 GMT  
		Size: 45.1 MB (45080555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc6f8d845eb2d7a99ad733d60426b1890e2dae97e2c100045f2a994f37727dc`  
		Last Modified: Tue, 19 Dec 2023 08:10:31 GMT  
		Size: 24.1 MB (24059302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaf87f01b13e2c56d32f7922d2c5a19f02303d7e15d431e44ce223f7f3c2bc2`  
		Last Modified: Tue, 19 Dec 2023 08:10:51 GMT  
		Size: 61.2 MB (61195731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43266347f9d44094d8ece8162f6ad34da5982cadcefa5741f7f44d4df8d2eba2`  
		Last Modified: Tue, 19 Dec 2023 08:11:30 GMT  
		Size: 210.8 MB (210766867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb68cb18300df68a560fc268f70c78ca7c055d4b8cddec272bb844e177b2418d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382964950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f4c85dcef57c264951aaaa9a7eefd7ffa3daeb32b9bd17cac512192065788d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:55 GMT
ADD file:3a7cff48546e976afb3192375ccd816fa228a2a86ca359ad2d25968d89736a30 in / 
# Tue, 19 Dec 2023 01:42:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:41:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54db10be8b28565099ed8931d6e2048335ac2a2e8633f5ee9961d35950099935`  
		Last Modified: Tue, 19 Dec 2023 01:48:52 GMT  
		Size: 49.6 MB (49615103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3258514d2e2ba8de515d7376cc008e3df15536a3972bbc964930061817df14e1`  
		Last Modified: Tue, 19 Dec 2023 11:45:54 GMT  
		Size: 26.0 MB (25951112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f1ab7417116c7641a520689c7837277c5b5d78343f1e4e4a42effbae89c744`  
		Last Modified: Tue, 19 Dec 2023 11:46:10 GMT  
		Size: 66.2 MB (66172700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ebe0a39eeac98f80c2f1e2d2f0049d2a796beff951e570d79a775e3e220ac2`  
		Last Modified: Tue, 19 Dec 2023 11:46:41 GMT  
		Size: 241.2 MB (241226035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cbe2dbf67545dc5c97c3c6f5b728aaddf86e84287e90c82d23ed35bfcac6adcd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397358797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170a759d81adcc81daeeb7b7a13324c354ceaed76dcb35dd0f258b4e3ac3bbcf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:35:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cab3bcda927a6bdf058c09d2eb156aa0af0222312987068a8db4995e0e7b38`  
		Last Modified: Tue, 19 Dec 2023 03:42:10 GMT  
		Size: 67.8 MB (67818215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9a37e534304fa065f9b443c37df037032a614c5be60ac7a59f1ad9b9ba36f1`  
		Last Modified: Tue, 19 Dec 2023 03:43:07 GMT  
		Size: 251.6 MB (251576047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:842f4d700da50c22ae477353ba1b0a6836e0ff1692a5bfc39a228db5acabbc8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374865556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cee0e4b099eeae2ebb4584c658a143c4511d49e45ba21bea37ebc7921a2104`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:20:17 GMT
ADD file:8ea6310c27e7f62f29291d04a24b83af6da2d5e3faa1996293119c2feddc0c07 in / 
# Tue, 19 Dec 2023 02:20:23 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:14:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:22:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b33999eae7d9b8d6555148eda58da0cc5207bcf4c08ed630879dc0190791680f`  
		Last Modified: Tue, 19 Dec 2023 02:31:43 GMT  
		Size: 49.1 MB (49068400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbe2cdae3821f18626a3cba0479848ecb8d93b32bc3d454eb52e1fe702148fd`  
		Last Modified: Tue, 19 Dec 2023 03:29:12 GMT  
		Size: 27.0 MB (26971496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ea464afe86d2428926a7a730b73d688b456e6e44aabdb66f961eac77674ae6`  
		Last Modified: Thu, 04 Jan 2024 20:23:46 GMT  
		Size: 67.4 MB (67368157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14aa92e89997a25ae255a7dea9de70c1cd43f9d2a03c42b211e5c892fdc5552`  
		Last Modified: Thu, 04 Jan 2024 20:26:17 GMT  
		Size: 231.5 MB (231457503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b45bc504ee4fda550cb99b9bb73dc89e0f0326fd347493a93457e2364575265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 MB (406135677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ec76a98fe283c076d6398adcfb0665dd8a9cdec4a43ee1da1c11f0a9c6377`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:24:15 GMT
ADD file:0c76fa40c0d4d6eec23b49588ff6dbe4b5563f6db327a13831ab7eb6e3f30743 in / 
# Tue, 19 Dec 2023 01:24:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9aa21f27abca3b3157546abcfde68519068ba019777333f48885704721c81290`  
		Last Modified: Tue, 19 Dec 2023 01:30:10 GMT  
		Size: 53.5 MB (53476480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4bac2e5e84f15314991062e11b3bcdec79ce34bab827dc518eb86ed33d8593`  
		Last Modified: Tue, 19 Dec 2023 12:26:37 GMT  
		Size: 28.9 MB (28929833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e9e5a914f7e92834cc5f6c63a7bcf55219a7fde6114e91ad54a5cf55e99362`  
		Last Modified: Tue, 19 Dec 2023 12:26:57 GMT  
		Size: 71.6 MB (71599173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf858753babf0e4ab185c8a2da4d466a6b6231570bb5f2ce34c9ec6332d4b1`  
		Last Modified: Tue, 19 Dec 2023 12:27:44 GMT  
		Size: 252.1 MB (252130191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c2a878a7c03349c52aee0fc9b529075acaadac507951f38f5fb7b0fcba8c3259
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.0 MB (371014955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c3e030ea21d6eeed017a8fbcd2ac6cbb93f398baee7c459119c721bd4320b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:25 GMT
ADD file:3ce2a6c625c267468f6ecc7899fd855c1705b7efb767d466e8b5e859b1047897 in / 
# Thu, 11 Jan 2024 01:48:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:15:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:18:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c1c69c5e90f50e1791d192ea58f134dbc8ecc231a5b815d4c7ee99ef3a1ff7`  
		Last Modified: Thu, 11 Jan 2024 01:53:03 GMT  
		Size: 49.1 MB (49091863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3694e83d440b396cbb77938e6510f4437f21e56dc3bfaed630e6caab9214d`  
		Last Modified: Thu, 11 Jan 2024 02:23:52 GMT  
		Size: 27.2 MB (27199817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47161a7187326816c278e7d750ac894a70682803dc239b5d8c20d926e36e792`  
		Last Modified: Thu, 11 Jan 2024 02:24:08 GMT  
		Size: 67.1 MB (67130864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce18ce061b7b10504caa95c78ffefd4c54eba93d2b4f83ecf1e907ba6e3dd60`  
		Last Modified: Thu, 11 Jan 2024 02:24:43 GMT  
		Size: 227.6 MB (227592411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
