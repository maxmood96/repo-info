## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:c3770bbbbd0551bafa97e26639c16e43f4789976c6d5be2c779b360e7b448048
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:26bfa26025b74751d6955671e511d0220e15e16c5dd01196c64c269ab68fbd20
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365568682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0449f6345f4d9285d33f821e3caec0b4f9b949b743948f98a91d601ce12a7335`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:47:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba418b28cb46180ce179bf48a7dfa7135087eefa79b479acfa16fedb4e4a1c2`  
		Last Modified: Tue, 13 Aug 2024 00:51:48 GMT  
		Size: 20.5 MB (20482905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a515568b5fe34e15585cdfd456e9acee67d565f25f2bfc42df67c7b99ed3f3`  
		Last Modified: Tue, 13 Aug 2024 00:52:04 GMT  
		Size: 66.2 MB (66238445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b00dc57fb0ca9e877a81f4e83ec904f749882262e375124a03d8727e638439`  
		Last Modified: Tue, 13 Aug 2024 00:52:38 GMT  
		Size: 226.0 MB (226011144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1681bcb26b04d6e7008b5553e6277ceb5413f1509b573713cbc2f3e3a9a635fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326235431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716998cfc77e470a5652ecc36e4a16f8e9530f004f2948e545e809f5e3367c9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:48:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9873310e83bd2c9cddf329c78833d832e9bbd909cf26e632b676e3b31b940`  
		Last Modified: Tue, 23 Jul 2024 03:55:11 GMT  
		Size: 63.6 MB (63564737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982638bae6423bbae98e0c502921f436b34355d3d4bf030c2252127b0c30dfbc`  
		Last Modified: Tue, 23 Jul 2024 03:55:59 GMT  
		Size: 194.6 MB (194599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b6cffdded486696d01044be124faf6afefa35c28402259fab0949e106904e28
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308055812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eead025bb596ebe6cd8def784662514169861219bea83d20c391d0d27e6a9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:43:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530b2c70788d78360d3f365fdef0a3a385f75d30ac92e588df91acda5d06910`  
		Last Modified: Tue, 23 Jul 2024 03:50:00 GMT  
		Size: 61.0 MB (61013856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f4bb1861e73c2193c46843eb11525964345067e7c1f80c54e7480ca0853eea`  
		Last Modified: Tue, 23 Jul 2024 03:50:46 GMT  
		Size: 182.1 MB (182121659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:28c83eba573a70d02d6e6ee32a0f418bf89b7d0fc772bf4d389ebd195133aca1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359297641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c148c5d6a4861f54f9530476d98863685f80847d2fc9e1a8c274d23f426ee3a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:28 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
# Tue, 13 Aug 2024 00:40:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:05:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:06:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42437a82bf9bbe8487117e25e8d86dc6640c415c01e295d2560ae15db12b5a94`  
		Last Modified: Tue, 13 Aug 2024 01:11:11 GMT  
		Size: 20.2 MB (20228217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6149cd0c731896a1b19323de76aaa6c32d3b8d0092d305902306e6795cb37d9`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 66.3 MB (66263804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e2d2f1dca9ca73d2634a64172028f2d993772867f4c04d016434ddd228825`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 219.7 MB (219650370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04cd0e8012a7b0a927453540343a58c40ce7422329b38254cc3e2c0fa5709eb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.2 MB (370192161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a14e845327d478743cc97f4cad35b0845c843799f0201dcea0ab4a3d804b16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:11:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a203d729458242dda28f4795cf80bb88746084ccdc8cce21ba2acd7dcaefb3`  
		Last Modified: Tue, 13 Aug 2024 01:17:23 GMT  
		Size: 226.9 MB (226923306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9028c225fe9b65a98fd81e5ad4b28ac2aa5b828cfb1f98ec22d39a175a306200
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332195395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d78f180eb1b796ab7aabca6af1df31c1b12f369e9e02d0bbf4a30c83c099656`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:49:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf5f50c37db38e90a50520c093b6fa2939d9fef5a62895ea90c91d02dbdeac`  
		Last Modified: Tue, 23 Jul 2024 02:06:02 GMT  
		Size: 64.8 MB (64814442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990154075f1f9e5c156fcb25dcc580ad4535cfc9df883915675c583a91f37a59`  
		Last Modified: Tue, 23 Jul 2024 02:08:16 GMT  
		Size: 196.0 MB (195964609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c18683a7b2e4a08a201c00bc455b420cb3bec97f5445c87e0b7b123a70689b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362845834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6421ee50a6f14c7c122aedb9c7582332b0d3a46aed1c235bb3fc86f978db3305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:37:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b98c88f8a6ca27a89215004b3cdac4fa255a74553ee93c0bb336155b16701`  
		Last Modified: Tue, 23 Jul 2024 02:44:32 GMT  
		Size: 71.4 MB (71413135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632e7382e9bc8051ac63dc520d51f93484e2c1c8f3c624baf6d2a99a37294f6`  
		Last Modified: Tue, 23 Jul 2024 02:45:10 GMT  
		Size: 213.4 MB (213409348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1f0fb710e4c77f45c369961d8f5ad1b5c3c2d6d6637879b7f0ee0cec7a11e1e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443858778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13763f9c3914a92f12e358871f27bfd1ee3de1d1a8f20a4e5a9c057826caed09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65deb42d9c749a528063c18ed3482c3235a8863523f7fc5d895330b910edd50a`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 65.5 MB (65455674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a959a2b7a253bddaf7fd68b258fe0255968fc0d4f52643281e2ac2de68e19e6`  
		Last Modified: Tue, 13 Aug 2024 00:53:51 GMT  
		Size: 307.3 MB (307284095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:104b8641b7f47fbc3c0cf767a00a4df89cd675e96ec4abf2fc9bfcc2e2b5b392
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334266471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8581bebdd6dbb28f2b1f3ea4479683d449a04d2392a92133ae50fad25c8b4072`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:09:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:10:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b90812b56a031f8fd0e591290e9252f35ca6f8f86d5550448fbfcba2c2560`  
		Last Modified: Tue, 23 Jul 2024 03:16:20 GMT  
		Size: 67.1 MB (67066609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3711122f465e94e5fe0e07180db63aa5750b29edafa7e72d91bbd960a4724a29`  
		Last Modified: Tue, 23 Jul 2024 03:16:49 GMT  
		Size: 194.3 MB (194286348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
