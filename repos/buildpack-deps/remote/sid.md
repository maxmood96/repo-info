## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:c23d2224ae4154277fa7851d3782560263dd2a2e976126ec4f6a99073c0c2495
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:60949139e0404aa4e8bfbc72a5f4026b4eefc2a9099ca8f8f5c125d1650f3925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334454470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af567b7e90c831565925eb290b259d59001da957c00379fe23e75b75e6a871a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:21c8f2db1ca60de292da0e982c4bd4b81bfe468b8d652fac5b9003ceedf12013`  
		Last Modified: Wed, 21 May 2025 22:28:04 GMT  
		Size: 49.3 MB (49250549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d79457730a0db09039cff8714fa8c41f073c5bed3529b5417fcd2b8736c7b`  
		Last Modified: Wed, 21 May 2025 23:20:43 GMT  
		Size: 25.6 MB (25585150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcbbec8ebb5599a6f3f7c58410495e59f3b554270ce0b5227dc68965286c92`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 68.0 MB (68019464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7711fab4f4cd78e37eb5166cfeb7e6fb24a203796a4d199054e65a9c5fa0a2`  
		Last Modified: Thu, 22 May 2025 00:12:55 GMT  
		Size: 191.6 MB (191599307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4db6756cbf50482faba9db27bbd3999b7f566da0fd71f580241c2510eb03b75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16049858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc28e67fc91f379b1d590df8190920f2e8bbff9407ea95cfbbd87bee40f8713a`

```dockerfile
```

-	Layers:
	-	`sha256:d65c99024ef76abc888a6f914255895aedebe20c062c8af8bdfb7f236a355f36`  
		Last Modified: Thu, 22 May 2025 00:12:52 GMT  
		Size: 16.0 MB (16039682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0015a70b41f6c592e48535c74ac6324b55201d696043dd425ebf1d44ac0ddea9`  
		Last Modified: Thu, 22 May 2025 00:12:51 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1aee4832dd6f72c3d8e53318ad37a2aa74b60f1b6f28c9be6b3779f8140426a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299499966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223b24367f49b9b9e7427a30472ec5f09856742f81324effd4bfa43fc4f7730c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:404fd683a770153140d6973002a75f89d6a436af748f330e29e1c3f0ca67e300`  
		Last Modified: Mon, 28 Apr 2025 21:08:23 GMT  
		Size: 47.4 MB (47437736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e0a1e0dfa2983e94d5e01ac25e7f9b86f8206e92fe7aac9b2c5f9a123c36af`  
		Last Modified: Tue, 29 Apr 2025 00:47:07 GMT  
		Size: 24.3 MB (24301061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245945a0a2cee7723642bd65373a025bca132437cca15092326e78c91ef6b8b3`  
		Last Modified: Tue, 29 Apr 2025 03:55:21 GMT  
		Size: 65.6 MB (65596414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a98d8a99c5fd3e1dd46a1d3b7fb5410a915c358f4eafefd7c9aa80e29f0a0ca`  
		Last Modified: Tue, 29 Apr 2025 06:24:47 GMT  
		Size: 162.2 MB (162164755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9378a41ad2ada44951892e9ffd008a0ddd4b155e2c1399058cd607b1f8d37b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15712879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44450294db86486cccb8e5a8c4685f530b6bb257d92c0a4dcea16a96c2b71bd`

```dockerfile
```

-	Layers:
	-	`sha256:016329ffc97e5f652eef1a4fd87111b6f348bc0ff402715c2bca95de1c3748e2`  
		Last Modified: Tue, 29 Apr 2025 06:24:43 GMT  
		Size: 15.7 MB (15702643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0910923779924839ce31ab19f7479449079922b2606ec48929b78e1ee7c53d9e`  
		Last Modified: Tue, 29 Apr 2025 06:24:42 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:233ba0bd1ea0e7cd4fe0c5f8d7fa2354bd0263b836940cd54540f12ec68e4166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282840700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcb8b0945ad1663d9f069d5e473ddc7773d09e4f0044766ad45e4247a2ce287`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4f09954038071c4b7538cdbfd367f3552df4666eacc240bbf717397e0b9c060`  
		Last Modified: Mon, 28 Apr 2025 21:17:18 GMT  
		Size: 45.7 MB (45690318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea9aa9d3149432dc9bb5c2fe207c68224ef45d2d9f918a0e4d2c3d72b6f2c6`  
		Last Modified: Tue, 29 Apr 2025 03:38:23 GMT  
		Size: 23.6 MB (23574679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafdbfe38e24dca5b7ad9f38f6e93d3d1bc4e6bb311befa9c69d791b516b739e`  
		Last Modified: Tue, 29 Apr 2025 13:25:06 GMT  
		Size: 63.0 MB (63010966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b3ed40494f63c60b8d406d9908c4a06189bd09517ce72b08f410ccd9184d7`  
		Last Modified: Tue, 29 Apr 2025 16:48:27 GMT  
		Size: 150.6 MB (150564737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3c1bbb55bb2d8905320267f2b4298545edebfabf4a6fa60b504e8a61c95a7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15712202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056f207ef57f67fb30ea94c6dd8fca2298f1d132d5c0c38a5a72c1cf4c6ebe12`

```dockerfile
```

-	Layers:
	-	`sha256:6be83947f53a4869844a281b7f3c1aba6eb21023df42a1936c72a9083e42082d`  
		Last Modified: Tue, 29 Apr 2025 16:48:24 GMT  
		Size: 15.7 MB (15701966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3debf9e021112001ab670447e2b293f7bebfb4baf46afa14a3f30f2bbc9f7cdb`  
		Last Modified: Tue, 29 Apr 2025 16:48:23 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5dcf9296b3268b89ce5ba2a2714b8690a5df0990fffa64cff9c91c62faab628b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324314588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d15f5445cdb09355271a9d6af29fa288643c957ff62fe489b192949d136575`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2f619c4109fcbcc024465075840b71159fc76526814180d90bfff14b20db08c`  
		Last Modified: Mon, 28 Apr 2025 21:21:54 GMT  
		Size: 49.6 MB (49618408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ba9361c22f0e29208e6629c0b8872ae776c0157ff0e94dd78175d7d69661ee`  
		Last Modified: Tue, 29 Apr 2025 01:47:44 GMT  
		Size: 25.0 MB (24957999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908dfd8b0d455e2c1c6f55953fed71aa4cf1e842409ba85abe5575ec744af67e`  
		Last Modified: Tue, 29 Apr 2025 18:38:37 GMT  
		Size: 67.9 MB (67856051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631743085b5a4d23061e6c4175bd37e2224cdaf4a681d93958d8fbe26210f313`  
		Last Modified: Wed, 30 Apr 2025 02:20:33 GMT  
		Size: 181.9 MB (181882130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8767fd5ec5ca6d777e729d0ecb3913659f69073dc85f84213e3f801e4a45a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16027080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13725d3eb952da999264abff239798299b51f915f1a416999bd95dce0083044e`

```dockerfile
```

-	Layers:
	-	`sha256:8450f7eb44718c47663738ed427c04f8479d4cd883e8c3b998b77d32f7ee08bc`  
		Last Modified: Wed, 30 Apr 2025 02:20:29 GMT  
		Size: 16.0 MB (16016824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0e32090bfa5644ed931b325f1db40c5d78908b699725b55fb313c5410c591f`  
		Last Modified: Wed, 30 Apr 2025 02:20:28 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9c97171eefd5a6945a5432c42cf3152a71c9bec4ce76ddded46173dc1c5f98f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342801333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a5e1c3b3b8063c9272e00e3e7b85f336bcd9a98218364f0b8ad9c61b4d0623`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c296d6dda96e0fb26dc4760b3366cec8a0723558334f5c902e1c373d0e43ab6`  
		Last Modified: Wed, 21 May 2025 22:28:10 GMT  
		Size: 50.8 MB (50760379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a77ccac61e5d039233fd2cf7db2ad5fed48827a001629e91bc009eff166aeb4`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 26.7 MB (26745468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61c02e4c2f4cf8b97da95199eb210e94faa26e3fbbf359e109faa57c15cbd38`  
		Last Modified: Wed, 21 May 2025 23:37:36 GMT  
		Size: 70.1 MB (70120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4e229f03fd37c6b9bc4e0d5c0e3e162856aa56d7e0ef3c3bc7e7ed3fbaa73b`  
		Last Modified: Thu, 22 May 2025 00:12:58 GMT  
		Size: 195.2 MB (195175285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c85c4b2f672f81a12e240ab03fff4093c42431024bd548bf44f9a917bf8ea09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16019715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdc51c3e7d7a551713160b551206dec2d1b7a8ca0c96cb2ffa4bad873d4cb00`

```dockerfile
```

-	Layers:
	-	`sha256:41ce78a1defbb11d46254a13d7fabd832d27e625189d6d34f4a61decd4cdacff`  
		Last Modified: Thu, 22 May 2025 00:12:54 GMT  
		Size: 16.0 MB (16009561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a00b2263ce7f65b59088280bedcad4a0dab7b825ebe342705273573641d15d1`  
		Last Modified: Thu, 22 May 2025 00:12:54 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:955e9f45d95462ddb7c68bf71f39d0bff0c8c7e5790095b9257eee8e8b98ea0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313741095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb3df745dd66b7661fcffa5592d8c4b3e331cdd6a54ebe47678c8c7517f4ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d206785716d2e915433eb85845aaf9607094981ed3c32854f9401982e23a7af`  
		Last Modified: Mon, 28 Apr 2025 21:11:40 GMT  
		Size: 49.5 MB (49535121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46b0656b2eaf48d740fb0cc28ea93ea835c76c41dc63d12f18a3fd227d3d57`  
		Last Modified: Tue, 29 Apr 2025 12:45:17 GMT  
		Size: 25.6 MB (25618095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b53c377a8e6571103378ce926b4efdaa12bf0271ca14fa02f969e6c3d97192`  
		Last Modified: Tue, 29 Apr 2025 21:19:44 GMT  
		Size: 67.0 MB (67015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac08213c25ed6d62c60f5a436de9d0f48ea9d0d7e695b46014601a8c1cef4f`  
		Last Modified: Wed, 30 Apr 2025 03:25:45 GMT  
		Size: 171.6 MB (171572244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a2da1f9d2506df2dc7d1751e20784b81b596a442c49d93e45fc2449b4ab0cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd6bb88afc48d8f737bce603e00b63f757ff62e6db40ec33f1567bf944a456b`

```dockerfile
```

-	Layers:
	-	`sha256:f1e9d048e1f22679328e61561f21ac97cae87cd2d5ec2959df95542afd470474`  
		Last Modified: Wed, 30 Apr 2025 03:25:29 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4b9ae7b17128e025ab97c2f2407d51d3bd4e81907ef672f92043ea742d907d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338716615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3ee1eae68ea0103bc3e8601ee20e3170c31f579cc31eabbe331b3c238fca0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d320c0b02fe20eeef6a5432aed2b294506f621139378d9f899d155d81d1080d`  
		Last Modified: Mon, 28 Apr 2025 21:22:39 GMT  
		Size: 53.1 MB (53078100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e713da9ea3255a6f791030cf59cd9bdead64cd96fffafbed2a4a6fe1aaeb2b4`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 27.0 MB (26960240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cab10ca498aa4aa931178447c0fd221d2105fe390900e832573ae0d70bd2a58`  
		Last Modified: Tue, 29 Apr 2025 04:37:55 GMT  
		Size: 73.4 MB (73356141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a860ec664ef616cc952e2b5c636fffadbace1cd95b6444e62cf94fe841533cd`  
		Last Modified: Tue, 29 Apr 2025 08:03:07 GMT  
		Size: 185.3 MB (185322134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f332ac565e9b6113d167ca9b29bec04b1b70f0f3dd2c400471973f077b09982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15933540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a666fd34c44726ace39f4e0ab0ca49e497a5ababfd74d3ba2309978b65967efe`

```dockerfile
```

-	Layers:
	-	`sha256:3f8442a54bf3f155c69d050c54e989cd7bcd4bf60b7e69234be5a7b932e5d3e5`  
		Last Modified: Tue, 29 Apr 2025 08:02:58 GMT  
		Size: 15.9 MB (15923332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a271fb50c2e9053236f60ac8a7865c20df9e08ef421c69a7c540ce5097d24a46`  
		Last Modified: Tue, 29 Apr 2025 08:02:55 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0d83223e3f53c52e666f313ba3a00fe274d50b62d9378f76d5d34f87998c08e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 MB (408389960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ec1fbe7245b75d6577550b9de8fea50b78e4ed042956475499949e89e6743`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70274c6f176412a652733a045be62228bfceb31afa5c428bc73eb440514be7e5`  
		Last Modified: Wed, 21 May 2025 22:29:51 GMT  
		Size: 47.7 MB (47737557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db4d1c372b0a8bcc5558ebc33a0807a079cce1bf7f64840912ce33adbe79d6f`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 24.9 MB (24915395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d77ca161501cc8afd738216058d54ab2ad4f404972c41e87bffedc3f8f0766`  
		Last Modified: Thu, 22 May 2025 01:09:16 GMT  
		Size: 66.9 MB (66891223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5afbeb1d7adfdf8c5da2c61d9a3ddddc1979f60739963d3d305e86b3f0f68d0`  
		Last Modified: Thu, 22 May 2025 02:29:16 GMT  
		Size: 268.8 MB (268845785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8449c958b0c1612b661417a4ff2f6dcd03a4dda71c56c944c2f3c4f22e72a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16105694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019ecf8f33e9773567d6e5b57cb867ebad6c897eb1c91ad141ead96fbb51cbc`

```dockerfile
```

-	Layers:
	-	`sha256:27a755c73678df61e7b03ac3b8599ad8a78bf7e837d462ab72673506d2fd9a57`  
		Last Modified: Thu, 22 May 2025 02:28:41 GMT  
		Size: 16.1 MB (16095486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af7578894e3d71d395e9492e0d1ec744692d25f681b329aa2dda5ad518cc77f`  
		Last Modified: Thu, 22 May 2025 02:28:39 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a2629be836fc3c96297ed23a64679ccd1c8484b6ae3435aaf946f2e731ca5bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306265541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd4a45b9db5186142efb38de3d42c4c5591c516bf9ddffbd3665d56b42d7425`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8157e1045a0b1a8c8f6ab28a26ace718f29668344110893144c8a16214d7a54c`  
		Last Modified: Mon, 28 Apr 2025 21:08:48 GMT  
		Size: 49.3 MB (49321224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ff5701e764e061146831a7cbe6697f1a1451a6db3d328a14bf9b0b7aedcd77`  
		Last Modified: Tue, 29 Apr 2025 00:01:55 GMT  
		Size: 26.8 MB (26765142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44ff1263d784021acfea0dd01784c46b994ae5ce4e21a5a296ca7feda4ed5e7`  
		Last Modified: Tue, 29 Apr 2025 02:59:42 GMT  
		Size: 68.7 MB (68657417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6b42a536dbcfb0ceabbdb006f8136059da06bae9772c1c63b72a3410fd3c8`  
		Last Modified: Tue, 29 Apr 2025 05:35:48 GMT  
		Size: 161.5 MB (161521758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:845947c0544d4e6e24bf4aa7e31b0e05234d642f7f49e15276aa483b5e6eff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15708432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89a5b27f201a7e0ca71fa0f42269e53e5f4f87595b2321a9700261e114da6f0`

```dockerfile
```

-	Layers:
	-	`sha256:214b7fe0f6cbf2f13b9ed44bb9cfe9e66cf1697884ea483fa30f3edbf4e8aa5d`  
		Last Modified: Tue, 29 Apr 2025 05:35:45 GMT  
		Size: 15.7 MB (15698256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8147aa884f114bec50d740f5c027c1dd4c6d1ed1c5af0001d31ab8187659d85`  
		Last Modified: Tue, 29 Apr 2025 05:35:45 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
