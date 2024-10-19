## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:8802c2fefeefb91a844f16047fc3f564d8e3db7b962ed24cff280e82ae44fcc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:03d93a4dc70e0132312bea3f1d241698a735458531e6df70f8de510a99be38ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286146913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3c744fb1b4abd4294a55843131e06d21bd63a052da9f1f5d0a5407fbbc7aaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dfce72fe356e6ebf544894d58f638ff9283ef9eed257a7a26f09653c15fc48`  
		Last Modified: Sat, 19 Oct 2024 03:53:52 GMT  
		Size: 193.8 MB (193760968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfd11ecc3b5e6efe6a85840a418c50473d20695918a939e92395a6673b25afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01547e315200ee1c635fc2b988ed54edf58553cc8109fd67f8b267bb649967f9`

```dockerfile
```

-	Layers:
	-	`sha256:3a816cfdfd4c5b798f42ea76c86af988d85dbab1ad7e6d7f12ce754eb5a04550`  
		Last Modified: Sat, 19 Oct 2024 03:53:49 GMT  
		Size: 11.4 MB (11359090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24bcad713b0485bae1e33d23f06741842a9e36907a3b77602c55b9240a031125`  
		Last Modified: Sat, 19 Oct 2024 03:53:48 GMT  
		Size: 10.2 KB (10202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:183ff55827bdffbd19e81d560907a07cbd8380d60f74bc70a57265edbb659927
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249689229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2b05eb94afe2d9f97e104b90aaacc17449044623b553b406ccb96822857a12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:41:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:44:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504d197ab129fb5bf6269a181811d7443fd358b01cf3d0cdbfbf1f7e94a778f`  
		Last Modified: Sat, 12 Oct 2024 00:46:05 GMT  
		Size: 49.5 MB (49527237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2e428a54e779d37be7f87db612976720765d94283996921ad943a495bf729`  
		Last Modified: Sat, 12 Oct 2024 00:46:34 GMT  
		Size: 157.7 MB (157703878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2fd75582deee680615c3b70cbdd5ac956126d09379bcf537ff0d4b5b656de838
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281353475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9191d37723b6c0372f40a06bcccdf93aa4a45f0358e7123aaf6c93703c1c7de8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ffa9891ee7f3191d73f9178aa9a6cf0571e9f85014da289756abf79e90d4fe`  
		Last Modified: Sat, 12 Oct 2024 00:08:53 GMT  
		Size: 46.5 MB (46481307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1003351ad394f136be5f70383549702edeefff5c3ed4d81730a00e936a8fb10`  
		Last Modified: Sat, 12 Oct 2024 00:09:19 GMT  
		Size: 188.4 MB (188355990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b70c65c43d980c1b41ebe36a2126d8c70856f30cef5b7987202e836d76950d68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303024216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ca3def268ac1175bac2d3cf5c33c7a4c812c79d36658645315c82e562a9fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:46:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080368c5e29f148040c44902a5c8ab4b32ec2f0ad63b12f764de4230a80ef737`  
		Last Modified: Fri, 11 Oct 2024 23:48:29 GMT  
		Size: 51.8 MB (51822495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd100af345e4d68ed2ef702d8e378cce86158c1173a29884475e29a3e55a2`  
		Last Modified: Fri, 11 Oct 2024 23:49:06 GMT  
		Size: 197.8 MB (197784051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9e15f8c24d6c90d02fdca80fec7999e7fc16cae1d9b1c15b76919544ce7039b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71077a13e9477b604f394e11dda03dfdf6545214675a73d35f44970d51de4496`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:21:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7cdd9669889c44132ee8d3640a1da628cf56156b39012dbe64ca81599329f0`  
		Last Modified: Sat, 12 Oct 2024 08:29:10 GMT  
		Size: 54.7 MB (54677266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e6827872bc7b33fc8f425500eda0f9a7c630a6ff574ee369076eed769eddb`  
		Last Modified: Sat, 12 Oct 2024 08:34:30 GMT  
		Size: 276.3 MB (276314931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c2ff9fe0ccb48def463608838a0f7bd03444d5004277c2e12d56b7c456cee2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266544571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d8e737d4389dd93d0c17d005a20d2a5786fb05dd66bfb8348d501dd5bc223`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187f132b69cfccea48cca74390b7916df3cce52677c59ff2df716bc3e9c8e5`  
		Last Modified: Sat, 12 Oct 2024 00:19:33 GMT  
		Size: 47.9 MB (47893672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419866cbc9cd0dd6fbc3dd57960aca4d55d2f875b27b9ea37493d4712702131`  
		Last Modified: Sat, 12 Oct 2024 00:19:59 GMT  
		Size: 170.3 MB (170301344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
