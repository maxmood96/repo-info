## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:b8c926db830fb9b548801ec12e86c7d3d6f06565ddb60c4770e6cf16626fe45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f8742bdb36590ad0888e03ca9725bb7260d8bb7f18ca47fece4b47dd74bc666e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312660807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dd81107941066e9681738364f7e3b5ecab4880fa5626430b20fbab7be0a845`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:25:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:25:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:26:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6422bfa32650e77d346bbb40c6b2a0dc34c863e10cfb1a117e8da9796694cd`  
		Last Modified: Tue, 25 Oct 2022 09:48:47 GMT  
		Size: 7.9 MB (7858969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335cbfc794fe106b207828e6c9d76fb72aa4631aad91b744e23442082275b8af`  
		Last Modified: Tue, 25 Oct 2022 09:48:47 GMT  
		Size: 10.0 MB (10001487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a348ba61fbef6dec66be0354c013afc02f0bba15b891b9625ac45bb007e9726`  
		Last Modified: Tue, 25 Oct 2022 09:49:04 GMT  
		Size: 51.8 MB (51843777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ac0452e7a7ce5a9781502e1bca3360740aa17c776748eb301c26ca8f5b294a`  
		Last Modified: Tue, 25 Oct 2022 09:49:39 GMT  
		Size: 192.5 MB (192508832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:38017f4c7c526b133cb4b7648f3d01a7b785b3032cec78b0e191f8940f22dd8f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278480521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e75bb822f7cc1e2794f333638190aab16e0c75263b5fc74af6de9ca98d5593`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:44 GMT
ADD file:68e8c9a779cffc9968c1d577e6367eb14306b9cb1ef195c63c2def986afcec06 in / 
# Tue, 25 Oct 2022 03:14:45 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:37:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:37:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:38:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a96a0f5b8ad36dd704fa61a4d79f60b2467017919db6ccc83b23de2d450aa97c`  
		Last Modified: Tue, 25 Oct 2022 03:21:42 GMT  
		Size: 45.9 MB (45916231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd5ac5b158fe16c9f433d43a240f34a43c487c5068e15f63e4b8d39950d235`  
		Last Modified: Wed, 26 Oct 2022 05:12:02 GMT  
		Size: 7.1 MB (7147662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c96180c4ced7c4701fea5d141a40207e07023179440f5fae4f42b21f491bda`  
		Last Modified: Wed, 26 Oct 2022 05:12:03 GMT  
		Size: 9.3 MB (9348913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4ec861b1eb1e561a265ce55e567d76fca7afe8f12be70c3994efc67e7e578e`  
		Last Modified: Wed, 26 Oct 2022 05:12:24 GMT  
		Size: 47.4 MB (47377145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312a0015e4c0d2af580cce4ba48f5caf0086e8c1cd391412dd6d6ee023cc4d42`  
		Last Modified: Wed, 26 Oct 2022 05:13:05 GMT  
		Size: 168.7 MB (168690570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:51cfaa380ab00d30f7c45f7613bf756ce2fb2ad77bb954cf058b8f7ce8fe8dd0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302618701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60243db6cc1a69894f2a5ea22d7a5a59d6fa82fd7a440142dfeedb451df23e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:37:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:38:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:39:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35873fa6ec375a28180771e63a96f2039703f6658efa32da2e83a64f6919bf1e`  
		Last Modified: Tue, 15 Nov 2022 05:43:54 GMT  
		Size: 7.7 MB (7726432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07615c620859a5288e844fd58e708c735c884a4b600e9ea4bd3f26ca5744f723`  
		Last Modified: Tue, 15 Nov 2022 05:43:55 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02969cbb07458e1786c56d183fed53adf7ef70ff25d0fc5541b85e728573ba7`  
		Last Modified: Tue, 15 Nov 2022 05:44:10 GMT  
		Size: 52.2 MB (52172432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaf27b3e7c3de1fbc732142598fbdca11a8003aa63760f28f28c9044218b926`  
		Last Modified: Tue, 15 Nov 2022 05:44:35 GMT  
		Size: 183.5 MB (183482470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:986002256185ea6e031552f9961c582f79bc59cfd0480c91dc617e385c631089
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf287ecacbd32c06e7567a97fa798639352e1b8ebee00ba2d94c64cebeee1c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:47 GMT
ADD file:7e14d4afa5499129c959c5ae5dc270e2fa04659c2c9b0527094cda3494c02d0f in / 
# Tue, 25 Oct 2022 02:22:47 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:16:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:16:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76a731c42f665e7334a622f65117ef9389e97a878b7c74bb4a10dfe9cdb296c6`  
		Last Modified: Tue, 25 Oct 2022 02:28:50 GMT  
		Size: 51.2 MB (51207943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee1fc3722feabf994120ab8f7d4abab754206d1ca425b7274ce1db428f7a651`  
		Last Modified: Tue, 25 Oct 2022 05:28:54 GMT  
		Size: 8.0 MB (8025806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2019db6202a77d9f3c2e49a64c766b8b67d4290e0e66e1480fd8c576078914b2`  
		Last Modified: Tue, 25 Oct 2022 05:28:54 GMT  
		Size: 10.1 MB (10128021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79afff7d2fb8bbf10afd83b8f08278ed493a12e50a8262a18a1b3fc227667ec4`  
		Last Modified: Tue, 25 Oct 2022 05:29:13 GMT  
		Size: 53.4 MB (53442950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9206c74214dfb44ab3f4b75a12fcb6bf38c7e04c253e88ff3af265d2e33152f4`  
		Last Modified: Tue, 25 Oct 2022 05:29:47 GMT  
		Size: 199.0 MB (199039708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
