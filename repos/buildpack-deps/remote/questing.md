## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:fdece09b7a5c707dce8e7f7ee82111e8b2fd8aa5fe1e38f30af9ae4385ceceb4
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

### `buildpack-deps:questing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fb5a008f84b257e1137a7a87e972b3d81af59dfdc0076c6b8e0108c7f8ec308e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272878122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431f688a1479e633d36aeb03572d7e7596137f0afb08554ad2147a4f1a29854b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:15:19 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:15:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:15:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:15:20 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:15:23 GMT
ADD file:b50ac7284775f5383fad903e47cb3f2ef479d7e44d6f8f04f9bd60504972627c in / 
# Thu, 27 Nov 2025 23:15:23 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:11:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a206cee1e8395be2f750c7fa3ff5be629dc0dea7ef665cc4c7aceaf244fcf0f8`  
		Last Modified: Tue, 02 Dec 2025 21:29:14 GMT  
		Size: 34.4 MB (34434358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7fa57b343181bd363b105c946eaab265755eee4a9a8704db66044551df9757`  
		Last Modified: Tue, 02 Dec 2025 22:10:55 GMT  
		Size: 19.0 MB (18957014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbc7e5b5f1fe8d02edf38381dc6ba47d6d1aa432a92a95a84c046ac3047f39`  
		Last Modified: Tue, 02 Dec 2025 23:47:25 GMT  
		Size: 48.1 MB (48134635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145bde576f75cc9380d82cc802aed0b28480363df4495d5f701df1313df5b3ea`  
		Last Modified: Wed, 03 Dec 2025 03:10:14 GMT  
		Size: 171.4 MB (171352115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3576ed2f48058eb558ff82b645bfd6096b167816e4dc15304c3041e8b10688d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11718761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3970dc1ce33e14501213154afb1d71c2c368295a6565adf4e99f2dd1ef42089a`

```dockerfile
```

-	Layers:
	-	`sha256:54e6ea4de7eda27d2a7a883b63247faffac38bd6b7c9a46b96d8f7dabe0f7bd2`  
		Last Modified: Wed, 03 Dec 2025 02:19:41 GMT  
		Size: 11.7 MB (11708601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b0d85ef9198cf1fa92a881f8f8e8008887a6d3529b63b8698a38d216f78084`  
		Last Modified: Wed, 03 Dec 2025 02:19:42 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:01c393a6ba216934d9efd03628ba0182b5224ef194860401aad570635fc95f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225350468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec740a84c772fdea0203b30f8e01f58ec62d03b49a34b78ac3ac72d17c1b4826`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:16:43 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:16:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:16:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:16:43 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:16:48 GMT
ADD file:cf3a8be0e74cddf6a500a4cf40ea2e6d1dcfadcb0ae21990673cc37126a3943e in / 
# Thu, 27 Nov 2025 23:16:48 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:11:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1bb758e80424e5fcb11e548572cf31e928938fa9aa0cae00bcb95c4138a586fb`  
		Last Modified: Tue, 02 Dec 2025 21:29:41 GMT  
		Size: 31.8 MB (31834462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cdfabd200070feb09fb34b8cf4182a319b4cae7401acb76296f2011517efc6`  
		Last Modified: Tue, 02 Dec 2025 22:11:06 GMT  
		Size: 17.3 MB (17335260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c7c429cb42506d4ab6d6215597549decc4c87e4366ce23b01aa338a31d47ec`  
		Last Modified: Tue, 02 Dec 2025 23:11:40 GMT  
		Size: 50.6 MB (50577674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a053be218e49d33b53af4a48d4d8d3a0f18d0ef79dec36252f0a36861cf22a1`  
		Last Modified: Wed, 03 Dec 2025 00:12:09 GMT  
		Size: 125.6 MB (125603072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d1a2a894d8b527fe40216a910f15a34c18f18c6740dde50481c6d94dcb93096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11460356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9ffaa6e69488488b767ec78f6ce9253442fd13f88d2baab46d048a67c14e7`

```dockerfile
```

-	Layers:
	-	`sha256:7c9aae61904c8a135b217a3e36725ac824417bc3e884fa0f9bfd03a2dd26f8ec`  
		Last Modified: Wed, 03 Dec 2025 02:19:51 GMT  
		Size: 11.5 MB (11450133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aace2c695a9b34073097ecf086fbb2ef0df6216084d8f760940c79290972540`  
		Last Modified: Wed, 03 Dec 2025 02:19:52 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:949cf1f84953e085b1cf40cf6166a138368c2ee2b19909bf8157dfcbc90a76e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261191880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f02207ef0131530923ab3032fa21c488774f0b539e6ddce49f2e92b8d28ca7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:18:54 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:18:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:18:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:18:54 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:18:59 GMT
ADD file:e9263cd3e11f533dc9f3fb889930c09c631fb75e6ad89ab6a2146821b2cd442e in / 
# Thu, 27 Nov 2025 23:19:00 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:10:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2f25135cc937748dc7f12ddd61abe8c7cc1f5eedc0322b8a68a7816b40f885d3`  
		Last Modified: Tue, 02 Dec 2025 21:28:44 GMT  
		Size: 34.0 MB (34041785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862e65d36700e00016fe3e22d70e37e155c00e70952167e3c7d3e9b449c828d1`  
		Last Modified: Tue, 02 Dec 2025 22:11:20 GMT  
		Size: 18.5 MB (18516394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048cc9d61153ec1806b1122f8553cac7a65d4aa132bb4138225a8def74e5789a`  
		Last Modified: Tue, 02 Dec 2025 23:10:43 GMT  
		Size: 47.7 MB (47742997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e62e28ff20056bfbdd80269b37f0595e56eadd7fb4c04c09aac8e2be3e0f19`  
		Last Modified: Wed, 03 Dec 2025 03:25:45 GMT  
		Size: 160.9 MB (160890704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d56c0c5d7e74508663c3fcbb0dd4ec69d570ab4172f3914f298fa927308c0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11773017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23256d6336b69ab620509156044902b710f1df5d96899737c9fbcc71c03b86be`

```dockerfile
```

-	Layers:
	-	`sha256:a3816ff71fee8dc8cf85ff6494ce045362aaafa5231e5adea153f097f0fbf5be`  
		Last Modified: Wed, 03 Dec 2025 02:20:02 GMT  
		Size: 11.8 MB (11762777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d303945cf72b6cb8b67e75329c8ef33a59d53f4b0dd8c064f9cd6b79fa365946`  
		Last Modified: Wed, 03 Dec 2025 02:20:03 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fc622442788e7ff7112f6198fc707a309e659693b06400b72504ac66bc522951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280637953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1b060cd39ef81c4a8a634feecbf709cbd58f405de1b260ac7e04562d4bcbfb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:18:21 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:18:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:18:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:18:22 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:18:26 GMT
ADD file:c60052f4baf0af16960125955d00ffced77f86d7216d8ccc1970073116299473 in / 
# Thu, 27 Nov 2025 23:18:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:14:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:052023144ae674b4b4ab26f82f1589773a7bcd1d86cae1f6ad2e372e7cc3e64a`  
		Last Modified: Tue, 02 Dec 2025 21:28:20 GMT  
		Size: 39.6 MB (39595804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10958d3dbb6807fff29fb93bc67ade7a05e527164b7f99ae47430b9d4cb04bcd`  
		Last Modified: Tue, 02 Dec 2025 22:10:53 GMT  
		Size: 21.0 MB (20959974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ede6d734e59ee38e0d651b3337536943cd79ba605982c13df75fca55379326`  
		Last Modified: Tue, 02 Dec 2025 23:11:08 GMT  
		Size: 53.6 MB (53555661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167918083d88dcacddae9c903271b4443ee73836f80522019a9204af7e7602fd`  
		Last Modified: Wed, 03 Dec 2025 03:25:48 GMT  
		Size: 166.5 MB (166526514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b86af6032ab6d7b6248eb5777941b4af80df4996ec82cee963cf531eec7d5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11691175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2babd37da574459bab0f798c431e1c1ce839ea5ac5cba3a4fa864bd61bef8e`

```dockerfile
```

-	Layers:
	-	`sha256:f8b3c06fe7252e3d9d4cda6f72e7654d135bbf4a91dd23661d20482119f478be`  
		Last Modified: Wed, 03 Dec 2025 02:21:14 GMT  
		Size: 11.7 MB (11680983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aef30d827180a899b2ea2ef0c633b9a00c27f82776ea093099e81433b4c04db`  
		Last Modified: Wed, 03 Dec 2025 02:21:15 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9a73fe41c040e12a6ece8ca4c096487445e4b70d07026a5310d35c5fbb1ccdaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241784329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0e361ef767a5bb4867f0f1a3fe97b278347178cca46c5efbf5d4ee40d0fb39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:17:10 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:17:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:17:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:17:10 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:17:12 GMT
ADD file:6fb7e51cfcb793f6714200cfa953fa57850eda7a571798229cb4ef58cdee6f7f in / 
# Thu, 27 Nov 2025 23:17:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:13:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cacee7f118ad009c16f8f35172dd48a3fb01d421ef7100077e95aeda6405e172`  
		Last Modified: Tue, 02 Dec 2025 21:28:22 GMT  
		Size: 34.1 MB (34096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb10874e9a431a6859624a2b833fad01e6c85500deb89ea0e98f035ed285469`  
		Last Modified: Tue, 02 Dec 2025 22:11:57 GMT  
		Size: 21.0 MB (20975453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28df6ca3ee8256c5629448d7dfd54e13e0e140544a4d3aefe1767613f285c46`  
		Last Modified: Tue, 02 Dec 2025 23:11:39 GMT  
		Size: 49.0 MB (48968270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820cb90a771e61815b105a123f698c35a30452438c4e9679a575009ea140884a`  
		Last Modified: Wed, 03 Dec 2025 03:25:42 GMT  
		Size: 137.7 MB (137743760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a759bfe72938e3549f89e9d75d912febf2a51003a415a39b9926139ae817090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11494287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d34fa32a3e8199df51b4c867a5156ae3207b492d3290021d2063d2ab81b263`

```dockerfile
```

-	Layers:
	-	`sha256:0a95a198012c457b062ed78a49a4901c12acd807894be463abe8c35ff63bff59`  
		Last Modified: Wed, 03 Dec 2025 02:21:24 GMT  
		Size: 11.5 MB (11484128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0fc5cb69d6b1f648b1773587cca394ea350e67b3f5eac5c29e1c22b18423a69`  
		Last Modified: Wed, 03 Dec 2025 02:21:25 GMT  
		Size: 10.2 KB (10159 bytes)  
		MIME: application/vnd.in-toto+json
