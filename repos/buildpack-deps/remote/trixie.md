## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:8c41d5a375d0caac32a40fe3b4c94dd9c009b0813b799b83794c5eaece57a5a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:30b101f86871eca0a9a768eb6dbd75e12740454ae3d8078bf844c160ab1e5e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.6 MB (378581602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520ea41ca75a155a46f8767b069be43b4938f89065a5e3468c6d70b28e1140d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad446e7df19acd39290d995e6d78ccbfde171596237968a140518b183d94c04f`  
		Last Modified: Mon, 08 Sep 2025 22:39:48 GMT  
		Size: 235.9 MB (235911680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5602837cb0eb65076a3a7fe915f37db184a91df4b2dfcfc940e995a0d5506ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2e5f515cfb9d0fddc298c75c10e6601d9731aea91329c0c7392021a553a089`

```dockerfile
```

-	Layers:
	-	`sha256:0b2f9ea16dbffd25ebbbf502e7183cb00662001b90cad7e6ac1200656ae7dab5`  
		Last Modified: Tue, 09 Sep 2025 01:03:43 GMT  
		Size: 17.2 MB (17207047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9150a97148a8943bad12961e6cb8b10a9ecae26f2d412e39d3c30e7420b912`  
		Last Modified: Tue, 09 Sep 2025 01:03:44 GMT  
		Size: 10.5 KB (10505 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:39e4fce66f0cd14fda7b87b90b8fa10f0df148c93d0bd659dacf4452e325126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342374497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21665a0a845743a945737762c6fdc64f3606c7c85042a0882fcc748f93a22569`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49b34b9ef926ce7ed8f011fe61446ff5495accfded522a04a8414730759ac407`  
		Last Modified: Tue, 12 Aug 2025 20:49:02 GMT  
		Size: 47.4 MB (47442425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10345871b22cfbefdba6d9f2d575fe7ebd340d456d55037a519d266903c1f87a`  
		Last Modified: Wed, 13 Aug 2025 00:01:36 GMT  
		Size: 24.3 MB (24338768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa2b20bf2d33c358d141989badced2a336e24163718df277bd1fffd0bce46c`  
		Last Modified: Wed, 13 Aug 2025 14:14:52 GMT  
		Size: 65.3 MB (65319013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a918cc6f34461032d9e2cd34bd173bec69c69070075ea1707b4ab36b71c15fb`  
		Last Modified: Wed, 13 Aug 2025 15:07:16 GMT  
		Size: 205.3 MB (205274291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46bb61b39c451021225edaa012e0fb629c1ec87b70b2864c33adb06216edd1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d7a4d81fd7ba5b8d9c50eb04b0bd2181a78f7d45389675d49bb6457f80c6d2`

```dockerfile
```

-	Layers:
	-	`sha256:1c4f10b8181ef8b9fa3e082394da7d5a12c93f94c6eee71298e4082c0c9ab261`  
		Last Modified: Wed, 13 Aug 2025 13:20:46 GMT  
		Size: 17.0 MB (16963837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0378d0ef9c95c7ea25e98183efbe1b9944051d67a04a83d4879ed4923c3114`  
		Last Modified: Wed, 13 Aug 2025 13:20:47 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6a4ef012d9bf91c6741867f901594f420819f349183f2ec6c3f3c297d5298688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324885097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2423863634332d57b6032852c056d79c17a83b06f65592557dced13417b2a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec56b61521700d996402c22c24c12a3a452e3a426cc9001df0aa805a0dab6b8`  
		Last Modified: Wed, 13 Aug 2025 15:08:05 GMT  
		Size: 192.8 MB (192840920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5b89a7e50801f39f42a0788e89c6232074b49e2f68c36613a6b5811e929dd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16980199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6debdd353d9d31c744dad401040bfa6181ff3eb07aed2713cc4ec476bcb2ba3`

```dockerfile
```

-	Layers:
	-	`sha256:a4535b1650760bc4b37acc25926db19e677c16613b3ff3039597b67e117bf0e5`  
		Last Modified: Wed, 13 Aug 2025 13:21:00 GMT  
		Size: 17.0 MB (16969627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4e582377b3af54c9ef5c05f6697b0748ae7a491ea932830516f6273729eb`  
		Last Modified: Wed, 13 Aug 2025 13:21:01 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9fb71b1ecc0e7b0d1f9c9c970d4e3f46d470fb20dcd8946a1dda80f962069a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368304651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f96aa7091f3a7282cfa872103a97dd44d0ea8318da7b6b8d5d6c6b57269e03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd600967e6c49c98883d12d3ca7ba50395f75eb436373e95780141122745a6`  
		Last Modified: Tue, 09 Sep 2025 02:13:16 GMT  
		Size: 67.6 MB (67583121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739133f1214d773878370d419c1d4ee91d9b3c13d17ef30cff3d20122c9738c8`  
		Last Modified: Tue, 09 Sep 2025 03:12:17 GMT  
		Size: 226.1 MB (226062463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:762bcad5b4fabfd961b851c4b6790e13de08c9ed8222db62e66a1954023e2512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17301938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e243b6dafbbf62d11bb233aca4049fec157aba6821d814afa0eff62fc932081`

```dockerfile
```

-	Layers:
	-	`sha256:e0f5bda0efd7c5b0607b614b4cae6f42817b3a2a759f8faeaa6bbdeae6651cb8`  
		Last Modified: Tue, 09 Sep 2025 04:21:26 GMT  
		Size: 17.3 MB (17291341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd3164e768243b28aee575262f423261a8ff5de818a193058dad1dd45c40487`  
		Last Modified: Tue, 09 Sep 2025 04:21:27 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:263cff889f7c27e260ebd210633235faf7ec2281c0800062a9fb982d46288e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387374427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330868fbc847ee470ff298c4d71e2ace384583764fd3a063c34afd96b530a850`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e6ff4859ead75e29b179b0636a999dd68cde264f9c74ad8882d9d5dcfc9c7`  
		Last Modified: Mon, 08 Sep 2025 21:55:26 GMT  
		Size: 26.8 MB (26773510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4adf19bf3e6f542f3c00d3fc4bb83f2ec48ccc9675502c518d9eb368d0232a`  
		Last Modified: Mon, 08 Sep 2025 22:13:48 GMT  
		Size: 69.8 MB (69794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab2abde2bd81e0c03b25daf07e77ac4663600326c0ede534dc39e08354133a5`  
		Last Modified: Mon, 08 Sep 2025 22:40:39 GMT  
		Size: 240.0 MB (240011713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d73cb06c73dccd5f620707a09ed5f4cbf181075c90b754b3db357ed2382cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17187118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bac9a22e906d9b152733ba319ded70de3d12392ee3c3bc6abb88045a165782`

```dockerfile
```

-	Layers:
	-	`sha256:63f1894f8b2831d02a39aadcbd8be0691943faf48a35d27c153c3bfb4a90c821`  
		Last Modified: Tue, 09 Sep 2025 01:03:45 GMT  
		Size: 17.2 MB (17176640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3d0e401b4602ccb650858736a6f690ec6f1c609ef0eeb40741c3960b7eb31d`  
		Last Modified: Tue, 09 Sep 2025 01:03:46 GMT  
		Size: 10.5 KB (10478 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7fd938360b8b8d0326175dfcfaff4e6ff6a087c5b15b6f4d2b9c25c65f907960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 MB (384128145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3504f4c15993384108bbc314f3f5f2c870dc3d12aaaa9a5156f02ce4b17e7983`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e609a63b79cb97e868edf62a4c9454838befd7ede70ebc96840a505bc31e1518`  
		Last Modified: Thu, 14 Aug 2025 04:25:41 GMT  
		Size: 231.0 MB (231013234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74d7e10b0cbafd719b894959a30ab90be61d9ef8c5d7374631cf7ebe5eb362b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17197731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4372e167f805bef75cfd3d54387ec3abc0d1ef6fa711b6fb059e7519f4e413ca`

```dockerfile
```

-	Layers:
	-	`sha256:14ad6791a508f6453d974541c891d5c7d70e3aa45d8e5e752daa51b1b1e6d64e`  
		Last Modified: Thu, 14 Aug 2025 04:20:58 GMT  
		Size: 17.2 MB (17187188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9982cc94de60a04907eebaf5e2a5e318c041a424e567b8b0fc45e0b793346a`  
		Last Modified: Thu, 14 Aug 2025 04:20:59 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:04aba2354ce276198927ebccda70ad9bcf141b21db867abbc4a8cd0b657b4743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.2 MB (462151147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b8225ded12d18ec25ea995f2ee37150b370245c2c2c72984b2c866a9761169`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0b64daccd6b787f78c1a1622c08097763f53e2dee005bedbf3141bbaa8af2`  
		Last Modified: Sun, 17 Aug 2025 07:49:06 GMT  
		Size: 66.7 MB (66658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4724973c76be5e6f7d2c97f8e3851c856b0b35bb5a799d4ccd81e77b22ffe4`  
		Last Modified: Mon, 18 Aug 2025 12:29:05 GMT  
		Size: 322.8 MB (322777953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:14a213f7da5221cb9fe152b15bdcc79d216ee9165794719114a430b19210106b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17268320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a7ead16af5336f38e4896c0b4b2d6ef35df5a0931f8b66bc0afe0304437c8`

```dockerfile
```

-	Layers:
	-	`sha256:72e826cfdadcca901abd4c98a7799b7765a1d457fecdfd4c72b48b2250e31211`  
		Last Modified: Mon, 18 Aug 2025 10:21:19 GMT  
		Size: 17.3 MB (17257777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:316f85da9e4a688cc86af3f9472094ae4f1886977beb939cbbcebceb4f16793b`  
		Last Modified: Mon, 18 Aug 2025 10:21:20 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cc0ad7b86390634f6ffc93996fd9cb67821096981296c921fb39b38d7b634cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351145610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cb874e8654098b2b412ac70e1f35dcc0e3502b84b377bfbed508b1522b59df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0559cbb94826f8b1e5c377d0a644ba7cd24eee336fc5523a414d8ad448427fe2`  
		Last Modified: Wed, 13 Aug 2025 17:19:38 GMT  
		Size: 206.4 MB (206400871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f64b9fe42007fefa29b40597f6d3fdf61a1e923c04c5a5c980af50187e5766b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16989377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffde49d157d37cc1b82673856de81a5c60b621ddfefbe2cee8edeef296bc9b6`

```dockerfile
```

-	Layers:
	-	`sha256:b72735a04b12c8a946d924e6bb9a1874e7b16133a4a80595163127f39d0d0baf`  
		Last Modified: Wed, 13 Aug 2025 16:21:37 GMT  
		Size: 17.0 MB (16978872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487e1fdf2c1a286020326cd1976dd5adab466120d6025e7f647762706919da39`  
		Last Modified: Wed, 13 Aug 2025 16:21:38 GMT  
		Size: 10.5 KB (10505 bytes)  
		MIME: application/vnd.in-toto+json
