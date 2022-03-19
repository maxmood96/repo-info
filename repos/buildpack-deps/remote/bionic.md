## `buildpack-deps:bionic`

```console
$ docker pull buildpack-deps@sha256:3b8b91e8ac5f6af361b274461447323f8d30a2d02b06ad80e1d580855d6fdeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:711f9198fc0fefc5fadd852ffc856129c39ad5b30cc218ffc33dd54e01b7737a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221262803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043b5581e482d74d87d7a273fee5d6c02b5194e0527c348f4aa13216b1eb6ec1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:38:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:38:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:43:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222ef3f2ac944896d21cb971be4b7ec028ac826242cd0451df060b0b4412b92f`  
		Last Modified: Fri, 18 Mar 2022 07:08:55 GMT  
		Size: 6.6 MB (6641832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3f005ad8fda9d934f3bab809914d7cf447e57835543823c59da423475b8f58`  
		Last Modified: Fri, 18 Mar 2022 07:08:54 GMT  
		Size: 3.0 MB (3022305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bdf22b8f5807b9c0526a9d14e169c45fbf72a2cc495e590f2968bcf46aefce`  
		Last Modified: Fri, 18 Mar 2022 07:09:15 GMT  
		Size: 45.5 MB (45484444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597455a035aafd313f924d74e80a86055df04b0cf358af47897db1a1aa48a048`  
		Last Modified: Fri, 18 Mar 2022 07:09:47 GMT  
		Size: 139.4 MB (139405588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:36515c95fdd99f961f34869564c9e335f87663b1e2a5ecaf114caa1a56763558
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189469725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5901da66f07f6420c59c7ae9a18c45c6513e87dbe05433e0ccd511e18a1b75bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 07:32:19 GMT
ADD file:05014e7be574a8703e7ca668f8ff20d708f1860234bc44e3ef9e9a15193ea2c2 in / 
# Fri, 18 Mar 2022 07:32:19 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:07:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:08:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:10:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d423dfb8c4fe22914d518a0a7c648903c4159e75b2ddd41c2d7dd27c5af71078`  
		Last Modified: Fri, 18 Mar 2022 07:35:55 GMT  
		Size: 22.3 MB (22308133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dd41a6c49eacf0df81b34978f371986d045163bc627fc8cc72de7188772b43`  
		Last Modified: Sat, 19 Mar 2022 03:40:45 GMT  
		Size: 5.7 MB (5712348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd796a264aa4c81e3c709b9f64a9058add3ff5a5d6182545c52efe99ffacdc7d`  
		Last Modified: Sat, 19 Mar 2022 03:40:42 GMT  
		Size: 2.6 MB (2584607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082f0bde1e152ac77e4ab26f624f3d2205c3ae15f1bbe59b9ee93647f4fd409f`  
		Last Modified: Sat, 19 Mar 2022 03:41:24 GMT  
		Size: 40.7 MB (40678154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e77c596598dca280e79a2a558eeec4f109cae46b1ad6ed4f0c1696978468166`  
		Last Modified: Sat, 19 Mar 2022 03:42:48 GMT  
		Size: 118.2 MB (118186483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4f8d2d22700c21ed1c8e8e857862e9943531bf0aeb62d2f84616872dcaf95ae6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205379293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee97f378bf8a6fa5ca92149a16d526b8189884a85b3159a100bf5403b0277776`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:06:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:07:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:08:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b00c8ed3e482790555b6ba75dc2fe88a431898579874f982bd42af6e94adaca`  
		Last Modified: Thu, 03 Mar 2022 20:16:15 GMT  
		Size: 6.1 MB (6082527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a1859624fa4241536a77dd88b7f379d0cfcecb8c9d1647065d1fce7976682`  
		Last Modified: Thu, 03 Mar 2022 20:16:14 GMT  
		Size: 2.6 MB (2570125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3bc0765bf07acd739d63b3109b54f69ce5a1785763501059461889ceea1a45`  
		Last Modified: Thu, 03 Mar 2022 20:16:32 GMT  
		Size: 43.3 MB (43279617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c295abf0e4234a0649136ef1aa4dbe6c6c84dd7625772677a3a1b64dc030290a`  
		Last Modified: Thu, 03 Mar 2022 20:17:02 GMT  
		Size: 129.7 MB (129717373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; 386

```console
$ docker pull buildpack-deps@sha256:769cfcc39b6e1d77c474e85867e453c7ebd97342ee084f2cdeff17cbf8043ca6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218565900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73aa226c519c3d5ce21e67753b99aa7aed4bd2d507079728ed05cd2d496f2c5a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 10:41:23 GMT
ADD file:72f05c1b10aca0acb5e79b003217b981354d67a2f72a45a5a48a74d5a22d8a52 in / 
# Fri, 18 Mar 2022 10:41:24 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:35:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 14:36:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:40:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ae2a3052b0bf32822826824df976f36386fcf8a79f3777f41da7a64101a1603`  
		Last Modified: Fri, 18 Mar 2022 10:42:30 GMT  
		Size: 27.2 MB (27162241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7b56172011c8d88198bee93c2bf6f3b33ad52348cb1380b5cbb47138aa4044`  
		Last Modified: Fri, 18 Mar 2022 14:49:48 GMT  
		Size: 6.9 MB (6930126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed6e7f33485b705fec685d6fbe7cb0623696f9ffab68a00b24fe2dc017b4eff`  
		Last Modified: Fri, 18 Mar 2022 14:49:47 GMT  
		Size: 3.3 MB (3252133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b475cba19b8800cf85b056af754966505777f465718e474d9901aca6d10253`  
		Last Modified: Fri, 18 Mar 2022 14:50:11 GMT  
		Size: 47.1 MB (47067894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0221d51e9f8060a527fd2ad118418a55053e30edb74e48ffdd3570479ca282dc`  
		Last Modified: Fri, 18 Mar 2022 14:50:52 GMT  
		Size: 134.2 MB (134153506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f8be3212545883e789575b44cb206986a40c19c2b59751190396154af46c6d15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246243860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27af270c150168216cbe66819fdcb0e591d1bb3ff03fb664b270ad9672984118`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:09:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:10:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 06:11:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:17:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1830b6c456b7475c45d963eda213b02483fc132dc1a3a8a912694395f1556c6`  
		Last Modified: Sat, 19 Mar 2022 06:49:09 GMT  
		Size: 7.1 MB (7056588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f35c7c52bcdc240668649aeed659e09476496c4c7a0fa05fcbdb7bed19e76d`  
		Last Modified: Sat, 19 Mar 2022 06:49:03 GMT  
		Size: 3.7 MB (3719308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ad29e0143d51c4eb9be5f7f43a5c00475708f80c406a070df25b58b889631`  
		Last Modified: Sat, 19 Mar 2022 06:50:04 GMT  
		Size: 53.7 MB (53723900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c405d423b22406b50da5cda99d864143776a6b4f74e3de1fef4c084bff0fc5f`  
		Last Modified: Sat, 19 Mar 2022 06:51:51 GMT  
		Size: 151.3 MB (151306008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd5b2c8bffcb885487d2f22b83ff20f7e4e7df9aae234262a6c27fbe3539554f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205472612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69db5d760393ecfd009cbd7cff902ba30245f92a84793ae7f210c3f3b00bd787`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:02 GMT
ADD file:ca83c77547f5f41417a9bcad24827780f3cecda3aadc05e3ea075ef651e7a96c in / 
# Fri, 18 Mar 2022 00:37:05 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:05:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 17:06:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:06:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:19966aaba2fa737074d039f29b54f413d837daaa9d85f02bc54eddd7d645b73c`  
		Last Modified: Fri, 18 Mar 2022 00:38:33 GMT  
		Size: 25.4 MB (25365461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f707de7995f967781fe849ea5a655fcb09a909fd6fb0b137984e23c20e247748`  
		Last Modified: Fri, 18 Mar 2022 17:14:33 GMT  
		Size: 6.3 MB (6332555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b377478018a8c1dec3ff1d3e1c0d8db2e042e1ab1fe80f7f615a0f777ad6d4`  
		Last Modified: Fri, 18 Mar 2022 17:14:32 GMT  
		Size: 3.0 MB (2974971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c065ee36aeeb2fa0b5ab382cbd1b4d5f53998d5179b40d2de303ae6b25b24`  
		Last Modified: Fri, 18 Mar 2022 17:14:46 GMT  
		Size: 45.0 MB (45014206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daaf5cfecc67bd5a4f07490b14311d87722c6e1a60d3dc799fe972cefdab3ef1`  
		Last Modified: Fri, 18 Mar 2022 17:15:08 GMT  
		Size: 125.8 MB (125785419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
