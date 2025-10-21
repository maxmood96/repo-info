## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:251b206d4672bbd42c916dde83d71e8db0389248afdda725112ee3dacfa4e683
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:abc4730fc7a89473a814b6d11287d05357a1e581dc8ad070ff0ca16cc19dca2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.6 MB (378612688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686a625a625b838ad67699ed9716fa88e43136c4f190bfe5a364540107981e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ade626d67af90eb146ef31070d6021beb378ab38f6477493190d674c44a1e9`  
		Last Modified: Tue, 30 Sep 2025 09:55:03 GMT  
		Size: 235.9 MB (235928303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34649050bd68ba3d44223aa47625a8c73d9d52d87bd9b774623602a1186bab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1ea85a92a88234d8627d687dc6aacddbadcf9b270587ee542d61d345ed01e4`

```dockerfile
```

-	Layers:
	-	`sha256:f5420931d69053c5f1bfe02cc1b701d78082935264e2c46790088f4af8ff05bb`  
		Last Modified: Tue, 30 Sep 2025 20:47:38 GMT  
		Size: 17.2 MB (17207047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0975b65a1d0ca039f548262d39547a401a585c464f4e074f2ffe1c91729aaaa1`  
		Last Modified: Tue, 30 Sep 2025 20:47:39 GMT  
		Size: 10.5 KB (10504 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bd2d1822f3f615d1516f4dcc95e71bad232f94edadd67b2d557d688c26856419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342776828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53de43684c49363d3011b79f5727f733e57902a69d2326f88368840821a74567`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36e1dd9ce5730c29e323bfee77881b6b709a9ef3833ed3a509dabd626e23ef19`  
		Last Modified: Tue, 21 Oct 2025 00:20:35 GMT  
		Size: 47.4 MB (47448771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5aab8f083c99dfceb8649e1078e500b3226031e7fdab550eda596ce5b675db`  
		Last Modified: Tue, 21 Oct 2025 02:32:50 GMT  
		Size: 24.3 MB (24342547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a322d2ac28a78c43ffaa81483b3e7182f4b364130ce74f60ef2317ccf71493`  
		Last Modified: Tue, 21 Oct 2025 03:57:05 GMT  
		Size: 65.3 MB (65325001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0853401f645ef1ad81b7e22147fbdfece36afa865cdb01dbd5272e030bffa8d`  
		Last Modified: Tue, 21 Oct 2025 05:15:41 GMT  
		Size: 205.7 MB (205660509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:56c0cf160a772dac007e884feac60921989194bc45f30570c3d731a996c00a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16979966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373602c1916693d927f6c0e60d4cf6c2f95c4899e3b5022e0d5cfd4cfac424a8`

```dockerfile
```

-	Layers:
	-	`sha256:5a3fad2bb74b1a6e07595fd70f22214df926897df25683488f03cad6f1580f58`  
		Last Modified: Tue, 21 Oct 2025 07:20:54 GMT  
		Size: 17.0 MB (16969389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0659c373435c59e7a8f31171b2c5e3fd744788d8b5a81f994f8596b118be349a`  
		Last Modified: Tue, 21 Oct 2025 07:20:54 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ac1e134f0e620ef803700685c6ef798a8d9e073ffbfe911ac6f0c7b0ece7abcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381a3af234d63163123d651594b2094d8632edc2f2a7f37bc6fc3d9ebc332f5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44df842311a95b0b7342e7e98003a42713a82b0548bbc4622c6034066983fd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678f36a1315fca6dc09573043e8f35db273ac271659700a4cdde87772b45f41a`

```dockerfile
```

-	Layers:
	-	`sha256:477c1e763582ce8b38eecc2bade06be440b93830dfe6c8cf63eba101263e36a4`  
		Last Modified: Tue, 21 Oct 2025 07:21:07 GMT  
		Size: 17.0 MB (16975179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1eda9243061e2945b5686c11df40c772d6d8b432e88f54ffd542d7b3cd01c8b`  
		Last Modified: Tue, 21 Oct 2025 07:21:08 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eef2010a1f39eba747dfddf68f7b69cf624c31c2179572040a4420df92e44282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368317148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4303500946ae484d175ccae0fffdd9d390282c55fd46bb2def292674af0ae90`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa24803fc7a76e7898f7a43b6b4f9851f1150fe7207758212555ada9266e62d3`  
		Last Modified: Tue, 30 Sep 2025 03:14:27 GMT  
		Size: 226.1 MB (226069106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f742075d8eaa8cfdb32b103e14ca981f4dcae94f0958530a90dd32a562d9521c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17301938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387ef1ba4e8549af024a5ba25e66b1080de31c457e32e7116b87a2764452a788`

```dockerfile
```

-	Layers:
	-	`sha256:e0fe19e656bdaaf53741c18fb5fdac488a93b89091d6662f3df880246febf18f`  
		Last Modified: Tue, 30 Sep 2025 11:47:40 GMT  
		Size: 17.3 MB (17291341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5f90818a8b8a99c4f243ebb90491ed9c131b07bdd783e6e8f39ec6c292f246`  
		Last Modified: Tue, 30 Sep 2025 11:47:41 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:54abaf0f902b007029fae32eb2b53eb9dd14a73b42bdc335018d1940c024a352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387412810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21efd2dccce0680df358da443de65048a2fe1b7e6a1631bb24160c6884db86ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5d861644e3a43dbea9917a86fd0d6ccf184bc7514ee58118ffa521ac4bc61`  
		Last Modified: Tue, 30 Sep 2025 00:21:14 GMT  
		Size: 26.8 MB (26774670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acddf1ffebf58f05179a0e8a785ab62df40c7d1c75ee543282d404ca07d3ffec`  
		Last Modified: Tue, 30 Sep 2025 01:21:21 GMT  
		Size: 69.8 MB (69794474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15ed8228df04c354000eb4cc1ba531137105148dff92b66e707805d4ba2826`  
		Last Modified: Tue, 30 Sep 2025 03:26:46 GMT  
		Size: 240.0 MB (240043437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:35dff00a018447080734c6a2aa85fb9141a970cff0d58d447c310602ebe161c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17187118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7cc898c08fdc414521a513d2ff4f0f25f0ce194de9ffe1ceba8b8257a54587`

```dockerfile
```

-	Layers:
	-	`sha256:1d9e60bde7a2ffc83abc0d38e4c2e3328f267af7868c385de2164eed183d2aae`  
		Last Modified: Tue, 30 Sep 2025 15:25:01 GMT  
		Size: 17.2 MB (17176640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b66be4c5051795bf0a71c916f06f3a4cd81be0767b4e6f511dc0ffe76b451a`  
		Last Modified: Tue, 30 Sep 2025 15:25:02 GMT  
		Size: 10.5 KB (10478 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b16e4f8e525a640a78b67bc36482806ee1b50d6045f6f50de1dd29d0408a47c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384231995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600a6699f97e3a5433b674e852ffb4c2a5b65b829eb8b3a9948249347b6ccad5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a0b9869d194af98b70e095598cab3ab85032828ead695d63f75204d7418fc`  
		Last Modified: Tue, 30 Sep 2025 09:24:30 GMT  
		Size: 27.0 MB (26995278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed492992022fa9e4a253b427574c9ab21d82072f73e353ad6f09e1555a92cc4`  
		Last Modified: Wed, 01 Oct 2025 11:14:56 GMT  
		Size: 73.0 MB (73034854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48553d2ede59ecf14cef32cc9d20fe7890483825372d31b7943ab6f87976b2a3`  
		Last Modified: Wed, 01 Oct 2025 11:14:58 GMT  
		Size: 231.1 MB (231092646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29e2c387e143c705ef64ed6716b9bd3c7e93355d962523874182435c09278fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eacee2e9f18d99fed5cff79b603c1903e7dc56a4ebf69cc15709c09f1577b4a`

```dockerfile
```

-	Layers:
	-	`sha256:d9cb80af45affabf019de1d8178ce3013e858d11273bbb5f7bfff9cfc99d8256`  
		Last Modified: Wed, 01 Oct 2025 20:47:50 GMT  
		Size: 17.2 MB (17192596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90beb317a1daf1f6a1239890c736ca1214a9e8465df2cc3a2b85e5e3088c0261`  
		Last Modified: Wed, 01 Oct 2025 20:47:51 GMT  
		Size: 10.5 KB (10541 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9dd0bb42a0983289292c9387e14dc974a28d523851388806f01cd4f1d4505789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466084022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a332443e97426c6e6f2e3b0f40c2a856d8820e488a49955b8bdb47b2e2c4f7fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8533144b875d90b1f9c5a4ecb4c26177d9b646c254cea7d68fd43c77c27f975`  
		Last Modified: Wed, 01 Oct 2025 10:56:05 GMT  
		Size: 25.0 MB (24952783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c645409e32b37950d400f06f75fff87e9a716322f248e5d01d290689226a51f`  
		Last Modified: Sat, 04 Oct 2025 03:44:05 GMT  
		Size: 66.7 MB (66659977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be72a6f5c272ab7d043f52ef88afbeabd5c7edafe2d741a13995b64d1d8764be`  
		Last Modified: Sat, 04 Oct 2025 13:21:26 GMT  
		Size: 326.7 MB (326701253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d87b11e1e557ede063a939dedf60c727843ae9a331d190b7aeb10aa2e1b9e259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a171ad0390ae6023a46999b8159d50e7bb914dfcb8c4efb1f32aa6ab14f36e5`

```dockerfile
```

-	Layers:
	-	`sha256:f57726a13be4e0e79495048ce2bfe8681e92552bc26d988758dc9d67291b7d68`  
		Last Modified: Sat, 04 Oct 2025 13:21:06 GMT  
		Size: 17.3 MB (17263257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8128a0d76253f45d8d9c21e1c5389c2208eade78a107ef86d2c25879e485769`  
		Last Modified: Sat, 04 Oct 2025 13:21:07 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5f73f24afc0a466d5bbb20f694159103bbb751a9905e86bf152e6ae2429442e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351233324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a92d5faa718db7e37acc57b13d816ae0597dc3e06210d092d3326da40a68c08`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae40148dca91a7d747a8331f403c812cb96e16b0e939c3f7e22eaed6bd4173a3`  
		Last Modified: Tue, 30 Sep 2025 09:36:14 GMT  
		Size: 26.8 MB (26782227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2360823d72f62f7ab99d1125b961476d915cd531da8e87d42d3767dfd3b86d6`  
		Last Modified: Tue, 30 Sep 2025 15:54:22 GMT  
		Size: 68.6 MB (68637856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e220bcc3f5844a343314a213e702ff36277cc749e3871aa8b07e38bbad44107c`  
		Last Modified: Wed, 01 Oct 2025 13:21:17 GMT  
		Size: 206.5 MB (206461799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9216e01718237427fe142a8e5f4f879e4e3c0049b52655d3b387be67abedda94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd70451d5b28fad9c713a1c5263313b8f73a3f8e6c3f63e36caefe163933389`

```dockerfile
```

-	Layers:
	-	`sha256:a233cbad9965aafd182187fc4c1ee2cbbb3f1372ebea96b6817fd3f625d14cbd`  
		Last Modified: Wed, 01 Oct 2025 19:22:33 GMT  
		Size: 17.0 MB (16984280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413ba6f62d9016526c85155c2c06efc1e6f90fda75b98903977e44d6561b25dc`  
		Last Modified: Wed, 01 Oct 2025 19:22:34 GMT  
		Size: 10.5 KB (10505 bytes)  
		MIME: application/vnd.in-toto+json
