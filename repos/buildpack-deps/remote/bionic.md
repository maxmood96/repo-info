## `buildpack-deps:bionic`

```console
$ docker pull buildpack-deps@sha256:0fab53fa36fbfa341fe978475fc347f0988ce79f9ba2380a6a4877d00906bf49
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
$ docker pull buildpack-deps@sha256:bc57779017d71b1a08afd1ea406121fa1830a1d573d518b37f5dc12582d8a948
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189472698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd83c0e698d7ac4512faa38c4f646f4221d49fc023c7b91d589f1108d8874b0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:10 GMT
ADD file:c60e89df1905b44d4771a78ca9fa8113b55681f00e5bb55e798028b77ce6c120 in / 
# Thu, 03 Mar 2022 21:21:11 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:15:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 04 Mar 2022 03:15:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:17:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f04b2e36c59d7fb6bb1129d2ffaff71df9aa51f235875df61b423ebbdfcc1ae3`  
		Last Modified: Thu, 03 Mar 2022 21:24:40 GMT  
		Size: 22.3 MB (22308282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e431ad97ffcaf1c68228dcb4bf9624755667fdf428dac81d5cbd251b22c35`  
		Last Modified: Fri, 04 Mar 2022 03:35:17 GMT  
		Size: 5.7 MB (5712255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c19bea23eeb8e7d57acd3ab7f212f26d69090b55badcd6895f6f6389931551`  
		Last Modified: Fri, 04 Mar 2022 03:35:14 GMT  
		Size: 2.6 MB (2584690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54df356838df872dac4dc29b1cfac075a84ba1fc6f14327bd37c730b4a0b191`  
		Last Modified: Fri, 04 Mar 2022 03:35:58 GMT  
		Size: 40.7 MB (40677575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064a3e6844e5e9b3dca7e5824af34346ceeb6332d43e8e0cce3d88b8fa3f4b0e`  
		Last Modified: Fri, 04 Mar 2022 03:37:24 GMT  
		Size: 118.2 MB (118189896 bytes)  
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
$ docker pull buildpack-deps@sha256:bb94c277078fe667e4cdfd36007dc41d205473555cd32e4eea5c7eeb4b23a70c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218569370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad2710d95439df211e5165eeb66b5039b76f78899e472382ae941a741daeb84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:18:47 GMT
ADD file:2ae34e7bffe3a59f3167a286025a093609188772be7b14601867a334bb3c0166 in / 
# Thu, 03 Mar 2022 20:18:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:37:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:41:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:250799bdfa37968bdaf47cc4d86f759e4e574d5e795f888e42c66ec0b7e92034`  
		Last Modified: Thu, 03 Mar 2022 20:19:35 GMT  
		Size: 27.2 MB (27161874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac28247ef04d1b842fabfcf6c1d41142412aa75bc7a718d9ee2f0a5294e7fb5`  
		Last Modified: Thu, 03 Mar 2022 20:43:48 GMT  
		Size: 6.9 MB (6930049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4db160b7628ac1a70c90af6b530d3f743602f72afb95d72926eb8e64f2348b`  
		Last Modified: Thu, 03 Mar 2022 20:43:47 GMT  
		Size: 3.3 MB (3252130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cbf4098c0549d70474da4743f711339b52599ece179881e218aeb9abfa3d01`  
		Last Modified: Thu, 03 Mar 2022 20:44:11 GMT  
		Size: 47.1 MB (47067930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87413c329694037f7040bd671b886aef5f4272680105efa43b0d55122537081`  
		Last Modified: Thu, 03 Mar 2022 20:44:49 GMT  
		Size: 134.2 MB (134157387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c2aab327f37923a67401f4903dbb2ca3f169edcae0c29c1fba83795dc2b9992b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246243280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de03fcf78c113c80ffd51468c969e1bb94b0190d7fa26924c9e97789181a7e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:11:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 21:13:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:20:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253aa808a4a4801d83aa1d00c4ad4634c1f77aad211d65ef2ae9e34abdf1194`  
		Last Modified: Thu, 03 Mar 2022 21:56:52 GMT  
		Size: 7.1 MB (7056561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945feb70f5ae95204f28dcb65ae6b9b5784e8fd4ad76bcbddaa6807a2347f9b`  
		Last Modified: Thu, 03 Mar 2022 21:56:45 GMT  
		Size: 3.7 MB (3719275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c0d1b13d6f5f94f46b37dca9eaef53960854bf39f26a3d8eaad6aff832e503`  
		Last Modified: Thu, 03 Mar 2022 21:58:18 GMT  
		Size: 53.7 MB (53723826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335ce2ca6462adb845c5ee2727d25a7aad47bcc0e7205f639d1efa3fbe35d62a`  
		Last Modified: Thu, 03 Mar 2022 22:00:43 GMT  
		Size: 151.3 MB (151305651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b84e11f1495074f75f8d1d7ff7002372b12bc995f5cbdb716511e70a2c6b88f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205466127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6600a11c2f5110e60ec287d4a5ad9405e9fcae2cbf56be4dc95089092e285a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:41 GMT
ADD file:84b8165a5044433cc2f9fdf9670d391f085aad3799d5e6dae035f8338dbe6081 in / 
# Thu, 03 Mar 2022 19:41:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:33:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:34:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:084e045c78b3a9e38ef6caaf47c3ef1c3d672d3cc2e60543ae9629511a5e1c8b`  
		Last Modified: Thu, 03 Mar 2022 19:43:09 GMT  
		Size: 25.4 MB (25365258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f451b0973e7815327265ae400866c266a9df0155f7711ddc54f80cda51301f0`  
		Last Modified: Thu, 03 Mar 2022 20:42:23 GMT  
		Size: 6.3 MB (6332491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae3cd2e93934ab0fa445573a52ddb393438bacf99a6402e72555da0ec0b4a31`  
		Last Modified: Thu, 03 Mar 2022 20:42:22 GMT  
		Size: 3.0 MB (2974972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60792c2aad4f31dd07cf0869cbe9a56153e7fa49039825aee8074f6d4afebbd7`  
		Last Modified: Thu, 03 Mar 2022 20:42:36 GMT  
		Size: 45.0 MB (45014464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653034ad6109264b96473c67cca948e07654bae4792aa75f8f592acbf2a5c6eb`  
		Last Modified: Thu, 03 Mar 2022 20:42:59 GMT  
		Size: 125.8 MB (125778942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
