## `buildpack-deps:kinetic`

```console
$ docker pull buildpack-deps@sha256:b05322e0ee14d6e79bce5c5b75fe7c5b9a53414e6bc1f728c50a80a2289e189e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3a758ae57c8a7346ba305b53acd626f697ff9eb9f0a1bc2e35ed8aa0fd4090cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258713730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ffcea5f1bfb263a26234b8ad41d79b047fde2acbf3c33f0f64f7d3e7a27f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:52:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:55:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62a5d402f83137154c8e54f4f370e9f9f70b5a6892f6ec8cc2fae7be0fd8ae91`  
		Last Modified: Tue, 31 Jan 2023 18:03:39 GMT  
		Size: 27.5 MB (27479169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242f8f31e97bc8f200f610260668952e0a909150c1e95f494e3165edd6a4e74d`  
		Last Modified: Tue, 31 Jan 2023 18:03:36 GMT  
		Size: 6.8 MB (6764654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddf4e3936d1208458d4e3e5395b8b86da6f3f7ef3b30242decd50ee0403f1e9`  
		Last Modified: Tue, 31 Jan 2023 18:03:35 GMT  
		Size: 3.6 MB (3635171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b0d398ef08d48d4f39203eb13897978a42e2aa1da1465591c472c03f5975ec`  
		Last Modified: Tue, 31 Jan 2023 18:03:53 GMT  
		Size: 39.7 MB (39740240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01848c64b150b130ec1ae2bc4551ec1f49701b2de7a636fb9197ed2381f48a9`  
		Last Modified: Tue, 31 Jan 2023 18:04:26 GMT  
		Size: 181.1 MB (181094496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce7c70076739ba63f556eb699ca14f8cea9aa71e0c829f91ef69a6d112a71053
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221844903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d4c66aafcef498970b5cfb0585f0a0259e3e44af1ff79408b112780ab34da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:02:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:02:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 18:03:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:06:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3689a8df2bef3da04eb6dd3992a8a12da08076bfc3b502ebfd175c90d3befc1a`  
		Last Modified: Tue, 31 Jan 2023 18:17:39 GMT  
		Size: 25.9 MB (25892003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd827b5dcd49a319ffaf18db83f4d8e6234d1a0a5ca59247e525d46959e950`  
		Last Modified: Tue, 31 Jan 2023 18:17:35 GMT  
		Size: 5.9 MB (5935215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c4c2c8c1755f8908e4f7f6c8064b5226752b53649ff4a6117d436f2601c4ab`  
		Last Modified: Tue, 31 Jan 2023 18:17:35 GMT  
		Size: 3.8 MB (3800385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f492152c4ab9f5296bf0518ba5fe9c7f99cd49599bfd99ebca9bc5c32d14b`  
		Last Modified: Tue, 31 Jan 2023 18:17:58 GMT  
		Size: 42.6 MB (42613683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca092843df5ccc27cc35048a327c2eff75993b952a2d3bac1923cad4afe4eb`  
		Last Modified: Tue, 31 Jan 2023 18:18:32 GMT  
		Size: 143.6 MB (143603617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:75712c8314b8699bf216ddf2252b05b7650004e43c3f63f261d00feb65a3b6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246697214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a2c33d0062a7f8588a0cb9df7c0fdd2f82dde2c2faa4468870ad8b74412aa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:18 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:20 GMT
ADD file:f61617371f6963c6be2852e2b94d04e8507feb8f77e3484c94aa8b9d0ac67f76 in / 
# Thu, 26 Jan 2023 12:08:20 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:24:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 18:24:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:27:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44d97c2a5ae0fb5d56de8a6242583e80e9265c58a742eb1e52d40264d9f034e9`  
		Last Modified: Tue, 31 Jan 2023 18:35:38 GMT  
		Size: 26.7 MB (26699721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b285ead03b32399f7eb21eb63769c45b64c8b1731dfc244904cc2e9a8262a`  
		Last Modified: Tue, 31 Jan 2023 18:35:35 GMT  
		Size: 6.6 MB (6595500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855afc623fecc9cad347ac6e791b5bb08dd8331201f22400b2764672b1e9a48c`  
		Last Modified: Tue, 31 Jan 2023 18:35:35 GMT  
		Size: 3.6 MB (3602406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb8fe5b73117b2d29e76fe2d924c4310d621681b761a3e4efcce5bd6842cb3e`  
		Last Modified: Tue, 31 Jan 2023 18:35:51 GMT  
		Size: 39.5 MB (39523097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a13a0356c3c1fefb6afeae0373f345a4200ce0ef8d8c9e383948efc6d1c22d`  
		Last Modified: Tue, 31 Jan 2023 18:36:20 GMT  
		Size: 170.3 MB (170276490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:39314d421779e71395dbf25c5a7c7a6ef6515a692304a576870c50b83b208938
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281283945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378e98d0d7fb14e25257a0ba00eb60fc2e01ca1b97ceaa7a95eef16b9248db6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:59:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 18:00:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:04:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a06c15ccb04b9b73efad888bdc885d26bd74537d9322b6629f3b3ef906c0756`  
		Last Modified: Tue, 31 Jan 2023 18:18:11 GMT  
		Size: 32.1 MB (32109752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ee7c83faf85e0ce7383151d494b3fbc177d548f264c95b2dcbf49dca2d06d2`  
		Last Modified: Tue, 31 Jan 2023 18:18:05 GMT  
		Size: 7.7 MB (7741886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e688b449cdca40b587631310483952ae87bf319f0b7d13251a6a085f60c05db4`  
		Last Modified: Tue, 31 Jan 2023 18:18:04 GMT  
		Size: 4.4 MB (4362437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecff49481c045e5964caf1cd33337e518465376e603f708da227d433ae19a74c`  
		Last Modified: Tue, 31 Jan 2023 18:18:35 GMT  
		Size: 44.1 MB (44142262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbb04761be0c3739265acca2d4d506ca2d2a045b958a8b9c295a0c33484a051`  
		Last Modified: Tue, 31 Jan 2023 18:19:33 GMT  
		Size: 192.9 MB (192927608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:055682a7d364b6446f71c183013b8fa09e34676449ecec2badd5b3c7501878d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279961617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6349540bb494e841c30d22cbe12393db1ab572bc07d37c0e26b18f10522e0f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:14:46 GMT
ADD file:7e2bfb25c400fe48fedbb3adb245a3bc6b40ec07dae2feeb339c704b967ce658 in / 
# Fri, 09 Dec 2022 01:14:48 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:27:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 09 Dec 2022 02:31:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:38:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:080423a9398e3d16c0feb2851e7596ddc2d8d33fdfb3bf0b4a881619b9b86c9f`  
		Last Modified: Fri, 09 Dec 2022 01:37:40 GMT  
		Size: 25.6 MB (25640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982116c46b9fce2e4125cb4441dc6ea9b142d29299c9688061563ccf1bbdcbb7`  
		Last Modified: Fri, 09 Dec 2022 03:05:51 GMT  
		Size: 5.9 MB (5927602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbcc60f8c38f4ecde864a8f7de2346f74cab29bba32ed107631a7787694cdea`  
		Last Modified: Fri, 09 Dec 2022 03:05:47 GMT  
		Size: 3.9 MB (3881582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb006617ee17454543d3385ca40746e427401f035dede49af59a38106e7731`  
		Last Modified: Fri, 09 Dec 2022 03:08:12 GMT  
		Size: 42.9 MB (42857867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfb100dffdbe660e12e145d20f7ed2887b177dad698ae515f00a459c4804a`  
		Last Modified: Fri, 09 Dec 2022 03:15:25 GMT  
		Size: 201.7 MB (201654307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d1b7f50c9f545d3504d52d8a1cd6dd4a15ce64ab075d2f1955dcef467fc3a47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228596958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d546f7822fba9006d358b9d186652f2af4a869ec2464c6c390bd1dd2ef6c9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:47 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:50 GMT
ADD file:a83afd93816f868be76d243df85b87a66b39d5ef0497c3cb8d0bba2bd4a27c40 in / 
# Thu, 26 Jan 2023 12:08:50 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:45:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:48:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5bec5e5b1f8afd82addaa8ef129ee5026d804c474c34ca3e565dfa18fa5f877`  
		Last Modified: Tue, 31 Jan 2023 17:56:19 GMT  
		Size: 26.0 MB (26029773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888884268a5ab3f78486597366fa902253286ebe039958a9950d8ab78853d5c5`  
		Last Modified: Tue, 31 Jan 2023 17:56:16 GMT  
		Size: 6.5 MB (6457669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7aa7ab93554822a6ee5149dc403f0ba1aa47ed227911574510630a9383bf8f`  
		Last Modified: Tue, 31 Jan 2023 17:56:16 GMT  
		Size: 3.6 MB (3625074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173761a853e728963d055e12ba7bf5951b85d93c0ac60955fa793be53aa69f57`  
		Last Modified: Tue, 31 Jan 2023 17:56:31 GMT  
		Size: 39.6 MB (39552159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2930464a0032aa36dbe69f2c0b3faceaa7a67f8de234438b28d703357998a09c`  
		Last Modified: Tue, 31 Jan 2023 17:56:55 GMT  
		Size: 152.9 MB (152932283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
