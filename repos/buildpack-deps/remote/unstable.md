## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:322fb18a5b6f4bc4da6929018b2211a15a951513479b183ba3bb2df48549091a
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
$ docker pull buildpack-deps@sha256:164f7551e499b2b453157efaaa3f7f5b86f396d194432b5118c3b99790d2e542
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345367181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e4e87350b66d0c7228d0f33683e168767ca1460e892d4c2c62c787b030e192`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:52 GMT
ADD file:643fde45a6d11f36b1178a022667e74288e58a263ac7999c7cb023cb3fcde3a8 in / 
# Tue, 06 Dec 2022 01:21:53 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:17:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:19:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8db6e5cd5802a750fd04af4eb64a857f779b9c2333d2d830a50d7b2983365c1`  
		Last Modified: Tue, 06 Dec 2022 01:26:42 GMT  
		Size: 50.3 MB (50309617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b904b10ee4925c81495d781c9278243be45e6e2feb4350d4e8780c3c15c9d65e`  
		Last Modified: Tue, 06 Dec 2022 02:23:48 GMT  
		Size: 9.0 MB (9019750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826135e5b952effdf73fc4ca5766716e2efde4728890f709a8e0629212bfb80f`  
		Last Modified: Tue, 06 Dec 2022 02:23:48 GMT  
		Size: 11.4 MB (11369325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1a31718aa1aa53871a059e3a80e9c5bd0d4a6f8fd55a8cc63db471e6014006`  
		Last Modified: Tue, 06 Dec 2022 02:24:05 GMT  
		Size: 61.0 MB (60970600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cceacad4f7faff0659c87a031e0b1c1b9fc1ebbcf84e2f793a48321cc4dc826`  
		Last Modified: Tue, 06 Dec 2022 02:24:42 GMT  
		Size: 213.7 MB (213697889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:499164c9d554391179f50ba31501009007929b2c5ec27d4bcf7e4c464250817b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.9 MB (315948763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c324f24a1bd31f9e4eff2befabd9bb5198ba5b8d5f4b3391f552c471d4c1fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:19 GMT
ADD file:7e649d148f5ac98acdfce2b45b373b5b22a9792e3d365d3f1dcb2414a59f4149 in / 
# Wed, 21 Dec 2022 01:49:20 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:22:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3175fea42c68213e6e72826c3ee7daa4a58070ce07ae526e91c30a8743d89be1`  
		Last Modified: Wed, 21 Dec 2022 01:54:28 GMT  
		Size: 49.3 MB (49270781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2f8a381ecb39f18e385e77a8e8d6e9d27b631c659084d0d9a3a82c5e9f9b47`  
		Last Modified: Wed, 21 Dec 2022 02:27:59 GMT  
		Size: 8.5 MB (8463955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681a42b466ccec4b7ac8c821ac8ac7d1787f7968ea77629bcfd8efa108d32f4a`  
		Last Modified: Wed, 21 Dec 2022 02:27:59 GMT  
		Size: 11.0 MB (11014376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf14e116100aa5dc86d38341ffec41bc259ac037aa38c189caa7b1d9f1d7f56`  
		Last Modified: Wed, 21 Dec 2022 02:28:21 GMT  
		Size: 58.4 MB (58378277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca7a3fdd294e0fa7a37c862441e1a9e14d11ec77a9ba69a413e16ab99554d02`  
		Last Modified: Wed, 21 Dec 2022 02:29:06 GMT  
		Size: 188.8 MB (188821374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e1e63fe7bc4a0e4d82e5850b14fdf78de367054f2288df259a33d9d1ee453fa3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301403178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe38e6fb2127b284ea531da4fbcc95e2da431b4b600661a228acd2b09d1cf532`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:31 GMT
ADD file:9f6e7ad60906ff390d6369133d129df5057cc1505edafd2cccc2eefa5265ddaf in / 
# Wed, 21 Dec 2022 01:59:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:31:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:31:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:32:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d12d04403dcef32bd0b6201954d02c0de421dabf04dd54d568898f376cb96c5`  
		Last Modified: Wed, 21 Dec 2022 02:07:07 GMT  
		Size: 47.1 MB (47080683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36680a9d2eba076180efb89a2b7a21233fc4e0a38e383b2c389f543e56a48be`  
		Last Modified: Wed, 21 Dec 2022 02:40:30 GMT  
		Size: 8.1 MB (8110360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edac00689713d5d2b7fdcc4f1c017ec260832d0c2a65021c7f013a4a71c9bdf0`  
		Last Modified: Wed, 21 Dec 2022 02:40:30 GMT  
		Size: 10.6 MB (10649074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb2e96f612174a7d5711371774c88238e9809c0d631f6a0e50ee1591e53bfc`  
		Last Modified: Wed, 21 Dec 2022 02:40:51 GMT  
		Size: 56.0 MB (56048613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743634afd864d242a2bd3c089012f456a2b5ef4dc1774ecf73eb0f088b989f35`  
		Last Modified: Wed, 21 Dec 2022 02:41:31 GMT  
		Size: 179.5 MB (179514448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0f4a0f12bc1458a49b5c7797c182376c69e9beaf6ef5da08b4b7ae791eab9592
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337764227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117a215c562155fb4546c0021983c5a3981df4a56aef76b3310313b93d85f957`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:22 GMT
ADD file:afdb0d23dc73b5f1a887a2dfc3fb8fc2ebf210e9ac6b5d6748cd89c77d9e436c in / 
# Wed, 21 Dec 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:09:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:09:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:10:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:951a6c4c03238810abf592f0f3beb641ea6b4153bfa55acf62944018b9ed669b`  
		Last Modified: Wed, 21 Dec 2022 01:44:40 GMT  
		Size: 50.3 MB (50335976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdda1c5e6e87491ced136c13ab5b4f5638649dbeff005a13d621df9a094822a1`  
		Last Modified: Wed, 21 Dec 2022 02:14:29 GMT  
		Size: 8.8 MB (8843497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae130f92dbc53edf856d24c52cbf32f0410d34ccacd94bac928422ef4f4fc7`  
		Last Modified: Wed, 21 Dec 2022 02:14:29 GMT  
		Size: 11.3 MB (11328912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c026988df51d7264167f40103dd5c01db4eb446f90f5f6787ce90289773298`  
		Last Modified: Wed, 21 Dec 2022 02:14:47 GMT  
		Size: 60.7 MB (60664891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29031604fd5a6df990bde16d9fe0ecd6be7a7eeb863ec7f3875215b031e4c0f1`  
		Last Modified: Wed, 21 Dec 2022 02:15:18 GMT  
		Size: 206.6 MB (206590951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:34bdfa9dd2ec9aa8eb6840d96725426fda35c299162155e81b968a1b0c177cfa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351289371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540b8b03df9a15478c1deb705b6028fa8d0885bd9a90615606e7551393376ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:20 GMT
ADD file:d73a77dc412cd093f533d8c6403c7a4a629d7a7d31b1ffc8555e0f7876d98ec3 in / 
# Wed, 21 Dec 2022 01:40:21 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 09:56:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:56:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 09:56:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:57:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5477ffb90e4da3fe8a2c9a63f402783b74fb55b190b59240e4d1d7e5b55a2da`  
		Last Modified: Wed, 21 Dec 2022 01:46:35 GMT  
		Size: 51.3 MB (51340127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17da88d33e2a230fdf9667832a8cc65fca073921763a6ecc2a858766d4f937d`  
		Last Modified: Wed, 21 Dec 2022 10:02:31 GMT  
		Size: 9.2 MB (9186105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6731e431ea7ae865d881e1efe5608caa34a7813792150546854d8a8462ced5ba`  
		Last Modified: Wed, 21 Dec 2022 10:02:32 GMT  
		Size: 11.6 MB (11565473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92098526686d85ac9d57db5247ad423ae9f730e32f823f543af5aa6acda0cd34`  
		Last Modified: Wed, 21 Dec 2022 10:02:51 GMT  
		Size: 62.7 MB (62693784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16972ce2d1d775407c0ca174164a43007e47ce6603d5585b691aec12eb2034a9`  
		Last Modified: Wed, 21 Dec 2022 10:03:26 GMT  
		Size: 216.5 MB (216503882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a72d8769a3bc75b491849c0298a639bf7f939ae7d08640a31a757d3ad7871f3b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325837639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11da1810d00b2cb35abbab49bd0fc9cefa40347b5887b2cd365571f3b41160cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:56:07 GMT
ADD file:f0c5ebbf2aa59cd4e0996c808ed4d378c47b86ca4c00f63fa5de02b4cb838334 in / 
# Tue, 06 Dec 2022 01:56:12 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:25:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 17:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:32:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfb5e33f7f324b83c5e49e84922c9f448eace01382dd0e6ac683debf1a61eb39`  
		Last Modified: Tue, 06 Dec 2022 02:04:23 GMT  
		Size: 50.3 MB (50319836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b834f7ef2a923258cac3647eea1dc30607526608cb7736365eb762f58302d`  
		Last Modified: Tue, 06 Dec 2022 17:39:24 GMT  
		Size: 8.4 MB (8384243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bab24553411999fc0ee1271fd159e73a742187f55b55da1666e8215102677`  
		Last Modified: Tue, 06 Dec 2022 17:39:25 GMT  
		Size: 11.1 MB (11118815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37e22a8513c4ccf09821ec9d4887f64f4be99e05b4a5b5385317c5fa9ffba1e`  
		Last Modified: Tue, 06 Dec 2022 17:40:17 GMT  
		Size: 62.1 MB (62073819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303080f947935f010889d2b63068ba7836a19366ed1f2f2a8bafe3ed6fc17282`  
		Last Modified: Tue, 06 Dec 2022 17:42:34 GMT  
		Size: 193.9 MB (193940926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:96cc824c738608c3cf2e82dce8a3b0ac27cbdc6197e9f482f099043213e570b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360602982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e43dd234d61dfa51a244cceeb5585b89cea95c9f29b29ece1696ec2405b892`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:58 GMT
ADD file:4af1feaa33ee2a3c1112b5ed0efbcccec637c4dc23a5af7d55343f6ab7005920 in / 
# Wed, 21 Dec 2022 01:18:01 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 04:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:58:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 04:59:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:01:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47dc200f753ddc67a9fec80382c7c2b6f164cb907748c309862373fa8d94c504`  
		Last Modified: Wed, 21 Dec 2022 01:23:50 GMT  
		Size: 54.3 MB (54332986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e0edfe8dd05f3e4610a7a82df7e8bb9b034431efe825b28230c1de8996756`  
		Last Modified: Wed, 21 Dec 2022 05:08:00 GMT  
		Size: 9.6 MB (9590429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8048f68261b2fdcd0cc93bbe51dd77df8e43b57c3da698cc1c679e192bf4360`  
		Last Modified: Wed, 21 Dec 2022 05:08:00 GMT  
		Size: 12.1 MB (12130299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b620fb2afe77eb55ca3e3b2572b191e4b091a398d986bc7b4e5242e9e7dd48`  
		Last Modified: Wed, 21 Dec 2022 05:08:30 GMT  
		Size: 66.3 MB (66306513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eae9313419424d5276914caac4ddd57e6b2463715d3132e6d6c0e0bb5fb0fa`  
		Last Modified: Wed, 21 Dec 2022 05:09:35 GMT  
		Size: 218.2 MB (218242755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3a887968fe43226ca614e3bdfba591197b3593e08bde65a9a38a179bf5715812
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359929860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0617997a465ac3f99d967a05d654c18e959edee32e325b2b1dc07db26768495`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:39:40 GMT
ADD file:cff1e1a432929527e9bb64bde53e2b614c941bd4631b7bd3634fdda8a7240455 in / 
# Wed, 05 Oct 2022 00:39:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:40:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc6da93595cf4d9d589de999765cc4f1efa5e0d8e23ca6dd8b73b18afdc8189`  
		Last Modified: Wed, 05 Oct 2022 00:57:59 GMT  
		Size: 48.9 MB (48857821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554ce58712f86101a4716baede25ee43c9c1fc550b39fb4b3e5fa1622fd3b00b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 8.4 MB (8388012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd132871253f925889ef836099addcf830644843a64a1529bddc510390846a9b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 10.8 MB (10750715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfc76b3f6f1ba447e697e6e2190cf70e757458cce81446b79426ae4cccdb03`  
		Last Modified: Wed, 05 Oct 2022 03:33:00 GMT  
		Size: 54.0 MB (54018661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e7099a4ad88bc20a780df4c500b9445dc2cb39e8ac84d70a11e8903e5b6448`  
		Last Modified: Wed, 05 Oct 2022 03:40:39 GMT  
		Size: 237.9 MB (237914651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1020daa28bd252923f31e6c81baa7be544634a88b4dd799c8358fdeb2281fcc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315609661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d87f5cb51d126c94b8400c2aee9083866d849c6eba1381a27a3196ec971a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:28 GMT
ADD file:880ff0ee3680abb7b9e72fb9457e71f7e35b2ef7a1d47d57ca68904588756f83 in / 
# Wed, 21 Dec 2022 01:43:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:36:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c9fbadd05736c9fdf511ecc5d2eec08182e6f9bb03d6f8f6e50bedf7a713181`  
		Last Modified: Wed, 21 Dec 2022 01:49:29 GMT  
		Size: 48.7 MB (48679509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058df70186424378c385e8a8dde6736d86be892623a861bc219d0d0bf7bbcdcd`  
		Last Modified: Wed, 21 Dec 2022 05:42:09 GMT  
		Size: 8.6 MB (8644714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ba6ecb7ed0072a0da77532fc6849229a054af60d61f10211a44454d4eb710c`  
		Last Modified: Wed, 21 Dec 2022 05:42:09 GMT  
		Size: 11.2 MB (11231271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7919d00635ff8b88b24be338278ef649b8b57436307979c87b00f4a665f9c8cd`  
		Last Modified: Wed, 21 Dec 2022 05:42:25 GMT  
		Size: 59.7 MB (59728904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd331962ca3258ab41a49dd2d5a5d182763930dcb96d2dc8b1e02de01fab2ab`  
		Last Modified: Wed, 21 Dec 2022 05:42:56 GMT  
		Size: 187.3 MB (187325263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
