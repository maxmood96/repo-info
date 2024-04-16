## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:b7751bc3a87afb7a5987a6097721ff380a3b4bbf7b12f82f5fef5372b0c22e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:259dd02ae96f2d1babcf2983e064912b0e3b659930fc6be79a8522535248e9d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318695257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7c40ab633dffd0bfaf07763af95a466147808ffc85bc8c9eb79fb712220c04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adea66a5a529e25830935a61441a370c0563b30d99ea2da7a49e53bf8108fe9`  
		Last Modified: Wed, 06 Mar 2024 04:18:24 GMT  
		Size: 228.9 MB (228943762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc576aae865478420b8c263d91396873b8b51979fa1d2312abc84781085a2ae6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238993610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee69b604550749404150bd0c2f6e5cdb898ebbae44b7143f8b6d3993ee5c19ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:31:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:742a70fdca3d3756e5061f666dde28e7d0a1ba3f3b1b354533743ee38dc188ba`  
		Last Modified: Tue, 16 Apr 2024 02:34:43 GMT  
		Size: 26.9 MB (26941976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cca02843e48d71776b41937e0fd4bf0048507a82e5f363b1d56426b0ded0fd0`  
		Last Modified: Tue, 16 Apr 2024 02:34:41 GMT  
		Size: 13.3 MB (13322647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721fcd37c5e6e19e3cecf422f66951707b931e2b724926fdc30affc6a223e521`  
		Last Modified: Tue, 16 Apr 2024 02:35:04 GMT  
		Size: 49.1 MB (49112266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3b2de1dc38d74085b89993f3a87639b2fae36bc4e9eac04b29650e202ebe76`  
		Last Modified: Tue, 16 Apr 2024 02:35:33 GMT  
		Size: 149.6 MB (149616721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84e40ee586abc6ee8adfd864d212cc7b447b3471ef021add5f1d5c7e4799b01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269964635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e773448fd8f96e799070ffec3ed6aa31fad4b190e6f3cc0e1b8c170c5f229f49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:09:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:210ca002167c3d3a57ad40d06950b6c35055e0f7239ae4a703e86b87f07b7036`  
		Last Modified: Tue, 16 Apr 2024 02:13:06 GMT  
		Size: 29.0 MB (29012773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968c2f4b081a4aee9cd23fc0fc6ed4d4b1355e00c92bcc674f2af81de39846`  
		Last Modified: Tue, 16 Apr 2024 02:13:03 GMT  
		Size: 14.1 MB (14131553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee1203d362e9c44647cde6ff8192f19c0f8500ce1dc4a267544745aadc214b6`  
		Last Modified: Tue, 16 Apr 2024 02:13:20 GMT  
		Size: 45.6 MB (45591970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f7559ad38c7119ce55cc62202645052e691ff55a47925bf6aebcf484eb9cc`  
		Last Modified: Tue, 16 Apr 2024 02:13:46 GMT  
		Size: 181.2 MB (181228339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:81f6dee71827e9fd6aa98c4a00beca500bb9280643dd06b9bd48244893c07f6d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296351463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145655b0ece9955d2f31c0064a4dce31f718be63f550de9a0235d14932d454d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:29 GMT
ADD file:4ed9f2ccb9342fb3acaaec8d21d9bf5029a86619c6c8878425eadc78e18003b5 in / 
# Sun, 07 Apr 2024 17:00:29 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:22:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:23:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:29:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5717fdb2c5cf6da9438e6e5f41f3cd785febcd2ef3fe59322b2a98bcde0cb94`  
		Last Modified: Tue, 16 Apr 2024 03:34:09 GMT  
		Size: 34.5 MB (34533211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d45733594feda8ec2c8c83b6a7581c528c52f1b682b06b5b676ca990ffab62`  
		Last Modified: Tue, 16 Apr 2024 03:34:02 GMT  
		Size: 16.9 MB (16866947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85d8a1232f38baee4dc6b751203269685b3e60d6c7c44911819b36ea9053da2`  
		Last Modified: Tue, 16 Apr 2024 03:34:26 GMT  
		Size: 51.0 MB (50953039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3bc2215edf533341e8ff80dcbe3f9f39ed972dc0c26c5774ffd8bbd79d3697`  
		Last Modified: Tue, 16 Apr 2024 03:35:05 GMT  
		Size: 194.0 MB (193998266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4e16431e8ed2b1c9d17789d619a19ffe306c918dbb21efe70086964d8eefc017
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261325771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928a99b6006f60ca72194048057f338728316ad0fc43ad834602fb36d858a5f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:34:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f8b3814528d1a4f48050c53a434c342d156d2c17e42c4995b43378d312b9a0d`  
		Last Modified: Tue, 16 Apr 2024 01:38:44 GMT  
		Size: 29.7 MB (29730630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7301652c4369a1a4573103c28643b88888a84fa00e1a3d3502ff8a7254d2ba7`  
		Last Modified: Tue, 16 Apr 2024 01:38:41 GMT  
		Size: 15.7 MB (15718546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54a0dcd66d035aac0741bc236991e5f9e83f328a425f1144d663d2d22217020`  
		Last Modified: Tue, 16 Apr 2024 01:38:56 GMT  
		Size: 47.3 MB (47290279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d375014086c095fd267f22b888c096b8a354d3ca1c139ff11c5a32b14d5ef03`  
		Last Modified: Tue, 16 Apr 2024 01:39:26 GMT  
		Size: 168.6 MB (168586316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
