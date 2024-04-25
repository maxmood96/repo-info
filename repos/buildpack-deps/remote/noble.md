## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:0d1173a412820dae75b6b6ed73a70fc940ce11523667622dc64a609d07f9269b
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
$ docker pull buildpack-deps@sha256:8191b3d88351edf9eeb7fde603966796e3e9fdf1d88b2f77f5e3ce56be8b33ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279145749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21fab80db20862511d14dd7ffeb3f1ce94364866f2e7d9e99b60099582baab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:34:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:41:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f5159575f7bbbce11277d1532c12d73076587ebb492562917370449a8c5e7fa`  
		Last Modified: Wed, 24 Apr 2024 17:16:59 GMT  
		Size: 29.7 MB (29702068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdccdd8b38d211dca25619ea8b5b92600ec3e2caa4ff8d1b944fe31205f9fc9`  
		Last Modified: Thu, 25 Apr 2024 21:45:37 GMT  
		Size: 14.3 MB (14300245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe0aa1bc9d67cba57636415e5bc438ae1f62a21bf52245d518bad083c5545cd`  
		Last Modified: Thu, 25 Apr 2024 21:45:53 GMT  
		Size: 45.3 MB (45297503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e70962c9f52757e69041621e2a151d450809056eea4de2ec46ce7c4a589b20b`  
		Last Modified: Thu, 25 Apr 2024 21:46:25 GMT  
		Size: 189.8 MB (189845933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fba462b0de10d3fc1e556341d187ee1abeaaa5390cfa5e6e7cb12f4ca288ae07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239406165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11bcb1f37c029efd557adb50f92c7819d5c599dcf0cf5457921f507fd0a9bd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:39 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:42 GMT
ADD file:158f9c2033bf15aea7323a8fc02ed64bb41784f98f36b5faf68a959346a86757 in / 
# Tue, 23 Apr 2024 22:03:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:11:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:18:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e440e8b3da7c90c5ade14456a5cbffec3e72a2bb2eb7d20b5c4eb2e63407ceee`  
		Last Modified: Thu, 25 Apr 2024 21:22:19 GMT  
		Size: 27.0 MB (26953117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b7edd08b76e28f02abdd681d6fa83e384b4a379d227cfacecec42f61a1dbf4`  
		Last Modified: Thu, 25 Apr 2024 21:22:17 GMT  
		Size: 13.3 MB (13323136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d678f0d4e69fa17c40a2d31c6c40d374cf984817b3413044359350f2ac4a2f`  
		Last Modified: Thu, 25 Apr 2024 21:22:36 GMT  
		Size: 48.8 MB (48841004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63a7bab664a656355773facd02d7812e31d68693cce6bf662c88a6711069b3a`  
		Last Modified: Thu, 25 Apr 2024 21:23:04 GMT  
		Size: 150.3 MB (150288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0dfe407439e7f20b27ad0315c6b63c4aecbe2d1ba474d9722fae77ec5a53464f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270271196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25bb9ebd94b41676093b56c20985b49a9db0b6acd1f36e36c0a0f72145bf48b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:44:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec7cb58592b61e9a11cec56cc368247d061905f8eee62423f6dddd42173504b2`  
		Last Modified: Wed, 24 Apr 2024 17:24:38 GMT  
		Size: 29.0 MB (29037830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bb3095dea3c00ae7a36d74265d34ddcbe154310bbaf23a8c2f113439f7b67b`  
		Last Modified: Thu, 25 Apr 2024 21:47:36 GMT  
		Size: 14.1 MB (14132359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adc3a2e35e547eb3555c53c61fadffa37ffc6a2fd89e690e8211e5dfe1d04f7`  
		Last Modified: Thu, 25 Apr 2024 21:47:51 GMT  
		Size: 45.3 MB (45259707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6546dbe565fffc62273aaa964cd39a96a278f8230b61d9ae3e4aaaba1a05dd5a`  
		Last Modified: Thu, 25 Apr 2024 21:48:16 GMT  
		Size: 181.8 MB (181841300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2035d79f73ff99f44166964184ed11dbe89b9b059b1459f47a5fd01d95be3056
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298479153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e934349dd546c09acefcd4c60031fee22887bbae6b95529e1e81f21fb5b9563f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:16:12 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:16:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:16:16 GMT
ADD file:7fd16485139d3989a1a5565c0d7fb14bb79403891eb470189d51dac672fd641b in / 
# Tue, 23 Apr 2024 22:16:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:54:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:03:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:376893c0d3e66eb0681db32a86ec72e75bfe0975d26041f1523ff33804bfdee9`  
		Last Modified: Thu, 25 Apr 2024 22:07:47 GMT  
		Size: 34.6 MB (34574708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2023c2abeac79352985ebf619d415cc8fa67dddc498f6ad865dbc3d20a758b`  
		Last Modified: Thu, 25 Apr 2024 22:07:43 GMT  
		Size: 16.9 MB (16867176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c6591512f42fa4807cea187ff6a02e62596b6a2be07717848e15e40e85fa02`  
		Last Modified: Thu, 25 Apr 2024 22:08:04 GMT  
		Size: 50.5 MB (50511089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b14927a042a0325869118f8a49e9774c22a477cd04ce1d94b220f22d329d31b`  
		Last Modified: Thu, 25 Apr 2024 22:08:42 GMT  
		Size: 196.5 MB (196526180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ecfe5ece12412cac60d2231ddb5974f7bb6969f7856e12a87f857704a41169af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261606552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888788ebbf27ca1d8300ed0d06ab12abdcc2e737dfa1f0a3104faf09ee2a8e85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:55:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09891c72d44d843dec0981794f145f31192710104498499b3283205e955a4699`  
		Last Modified: Thu, 25 Apr 2024 21:00:21 GMT  
		Size: 29.8 MB (29781724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2975750ba9fad7e23fa7d0af87613454caf33ef321c9ac49fa93bf1d2bfe84a`  
		Last Modified: Thu, 25 Apr 2024 21:00:19 GMT  
		Size: 15.7 MB (15719433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d811a46d99d53b3788e1b7560781567618e1e9479b7504d00c1436a17776d73e`  
		Last Modified: Thu, 25 Apr 2024 21:00:36 GMT  
		Size: 46.9 MB (46943012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91065c2b40d63023dce7a98729260c36aca20758865a8be568f4436d5088f1c`  
		Last Modified: Thu, 25 Apr 2024 21:01:07 GMT  
		Size: 169.2 MB (169162383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
