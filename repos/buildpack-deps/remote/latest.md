## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:989305d52eb5be7fd40f981da484f543106f0ec3b617768a09a55904028f2a5f
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

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3c52d2a6abfc14e39e9b15721269a151f5d457ffce2480bb49c69d96aebd4625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378717115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7766cd4750357a9c7e1e0c2352cbf36181cedd1e61c33a29f6129310600ab003`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:39:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793e3c6bce826c77a6bfec52e3e42691937f0e5701d8efa06d32850314d3f30`  
		Last Modified: Tue, 24 Feb 2026 20:40:19 GMT  
		Size: 236.0 MB (236030458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af317cbf97c3ad429f67acc373cdc5ea6a693606cf8b4952d6d3c57a8229722b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17218972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91164895b54fdac641485c33d85c8503f25a42a2e8af349bdcc1b9b78515c2c4`

```dockerfile
```

-	Layers:
	-	`sha256:99325ae869ee579ba17ea5c457506ec7f5f68760e4aa49f5351d7ebeb310c238`  
		Last Modified: Tue, 24 Feb 2026 20:40:14 GMT  
		Size: 17.2 MB (17208510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e031324271de6369c411645655a7f15122c40cec1d60d70cf2c261d5a300fa`  
		Last Modified: Tue, 24 Feb 2026 20:40:13 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cd198b541fded26c798486392e92b8aad5e83257f8f4377a95e74493aa34f501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342860771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4863b00d5603a38e25a42a4b56fe009f3322ec4526b6c13887f72ff90b1a3845`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:18:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afe525ee94a6eec8f0285b6d37bd019b53a0d3e972edf130127870dbcc171e`  
		Last Modified: Tue, 03 Feb 2026 03:26:40 GMT  
		Size: 24.4 MB (24355517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648cbf60fd3bc74c2c5bd50ba637a7b59518c4e57992aeed5e381e96d894fe6e`  
		Last Modified: Tue, 03 Feb 2026 05:17:31 GMT  
		Size: 65.3 MB (65318442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa81d14f2f4b5520f7fd704ffec92d5671ccc4f12e6d6ac5b8e88424ba2bb47f`  
		Last Modified: Tue, 03 Feb 2026 06:18:47 GMT  
		Size: 205.7 MB (205732815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13a71c7c0e24481bebc0d88a01fa912d7f8af0cd1ffa5c896df1e81a6c52fb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16981242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ba42b8261b4d60b7d161c37ca8d567f853f02d78a116b9f53a6f03f67b6109`

```dockerfile
```

-	Layers:
	-	`sha256:3196b6163225bea51a19d5df06fe743d5ed9cac3713fbe284bcf172cbb5e164b`  
		Last Modified: Tue, 03 Feb 2026 06:18:42 GMT  
		Size: 17.0 MB (16970708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d0b35bdd083390cf0607e137198a9e51e207e3fc265feecdb0a3dfce7241ee`  
		Last Modified: Tue, 03 Feb 2026 06:18:41 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0870b01a23eabe46488f142828678b08cdcc366f74eaf2cc1ba8e3dd631a3762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325374961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a448b2fc467c364040aa77794d6d34694abb59b08fa62ccced2ad373346c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:21:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e712004ad7e72ac7b512e7e067d08c1f627b7b81a230302cbad4864b08acbdff`  
		Last Modified: Tue, 03 Feb 2026 01:14:45 GMT  
		Size: 45.7 MB (45724966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74387350d2cb71494f8cd51684a1223fa4d67c2770958430649aa3d99f0d84`  
		Last Modified: Tue, 03 Feb 2026 03:32:37 GMT  
		Size: 23.6 MB (23628323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eaf2b8f43157ee85fb0c9ace18005d09181f51842f1543a4a0e4d1072f633e`  
		Last Modified: Tue, 03 Feb 2026 05:01:35 GMT  
		Size: 62.7 MB (62713563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c5d525e14902ad210e5a6126a0f6db1a0db5f1566825247283b80dd0ba7089`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 193.3 MB (193308109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89460a0bc8f661ec54393db772417832ac716bdc5e19d4fb95d4907bc739bfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e47b5639b06fca9ae0f4cd5b40565079dd8c5b4509042e8be204556238bb7e`

```dockerfile
```

-	Layers:
	-	`sha256:46fff3d7e8f0f2c339faf1c7d78ee131c1412facf8465248e3e2704311b6b021`  
		Last Modified: Tue, 03 Feb 2026 05:22:28 GMT  
		Size: 17.0 MB (16976498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f2c485174356b0cef6b4dc11661dbd8f08a44e17e584f86784c4d95166cea9`  
		Last Modified: Tue, 03 Feb 2026 05:22:27 GMT  
		Size: 10.5 KB (10533 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4fbcfe768e7c5fa47a536208b39e0c87b9e2e892910f313326285352519b3141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368413375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ad4fde872a99df77f8630957e2db7d04eede2e7a0d317a0e2f83191e75783b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:22:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642b703f20ff3b5542fbad2e6a1427564db5472e2cdb9317bae6a64ac490e2e2`  
		Last Modified: Tue, 03 Feb 2026 04:23:14 GMT  
		Size: 226.1 MB (226145665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:19d90cd9f5c87bdbe8c9acc6627cb29907aed62f90aee8e927f7dd5e07b3ff79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17303358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8c1b955fc25a549697c5205a815d69dab4598c891f045948d935105bc21282`

```dockerfile
```

-	Layers:
	-	`sha256:067bc3177565d08533130d9e21740aacef49e2b6c9ffe1d1bb2be66fc68c0b79`  
		Last Modified: Tue, 03 Feb 2026 04:23:10 GMT  
		Size: 17.3 MB (17292804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5544de1480f9baafaaa8fd95e7ba755f6c67c4ac902fc80eee8fcd8ae9d7497c`  
		Last Modified: Tue, 03 Feb 2026 04:23:09 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a58dcb5c73545180352c6fbf12b886d401a9e48559dc244f163c2aa8818c493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387506796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c145f9d4d1c9f39eb33a3f799944b7687d0599b2c1d9d4290d792a7b668188d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:19:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5feef17113a2aa83c39ec2ba574788a1b821bc584f7b08f61d771fffd3746a`  
		Last Modified: Tue, 24 Feb 2026 20:19:59 GMT  
		Size: 240.1 MB (240127017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55ee0f3a56b679ac91e999bede70160b21b97e8066bb3a3df3859f20a8cecb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17188537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b246ab1d442b8ae4ffd41af1c59aaee73c9b15d415e08a347fb348fd3a3028`

```dockerfile
```

-	Layers:
	-	`sha256:a8d7697e6956995500c7c34776792c7b9fb54fc22b7c8de620782fbaeaef6cca`  
		Last Modified: Tue, 24 Feb 2026 20:19:53 GMT  
		Size: 17.2 MB (17178102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e69fe29800418d4038e3077852b9147ae657ce9c9c0cdb362f8a08a065e884c`  
		Last Modified: Tue, 24 Feb 2026 20:19:52 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:32708b8aeeda716f7d947bc6ddd256b98c07fe9bcbf1e2421b687e03da15fde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384275064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27cd8cc2d656a994ad3bccc55d302ea5429d22df6f19536c53185de179c29472`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 12:44:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bdc2ae5f94587ddf291ce56c3dd3c244bdeaf3ba39bf6598fe7a02816ade7e`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 27.0 MB (26998144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee79ae595ce83805d9060f1c610385dfe6280391251ea73a1f48c7cf8bcb3f09`  
		Last Modified: Tue, 03 Feb 2026 10:38:14 GMT  
		Size: 73.0 MB (73032214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7011848dd7a5865dc436775ea09207344e8392221f2687f313bf37e160ebf0f`  
		Last Modified: Tue, 03 Feb 2026 12:45:50 GMT  
		Size: 231.1 MB (231132591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fe4b60e394f3618e7362186ad74dbf57a20f7745b618d326d99d87e7d0b7305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17204561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf74ce93c51a53c6f1f567f6130325f901a52a6ec388892329e962c57f02bd49`

```dockerfile
```

-	Layers:
	-	`sha256:02ead10396132ccdd05ab6ace73ed70dd8e2b058a7ff564e3b57039c267f59c7`  
		Last Modified: Tue, 03 Feb 2026 12:45:45 GMT  
		Size: 17.2 MB (17194061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482403859159d56032ca97d8425ce99798399984eb86c497bc0a2ce22d465dd8`  
		Last Modified: Tue, 03 Feb 2026 12:45:44 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9797b95e7a8024e449483644bae75a9bbd5d7091549703e44b5800e705d990d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462311043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17b11e24b3c12f1036985b3f32b4864816154db90622b524b809e80cae72cc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Feb 2026 23:50:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e689506e8938c3b552c90ad33fbba57defdbbcda283a92391186d21213ea281`  
		Last Modified: Thu, 05 Feb 2026 03:20:07 GMT  
		Size: 25.0 MB (24953161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518328709aef2ec161ee90f4be9eea82346936a41f7fadae6c748b8ca89b81be`  
		Last Modified: Fri, 06 Feb 2026 08:00:06 GMT  
		Size: 66.7 MB (66660429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dd222d089e5ec8525740a9773119127deb4445670cb55d9cfe85879ac17769`  
		Last Modified: Sun, 08 Feb 2026 00:05:56 GMT  
		Size: 322.9 MB (322920690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7577b747f134b7214bd84d83491fceb9642936d0b205180f15438ce17e720e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17275150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2e017b5634fd7dc8d0156d67ebb66a9a722a21a9596506832de14a192a7524`

```dockerfile
```

-	Layers:
	-	`sha256:4635ecb9cafc32287c5227aae8f43c49e3dbc32c7ed54766104adf7c3108dcaa`  
		Last Modified: Sun, 08 Feb 2026 00:05:11 GMT  
		Size: 17.3 MB (17264650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40058a65de2e659032b25c9f7bbd2b60dab483d6d45430dc7e6dd8bc0c1e9ad7`  
		Last Modified: Sun, 08 Feb 2026 00:05:06 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:90dd44caddbbce9d4f3f940d2300a52fb2e82ed51a8c67152562d5aa95f21127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351304847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f38f55b26943f94de47a6e2fcdc2af7dc49ea4ce80a2600821d6d823c3b9cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:14:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3c6a3ae754d274216ffbec3754da469ace4e7c5b6e8e123969f0516b4a968`  
		Last Modified: Tue, 03 Feb 2026 05:29:44 GMT  
		Size: 68.6 MB (68623115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef461bcc2a855bcca63ca1d51d438b861a0e2b73096c42b9bb7654c815665d8`  
		Last Modified: Tue, 03 Feb 2026 06:15:17 GMT  
		Size: 206.5 MB (206532637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c14a9965ac0f326069883337a470b10ad1cb89dfa944ab605316aa54778a04ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16996205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c3d7040be089ea8ca7b7011b9e4dcec205108d6d2a7f1fdb3f6e0d0d16f650`

```dockerfile
```

-	Layers:
	-	`sha256:99f171d42b622ac8010a76410822d19147bf79dceb2146adb2c77047ac78e0c6`  
		Last Modified: Tue, 03 Feb 2026 06:15:14 GMT  
		Size: 17.0 MB (16985743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded6dddd26068acbd6362f8a09be94a7d18dcd3201791e22eaf94eda5a718303`  
		Last Modified: Tue, 03 Feb 2026 06:15:14 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json
