## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ecc5dbd2ee948505cf6be028939419b70a8a4d6ee904063407b3cb89b45a2a00
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0671dd909626fd8c20aeebd69e0398ea1ddced50f49d105ccda3d11188e0e6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337211268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4ae72ac796003b6f98352d50c6615b0774b18e4a1d40e0726432dda7261201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3cdde7daa1c8617934a7f6fc5999acbd8f13f45edd54e774f4a3af8f31fa8`  
		Last Modified: Mon, 08 Sep 2025 21:54:27 GMT  
		Size: 25.7 MB (25659714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c7415b1ab77e9af8efc826d62011c5a0c0c5ea052f4de5c46ff0ed4fc8b2b4`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 68.3 MB (68266149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee5514490a257530e1199c21bebc026e02392c336771451b453d5eb90b6115`  
		Last Modified: Mon, 08 Sep 2025 22:14:56 GMT  
		Size: 193.7 MB (193710370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41b5a93efc7dd73975eee1d6dcb2c52e80d27331700a60fe570a45682caeefa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16285471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b32a83e51ac74ab448eb05fd74da8115ee83041c832da2837aa62d2d206e98a`

```dockerfile
```

-	Layers:
	-	`sha256:ad5929115a0ee37c71aec49832bb818896e5ee32e82772e83de28044f681faa2`  
		Last Modified: Tue, 09 Sep 2025 01:20:16 GMT  
		Size: 16.3 MB (16275284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944c42f7f911f06b2f3be8c882a19e686aaa986b6fc4a04b1f7ddfc33e96359d`  
		Last Modified: Tue, 09 Sep 2025 01:20:17 GMT  
		Size: 10.2 KB (10187 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b6d456ea48e54c18b7221ba08b7f98ff67258d9856e7cba1ed7f0d6cd268b428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342770080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4099cff28979d6cfc4fd581b4e674fa87d61d39c3c2183d9e9a03a0c4014c63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2fa5a98b9608d692994d9abcc2a7007473cf39d4da546665901804b35bd8b320`  
		Last Modified: Tue, 12 Aug 2025 20:45:48 GMT  
		Size: 47.4 MB (47442421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e8c08416a0595c07b904b87179f903faee6f0a25e5b00b485a3c0b0df46b2f`  
		Last Modified: Wed, 13 Aug 2025 06:07:53 GMT  
		Size: 24.3 MB (24331053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1486224fc8f64dbe0bf66d7516691f5822dfff3ac064ce9811427c63fb10b9c`  
		Last Modified: Wed, 13 Aug 2025 12:58:51 GMT  
		Size: 65.7 MB (65730182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67446a3d10ae9d03ae843fc879c4f1736fb18c208963a5bb5259ca4d4ee16227`  
		Last Modified: Wed, 13 Aug 2025 12:59:04 GMT  
		Size: 205.3 MB (205266424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61b9ec4000332e992e33599b138ae6a7151efd3e606849fe7f85fd96873c7cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16995194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70ef1311c3a186e25d9f6d549b40284f4a8450bb720af3d0357472d373fcd5c`

```dockerfile
```

-	Layers:
	-	`sha256:211702e95625ad2127681bbca87f797abb53ef66c5cd15f4af1c415150d9906a`  
		Last Modified: Wed, 13 Aug 2025 13:20:26 GMT  
		Size: 17.0 MB (16984946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3d11f9002a4789a13f8a199d8ee6a7e6f3db671bf7f34555007d76a8abc0b8`  
		Last Modified: Wed, 13 Aug 2025 13:20:27 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6e4774d05cce91af7f376560a20761800e56c247f283c60535cb0828c49aa454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325314081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6786763404cca3df514218e33f2d3172399ef83ab49a5241ac0e8bef8fd2cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ebefa9d9514d88e860c22acef070a7914aeebb2faf205f156980b98aae6239b`  
		Last Modified: Tue, 12 Aug 2025 20:47:38 GMT  
		Size: 45.7 MB (45712626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e92b397025ea1962fe06ac411410e1176db804c6ecdee14d21141a79f11c0`  
		Last Modified: Wed, 13 Aug 2025 17:21:05 GMT  
		Size: 23.6 MB (23605493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967cbb10d571d2d7a67996c18368f0902c78e7191a91127a26dd33377934be7`  
		Last Modified: Wed, 13 Aug 2025 18:16:13 GMT  
		Size: 63.1 MB (63135785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1b65227c9808136678b43cee51c02b486f9fe12e03f0385f89df6a9b5f3b8e`  
		Last Modified: Wed, 13 Aug 2025 18:16:37 GMT  
		Size: 192.9 MB (192860177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a04bfee3534cb4f4c9cce1d4f9eb971661da3619115b8d175a74a95982eaf595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17000984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1518996b2d142bd8ae1dde6712b27c2e3054d1f40bf0ecc11d24b693d7a15f33`

```dockerfile
```

-	Layers:
	-	`sha256:1499d719304e83b24ec85a9fa4d7a0db7ef25dc3f4df5efd4d494b70e2895dee`  
		Last Modified: Wed, 13 Aug 2025 19:20:26 GMT  
		Size: 17.0 MB (16990736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23996171c6c5fa2bdfed1bb07368a08829842fd593a4298221faad6d9cc675a2`  
		Last Modified: Wed, 13 Aug 2025 19:20:27 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:73b4c45258349fb284cfa0776daf58926bc090d9c5d1ac57aa90a9064409e287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368664401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11237d5bf052103391ce6fa4f2a8553fda9e73a386b70dc076e7f93c4bb20aaf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:273757ec3c30b589868c996d06fc6679616be5750d77150b4ff9e1c76d62fc59`  
		Last Modified: Tue, 12 Aug 2025 22:09:33 GMT  
		Size: 49.6 MB (49641601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061b8abd2163f95be76efedd7a660366135f0445c2148195b2efc5c8b4e4520`  
		Last Modified: Thu, 14 Aug 2025 12:01:20 GMT  
		Size: 25.0 MB (25006552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2b605603692665647b54ba968c38451a923c1631c8391126b72c47d167dd3`  
		Last Modified: Thu, 14 Aug 2025 12:01:25 GMT  
		Size: 68.0 MB (67963901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc1de26bc7a6956554eb4bfa0b513c3bb1629c27d587d730cf8413cb6adced7`  
		Last Modified: Thu, 14 Aug 2025 12:01:30 GMT  
		Size: 226.1 MB (226052347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7d8e1b68f1a4ddcd868b187fa599ca9a46b9f6de761b61533b386b53fc84493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17317306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bef2132aa60a59957d97ed51f8837d74f25a720cf496138b67a7f03b1105b26`

```dockerfile
```

-	Layers:
	-	`sha256:496b2ce03da18c9e4e2f950393ab44a3552e19f51abdeae4d2967362969607ff`  
		Last Modified: Wed, 13 Aug 2025 22:20:37 GMT  
		Size: 17.3 MB (17307038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45113905ad4cf20debba201c01e2781924e08f5abc5c55c328421b63e3f8a48a`  
		Last Modified: Wed, 13 Aug 2025 22:20:38 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:08eaedda36542e61fc65553d9f1d53f2d5a2e4330a9af65468b5e7060eb76a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344619444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21bbce0b8a37c1f1adb316d7deda3d102e7ee4ff9700e9c23d47759914210c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160456f8adc4b90f7d6b65b9febd09b29220d231ef5935250170717564dfc2ef`  
		Last Modified: Mon, 08 Sep 2025 21:54:42 GMT  
		Size: 26.8 MB (26824472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73639472e8dad9dfb716e8a6bbce77939664b0fab7a79dae0ea141902d199b`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 70.3 MB (70328423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a3adacc8033e0fcffe64a6266d1b994745bcc975f06392418750d911aad457`  
		Last Modified: Mon, 08 Sep 2025 22:14:56 GMT  
		Size: 196.4 MB (196416739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ba999df8ffea0425f7cdc56088842ed6a616ae7d260660bd5c66dc85b00323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16255263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212070e1d5a2e8a2164a8e38f7fb89b2db857531a42f8893146b58e4f0d7d36a`

```dockerfile
```

-	Layers:
	-	`sha256:34133ebbf169d898c84974f9dd1b634581b915cc734f8e1cd56b8525f71fe780`  
		Last Modified: Tue, 09 Sep 2025 01:21:04 GMT  
		Size: 16.2 MB (16245097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09478d013a06b76f42404fad777bc129f6b64e157adccb2e3d314bc643773e0c`  
		Last Modified: Tue, 09 Sep 2025 01:21:05 GMT  
		Size: 10.2 KB (10166 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:452db49c84cac4be723e3784c15fa70a1c4f800860ff6d42798bdb46047274d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384597067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ec25148d8a049a682aeb118b92bba246e417818eb9346fc40061a42df04067`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b7a7f44f45faa95497b08557d13fcde72165c528469e03cbf308c4f4631f2dd`  
		Last Modified: Tue, 12 Aug 2025 23:06:59 GMT  
		Size: 53.1 MB (53103377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840e735c8e0187da0a3a1c46a694c6d194b251001f4a96704e0ac845ec18ebe3`  
		Last Modified: Wed, 13 Aug 2025 12:13:41 GMT  
		Size: 27.0 MB (26986919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f0a22fc2b7b0872f52cfeaf5aaae68c408642a3206537713bb64955507caec`  
		Last Modified: Thu, 14 Aug 2025 12:01:53 GMT  
		Size: 73.5 MB (73466445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8746ade2d96846be2b9b50ca7f68f1e13efca69ba4014175a9657b8bba85632`  
		Last Modified: Thu, 14 Aug 2025 12:02:02 GMT  
		Size: 231.0 MB (231040326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3dc94ad15927c8d08d85ee87706579d95bfe1bddb7a044d476955b6a6be2162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17218517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bbbc97fa1aa6235ee736d1681125426566db2996f7ac3e1b58e40c1ba80d2f`

```dockerfile
```

-	Layers:
	-	`sha256:3731a3c2819218b486e7adcd70d2054f1587ebe553707ca2ce62bea025742a73`  
		Last Modified: Thu, 14 Aug 2025 04:20:36 GMT  
		Size: 17.2 MB (17208297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a0b2e8085955fb8c92ba7df1cedb73f1d001886ed5ae3c8365050601857673`  
		Last Modified: Thu, 14 Aug 2025 04:20:37 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7115d9fa40417e75001f81ca708baebee92ac232d22fb58393c6abbff6f97ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.8 MB (469832035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a32da9f19b0ec5861b522c1197d59daf076d193b7d83953460247a27651bee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18eac9f463d6a4f3c60a520935227506dbdb88fbd69eb2d7f1db2b18bab3b76f`  
		Last Modified: Wed, 13 Aug 2025 00:59:52 GMT  
		Size: 47.8 MB (47764299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40195d2e04aeb657d27babb7b990135b099dce2244de1f5f044377d8fb07f57a`  
		Last Modified: Thu, 14 Aug 2025 14:40:45 GMT  
		Size: 24.9 MB (24943412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7119e17d753e3bb840f4a76a177110ecbea100d2e7b7d1921aa4515d0cee3381`  
		Last Modified: Sun, 17 Aug 2025 07:36:43 GMT  
		Size: 67.1 MB (67098945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f944222f7d2b4195fa959eb5755d1e75a6b7a161124757cfe2dc83ae0f2557c`  
		Last Modified: Mon, 18 Aug 2025 08:07:34 GMT  
		Size: 330.0 MB (330025379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0718c8ba93fd8da5312441fc7ef41183a90cc50f979aa57c3b37d15414b4f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17298013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98137fa01464d8eb2808bcddc5456a865222883e18a6e10b3cebeebf24b28199`

```dockerfile
```

-	Layers:
	-	`sha256:5c96399eea203e57b0ca18d81bbd2b3a960becd1510928492d35acaf5ddd420d`  
		Last Modified: Mon, 18 Aug 2025 10:20:58 GMT  
		Size: 17.3 MB (17287793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0da4aa0a1fb251e9796fe50384ac11a06b31166eb0fc83001b0a61b07a518c4`  
		Last Modified: Mon, 18 Aug 2025 10:20:59 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:77147b962d2d4713841c6a917d62e38cf4264aed9148c7127850dd62fb722079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351540894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3204139ee5c54ac43b156a7c5dddec3bcf81036a7f26aae567807fc43b8b6b64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:737129d56eecb9e531486098db9ca11053ee0c83738b761209455c817b0cc095`  
		Last Modified: Tue, 12 Aug 2025 20:53:59 GMT  
		Size: 49.3 MB (49345157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788bc8e33ee7a99a1a339be1f8a021249410c7933d3ffbff46b2196b2aeb3d7a`  
		Last Modified: Wed, 13 Aug 2025 11:11:36 GMT  
		Size: 26.8 MB (26771668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa37d0c7666ac39e6f0ed83896f1e13ab06ca2c907f41a30b77846a3633dbc`  
		Last Modified: Wed, 13 Aug 2025 17:37:02 GMT  
		Size: 69.0 MB (69049583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673627cdc713f706ab6327ec4e4bee351b0e99c6c2d88abd1a76d56de9cab27f`  
		Last Modified: Wed, 13 Aug 2025 19:38:05 GMT  
		Size: 206.4 MB (206374486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:245dba916e22f41c8e85d7537c72973e8b97808ae476f088d75da16dcf205478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17010177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901b15b3288af4600a114c010ae08d9aecc07e65a0034c0f27b1f1de6bfaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ff4bf63721290c3b0cdac3955955bfb650368cffc2fa3bc6973dde2c591e59f4`  
		Last Modified: Wed, 13 Aug 2025 19:20:59 GMT  
		Size: 17.0 MB (16999989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4243d08f8ebb6d7142602f45499a1aa26a48ccd1bfc927314d4ee47988f66f`  
		Last Modified: Wed, 13 Aug 2025 19:21:00 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json
