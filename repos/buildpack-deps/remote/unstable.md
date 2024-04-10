## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:5ddc94db4dfcc2492d2b32940e31de5dea26bac869cb441b80ce11444431ee26
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
$ docker pull buildpack-deps@sha256:57ac383c326ff712bab6fd9b199d44510599a4e0281a3aaca37b8586d45a2223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.0 MB (387988231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43d2453de4fe2fb28496f33f2180811f598511875812a4066bea677fb343dd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:39:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da143e0f6d9787b0c89d6405a787ded9de6dcb65f3b9717f82da42f10ff997b6`  
		Last Modified: Sat, 30 Mar 2024 21:42:57 GMT  
		Size: 66.1 MB (66121672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c86b463be435223351150e682274c024736e2d18e8692edb2df9fdbbc0c419`  
		Last Modified: Sat, 30 Mar 2024 21:43:36 GMT  
		Size: 245.3 MB (245265582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:48fb4f0ca521b5a52c782f780e15840c8f4ad02e69a4e7c5ee1a5f739d2ea391
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360956786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f248e4a461676a68a8adffe7498c8578602961e0b730820838d17c6ad823d3fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:50:32 GMT
ADD file:4a9afbefe640815ceed7c04b5539d7c65f79afb1c50420641fb90ea84d9456ee in / 
# Wed, 10 Apr 2024 00:50:33 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:51:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:435c81b262aa45b615a98b5b08f6124900f0a2f8c1b016424864ba2f1ed5bea0`  
		Last Modified: Wed, 10 Apr 2024 00:56:32 GMT  
		Size: 48.9 MB (48901894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1396417efc6e373a240285f028c909e31f5fb9efd13378c97dd450e23ed90a97`  
		Last Modified: Wed, 10 Apr 2024 04:57:34 GMT  
		Size: 24.0 MB (24026275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76004e4bc491beba63b8855446407f9a2d7d9e8296c8b5bc053170acc6c366d3`  
		Last Modified: Wed, 10 Apr 2024 04:57:55 GMT  
		Size: 66.2 MB (66197915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e1b193533db9a069e7ae250e0775cf84487ec8262bcbb88a77329463085787`  
		Last Modified: Wed, 10 Apr 2024 04:58:37 GMT  
		Size: 221.8 MB (221830702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:871e0f29584780024f2204c980284b9c9391fec747286a83190d491d200a6814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332812461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee2aec038450d0cf24a4e37e4f23eda53bb149657b4ce73450749cff557bbe8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba4b082de66bbca9897c8dba7f31512bba321ddd2a661347d670d910b4ef36`  
		Last Modified: Sat, 30 Mar 2024 21:30:50 GMT  
		Size: 61.3 MB (61251721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9506c1ec3f4d514c50744f383e5d6be73cb1ec6ad9ff611f2f6c6044f529c896`  
		Last Modified: Sat, 30 Mar 2024 21:31:25 GMT  
		Size: 202.1 MB (202137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2210f307f8743f3ff1afcc23c9c646c581c66a65c9460a15f0a842b6cbc88769
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.3 MB (392324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6cf9cc1a2347a5b5de6e5aef9270141af95fb1d8d41cffc39b1a6adb365828`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:28:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5adedb09bcdae19c9c078aeaa62769929c3099af358e94efbac1473c079342b`  
		Last Modified: Wed, 10 Apr 2024 04:34:38 GMT  
		Size: 24.9 MB (24946126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a0d5b61d3a348879655c04f5c1126df0827ea0ca894a127660c330ef8602e`  
		Last Modified: Wed, 10 Apr 2024 04:34:54 GMT  
		Size: 68.7 MB (68702497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64f3917d1c535fa410055152988df006865c9d281e95cc51412df61ddd63191`  
		Last Modified: Wed, 10 Apr 2024 04:35:26 GMT  
		Size: 246.5 MB (246538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:54905ffedef969cc2e213a1e9a0fada1fc515acd5d1f63592aaf3178675e51bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387860877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fdfccb3460ac7002fa33cef8001a4588dbfc8aa65b902e39c6fb38fd8f1ecb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a15da4ef836ff60f9c28ef8b15ef8794d788a67c0a3d58b61d51a0e65213a7`  
		Last Modified: Sat, 30 Mar 2024 21:21:45 GMT  
		Size: 67.9 MB (67876237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51302bc05c4c173523b513edf1b3957871cd4387ae1b1a565c5bd4a3eddb7c6c`  
		Last Modified: Sat, 30 Mar 2024 21:22:41 GMT  
		Size: 241.4 MB (241417390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b5224f59c01c64b248e9f48214432ae69669ab3e3bbe2f36a4412b60b58e4fdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357495125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3615639b43b8508a560b974f0f2c8153011ac54069af729c882ebd1149beda34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec5d517bc6924cab27f5df1f01979046acdf9cdb844cd5281549ae70cffd261`  
		Last Modified: Sat, 30 Mar 2024 21:49:28 GMT  
		Size: 216.2 MB (216190767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ec624754a8b69473cb9b81413a4b282e6cb28ba8f672f0e5a99247b21d660ebd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401680790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb5830486e828fd2cec3b7fe5910b5925f3d26950aa5db6ee446be40af0f264`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95220faf903de5c246bc60d7f00054712c075484056449785d59c657e22436e`  
		Last Modified: Sat, 30 Mar 2024 21:45:39 GMT  
		Size: 71.7 MB (71689301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d202211364551a66c5bdc24a551df53c88b1d009232162339febb791ddf65fb7`  
		Last Modified: Sat, 30 Mar 2024 21:46:26 GMT  
		Size: 247.3 MB (247336595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1c9ddd9530a45d20762adb57ec2e4a54811657e63ea191369953df8b7928cf0d
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428490682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07901e48486434c12164a569efa963478849a6a283fe7cd212d8ec5c0b457a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 01:32:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 01:39:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8bfd6a26c3a37b6a00ea3d238fb8eed745384d2bb98efaff22428174a68f6a1`  
		Last Modified: Wed, 10 Apr 2024 01:11:44 GMT  
		Size: 49.9 MB (49941022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a180df00bec725b09dac77cce3dc37d1d711ae817d8b4a36f2aa34d8d552ed`  
		Last Modified: Wed, 10 Apr 2024 01:39:42 GMT  
		Size: 24.9 MB (24904024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce99732b9cfa4521c0ab9070c5af6f235f8b3d7977ca84c4ec174dba2588aa`  
		Last Modified: Wed, 10 Apr 2024 01:40:47 GMT  
		Size: 68.0 MB (67976903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee47bc0f29c27ad588a2d49b024ed8a5415e1d7952943fa241190b9956657a2f`  
		Last Modified: Wed, 10 Apr 2024 01:45:48 GMT  
		Size: 285.7 MB (285668733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4bb0ce013670aae1801c1a36a4458da7b41a079951d7d46f758813926a26f386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369323131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92206efd704f5b1ef33db0289e2f80885e1e5e85e0ce41ca5c64eb7acc42547`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:45:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8b2bab401823952dea39f0a278dd656c849280f02e7b6f21ca4deddc0219d`  
		Last Modified: Sun, 31 Mar 2024 00:08:23 GMT  
		Size: 67.4 MB (67423448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1739ba0e83442ddf7c0d49fb3fe672de89ffe6650ed119a9a2c0737076f8c316`  
		Last Modified: Sun, 31 Mar 2024 00:08:56 GMT  
		Size: 224.7 MB (224700849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
