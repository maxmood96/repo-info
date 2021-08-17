## `buildpack-deps:stretch`

```console
$ docker pull buildpack-deps@sha256:9845c5be4c04ab3749c808fae292b24479948ee9edead86aed4ab44ada98722f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7140662b65e0e50b57644a55d12cde26e955fa8697dc363f06643bfc8df1dfac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.2 MB (325207071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe35bd8b28ed0f3b5c033b305de8ff1f004be0241f69a4687617ce4d5fb5f03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 09:25:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83600c1b4583abb5830c6d4a039cbab9a102ac1a7b3b779854638a371bb7128f`  
		Last Modified: Tue, 17 Aug 2021 09:33:12 GMT  
		Size: 11.3 MB (11295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae15c65bfa0fdc9053dcb734e6c034f5394ea0481dee3277f6e3e9fa07702d0`  
		Last Modified: Tue, 17 Aug 2021 09:33:11 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c058edda50f20bd5b06380342e9d99f7138770d79e0b031565dd0c7707fce`  
		Last Modified: Tue, 17 Aug 2021 09:33:34 GMT  
		Size: 49.8 MB (49761551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cdaa0fd103b33659feffaac5fd7cc202fbf1d8061ae2bf6da5a4540db9aced`  
		Last Modified: Tue, 17 Aug 2021 09:34:21 GMT  
		Size: 214.4 MB (214427261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c5429a40f146bf912c705c832cbc25389f3d2161675a42ce9e472082875b03df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309139494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764861d75f807b284332aa3fa8c966915b39d39bee1b8d8f7254843d50630b01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 02:00:50 GMT
ADD file:77054e1fc1091d0e0800f856514f36121a7b447fd1e2df32e6c8ff77e6136c66 in / 
# Tue, 17 Aug 2021 02:00:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:30:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:30:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 09:31:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:34:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bfc6a97ccb61e1bee683ec639f55514bc40b09ef15dcd73c928632c03b3df06c`  
		Last Modified: Tue, 17 Aug 2021 02:18:40 GMT  
		Size: 44.1 MB (44091900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20f6698538a8926450e2bf8d1e9e1f5630637ea61c2b25c184a6a10a108b3e4`  
		Last Modified: Tue, 17 Aug 2021 09:46:08 GMT  
		Size: 10.4 MB (10350685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e83002ce3ccf92cb337a353e881e214497f7e55c7a28f556743242710dbd1a2`  
		Last Modified: Tue, 17 Aug 2021 09:46:04 GMT  
		Size: 4.2 MB (4161501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189296784b99bb4cb5b5de65a61b6597c48637dee4490557ff3e564713b772c3`  
		Last Modified: Tue, 17 Aug 2021 09:46:52 GMT  
		Size: 48.0 MB (47983610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec91ec6f66e8da219762222b74940c02cf181770578d198d2f2575e5efea404`  
		Last Modified: Tue, 17 Aug 2021 09:49:01 GMT  
		Size: 202.6 MB (202551798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c7cf9bafe33d73032d67e82c456979865d9d0286266e75dc286882d65295bc09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297164640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bef04d86703f9a5ed20d6deac43e41d488ea0c4c86722ad0acacb0a1326b2e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 02:06:56 GMT
ADD file:544c40297b94c3ecc6561cf7bfef1cdf9763a18ce5e24b6841a1b70d0516d41d in / 
# Thu, 22 Jul 2021 02:06:57 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:22:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:23:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:25:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3cc5e47308fe8ded537d7ffdcaba46fcdf803cfe9878bd9264754a50eaa128b`  
		Last Modified: Thu, 22 Jul 2021 02:20:37 GMT  
		Size: 42.1 MB (42120108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf69efd3b547fe4dc472fd34a54c466b82ce51b7f04957779206b5ea0ef9160`  
		Last Modified: Thu, 22 Jul 2021 04:41:23 GMT  
		Size: 10.0 MB (9950872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7430ae4c6b93ca669cc72566a38f952b74dece32c5897c46e51a5907bd5a0c`  
		Last Modified: Thu, 22 Jul 2021 04:41:20 GMT  
		Size: 3.9 MB (3921255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5849792410ce49abbe1ff9b523687c9a52997076c1137a38ade9efa2c1e2a2`  
		Last Modified: Thu, 22 Jul 2021 04:42:08 GMT  
		Size: 46.1 MB (46125851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fd43aabdd97259cc604cf1eb0eda35346af7a1b26df5e7ecd221e1a066c5b2`  
		Last Modified: Thu, 22 Jul 2021 04:44:06 GMT  
		Size: 195.0 MB (195046554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ae83af90d691f92f963003f326247d07f0c63572c001d5180e68382aab10d6e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (306982017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fc2be127f7f58a889012cda6a9554a463eb77fec3a18ca69c952ed841b0872`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:56:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 07:56:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:57:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e420ab67f91937cc8165f5fb2e94bdab905576eadca5515be250bc6212fe50`  
		Last Modified: Tue, 17 Aug 2021 08:04:49 GMT  
		Size: 10.2 MB (10215748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce4bbd3804fd1154090db6722050023d8242e910e02ed7d2c09b9795a9d5ac`  
		Last Modified: Tue, 17 Aug 2021 08:04:48 GMT  
		Size: 4.1 MB (4096582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef28464eb814f6aec9fd29bb296de85a00b19fbb82a37d054836d456c6c89e5`  
		Last Modified: Tue, 17 Aug 2021 08:05:09 GMT  
		Size: 47.7 MB (47737246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718fbc9c6e759c3ca24d0ddaf5a8ffef316cd17ec7a99f5d6d594acbc059b130`  
		Last Modified: Tue, 17 Aug 2021 08:05:49 GMT  
		Size: 201.8 MB (201754789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; 386

```console
$ docker pull buildpack-deps@sha256:730dd341c80f904d29a15532a89ac80632e9ec3ca37fb49b5a42598754088a9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.7 MB (332745158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd95a9c0c53c01589fa6e35930e9b20d5c53bddf47bf357d81da909585990bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:43:45 GMT
ADD file:e05a48da77b08cb5622f87152f4378e29fbb9bc65a76c762d45e488e30adb647 in / 
# Tue, 17 Aug 2021 01:43:46 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 02:04:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 02:04:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 02:05:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd774782ceed955e627fdc8415668afabdebb5525036f0dc871ec023eb317787`  
		Last Modified: Tue, 17 Aug 2021 01:54:38 GMT  
		Size: 46.1 MB (46097220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aca3d286261da95e058ae37c67e002a572b7dfc1dd7fe13d83060357489bfb`  
		Last Modified: Tue, 17 Aug 2021 02:13:06 GMT  
		Size: 11.4 MB (11353003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5827d22bbd8aeb7ef47c0fb18407f27411bd8008e1189b79f7c7c3dd1a6adfb7`  
		Last Modified: Tue, 17 Aug 2021 02:13:04 GMT  
		Size: 4.6 MB (4565010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f484f8f178f4bf3f3ec40912975a9e55159419f752b4683fcf11d9317be62c1e`  
		Last Modified: Tue, 17 Aug 2021 02:13:36 GMT  
		Size: 51.3 MB (51265260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686652807b46ef0616820485447143dc2d8fe496a532ae72c2cb0b508e67be60`  
		Last Modified: Tue, 17 Aug 2021 02:14:31 GMT  
		Size: 219.5 MB (219464665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
