## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:0658bee092d2e837c5020aa7effee407a2c7b3bbc59cf1da6235c482ce4382a7
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
$ docker pull buildpack-deps@sha256:17bc4bd22190703d8768aeaa3ca6bcd2210fc641746d2454585be08ce56549bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349646719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614f6de95aa626bece07ebe03b846284624db6354ec954386925ca06485d0083`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb3d107ad7b8f22e25af7c2ea21540943257d714d5f5258c8275e541fd460cc`  
		Last Modified: Sat, 30 Mar 2024 21:20:04 GMT  
		Size: 63.8 MB (63848526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8556d6df8b94862fc63dfac7c0bcbae4ab10302c1f9ef0b871b8fafd147bd6`  
		Last Modified: Sat, 30 Mar 2024 21:20:42 GMT  
		Size: 213.2 MB (213207955 bytes)  
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
$ docker pull buildpack-deps@sha256:8fdce59c69a1449570ad7e28d7d6a3c93d6d22fa193133eeb50a19328c2ba05f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378477580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1747b554c7d67544ddafb675e6be262cebdf69160ca27b8626bdee79cab5a26f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:39:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544cbfb4f7236143d102b4ef349f35d3d31527535f242406bbfd2d42dbfe60ee`  
		Last Modified: Sat, 30 Mar 2024 21:43:05 GMT  
		Size: 66.3 MB (66331165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c307077e7d76abcb4bd4d45c8ace8d03bf5ecdf42e3cc300d9004aa74bbf1a`  
		Last Modified: Sat, 30 Mar 2024 21:43:36 GMT  
		Size: 235.9 MB (235940025 bytes)  
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
$ docker pull buildpack-deps@sha256:b8c90681410c7a219fb7f7d04aa57e2cf52f01af353243fb0b0f43a1e8e4a827
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (420983437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2f4a3271f92c24c8642e98dae057607e7c994185921ee91f6a528279ae0b81`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:26:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259a8b8d1c2e3af16628db8608e828fa16ec2c3aadfd7660f4716db301738d6b`  
		Last Modified: Sat, 30 Mar 2024 21:28:40 GMT  
		Size: 65.6 MB (65606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0b2e0b74b3f4b89240082a552a105f36e18ee01936ae286a1f1b860dc7521`  
		Last Modified: Sat, 30 Mar 2024 21:33:41 GMT  
		Size: 280.9 MB (280894516 bytes)  
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
