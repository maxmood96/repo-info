## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:987f1ae8a32e7ca9c8c00abceadf9cb18a809d4f1ca4aec3aefc228e4c099713
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c87bfc0326e35eccaa5a1c78d3b894a3512167ef748856e1ac03ce82ea61f236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286667068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9111db4342fa7443dbb506583cfb0bf7555cd9e849a00f12bcd975967b4fa39b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:04:52 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:04:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:04:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:04:52 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:04:55 GMT
ADD file:5a3b3d88836037412b2e65304a34ae9b8902e2e18f2142a9d7bd31359c280c79 in / 
# Wed, 21 Jan 2026 02:04:55 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:48:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c261c4d22b0eb03c17e9c8acc3b714b4abd96cd3b2435def412cb5367ae9e85`  
		Last Modified: Wed, 21 Jan 2026 02:53:34 GMT  
		Size: 33.7 MB (33675624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55883c6a0c594fbcd6607363867fa967d79095f04962e66e55fc017c45bdf9ec`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 25.5 MB (25540862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7c12cf5baaadcbf588ddfb059911902c7f881b12e3dfcf590fb3253dbbf76a`  
		Last Modified: Tue, 17 Feb 2026 21:16:38 GMT  
		Size: 48.2 MB (48246127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee7a79d8b039a27675d2a7e982d140f22029513912fd130ab04ec4ee6a4aeaa`  
		Last Modified: Tue, 17 Feb 2026 21:49:15 GMT  
		Size: 179.2 MB (179204455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c73807b8f120a7c024df63962bc3cf569b94f92c56dea30c9934d63b437f0c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12941483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76594627c742f96417c6e09f0150b4af31b18c13d267d3139249b6d5bc49225`

```dockerfile
```

-	Layers:
	-	`sha256:95689ac2950f8a3d65101f7156e58dceff2e72bf9767d5ba5ed43f1128401cc1`  
		Last Modified: Tue, 17 Feb 2026 21:49:11 GMT  
		Size: 12.9 MB (12931323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88360a53923901b748d1308166bdd266ee3531efecafb0c7e3fd33a2154cf06a`  
		Last Modified: Tue, 17 Feb 2026 21:49:11 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:499dcf28df10bdb9d36c9acfcb375f284562b1f4afaaf4cc23419fe4037ae3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240839038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2665a759c52ebd16965cb10b059c71c9ca8b27cd70f84f6349fab97ed272fa5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:08 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:09 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:14 GMT
ADD file:64f8302e71f30ce19eeb546a74e2f2ee518a1401afcf8395ae4cf115f7f4007f in / 
# Wed, 21 Jan 2026 02:05:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:43:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:340f1c91e91d4fc6dea29a48d805d764635f314ec829f043b408b97d421fefcf`  
		Last Modified: Wed, 21 Jan 2026 02:53:47 GMT  
		Size: 31.2 MB (31166507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd26212152f3531f73c0efa5d9e16bb1fa6f236b022d20f6d2a2aa31de3742`  
		Last Modified: Tue, 17 Feb 2026 20:11:45 GMT  
		Size: 23.3 MB (23277470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ad20d12978bce616b4ffed9f3567970ab2a667a2ba6a1d53f2eca93313a5a`  
		Last Modified: Tue, 17 Feb 2026 21:16:44 GMT  
		Size: 50.7 MB (50746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b464a3eabba9965acd30f84401931b45444a4a2e3b7261735315fae6e7d1b0d4`  
		Last Modified: Tue, 17 Feb 2026 21:43:49 GMT  
		Size: 135.6 MB (135648878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5f71752c4ec97d7e7997834b57abfee40688d816dc3ef2934d2c54386dfaec36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12682427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2aa1a12aea2edb74d312aa39f2ef0b3d382043c0fcf99933695e3de7edd247`

```dockerfile
```

-	Layers:
	-	`sha256:d6f01869ce916623479d6ab2774824c37c6db8ea7f4f5179ff5122be5f14ded9`  
		Last Modified: Tue, 17 Feb 2026 21:43:46 GMT  
		Size: 12.7 MB (12672203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dedaabded655abef8fe918dc164b61ed17f691e5157717a04f7b9c6de3a429`  
		Last Modified: Tue, 17 Feb 2026 21:43:45 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5785e1b2c3112c32090eaf084bd4ffe038b1cd40b1ce53cc29d71980b0ac9d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275622222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff619d6ecd904cb157ae6df21d8ff78106cd56da284df7eeb53e5d2acfd7fd31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:06:33 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:06:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:06:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:06:33 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:06:35 GMT
ADD file:a11224ce0bf3c5f80538743d4c0625b9323c82858600072ca8c1663ae7960103 in / 
# Wed, 21 Jan 2026 02:06:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:48:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53aec10ada41ffe8ba1d5de5418a311240cc814b8b270a9f91d069cac334f70e`  
		Last Modified: Wed, 21 Jan 2026 02:53:41 GMT  
		Size: 33.2 MB (33228686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900559816bd40c452d3861268a03da469284a99c9639d5aaa515e1c92b085722`  
		Last Modified: Tue, 17 Feb 2026 20:12:12 GMT  
		Size: 25.1 MB (25115471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f14a12aa56df8b0159701e00f2a970d29375c71ccf8a63f858e744a792ff84`  
		Last Modified: Tue, 17 Feb 2026 21:16:37 GMT  
		Size: 47.9 MB (47885944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d64738259ea0a17c00041cc87cd87461df119f280baadf741bee45a92a76924`  
		Last Modified: Tue, 17 Feb 2026 21:48:50 GMT  
		Size: 169.4 MB (169392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e2e76258297ab658e18b1e4a1160abbaf48bcf4f2934122742261c0ad590353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12995728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae17c5b7ac15793b0cc75f6bcd4b449f871609e621b3a21b4551faeb79c49b9`

```dockerfile
```

-	Layers:
	-	`sha256:385f3382bce7d7e3a294054bdb11976cecdb45cf43535219459422e3be11818f`  
		Last Modified: Tue, 17 Feb 2026 21:48:46 GMT  
		Size: 13.0 MB (12985489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbac705b961e84e6f95f9ff18136b5cbb404a6c4eb00b83e90fd4eab0df8877b`  
		Last Modified: Tue, 17 Feb 2026 21:48:46 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5c01108352d0133986d7e8d195bcad51d97831920ff47a687e5e65930eb6bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298834795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c93600b85b49b205864af533441a7385eb1de6cfafddd11744a902362ed8829`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:01 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:05 GMT
ADD file:965035165b5a9607aa8c5bb045af27bc17ad5f8ba33ecbe10426988d7c087ecc in / 
# Wed, 21 Jan 2026 02:05:05 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 18 Feb 2026 00:26:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5ed12c0213034851f152051b56017b1e654738743050659fce37a1a1aabcb6e`  
		Last Modified: Wed, 21 Jan 2026 02:53:54 GMT  
		Size: 38.8 MB (38812135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b035f88d928ca302b9ff3aa9991b0d88cdc1af3c26cf3a2e90174b06d0494`  
		Last Modified: Tue, 17 Feb 2026 20:13:43 GMT  
		Size: 28.3 MB (28317642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf98c8b2a343a74d54a62e9cc6362df8445c47cce3a012b806527aa4d9383c2`  
		Last Modified: Tue, 17 Feb 2026 21:46:52 GMT  
		Size: 53.9 MB (53945243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071854e5fad9251a5fb006d72bcd0539e2f734cc59e50fb7f63189bf5e2c9b22`  
		Last Modified: Wed, 18 Feb 2026 00:28:23 GMT  
		Size: 177.8 MB (177759775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:58cc4a4f26ae68bdbfb98f04e24f60e9ac8f7d7c934008782a4281f684f5b3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12914094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbca641a5d0d4ebd69cc4a1b99713daf04af1b4045a0251f0825fd9d1408687a`

```dockerfile
```

-	Layers:
	-	`sha256:05d7bdd06473aee6dc295b36593626af89c5d406ca0317d74c2a7cb61791bd3d`  
		Last Modified: Wed, 18 Feb 2026 00:28:19 GMT  
		Size: 12.9 MB (12903902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a149b2a91a5bd1fafa70019c88c072d904ff9a46018f133d742c9557db7c62a4`  
		Last Modified: Wed, 18 Feb 2026 00:28:18 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f4dde7bda0bfc0f74bd2fe9546f535c0efb8e857277ae98569d16af5c44c6243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261998599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c28faa72d05d68bb0a52c0943953c05181163854d6a9134d142e1c32636d0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:26 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:26 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:28 GMT
ADD file:a31148f1b2b73c9ddb2dbcb9c6eaf377794bd2a5545e9afc25bfda0d0fc4e29c in / 
# Wed, 21 Jan 2026 02:05:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 22:25:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:880c3ab78503e9d5bd5e9fa7f060185c8b708bbe723e3ff052d6be540d75a79b`  
		Last Modified: Wed, 21 Jan 2026 02:54:08 GMT  
		Size: 33.4 MB (33399085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f623ab4e89aede42d0ac17c3ab466b025e769853ef72fb583d67b2bf772fa96`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 26.1 MB (26085879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248536fb814edf3e4faf020a543efc6bf472f95f7150cc07072ae3a9b4e79ca4`  
		Last Modified: Tue, 17 Feb 2026 21:15:53 GMT  
		Size: 49.1 MB (49097514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c38ecf3b590d3e16ecad7c2f9ca95a7815778a34a7c4b3e0adcbdf00b45653`  
		Last Modified: Tue, 17 Feb 2026 22:27:06 GMT  
		Size: 153.4 MB (153416121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef0156b509a973658568944bace7157650a3b5e25a9b260f4e5033a6b03f976f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12727433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9775230df6d6919ab82c4b528c2394d2936d95ff64000e43d6587ee15fd05995`

```dockerfile
```

-	Layers:
	-	`sha256:20965e7759be789e6251893b5a6419c742b42c2d1fca444276b43e6b7e98c93c`  
		Last Modified: Tue, 17 Feb 2026 22:27:03 GMT  
		Size: 12.7 MB (12717273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ef761c97d16653ae00744dac2ffef9c0ed467423ec98889b3090efe6dbb7f7`  
		Last Modified: Tue, 17 Feb 2026 22:27:02 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
