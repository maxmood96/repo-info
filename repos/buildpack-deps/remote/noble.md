## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:01e5d146da1d942f8440d808f80cb8dfeabaeedd3e2b61db81b408d321a9440a
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
$ docker pull buildpack-deps@sha256:879e18b206012f7db46b91534df17203caf6896a7df96c4934e2c1e884672976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274730085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28d9878ce0ee9c1a569796d61477d849863690263fe296bf1996af9110f1e16`
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
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f15f492705b1de8136aa0d2c2d9eb39c00ca05d077cb49934724c4bc48ecf10`  
		Last Modified: Mon, 15 Sep 2025 22:12:09 GMT  
		Size: 13.6 MB (13624812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1313c778bf6a9ff7cc448fb8f14ad32be55019475933c62e3603fc4f25f29f66`  
		Last Modified: Mon, 15 Sep 2025 23:13:58 GMT  
		Size: 45.3 MB (45333738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be817d3c5cde28da75b5008d0e172f3a074b5a9536905f0400f2368ff6879e`  
		Last Modified: Tue, 16 Sep 2025 01:26:28 GMT  
		Size: 186.0 MB (186048085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fc0e18dc6605d51b7782fb57776c8aa4af7b512a6f7adbbd4f6662847f818eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a070cd662a46e767c2620e5c113aa7aff3102d371a4021fde8ad68d4e2ccc4`

```dockerfile
```

-	Layers:
	-	`sha256:b5f97375dd2eb6db479d0631c52400715d7ec52936928e3cc10d2e263bc8856a`  
		Last Modified: Tue, 16 Sep 2025 01:19:27 GMT  
		Size: 11.7 MB (11732779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b67b02cf327c94a5186e587ad1a70fdc96c232a9b7383313baa7bc8af678b0`  
		Last Modified: Tue, 16 Sep 2025 01:19:28 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5340522e59e8bf3ff805c366b513576e89f3d32a6abfac22d5a59001aa1b7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236790245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2edd3c021d37bf593188bdd6073542c9a60ddf1c959e9d2a5cb7dd3b799b71`
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
ADD file:724937f3170b06318ea1d68d111a29f384243a4dcad8729e0deab590d6d690bc in / 
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
	-	`sha256:d7ffb5187e159334b70dbe49cbca848457358d2d2b56fe7072a42dbd9ac9c7cf`  
		Last Modified: Wed, 10 Sep 2025 09:09:41 GMT  
		Size: 26.9 MB (26852474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb7afdd6f69b5972a86f2f83e308ff30d49b2ee36b8a9c2108e1ad3afc6ae8`  
		Last Modified: Mon, 15 Sep 2025 22:09:53 GMT  
		Size: 12.8 MB (12783833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b329d0b7d213a4be22f22f475757819ae3aaf1b0d685afb7fa67f4be2c1c0`  
		Last Modified: Mon, 15 Sep 2025 23:14:00 GMT  
		Size: 48.9 MB (48865262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23af1e9cb9c67fb55da4b4e4e5aa46e5b280f3101ea356ede63171f0ece59141`  
		Last Modified: Tue, 16 Sep 2025 00:14:22 GMT  
		Size: 148.3 MB (148288676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e2b15dc5954bd6979a203c20b6e8ea0aadfb2af89a0e49f453b38f99d4c0abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11068728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8542f00a8907acc294fb25957749f54edb51e646ae03006cdce4568543b950d`

```dockerfile
```

-	Layers:
	-	`sha256:d3ee2b1fa5a84ef9f4a5a338e392c1d989c2c3b89b43e30866acc911beca90c8`  
		Last Modified: Tue, 16 Sep 2025 01:19:36 GMT  
		Size: 11.1 MB (11058480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dad053bfcb064766c361fb7bac4a7a0b9028eb567edb2b07e2e27955cb5c926`  
		Last Modified: Tue, 16 Sep 2025 01:19:37 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed348adf5a426d1a110ef2363c64f1827649113df5a2cde9a449ca93f158d9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264255621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8a2b0358075191856cf289d792f500914bd28117913254268a3db4165c5901`
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
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1322a08d432101eaa67d86cf47e2ec84c226aeb9c10d0f3c36d5ae39592c62`  
		Last Modified: Mon, 15 Sep 2025 22:11:37 GMT  
		Size: 13.5 MB (13460309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8945f046ac130c626cefeadeae71f3c749117955f05d96a7f48e52f75a0165`  
		Last Modified: Tue, 16 Sep 2025 00:12:36 GMT  
		Size: 45.3 MB (45308282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33aed0fc38e614ce5b226e3572e871e0beab07a0da826b6e3bffc298d97a4721`  
		Last Modified: Tue, 16 Sep 2025 01:30:50 GMT  
		Size: 176.6 MB (176625713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5b6c79269342a8a40244be69e652f5fb5cee942db12d604f1f6c92bc9a835396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11292512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f715224f544b9e61fe5493cd5e6c4d2b8649d2c560d90d57572e9a729de053c`

```dockerfile
```

-	Layers:
	-	`sha256:546fe811a6f386c2bb728f5365b2ccb28543f3471801a189116a655e7ad8495f`  
		Last Modified: Tue, 16 Sep 2025 01:19:44 GMT  
		Size: 11.3 MB (11282248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6f21ca24eed2fca699f0310fdfcc20b922b6c08ecee91f6ec6b12e0a4346af`  
		Last Modified: Tue, 16 Sep 2025 01:19:45 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e0a0902ed3e0998a170860ee6f9353381e137b6a6deee56c85297494b06427e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290293130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be734f29490112c32f3e52b6195dcb8679d6e7d2a8aac81bdaaeaadd8b124541`
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
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c837ddd2ff9840a8084e110a0603180382a7fcc929a7f65af65d4470031ecf`  
		Last Modified: Mon, 15 Sep 2025 22:10:54 GMT  
		Size: 16.0 MB (15953067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d665a438d7ff06d9f0fb03e9b189432d711170c64f06655f88385714c2b57a`  
		Last Modified: Mon, 15 Sep 2025 23:52:56 GMT  
		Size: 50.3 MB (50339554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c7f30551e28d0c76bd7fc13aa8f09f20df12ca30e779e9f0ade8a48efe0ec5`  
		Last Modified: Tue, 16 Sep 2025 01:46:00 GMT  
		Size: 189.7 MB (189697382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1805f14c19a431c6b27ec3d3c6fe55d786c8588b57de4aa929080e7537e96d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11239901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecb00219e8f2ee57d1da788ae2d14ea9563a2ae9e2e10bca803c7465eaf14fb`

```dockerfile
```

-	Layers:
	-	`sha256:e1588071630b6176d329d1c7f0e75ca617b8adc0354fe9eaabb17cca143eace1`  
		Last Modified: Tue, 16 Sep 2025 04:19:46 GMT  
		Size: 11.2 MB (11229685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b84ab0cc9b63d68cf65b89b87a6921187658cf0ccb3bb96cd424ae9937ff26`  
		Last Modified: Tue, 16 Sep 2025 04:19:47 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:721237cc8efcd6cfea871333d7c509f07edb67a2371a0858833d68a2eca4126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0b137f3c3d9d89e04cc5a059920098ac0badde482c8439f31aca077f9a7e64`
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
ADD file:0b905a81cc9e876b16249002e7c59885fde69ab451fd1b6e5768dd8a4b2a9d1d in / 
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
	-	`sha256:6d2d7ce17575561a3deb2625d73936f72b9f13abdb7e3366b85dbb55c4289f94`  
		Last Modified: Wed, 03 Sep 2025 03:54:05 GMT  
		Size: 31.0 MB (30951461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f53929a6a5f607aaa4e68ea9cb5f98cb8da460165b394870ba679a77d84fb`  
		Last Modified: Wed, 03 Sep 2025 16:52:16 GMT  
		Size: 14.3 MB (14330253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efed863832db13d72a3c81acbc9a1dd0b55a579253720a8682bb487641abe5fe`  
		Last Modified: Fri, 05 Sep 2025 18:46:38 GMT  
		Size: 53.9 MB (53875883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ecca00958cf959a89c655355104eb8a484717471eddfb3f8dad00b3b326cd8`  
		Last Modified: Mon, 08 Sep 2025 06:21:34 GMT  
		Size: 231.2 MB (231231573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:53f7212cf87ee57173922bd1c531f495f89ff310ecb7a25b835ace970e2493ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e65baa254276a398c2435f9fcde8e94d0c435ea41cc61b24a89c42168f0c5`

```dockerfile
```

-	Layers:
	-	`sha256:6b55c44c8de0576a9595504a5a722ca4dbaae63074755e128b60d8fefc44ac90`  
		Last Modified: Mon, 08 Sep 2025 07:19:57 GMT  
		Size: 11.2 MB (11222916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566636deedbac65f8c21234fef4ffd2dfe94c8a0a2d33c8653b2a5d7d18d7dca`  
		Last Modified: Mon, 08 Sep 2025 07:19:58 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d3986a9eca6d5bbd0a37ed2ecc43decfacfde5b66e940174421489285be0f5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253041482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f0282b6e475659fd683e26008a07d47dde90e74744c1d037d3ecfefe352c26`
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
ADD file:c24f61277b8ba0fc6a9f5e3c821b272fa1878e300fa010e5e8c6bb6b789470a0 in / 
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
	-	`sha256:1d6a499251c4e5e59ef209845254eb72c5efde9542271f270cf1a08fa823dfda`  
		Last Modified: Wed, 10 Sep 2025 16:24:53 GMT  
		Size: 29.9 MB (29906591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5addaa29204c79a9906cd7ee74dee50da001c444c82184247c8539ea88b9594`  
		Last Modified: Tue, 16 Sep 2025 04:19:26 GMT  
		Size: 14.9 MB (14938285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf900e5d5f06d96144d0fdbb00fcbb48744678cfe7c416b3dc4001f8491d0`  
		Last Modified: Tue, 16 Sep 2025 04:19:28 GMT  
		Size: 46.8 MB (46780180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cee23f08e45368700c4bc7780aa03c1ee606f062ad285d7413fab785f17b220`  
		Last Modified: Tue, 16 Sep 2025 04:19:34 GMT  
		Size: 161.4 MB (161416426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fc099539f4c29ab20bd1d9c439122fba4c7a2563524f28822e5f09136336aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11083716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefd728219ff17e5d97dcb5f2d284de52b1aee25822543ef8bb0d53fff648b66`

```dockerfile
```

-	Layers:
	-	`sha256:77ecc23dc806f5fdde29b17ff14081b760099f9e2b877333acd06413b0235d5e`  
		Last Modified: Tue, 16 Sep 2025 04:20:01 GMT  
		Size: 11.1 MB (11073532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a2bd3dfd47c48a6dd0262713f7f71ebce169e05ef2bfc7bcd00d5a5fa00b05`  
		Last Modified: Tue, 16 Sep 2025 04:20:02 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
