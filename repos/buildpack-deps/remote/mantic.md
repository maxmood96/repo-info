## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:349960544de64976ecd309f2f3cf44d4ca7df04a1a496e2683f134dc3a5beb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cba5f3ddf8388d55ed9f6575379da692fa6044db9bb7039f85cc906e42c44b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270104718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a8349adf4f66b22ecb260869d4477cc63644ac1b6416ffbc23018c0ce9d6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 03:47:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:48:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:50:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f87743a51ebd3c3339057ac4b3ec85dc6978d0b2810c7e52fbb67db0710e9b8c`  
		Last Modified: Tue, 04 Jul 2023 03:57:50 GMT  
		Size: 27.7 MB (27723058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d294972834df62fa5155c9ab227aa39a4ee9d4ff010b19bc7f855b772262f2d`  
		Last Modified: Tue, 04 Jul 2023 03:57:48 GMT  
		Size: 13.8 MB (13766640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b6edf84d2734ddc13188542334cb7491b5163fce6d690d663129665b1037f5`  
		Last Modified: Tue, 04 Jul 2023 03:58:04 GMT  
		Size: 44.6 MB (44619956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42992b05358515554e3eb370fe2b168b6879759aa9733a6a2754606309ae19f8`  
		Last Modified: Tue, 04 Jul 2023 03:58:36 GMT  
		Size: 184.0 MB (183995064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:921967c654e2083ce30850f91734c3da1d2820a08e022ba46181116069068cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233334849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d855f0b55d2d430e1d112889850066973640c669995c1cf4f7e2008b7cfdc3fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:41 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:41 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 09:16:48 GMT
ADD file:53ef0e936c198583128a468b64a8223b792a28cbd74935a7aaa5fa145b4053b4 in / 
# Wed, 28 Jun 2023 09:16:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:17:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20af62948d2ad360ef116fe2eef1820df7f5aeee326beae2e81efcc6e366f665`  
		Last Modified: Tue, 04 Jul 2023 06:25:22 GMT  
		Size: 25.3 MB (25270588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ac3606f55aa9aea708e379f37c263f56752be04b8642f50a6f4c8046333a8`  
		Last Modified: Tue, 04 Jul 2023 06:25:19 GMT  
		Size: 12.7 MB (12682677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad2008a4cd1ae83435a1e4de359cd60f53b9915ddb8ab1af207bb42c8151c1`  
		Last Modified: Tue, 04 Jul 2023 06:25:39 GMT  
		Size: 48.8 MB (48768734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2883e80e895076087685cae40c858644706cdab4acb3e2d640594a8fd2cf34e8`  
		Last Modified: Tue, 04 Jul 2023 06:26:11 GMT  
		Size: 146.6 MB (146612850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d9249ef7175fc52c9dacde20f2f7c15c57b04992575a2d384e2d5d64b5e51d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259526693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cef9e4596c645f243852e6f874b000844d60144e75ee1ce90039fe04dcfc9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:48:57 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:48:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:48:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:48:58 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:49:02 GMT
ADD file:40c27ea75a8cc64630db8f6d3d5c770eaa2fd339a996f54bab5f7e912d333d68 in / 
# Wed, 28 Jun 2023 08:49:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:20:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a79642e11e4017a06f5c62b8100430987499aaec88e4faace4d954add4f7c0c3`  
		Last Modified: Tue, 04 Jul 2023 06:26:33 GMT  
		Size: 27.1 MB (27075337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809bd1eb3409186f408adf9b158ad6ea72d1135884bdac11ef3a66c1d5758d38`  
		Last Modified: Tue, 04 Jul 2023 06:26:30 GMT  
		Size: 13.3 MB (13349478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9c06373fcaa28267ef4034fdf86623a4cdf64765b1eb01bb141a1bfacb89d2`  
		Last Modified: Tue, 04 Jul 2023 06:26:46 GMT  
		Size: 44.5 MB (44463835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eefd733e7e33d90e33278d0a8086fca313dbfef17e5427c4f7af6d7aab8ad4`  
		Last Modified: Tue, 04 Jul 2023 06:27:12 GMT  
		Size: 174.6 MB (174638043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:61c13f6ca6f476f0c42a3bc48da4d89089502449b3471d6a686e318efb3e8120
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294683789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73119f9cfe2e3983c7b8e19d0b905de61f88972351f0fbad33216895edaef037`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:23:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:34:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:add2cbebe3a583002ff52a300bd69d6b961b4a7735c4612e8030bd26ad555288`  
		Last Modified: Tue, 04 Jul 2023 04:45:56 GMT  
		Size: 32.0 MB (31951571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de6196fb1fff1ebdd9bca2afdccb736f7418000536393564f88be29d3b0c74`  
		Last Modified: Tue, 04 Jul 2023 04:45:52 GMT  
		Size: 15.9 MB (15859335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce64e4b1ebabc1c300d88412d9b3c89e46389306d0ece236088cc4721eea35b`  
		Last Modified: Tue, 04 Jul 2023 04:46:21 GMT  
		Size: 49.4 MB (49350225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7bfdddf74f5b8128e6a4a1213ce8535d9eb482ae1d58df3b0b6463bafb51ce`  
		Last Modified: Tue, 04 Jul 2023 04:47:19 GMT  
		Size: 197.5 MB (197522658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dbdbeabb54f839db9617ee9c41738ffbc4137eb3ec6fb725e011d1219312bf2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241549270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89c42c2991ff218b5d57b35aaa6ad66aa15ecc957ada69256525b873010457a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:24:14 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:24:16 GMT
ADD file:6046e0887f51e3cd521761c62077e42ceb11c3a32d6ecd6b0b32f7d9fbb83dec in / 
# Wed, 28 Jun 2023 08:24:16 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:02:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:04:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf75cf22903e603f6b662ed0bdaeba640fb3db595fc4e05130338ae41ffd6033`  
		Last Modified: Tue, 04 Jul 2023 13:10:13 GMT  
		Size: 26.3 MB (26283976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5404c9da3b69bcc3c3a86e6e878cc44611e5d7f676496e0e7c8d051b9e31d156`  
		Last Modified: Tue, 04 Jul 2023 13:10:11 GMT  
		Size: 14.0 MB (14021238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f702959704c6a66c4bfa75dbb5d5d386c242aae11f591a77d59350284a79c`  
		Last Modified: Tue, 04 Jul 2023 13:10:25 GMT  
		Size: 44.5 MB (44477774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bba3f1de06714eaf0ee83c42337f882cfaf72f059b17fb9e8c6883ef3e4014`  
		Last Modified: Tue, 04 Jul 2023 13:10:52 GMT  
		Size: 156.8 MB (156766282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
