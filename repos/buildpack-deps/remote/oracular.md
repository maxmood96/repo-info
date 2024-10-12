## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:64ae8f704afa87927103ce407efb59de22e2fbb76aef110b3b75da2a7f552301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:688a8d17441926d680c64d52a17ba261b73b29bd6955bedb3ae74a10c8716154
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287552644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6447aa6b1e22be7b61d8470d3398317b8705fc464924d411b8156ecd6057f40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:15 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:18 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Wed, 09 Oct 2024 15:42:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:45:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:48:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43ed7ac192d3f50e551118286d2a59c5cdf9ae247515319b137995d2d91c1857`  
		Last Modified: Thu, 10 Oct 2024 06:10:56 GMT  
		Size: 31.5 MB (31497006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebe8581de16e2d108a8b8b443bb95f82e5cad32c8f55539cb51fdde9b3436ca`  
		Last Modified: Fri, 11 Oct 2024 23:49:36 GMT  
		Size: 15.4 MB (15351852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd7d65218420548fcafac6b160a3d5aa59ecc023e7dc66b84b5bc87977eed4`  
		Last Modified: Fri, 11 Oct 2024 23:49:52 GMT  
		Size: 46.6 MB (46552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00338c9ed1170da053bb792bbac38340426de9df9e9b33bc25b0145812151182`  
		Last Modified: Fri, 11 Oct 2024 23:50:24 GMT  
		Size: 194.2 MB (194151652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull buildpack-deps@sha256:a5dbad1736e445c9255daedd2291c1ed47071678ec62d7597c9bfc2e6151dc4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387512083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d6847932498e61a798352ad0688d37e20d3985f1cf61de61ff856afb6b0c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:10:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b19496a8d9dc226b4d60c0384e37525cab9161d87adbd6637828dfdeb65fda`  
		Last Modified: Wed, 02 Oct 2024 02:18:51 GMT  
		Size: 54.6 MB (54636883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1257422a528ad068c80493bd9a6a64aeba863bbaf8a67d7570a247d274ff1c15`  
		Last Modified: Wed, 02 Oct 2024 02:24:08 GMT  
		Size: 276.1 MB (276124113 bytes)  
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
