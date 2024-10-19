## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:a2c379af057a249a7ae251d68571aadf7dd43837219ff38e4e797eaa408cf417
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:28ea314ba57e342bac3799c06c1a8d44cfe585fc0f66bf3719030da3cb2942d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279731027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bda0190071cc444553b7a709fd8cd57d63a7c2c2186ba13b47282c6abd6acb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed0593d2f3316b832ab07d1fbfad306dbde92bee837a9184eb10b2a3300bd0`  
		Last Modified: Sat, 19 Oct 2024 03:53:25 GMT  
		Size: 191.0 MB (191026289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74cb68ef31f5c607d038fcb183848fcaffb976bd546d14dae852e490e46b56cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a8a6050b4550be41f53ffa005549538f26068b3cacf2abfa1da72aa307bd59`

```dockerfile
```

-	Layers:
	-	`sha256:d7c719a514e8fc78963ff42a7fb6ebbd21a0ff436cd8a5186432d7a685f011cf`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 11.4 MB (11363167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096c09217c24f206f019b6dc90b89e2b27ac53a5d6eaf8626e3d44371ca1646`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6df0bff9783b406ab00cbbda757f863979ba37f124d5f652a7aef6590dd93034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239782925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2613357626d500c34646039b65cf3728fcb7ee25fcba491909817b4d127793`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a981c012b2ef93c0e4d3e5c624f415b9703e3e959bb801b3dd95edaebb3125`  
		Last Modified: Sat, 19 Oct 2024 08:19:59 GMT  
		Size: 48.9 MB (48888193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6111e812a892c1df5c539e5b9144e27e342290cd1693c23ea9a0fd9af6cb81e`  
		Last Modified: Sat, 19 Oct 2024 10:39:31 GMT  
		Size: 151.3 MB (151254413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ddf5e5c2e97e71884c6af59abaf942dda549a0a8e4349acddc30bf53aaca77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10720345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69080b2ac5985eaef5312663eba1507c3e224f0ca99d510ec3e6c5f24af1e6af`

```dockerfile
```

-	Layers:
	-	`sha256:ff09a1a21c7a669640b186c38daf3432183226bb6915336b625e08abd0f519d8`  
		Last Modified: Sat, 19 Oct 2024 10:39:27 GMT  
		Size: 10.7 MB (10710101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7cb0cfc1d43f5f4dd6b09ac9eee91b4f76fb782e39f64fbd2831d27f34b482`  
		Last Modified: Sat, 19 Oct 2024 10:39:27 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e86d60447a52a1d6346524144985645a0423e4438ac233095fbc47d240456122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270652388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61a37454df2d40c917660e881cfea5faf51970ec24bf7ec4bcbf36147b9cf49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3b9ee069311be4d8fca64a1f65e93cf73601746ef5283dfcbda615585143a`  
		Last Modified: Sat, 19 Oct 2024 06:27:05 GMT  
		Size: 45.3 MB (45297451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ba6826884a2dad7daedbb1abf09b61205cdbe1087c0d7f2cc328a44d2576`  
		Last Modified: Sat, 19 Oct 2024 12:49:21 GMT  
		Size: 183.0 MB (183016310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:487291d9e5158e997ddcee07b7408e8ec4675ebf87af60ea1b6acc29af0ca097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377595d1f627e3b763cc7f7cc0d30f37e6d0cd1c2475fe6e99bdf32a75aa21c`

```dockerfile
```

-	Layers:
	-	`sha256:73bdac28c0f1e731d44a1bd44adbf20ae706d6d04310ea44cb41713a52d534a9`  
		Last Modified: Sat, 19 Oct 2024 12:49:17 GMT  
		Size: 10.9 MB (10932639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b7bed5da457db1844d3d47e9497ba0a94df919a495851764dfdaf6d6d48e2c`  
		Last Modified: Sat, 19 Oct 2024 12:49:17 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b136aa8ebec3bb967cc748b99e9041c7df81fa0657c03f91136c543bc747513f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298476454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a7466eeae1673a2a6eac2e305c1e044edc3a09b06556eba461f50b1566da56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48479dfc2b7d427cb9b67d6c2ae25148b5cdad254e89920f302994550cebd409`  
		Last Modified: Sat, 19 Oct 2024 05:30:15 GMT  
		Size: 50.5 MB (50501654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c1db9206641309be4ad1ed79478d79b600494ca52532597de42a2b7a249d4`  
		Last Modified: Sat, 19 Oct 2024 14:06:18 GMT  
		Size: 197.6 MB (197595327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c01988cb15f09691ff8b01e0328e80006a031f3258d706abaf30c43e0319b9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10890029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6fed5214b877e2ef17d810fdefb5ec60b07bb5cdc66600357fe12e36dc36b9`

```dockerfile
```

-	Layers:
	-	`sha256:467c9adaa1534646b005cdb1ef70ebbebe92475898081a075c6e0177838ba246`  
		Last Modified: Sat, 19 Oct 2024 14:06:10 GMT  
		Size: 10.9 MB (10879813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f22eda885975b6b07ea3ff187a442f984cd2da711532ddcaa211c23421c961`  
		Last Modified: Sat, 19 Oct 2024 14:06:09 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a48cd0fe0e3c96594b73a23e16a9f5f31cdd20d3dbb21889bec661254886606c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330029007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9914ffe80b60c5d35aa4ca731a127513eab9e5a4d21a9f132c9eaa136e80143`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0a2eaf274204c5bf93c79db9bc33e24b045b07aacb49995d18798544f6f56f`  
		Last Modified: Sat, 19 Oct 2024 05:41:12 GMT  
		Size: 53.8 MB (53801364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a00631efcf264d6f9c5d8e41eee22c784fe6c727c1b65108038ef79a629b0`  
		Last Modified: Sat, 19 Oct 2024 07:50:42 GMT  
		Size: 231.0 MB (230955642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de8c1a1ec27d92b20abc2f5650dd64af570c41d20931db30c0388d3370ed6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65989ed3c96055e01b2f0033330d1a72ca1763345e024c3b6af226128a57aa98`

```dockerfile
```

-	Layers:
	-	`sha256:93701c93d6240b07395f73b128019d2a57242924acf950bccb621dcad2cb367a`  
		Last Modified: Sat, 19 Oct 2024 07:50:13 GMT  
		Size: 10.9 MB (10868736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebba5414a868eb48c1037144a61dd35172010195fb71a791d9d80cb2a56c48a`  
		Last Modified: Sat, 19 Oct 2024 07:50:11 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8882db19e6755eb70cff00b9ab99c4e1eee12dddd74c4c6e46b0541cc6c8e4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262094181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cffe492eab9f9ed8773d2b2a20e04bac69cd7543c8b9a9fb973fa1c15cf7dfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949ce1635c27257c28d76c25291d89d75979fb73e8177e9220f5e051d01fddf`  
		Last Modified: Sat, 19 Oct 2024 05:13:20 GMT  
		Size: 46.9 MB (46923171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691bf2965046c25f376c2a1cdfcbd9c93c528a56464249e4aaff8d9bfe446e3`  
		Last Modified: Sat, 19 Oct 2024 07:01:51 GMT  
		Size: 170.2 MB (170176623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7807c6e272fe6f4640072ea3e39d7b2cd741f5025513129276568b362c231d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10735725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9020d42999b45905436b9fce6b0368db0877f80ed31d2360ad50c6cd1fce82bc`

```dockerfile
```

-	Layers:
	-	`sha256:508877c0409dec14e70443d06c870e2ed2fe781820e7ed895cb0de132f6f0125`  
		Last Modified: Sat, 19 Oct 2024 07:01:49 GMT  
		Size: 10.7 MB (10725541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c395543308d5310678a3ac6bed1a1588cb39882a045f402dee11218c16300`  
		Last Modified: Sat, 19 Oct 2024 07:01:48 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
