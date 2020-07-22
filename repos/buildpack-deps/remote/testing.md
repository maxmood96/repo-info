## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:46ba8602b9415ab7b9ab6e70fc346b4689b1930d26d0038d098ddbae6cee3441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:57aef7de1cdb9e759c80e37fe791a60c8c97223d32ba4e82646e488cbacf221d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325522161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c73090c8673aec5852e87ff0e55e82f5e1ee2e52a835d2c40a5ec19ca9dddf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:10 GMT
ADD file:5c0c0fbac6fe503c1d3e894e0b3b1081172862074ceed378a7e4b82810536415 in / 
# Tue, 09 Jun 2020 01:20:10 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:44:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:44:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:45:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:13 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07f1101e3e85b531862163b4177bce7f401eac107a6537ab74195b395aab30b7`  
		Last Modified: Tue, 09 Jun 2020 01:25:12 GMT  
		Size: 51.4 MB (51413507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3778b8917e949d9f5a076dfa475de8efd560f3537663e53ea97e720164dd04a8`  
		Last Modified: Tue, 09 Jun 2020 01:58:55 GMT  
		Size: 7.9 MB (7920377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4483e6954e0bd5f111c062eb05965cd7e6719912e726370891437022744c5b6`  
		Last Modified: Tue, 09 Jun 2020 01:58:55 GMT  
		Size: 10.5 MB (10488194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4457fc20950e802370e7f15361944b8f58ae25f895ca6cd42e008e97f37e60fd`  
		Last Modified: Tue, 09 Jun 2020 01:59:10 GMT  
		Size: 55.7 MB (55674519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dcee82f1257b02150abd101eb520dc5c25b1c321e1d7eacc4261ae147e340b`  
		Last Modified: Tue, 09 Jun 2020 01:59:47 GMT  
		Size: 200.0 MB (200025564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:425ed04e9f7cb99e6afe88a392cf818fdc6e6bf4a22214384b5254dd1f577080
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296954782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9c18be4d22822d436ad3abd73957b0fc16c8c60313d0d9c63aa4da686d5dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:50:42 GMT
ADD file:ce6e6e497a66e2260260f97fe2b75c1b96d64554c5be6b85940fc97e2668da58 in / 
# Tue, 09 Jun 2020 00:50:47 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:27:37 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0cdc268ccc707144d53d65848999b81d39614c650312788e7e7f99c56bad6d97`  
		Last Modified: Tue, 09 Jun 2020 00:58:27 GMT  
		Size: 49.4 MB (49386621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86dad966a8a2c2ed7fa83ce42c1fab459f250a20c801eeaf7703e5022cf7bfe`  
		Last Modified: Tue, 09 Jun 2020 01:56:29 GMT  
		Size: 7.5 MB (7500258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380110dfa23bbdc9c556dbde735e0c5c0b768f93dfc86e54d0c9e2adb417562`  
		Last Modified: Tue, 09 Jun 2020 01:56:30 GMT  
		Size: 10.2 MB (10175863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1be4fce84e1c9c761b63c553df33838f2c301c69f612c6a0c17003702eadf4`  
		Last Modified: Tue, 09 Jun 2020 01:56:54 GMT  
		Size: 53.3 MB (53307662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8388b5fc5bcc9bc0d7d2acc967a0bd5cfbfae03e084fa408578eaac075c94f8b`  
		Last Modified: Tue, 09 Jun 2020 01:57:55 GMT  
		Size: 176.6 MB (176584378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4e3d210d206bba445843eaba2fc303aefc8ac7f31a9af2bbe6b8ef8662e36143
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291330420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba052a69263334c26e38cef9dc3e2ed9d7586064bd2119b447db5e98244ac81`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:59:35 GMT
ADD file:2ade41d5fab2319a3cbf973cc24aec4f6b9e2b14fa04578886fa1cbe30e511ef in / 
# Tue, 09 Jun 2020 00:59:37 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:37:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:38:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:38:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:45:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c27049a799a3404864ae1732d5aeaafaef7ce0fbbde552819e2c88bf38ae9da`  
		Last Modified: Tue, 09 Jun 2020 01:09:22 GMT  
		Size: 47.2 MB (47197823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b26b1bf1a6c82f64fb3246383f0e2081a0624861a1d56ae6b025e7406652be`  
		Last Modified: Tue, 09 Jun 2020 02:09:55 GMT  
		Size: 7.2 MB (7243223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad054395bdad7163609959df4dbaf402b1787fb76da08b5c5f89358ac9f2e1`  
		Last Modified: Tue, 09 Jun 2020 02:09:55 GMT  
		Size: 9.8 MB (9823296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf531c73c6f446da9fd9e5bfae5da82ba0d7fc288a2c05cb2981e723a94e0fc`  
		Last Modified: Tue, 09 Jun 2020 02:10:19 GMT  
		Size: 51.1 MB (51087430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154b30b2124bd929686819651eb81c952b787fb9c92f9ad64a92f80deb2bc163`  
		Last Modified: Tue, 09 Jun 2020 02:11:12 GMT  
		Size: 176.0 MB (175978648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30d92ad1321fc59bb381f5035799610fec5373067bbc3efd3f101ffd8f9b9161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329537288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cd90b60a941d141fcff77308cfe5b60a4b4e459f268e1358b3dcc30f59c01c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:39:52 GMT
ADD file:19b87dac8088f103e1a9992c229b17344439af0da8af45bc6d678f69471077d4 in / 
# Wed, 22 Jul 2020 00:39:54 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:09:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:12:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:16:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:508fd3fb95b7fcde22f3f927caabf293cc04dcbdb4c45b85a5130d5122e12a0c`  
		Last Modified: Wed, 22 Jul 2020 00:46:40 GMT  
		Size: 52.9 MB (52886369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5915a33a39d2dc36bde47815617bc03c29dc80e9539719e24091c59faeb64f73`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 6.6 MB (6634801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ea5d467b9d2286b1dcd428b411982c7ca3d5a2471f013ef721842af48ec9b`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 10.6 MB (10591622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ce2f62ac83f0fb7af53d2e4faa8b93e2b37157d2cfd0eb7725e95b633a33e1`  
		Last Modified: Wed, 22 Jul 2020 01:34:12 GMT  
		Size: 57.2 MB (57203269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40485f6c44a09a9e2f05943531673fd9c708341542a5319cedb5ac1627bbbb39`  
		Last Modified: Wed, 22 Jul 2020 01:35:14 GMT  
		Size: 202.2 MB (202221227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cd58798f69951c43875c290624c1240a4d33de2975ef6c55bd86bc804ab5c72
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.3 MB (335305440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f63250a4e558698e84e147f92bd46b466e7a078a18599c0e0eae38730558827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:02 GMT
ADD file:8b8ef4a5f8149eba4e2e5c50f0e95fcf5b9e729c8fdf74e04ac12871a5e80281 in / 
# Tue, 09 Jun 2020 01:39:02 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:09:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:09:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:09:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:11:12 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2c89c7c8738f073b61540c4d15c26608d6fa4a9756e727acf258769f4f15726`  
		Last Modified: Tue, 09 Jun 2020 01:44:12 GMT  
		Size: 52.5 MB (52522870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68ddf662651a633a2f0e4f65ad7228c24d57d8b14286a1b62fac342f6375f75`  
		Last Modified: Tue, 09 Jun 2020 02:30:14 GMT  
		Size: 8.1 MB (8099334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efad6eefe2105d3cfe168434dd0f3ae253e5013636bf2e2cce89b8545995ea84`  
		Last Modified: Tue, 09 Jun 2020 02:30:14 GMT  
		Size: 10.9 MB (10869142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66019f865e61d00591abfb7d0e9c883b48388b55debf3277d36172b8bd3a424a`  
		Last Modified: Tue, 09 Jun 2020 02:30:44 GMT  
		Size: 57.5 MB (57524657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63051886523353ddda4258e86ad1598f62e2b11a5232f287b36c3b3fd014e4eb`  
		Last Modified: Tue, 09 Jun 2020 02:31:45 GMT  
		Size: 206.3 MB (206289437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13de900c75ac5e7cfcd6c1f1d187e6ef556ab0edabcf13535778a2be39ca9557
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307590948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b755ca06726f21c0d6278bc1a2667a402a2bdff99739cc49bcdbf1af28b6ae82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:08:53 GMT
ADD file:080fe104a5c84718f0c41015a3a4bf48ef0d94088beb50e3b0346ea572302008 in / 
# Tue, 09 Jun 2020 01:08:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:51:05 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4295b4a99b75e24118d0a604e63b142af1639be17451d6724215fd11e6fdd041`  
		Last Modified: Tue, 09 Jun 2020 01:16:09 GMT  
		Size: 50.2 MB (50162108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6b19c74224bd3e9030de803cd7b2cf6f938ee3548998819522a786837b1caf`  
		Last Modified: Tue, 09 Jun 2020 02:06:44 GMT  
		Size: 7.4 MB (7447679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e65e61fe718bcf10bce9dbbedd4844ba55e178913be199a5e4cd26a5ca17f1`  
		Last Modified: Tue, 09 Jun 2020 02:06:44 GMT  
		Size: 10.5 MB (10505180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ba7560d369d9be99a66746b1d7e1a04d087826851c960badca01c94c787d53`  
		Last Modified: Tue, 09 Jun 2020 02:07:39 GMT  
		Size: 54.6 MB (54611456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847c3db2a068a9ead3d44a857cd0c78a6f1b3ec2f3c829c93e03d666cd8573d7`  
		Last Modified: Tue, 09 Jun 2020 02:10:07 GMT  
		Size: 184.9 MB (184864525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c788945a111f2d0900d07504118266967b166a161b858b84dcd6c9f3842e47d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345028228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62233bb8ffd03681cf56aeb933e5c974f80a28a75b6d18e174f1f8f47766f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:21:05 GMT
ADD file:6e35f025b9b04e8864b94d9eee0225ff993cbeedecd7bd805002a3c5d3a76bba in / 
# Tue, 09 Jun 2020 01:21:10 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:45:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:46:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:56:17 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92571d4834cabeca9400dd51bae9bdc41218cc857202b01ef83f6ee357784097`  
		Last Modified: Tue, 09 Jun 2020 01:28:39 GMT  
		Size: 55.1 MB (55147983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088d8f42ecc239b36ce954e9d66d43e9651f30b809d5d1be486643a2ab46659`  
		Last Modified: Tue, 09 Jun 2020 03:40:52 GMT  
		Size: 8.3 MB (8345448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db3ec7901544300bb7ab1472297521c3c44db747007d75b46b2cd95b1eb1af0`  
		Last Modified: Tue, 09 Jun 2020 03:40:52 GMT  
		Size: 11.2 MB (11227910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a032438787728277a3f2f6530d043962d63b3ba5c4109fbd329f60f903394f`  
		Last Modified: Tue, 09 Jun 2020 03:41:39 GMT  
		Size: 61.1 MB (61067583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898822b7b6bf9f88828b7279adc80d4035610e92f41cfe8a2a060477ec88e766`  
		Last Modified: Tue, 09 Jun 2020 03:43:19 GMT  
		Size: 209.2 MB (209239304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b50ea5b15ef57ee65a721a83e219dbcfb4de678554122858efe4cbd7959333ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318357527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f2ec56d1912b5615815aa19a1e976f1c8c025f9ef2b80c9a32cfd01c91b234`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:56 GMT
ADD file:64e5f3d6bda82e2ceaeaede4b9646a695e0b5c2daf32f3ceac3f8404c189999e in / 
# Wed, 22 Jul 2020 00:41:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:03:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:06:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eec92be71167cbdfe66ed0a95cf2650cfae8fc7e2f6d3c038707f63a74aa347f`  
		Last Modified: Wed, 22 Jul 2020 00:45:06 GMT  
		Size: 52.4 MB (52406289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c7d5f37f3ba0ac86762ed35d75a67c2913a5142f0395028219243aee7bb41b`  
		Last Modified: Wed, 22 Jul 2020 01:11:26 GMT  
		Size: 6.6 MB (6599170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76cc1489ae85b994163f909e22b33f76692a45947a1fba3d3d821d5327b317c`  
		Last Modified: Wed, 22 Jul 2020 01:11:26 GMT  
		Size: 10.5 MB (10460561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9640f5165a5b3657fe9e2a6073f569c99ab970b92a2820d0a281d0ab86fba7fe`  
		Last Modified: Wed, 22 Jul 2020 01:11:39 GMT  
		Size: 56.2 MB (56215083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cb065f4494dda4218965778d0d3e61b00e71336b9128b50b1e21ee935b6f1f`  
		Last Modified: Wed, 22 Jul 2020 01:12:11 GMT  
		Size: 192.7 MB (192676424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
