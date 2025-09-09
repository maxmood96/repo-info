## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:9d254bf0180e86043f911a6344719e5ce2a04ce62f0d243d86336b7fbb25c32e
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
$ docker pull buildpack-deps@sha256:ee7ec0c3d2ba200fd29b2971e8be0a82cb1d51e80be120f36b220316ca2c0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.8 MB (750782306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bb8a7470be5b7406182730ed388f50740fa2dc5bbd0696b6bfda218a46425b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ef32ff63c929905defc6f655e25216327571899c86b682cf8814eb2c3a0a3`  
		Last Modified: Mon, 08 Sep 2025 21:55:00 GMT  
		Size: 25.8 MB (25793066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb01fb26197afce850c60aaec10a56aeebcb0718e65cd705a94bc39a9af78544`  
		Last Modified: Mon, 08 Sep 2025 22:13:45 GMT  
		Size: 68.3 MB (68329540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1044666228e7193c32a9391acbd493cff11224ca2c03e5727f784658ce3739`  
		Last Modified: Mon, 08 Sep 2025 22:15:43 GMT  
		Size: 607.0 MB (607001710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c708fcee5d9d42734ad33e29b5626a520c23c2a6b872f5e0a4f9827926784908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16295247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cdd46e47d729cbf4171eed6968ca7318fa91549f40041ede9e7a25976da37c`

```dockerfile
```

-	Layers:
	-	`sha256:1a02911e3a00254db1ca4744088f927089b64fe85f11eadbafc95e39f5132dff`  
		Last Modified: Tue, 09 Sep 2025 01:21:38 GMT  
		Size: 16.3 MB (16285072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7825dd670b95a4cc83d77e8d7c09b5a87333b1124a273e5923ea7cd9ea5865`  
		Last Modified: Tue, 09 Sep 2025 01:21:39 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:539c5586946c3135220d7e694e635f723dbb1e9608850dd33678093c6d5f16c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687543516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9338a9657cf586c3da372e95cfbfa2e1542a97a65c2750ce4a48914cf6e77e70`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fbbf51ad93abaf2c32c0bd2c116235b9ebbdf46c27b1eb3a1de581d2505529d1`  
		Last Modified: Mon, 08 Sep 2025 21:15:28 GMT  
		Size: 47.7 MB (47745321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a27ea3b595194ea4b57e98121e28094f76ae480ffaf98bb45b0ff375de320`  
		Last Modified: Tue, 09 Sep 2025 01:32:11 GMT  
		Size: 24.4 MB (24441403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066f85c5e5a320fa62ace82553ffa0f839dcb88ebbbf0a438e8427cf81a027e7`  
		Last Modified: Tue, 09 Sep 2025 05:05:25 GMT  
		Size: 65.8 MB (65802066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413b0514f95d8babab63d2718874dba1b98660df3a780117dea9d74e2d1866ef`  
		Last Modified: Tue, 09 Sep 2025 05:08:21 GMT  
		Size: 549.6 MB (549554726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49fb564edfe12a38a56cfcf3e9963c568bac713af3b1de33d6a3a7e59bb066f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16047501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf69869ffd18ad718f44728e50b648a383e5c5a6f21ef4d5c0d89ece99cc08f7`

```dockerfile
```

-	Layers:
	-	`sha256:1b66d4fca3c804d13d3d7e12f0c1d706ce17ffb8d1252275383da1c42526dedc`  
		Last Modified: Tue, 09 Sep 2025 07:20:48 GMT  
		Size: 16.0 MB (16037261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff1bc09d4662afc957a5e77143f00e3668dbe4c1b0a0d407561a0e24e09f78d`  
		Last Modified: Tue, 09 Sep 2025 07:20:50 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b60afe0525708601c4c6161e900d63ada2a732d1d7da423d0bf4a03545152a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676089212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a2e5971b3a57416593b5aed069b5999ead1c3fff6eae6d3041979c6edeca83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d30a0c5c579644a88a894fd0b1f1db229651b30c974b07aef6ab9bcde5b64440`  
		Last Modified: Mon, 08 Sep 2025 21:15:47 GMT  
		Size: 46.0 MB (46006695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf528d0788e249a97adf6d73be0b9ae329c2651a09b55c47f7bfbe9fc96a9cd`  
		Last Modified: Mon, 08 Sep 2025 22:48:40 GMT  
		Size: 23.7 MB (23710180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717220db35946b78b9fb18d38321ad58f2681e6386e6e8368e047874b841311c`  
		Last Modified: Tue, 09 Sep 2025 06:19:30 GMT  
		Size: 63.2 MB (63213996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533570c355fad30283f389efa2203bf589822f15e8001d3aeb0107fe223876b3`  
		Last Modified: Tue, 09 Sep 2025 06:21:56 GMT  
		Size: 543.2 MB (543158341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b1b4f19c09b8f1ea3323bf536ef4d2e38d869c1034b45bc3f0843dc16ab6dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16053053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f164c3e22b58400be25ad55e35587d3d1734a1a6fe8c7669ba2852544698a4e`

```dockerfile
```

-	Layers:
	-	`sha256:7da3c8c563f00599da3b444c11c7f6df723fe44045ecf50cc0f2eb564e453002`  
		Last Modified: Tue, 09 Sep 2025 07:21:07 GMT  
		Size: 16.0 MB (16042813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3c5e838dcd24e731d4be842dc3464fab6e29e6260043965b0d984fcc85205a`  
		Last Modified: Tue, 09 Sep 2025 07:21:08 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ee993fb85400fc314e259ff995bb28cd88d6abd5a02c793942bf08a1de2288e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.5 MB (751523997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b355c06002519a8e4d85663c5231802807d87707c5e61569c370339a086c3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fde0f8298499f83d08590922e2548966d7839a982d2f61f9bf20422631032`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 25.1 MB (25121637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7a4b2e0bfb6f60fbd361b9831a03e03dd998e97fef4054fc95dce3d9157a05`  
		Last Modified: Tue, 09 Sep 2025 02:13:15 GMT  
		Size: 68.0 MB (68033143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a7595ca8427163c15cd59936d222e4c2822d936f42b08a01122a92a5fa0c18`  
		Last Modified: Tue, 09 Sep 2025 03:15:45 GMT  
		Size: 608.4 MB (608434496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cde5b39b51fd020c6e804157987ad4dd6b9820639aaa90f8f662e5bf1f45856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16370510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a239875a630c279a6c3a221adbb7962385cc770a2397d3831bf73576a6b036`

```dockerfile
```

-	Layers:
	-	`sha256:5332bbbed5d257b9dce5a88a73754a5a61bf81d7fba7041fa8e79e30e75b3f51`  
		Last Modified: Tue, 09 Sep 2025 04:21:56 GMT  
		Size: 16.4 MB (16360254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4ffe69f40356530c6bb51f5566694478f65bd40ce85780317d97bf5ef2273b`  
		Last Modified: Tue, 09 Sep 2025 04:21:57 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:135d7fcf5687281b007a35aafb4c58d43ca6cea2e72b54fd9ba9c11f98eca81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.0 MB (745029071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6ae19c195d8c72addc8cafd265ba57dba4544ac65ce6d0f1c82f736e9efa6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb4ce6e6dabdd026c92e91d6d35c69c5877c49180dfc2038eceb2d3a81ffb31`  
		Last Modified: Mon, 08 Sep 2025 21:55:10 GMT  
		Size: 26.9 MB (26880746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cf30a6a5b2b470e48344ea274a9e04bf7432fce9adcb8cb91cb62f15698361`  
		Last Modified: Mon, 08 Sep 2025 22:13:37 GMT  
		Size: 70.3 MB (70346053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf5c59de389954d80f6ce5b44638dba34d56e70321f9162e0c6d2efa2b73d3`  
		Last Modified: Mon, 08 Sep 2025 22:15:43 GMT  
		Size: 596.7 MB (596688659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f36b54254294da7e2de67ca7e7221ed8850060d7ebbc8553fcc1a624fe344ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16265014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490f7728e514e24ad21fe3907bfb56257e50256397a8935468745a0597fb6e83`

```dockerfile
```

-	Layers:
	-	`sha256:a10d88888e1fb2a63c0efcf6d0311b971ddbd9b0c7c3c2901cdc33bbcd502d03`  
		Last Modified: Tue, 09 Sep 2025 01:22:41 GMT  
		Size: 16.3 MB (16254860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4d8da91e175668755feea1bf823eb1b02d46bf2cd32c01ada51a6e3372502c`  
		Last Modified: Tue, 09 Sep 2025 01:22:42 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e92d080516a7d74264b70445193b1e2993f2c4fdbb4b60110596127703d5f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323214493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d476c8a0d61b38e10c8095c84ef27fd9b1c467bd60690128f71f3f158028dfd2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5da413a3f50eb44f07bba0eecd786bf3efd93a4ca4c52ba8109a9b9ba14e688b`  
		Last Modified: Tue, 12 Aug 2025 21:13:15 GMT  
		Size: 49.6 MB (49562283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d257b869b2a60078b7a65964ab94a9b367c5ab49593e2c17c1f7845cf6eb2`  
		Last Modified: Wed, 13 Aug 2025 06:40:49 GMT  
		Size: 28.5 MB (28535525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86fe6006038239df0ed2d48c27073d2bc03b5547e42ef3e28ba6ae24c42e7f`  
		Last Modified: Wed, 13 Aug 2025 19:22:34 GMT  
		Size: 67.2 MB (67186448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5200e8b4afc50ea558b5c358e93dd23057fa272ab1fa20e18ab8d8b3af91b104`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 177.9 MB (177930237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2bf7543ed2f2be5ee2e9a2d471340fe2165f8b10af73a799f153417bdecd283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc6be1ebcbab7ec27757f0d14c53aa806cece44166a0e8903ea95d266798ba8`

```dockerfile
```

-	Layers:
	-	`sha256:b1bd668dc038ff262a764cc57bb489d410c1884ffd5a858e1c9ff54e9f036acb`  
		Last Modified: Wed, 13 Aug 2025 22:22:03 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8483d6279539c31b712b95308223d9451626f6c7c78becdac0ff0f794ec02fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348425331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14965229893a0c205915170801a2fcadce8f6ece9611b958dd5f78f3c96a676b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ae7a451fcc7e9bebf7ef51b031f5ec2600e7c017efb66e1de76397538aff917`  
		Last Modified: Tue, 12 Aug 2025 23:09:05 GMT  
		Size: 53.1 MB (53147748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ea27c6408465e04631c45f46084191d49262124cafc6550f5e911abd6374`  
		Last Modified: Wed, 13 Aug 2025 12:14:50 GMT  
		Size: 27.1 MB (27069254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca3385b479d65092a57bf9f294af41066b99dc31de27938a478b8d7dae4e82e`  
		Last Modified: Wed, 13 Aug 2025 21:22:30 GMT  
		Size: 73.5 MB (73507342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a33dadb21f3de9afc0a83f58306df9d6910807e3bb2ce9b03400946f47da9`  
		Last Modified: Thu, 14 Aug 2025 04:10:46 GMT  
		Size: 194.7 MB (194700987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d279a4f066a452b27641e1ae83be148a5b8a758bc5497f6273177d0e7909f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16340953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8aee994a2175f4c64dee24bdc66d470ad700bcea066170caf538dbe62441b8`

```dockerfile
```

-	Layers:
	-	`sha256:f7c8d6e272e57b2d8b1ee4f1030256fe910feb742af074a675612fae74a609ad`  
		Last Modified: Thu, 14 Aug 2025 04:21:19 GMT  
		Size: 16.3 MB (16330745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd087ded9930c2c4767ea5826df94400d54d4ddc69d520517694163046cc0ce`  
		Last Modified: Thu, 14 Aug 2025 04:21:20 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:10860440fe36cae585b70c82a35f7866fa876a06e19149c7e4531e1aee52c39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.8 MB (415822559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e9e2df9e8358d2dbc9c6a5d2992f4119fc61f0e1729f8622c943c26f3d0678`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9e91ea2edc2d111f6a67eba934b0ebded0b74c51de6a807b73d07cbf965e132`  
		Last Modified: Wed, 13 Aug 2025 01:03:20 GMT  
		Size: 47.8 MB (47776559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9f489cd1777e5b300ee5ecaa1ee0eb257910fbeea3b4885aa18546f4677f`  
		Last Modified: Thu, 14 Aug 2025 14:45:40 GMT  
		Size: 25.0 MB (25043691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca0dbc65f78a497c831d706ac3403d38aa6f98f2a4e700c685ca0e3cd72cd3`  
		Last Modified: Sun, 17 Aug 2025 07:42:58 GMT  
		Size: 67.1 MB (67121641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf97afdc7c0a9ae1c9081a860559b0040092ed81ce9a766931ce70e1f08063`  
		Last Modified: Mon, 18 Aug 2025 09:08:33 GMT  
		Size: 275.9 MB (275880668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9a4becd88d8122f6d5c872f15a12ed7ec85b245618a2043abb03843f7e5d990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16341685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3259d87fa8a24926cc2d2787f645270a8a5d9c221e929017dcd70dc454ca7adb`

```dockerfile
```

-	Layers:
	-	`sha256:87676debcfd6b7264acadb2095c8798685216e54eb87d443913862cd5bc7c2ad`  
		Last Modified: Mon, 18 Aug 2025 10:21:32 GMT  
		Size: 16.3 MB (16331477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12353a27f79432144a9210edd85e932f28d8dd67ff68ba81391b762feb4fb7b5`  
		Last Modified: Mon, 18 Aug 2025 10:21:32 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6dc35a1d8a9f0fffd43e6bca573d20d673dfcd6887f166f667050a56af313259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317880973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065b0ab5a283a03d1bdac480d03e1ee5b5ca1ccadb85472cf2f2b6b90ad48201`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4959d43b6e4e3bb883ad4324fbf3d2d46fc88486af520d990c753fc3a7ba0062`  
		Last Modified: Tue, 12 Aug 2025 20:56:23 GMT  
		Size: 49.4 MB (49380676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9f068820d21f743fb7a4899ffdac4cbb3c9018377c7ccd9ea60dfaa661d90`  
		Last Modified: Wed, 13 Aug 2025 11:02:14 GMT  
		Size: 30.0 MB (29993315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c726bc62e5513d157547977196ac5e96f4f6b0c75bcf55735caaa59100d378`  
		Last Modified: Wed, 13 Aug 2025 15:08:18 GMT  
		Size: 69.0 MB (69018547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84103ed16a9a275b646f4ea64c94e011b85a3cd1424906ca73b63a9f9bf6e429`  
		Last Modified: Sun, 17 Aug 2025 07:13:22 GMT  
		Size: 169.5 MB (169488435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f915fb56c186390e11dbe030e0d11a4e99b4dac87d542e5f805a8edc82f716c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16133408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77f46e84c1bbbb0f790d270873cc50dede6194ad3410ea9f012f0717b5ee30`

```dockerfile
```

-	Layers:
	-	`sha256:30e5aa21c76971ca0a08c953a147530b760c34be9d2e90a4be32f93e4de056ee`  
		Last Modified: Wed, 13 Aug 2025 19:21:53 GMT  
		Size: 16.1 MB (16123233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a237f60a2c3689e58bfe6ca21b9f40332c3e0195392b3d292546a5c1ec75707c`  
		Last Modified: Wed, 13 Aug 2025 19:21:54 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json
