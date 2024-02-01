## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:ed4c3524dee1dc8078b6461660f9fcae37173977a3e46ebb1e39a0867d1902c3
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
$ docker pull buildpack-deps@sha256:169324d78892d54a26963dd63352e483624df43a66519dc0da809bc5806e36d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411829417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0012ce685aaf6184293aa150c4c0b36deae27bccd0c3e69846c998bea1ad21c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:29:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b5ec6ffb24174c2e8d7b59efdd6b0613b5bcef62a7cde965c456ae6a2b2ea`  
		Last Modified: Wed, 31 Jan 2024 23:35:43 GMT  
		Size: 66.4 MB (66425971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a184e8b47a1727cd21427c2dee2e8a6f3115ef79fef28d35348016479e476b31`  
		Last Modified: Wed, 31 Jan 2024 23:36:25 GMT  
		Size: 268.7 MB (268727614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bbb57464ac66ec70c19c9c2893dbd7a8b0b6a94fc4bef74e85c7902fde9f62d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369083888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9adc5bdb8e634c2ac9e5a8ea25050bdf234804c602643a80739b5d9ffd7248c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:19:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162728a10cded66e397f0df0db68b9dbb11c61c6b79d3baaa731a13664cf8521`  
		Last Modified: Wed, 31 Jan 2024 23:25:18 GMT  
		Size: 64.1 MB (64084887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee4e2f462817b287c66187ea14cd84563505c938a524b8b18f70f4647313ad2`  
		Last Modified: Wed, 31 Jan 2024 23:26:02 GMT  
		Size: 232.4 MB (232354211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d27b106950812dd6e99124eefab26434b4645d2d03dafe55694c6df13aaa7dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352098769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2eccf2ee6c64c1a12e0014aeb302632ce3f5ef3ad7808ab3cc60948217bd51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:53:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:55:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d5c17bde538214384a501538668ef9f5559e9cda83e4b7913d622823ccc1a`  
		Last Modified: Thu, 01 Feb 2024 03:02:04 GMT  
		Size: 61.4 MB (61445900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c2e9b449796e0d1f2fe06bc96516088f81a158362ef93789c88a92cdd7152`  
		Last Modified: Thu, 01 Feb 2024 03:02:46 GMT  
		Size: 221.2 MB (221205326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5cceba7add3138cd5036d039e05b3741b5554a2e75aa358a00178d9dbf07a417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.7 MB (399740160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8ea879302b206dc6cab6a5c13cf1db0ea988bc88c8e90eccb9509beb9ca5ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:49:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2cf8c96bc8d8d3f9a21a0e32a3a2e78e0e214cf8eabcf8557a33907fe41c6`  
		Last Modified: Wed, 31 Jan 2024 23:55:07 GMT  
		Size: 66.5 MB (66539836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5323d8abfd6729b2ec644ba5d2746fefc2b0c082516df2a62c9824abb27a7907`  
		Last Modified: Wed, 31 Jan 2024 23:55:40 GMT  
		Size: 256.9 MB (256947291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6fd5852b23d2806ab37b0fca5e70f5662c9beeb49c025e6f96406e7081d03027
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (408024921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3df00b9ffff249d715ab097ae63eebd1578b53e2c051bb1708252005a0aff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:42:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad4f66a2cd19b6eea3bc0f180db9669dac381b31d1500c7c9b561e5310599f`  
		Last Modified: Wed, 31 Jan 2024 23:49:21 GMT  
		Size: 68.2 MB (68224658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe5a975d38b389f8e13d306a52b282e5e5e79a0ab45543efe60de531f525987`  
		Last Modified: Wed, 31 Jan 2024 23:50:22 GMT  
		Size: 261.2 MB (261157854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e204d973ead7cc9b7c4f1685db5fc42121ecf47cd34db73e9de993b154035b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.8 MB (378776131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a6e7aa6d535e9480ef49a1e45249776e91ec4c3296fed72f685611542c8443`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:35:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bae2c96b6133a9c62aa17246799e040dbce8e2ce06213bc63d1ec7c2e221ca`  
		Last Modified: Thu, 01 Feb 2024 07:52:48 GMT  
		Size: 65.2 MB (65236018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f89ac0febda87ad1ba70e78d3946224343691268ac714ef2f9b1023a6698e`  
		Last Modified: Thu, 01 Feb 2024 07:55:26 GMT  
		Size: 237.3 MB (237328354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:966835a25e3d7a7d337aec37e74a0ecf014ca86ce0c5a1c29fb049d9b1aac163
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423499249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45e81aacf6b190c3e5b7079e99f9b1c8b3b135d2c2799c200df1fa2832393b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:41:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bfff2a14e6e587d4c11641dfff4fc47965b3e5a5be2c00940d05089da4f95`  
		Last Modified: Wed, 31 Jan 2024 23:50:28 GMT  
		Size: 71.9 MB (71937073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c37b376fae9652527604ce30a952fd7e31e1ee0519177a6a9560c684924741`  
		Last Modified: Wed, 31 Jan 2024 23:51:19 GMT  
		Size: 268.9 MB (268883342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cf306643fc52c8ffb549d64ca6cb90dd4d8045a6bb26cfb3ea09670657581f9b
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612f38a8cd5bccb124d6fe189bfe0f9165c382d1ca4c5b1a909ba37e9fee531b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:41:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f8b671531c36b200b6e84dd21a3c784a776685b99bb9638b337cfd52d06fb8`  
		Last Modified: Wed, 31 Jan 2024 22:43:30 GMT  
		Size: 65.7 MB (65693017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fb34953da70cdb0c9a80fb3ba5c765f0a6d96c77f79a0cafcc9dff16dfc62a`  
		Last Modified: Wed, 31 Jan 2024 22:49:25 GMT  
		Size: 300.3 MB (300254507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2e324ae53d9fd5db2018731bbe7fcbcbab4172d4ecaa9a3613e96e61232483cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388238210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005e32576495a2ec040447a36691b99b28f1a28743a3a33fe8a378bdbea58739`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:43:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c0a5ccbf3d4c81b3650225ea3b2d9eae4bd38f2e909a10e6c82117a577b24`  
		Last Modified: Thu, 01 Feb 2024 08:21:22 GMT  
		Size: 67.5 MB (67535565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d73b1c78c6ad532b4f42a143c03c1198813b160bb51460a53290871ac728a68`  
		Last Modified: Thu, 01 Feb 2024 08:21:59 GMT  
		Size: 243.5 MB (243473683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
