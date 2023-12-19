## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:e6b37bebcc02476b82ae0cc3d31f7f0a6d6f91157260656a80a75e2a19bda489
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
$ docker pull buildpack-deps@sha256:c845ddbdbb0fa7e4bd3cf5974fc76b42adb5f8c56dfdb8bd4bc1cdf5eea8a316
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (403022326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37917f3f1a9598b7f32def6b58c12fbc145e485fc831ce2aaef3982ae65869de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:38:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9565a064a4e2c8d2e24ea50bb5793fd5453d880cc1268075d4c95136016c2`  
		Last Modified: Tue, 19 Dec 2023 04:44:29 GMT  
		Size: 66.0 MB (66049037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6485f47f21b2f643a2d43d6b92fe5745eb69bb2804ae95f0bebc3e1ec52b8c7b`  
		Last Modified: Tue, 19 Dec 2023 04:45:09 GMT  
		Size: 261.0 MB (260959970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3a4fa67d6308c9d11531802a1714b7e3a30f7a0e2fdda70c23e2ec9565eb1350
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370914489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b521f21f6e40b32094690d87fef9846447df7e982f17cdf3775c7078d652fe9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:28:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1076957cedc8a5a67b5ef8a93c803e6193f70ae925dc66e3135d08c87986fa`  
		Last Modified: Tue, 19 Dec 2023 05:34:49 GMT  
		Size: 235.1 MB (235059785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c4f3adafcaaa3a74ab0c389dbee048e266cee7902ac8f2a0c9b3b329206a83f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.9 MB (346946886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9651f5c610972ab54d4d023955e6103f1ca8ffe1648a9a4ceeabd6b881b0981c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:12 GMT
ADD file:5e0189fc7402da5b92ea3c0f1e4cde0f5f56258cfb29bbf3fa29767c1d430c76 in / 
# Tue, 19 Dec 2023 02:09:12 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:01:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:03:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ad57ea9eca16d7e9ee7827f31dfc15f264b708ab11728a7935b2f23ec3f42d3`  
		Last Modified: Tue, 19 Dec 2023 02:14:36 GMT  
		Size: 44.9 MB (44898763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd55d116127ea8cdc765d3307e52ea259fb1ac1a89e4303e4ae51e5781e544d6`  
		Last Modified: Tue, 19 Dec 2023 08:09:24 GMT  
		Size: 24.1 MB (24091856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a0b12321836cb81d9731b0251034aa0aca0333c7b777bf5565787fd9c86a6`  
		Last Modified: Tue, 19 Dec 2023 08:09:42 GMT  
		Size: 61.0 MB (61025413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd5af8e3c55dbb5066fb3d6f4342030e6c5371f638082299c9ef1f4fd0b7cd8`  
		Last Modified: Tue, 19 Dec 2023 08:10:20 GMT  
		Size: 216.9 MB (216930854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e20fa8d58f288f40a7caa444c147017beb16cb86bd5b9c6643c78f5987316dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389318431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3788047583bea1aaa8992313e98de6dc266c2a82f79c1190e19df2dc83ef745e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:39:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f38ee39d2143cc6781c8d40b267519e59c558f7902df442f2e5ecfcefb01689`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 49.7 MB (49689786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec939d1d3b6574ac3482db9be62850fd83b1612f01d44fb296af8ed464c33f1f`  
		Last Modified: Tue, 19 Dec 2023 11:44:56 GMT  
		Size: 26.0 MB (25983709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591136ec6e5960d51ec4ac04b638e9bb1afe645fd53be0f002e76e7d236d522b`  
		Last Modified: Tue, 19 Dec 2023 11:45:12 GMT  
		Size: 66.1 MB (66149784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5ad01f173df3982c94ba452286767ffb8a3e0e3eb42a4d4551877d1056860`  
		Last Modified: Tue, 19 Dec 2023 11:45:44 GMT  
		Size: 247.5 MB (247495152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f223534a49fdd91590e92469d3b44a3b66e5187cc236c26c9f45150a59d0c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.8 MB (403778905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9a75df9181fd5bf88807fe290de501affc38a281b1db10a31e07aa69e35cc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:33:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e5706d82a57d517f5b2faa92178f9346b9a474417ad5a9158a842164e920a6`  
		Last Modified: Tue, 19 Dec 2023 03:40:36 GMT  
		Size: 67.8 MB (67809651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1c36b513ad68c22e61b529691192c0fc48c4d221456d5d0e9c2369fe1553ef`  
		Last Modified: Tue, 19 Dec 2023 03:41:34 GMT  
		Size: 258.0 MB (257966559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d5e4e403e5b231279b9a643c0e32b8d3eb8d640c2debc18a403b750a5ee69bd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372669397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6405ec487dc34ccbdc687f1e61d093d714dda4add87ff3db3ef75cd70e666ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:08:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:15:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539b334e5a1b4f830e2cb90767d1d6bd23065595b3d40e6cd589ec973f33276`  
		Last Modified: Tue, 19 Dec 2023 03:26:15 GMT  
		Size: 64.9 MB (64877294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0428530ea0a6a33939b2c19cf5f38e214292abff9ad746bdc4afcfea7397bcd7`  
		Last Modified: Tue, 19 Dec 2023 03:28:48 GMT  
		Size: 232.3 MB (232306893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7c59c7b1d7a8d1ad9e1365acb6187cc0c56f7faf991c90e3f5b74c7e21601af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.5 MB (412493320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118e9cf52ba29c12c8b430e13c7830977d77914fe311c7009d7ff4db169b33bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:00 GMT
ADD file:ebe2bb6638a51888bf27d1bb5ca609a91df94474b4abf70f874e60b653885a2e in / 
# Tue, 19 Dec 2023 01:23:03 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:02:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:13:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:97954753acf4d5cb589b2a49219ffbc5c86834cb864ed80f516370017ea3c569`  
		Last Modified: Tue, 19 Dec 2023 01:28:17 GMT  
		Size: 53.5 MB (53455717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf9bc2559c9bc0dde88b00d18449e9a40dea5919313c9dba6b3a432f24542e4`  
		Last Modified: Tue, 19 Dec 2023 12:25:16 GMT  
		Size: 29.0 MB (28960588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bcb9d372effc2b9eed2bc00b534deeaf705ecf5a3705a53bce008b65768d0a`  
		Last Modified: Tue, 19 Dec 2023 12:25:37 GMT  
		Size: 71.6 MB (71584185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d68a49298b0a4e3725e9f200ab89754fd611e60f4a3da3511f6c2e48d2407a`  
		Last Modified: Tue, 19 Dec 2023 12:26:23 GMT  
		Size: 258.5 MB (258492830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8da7b54261080b809f45176c4399c2a846f298c5dca668c5ef9d891960e05619
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.9 MB (435912718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66322a3b41a21a07cd1c50aaacb0216d49a586c240665706c1eb10bfe1357d36`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:41:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe6c23c39483f54e5cc09f3805cbea29d02f6bbc773bf62d752dbdc74d194e3`  
		Last Modified: Tue, 19 Dec 2023 02:43:08 GMT  
		Size: 65.3 MB (65295558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cdabb923ae43d95eb49f5a86e41045d58be42c151b0890419973020357d956`  
		Last Modified: Tue, 19 Dec 2023 02:49:01 GMT  
		Size: 296.6 MB (296602883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6eb7b3c0214124b542533ba0fc31d39e82f75308f588e3baa495d169984e5ca1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377122453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730c494cd57b015272ae2ee4e507a11fa9dc82e54e83c8c5bd7da9556d868828`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:58 GMT
ADD file:787d19e6a77aebb4de0df132b1de8d62f9d4c2c2d0181bd2c57d043a742aba66 in / 
# Tue, 19 Dec 2023 01:44:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:49:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81a71db9a04e29cf0934e3f04c4935c1dad336d34d53ea6877240b19747c865e`  
		Last Modified: Tue, 19 Dec 2023 01:48:45 GMT  
		Size: 49.3 MB (49328178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f2e8658adec6b0269494f8fb2af7c207978a293ef3251001e591960530e6fd`  
		Last Modified: Tue, 19 Dec 2023 07:55:14 GMT  
		Size: 27.0 MB (27038321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966a7cc784826f7ec8c32d88dd36bc8a9262f3b9612fd9916ba143c8e3362629`  
		Last Modified: Tue, 19 Dec 2023 07:55:28 GMT  
		Size: 67.1 MB (67083999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0a1c8816b878e3e009d2c77bee6407de8c6e49137b7353e5999f199ea5a4e2`  
		Last Modified: Tue, 19 Dec 2023 07:56:02 GMT  
		Size: 233.7 MB (233671955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
