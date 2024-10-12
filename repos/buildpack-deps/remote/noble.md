## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:2a1f6d7301dd3b498c1bb1a7f28d4787bd5966f04e6ea54793948e633910a27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:194f6e67912ea20f32b603376334cb014bbb369f9552dc023056e5a5cbef3933
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280279950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304783ba203337e5337d940dc7b8f879bc44896e721fcd966f587c12a7de3f36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:41:37 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:41:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:41:40 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 10 Oct 2024 07:41:40 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:40:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b5ff6f3bf8380732596c0d88127072ad3ade77c0b660a419be02e5b74d17b`  
		Last Modified: Fri, 11 Oct 2024 23:48:39 GMT  
		Size: 13.6 MB (13617675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e923f23d6111f25a1ed5c513699e6b8610c1fd3541c8d558e4a047f92cf79e`  
		Last Modified: Fri, 11 Oct 2024 23:48:54 GMT  
		Size: 45.8 MB (45803803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8952ef8a78fcc55864dce84a3331886bab9c297c03cd0370dc5224dfc8f29c1`  
		Last Modified: Fri, 11 Oct 2024 23:49:25 GMT  
		Size: 190.2 MB (190245194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4fad6562cb6050443abbcb3027356a2956de0de4bf71941365dfd649d9c981ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240486359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9da86a45330407b1c4130fa38dda4f3b3a8356f84a3a21b53118b5612c69bb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:40 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:41 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:43 GMT
ADD file:a30667697f58d730cc31ae308b1ba41bf25987733d14114fca71a90447988801 in / 
# Thu, 10 Oct 2024 07:43:44 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:39:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ebc4eee72d0a91a5a59ea1b60758bd4ff0e56e71e15430000cf9a33bd0b45ca2`  
		Last Modified: Sat, 12 Oct 2024 00:33:04 GMT  
		Size: 27.7 MB (27734482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4569d89fe8b49f32a79c828326d80ca875082c0fac286d85ca20d5e42d607adb`  
		Last Modified: Sat, 12 Oct 2024 00:44:56 GMT  
		Size: 12.8 MB (12775066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21917cb06aed5df1c331e743825da573c40b65970048da822fc836b0c3cbb5c`  
		Last Modified: Sat, 12 Oct 2024 00:45:10 GMT  
		Size: 49.3 MB (49299621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b2be4b53a51dfb2853139e6690eff3f4b0c0d10fe7cc2ae8c77dfa144486a8`  
		Last Modified: Sat, 12 Oct 2024 00:45:38 GMT  
		Size: 150.7 MB (150677190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8c9693bcd1bce4fc9ade51bd1973797816d2158a58f1b6db806a00e578e31c17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271388014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f951aba9a12e513bfbce34126af2f2dcdd3f8312336bf4226147ca524adfaf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:44:36 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:44:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:39 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 10 Oct 2024 07:44:40 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:58:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:02:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2774e2077824bb6f6c4d20aba3eb095083efde5131d2b61d94e9cb99d548b6`  
		Last Modified: Sat, 12 Oct 2024 00:07:47 GMT  
		Size: 13.5 MB (13453285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6173824c2652a82d7289eedb2df956fa90acadda3114bf4b1ca0b7092e1186`  
		Last Modified: Sat, 12 Oct 2024 00:08:02 GMT  
		Size: 45.8 MB (45768708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6e7edc3dd1f6e5b494c39033b1b0d7e64675a78cfa3bc06f26543e2eea7a10`  
		Last Modified: Sat, 12 Oct 2024 00:08:27 GMT  
		Size: 182.2 MB (182212435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7efd1138283abc02eaff77f373899afca9060429abc3cabf4ab922c4d0e383b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299159167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0d7dba240b62094d5596bdd138daab59c26703bc268b3d65c712a16b3d8fc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:56 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:00 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 10 Oct 2024 07:44:00 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:37:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:40:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c849c5c10301132208a8a8eb256192428c2e1559d2ce14590adb9fd1b2f0dec`  
		Last Modified: Fri, 11 Oct 2024 23:47:04 GMT  
		Size: 16.0 MB (15991319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb583f9c2bce7f331747939dae9021e4434772a15a2b859f64613f61ad2db69`  
		Last Modified: Fri, 11 Oct 2024 23:47:23 GMT  
		Size: 51.0 MB (51027269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b761bd404c1bfa369d09dcd3bb012ed55669594057bb5384fae93634c6e4da`  
		Last Modified: Fri, 11 Oct 2024 23:48:00 GMT  
		Size: 196.6 MB (196627310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:45f3312e6c2a729d57cb1f2b7610fb271b2c90321c7640ab9cbfb34346af7dd1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330651353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4858134d5a2db71f30a48e380017fb3484e7e002a7377773dca02c81f37d0bae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:59:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be136966d9b6f5be3f056d30013c4a4cb14f67709ef491a0319722e2e90095`  
		Last Modified: Wed, 02 Oct 2024 02:13:09 GMT  
		Size: 54.3 MB (54279540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df3932963d582081c4a83ba0f2ceac2157bf5102dbf61dc9d03b1bdd38f81a5`  
		Last Modified: Wed, 02 Oct 2024 02:17:20 GMT  
		Size: 230.1 MB (230105741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:24e9b2217e9aac3e33313c15fc6b863683d59d7219aec1c3674efc4ef728adf8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262338621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cd3e4f86c18667ce7b4be785ba9cbde025ca161ca4abe801838a3c24d48790`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:54 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:56 GMT
ADD file:ed84c120e781b2f48856752e1e38d21db0bed5e09a2a64f961f004a4906abcb6 in / 
# Thu, 10 Oct 2024 07:43:56 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:11:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:14:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a910e51df11a454262534d20be5086f0295f8d4d50f522217313bc46283e5bd`  
		Last Modified: Sat, 12 Oct 2024 00:18:33 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c5a4df11065e36fe6c0e277f79daf85a05b7ce947635f9667cb234820bb395`  
		Last Modified: Sat, 12 Oct 2024 00:18:46 GMT  
		Size: 47.4 MB (47406892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4be425c7fd8b2ee60f4c6c98266f08480c451d9eb5d6e702c364e2cd44834c`  
		Last Modified: Sat, 12 Oct 2024 00:19:12 GMT  
		Size: 169.3 MB (169292660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
