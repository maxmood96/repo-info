## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:91adc5e54749eb4e9e72dc22e6786cb77d53969094fe7792365ce90f5a4c5ca0
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

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:30b101f86871eca0a9a768eb6dbd75e12740454ae3d8078bf844c160ab1e5e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.6 MB (378581602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520ea41ca75a155a46f8767b069be43b4938f89065a5e3468c6d70b28e1140d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad446e7df19acd39290d995e6d78ccbfde171596237968a140518b183d94c04f`  
		Last Modified: Mon, 08 Sep 2025 22:39:48 GMT  
		Size: 235.9 MB (235911680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5602837cb0eb65076a3a7fe915f37db184a91df4b2dfcfc940e995a0d5506ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2e5f515cfb9d0fddc298c75c10e6601d9731aea91329c0c7392021a553a089`

```dockerfile
```

-	Layers:
	-	`sha256:0b2f9ea16dbffd25ebbbf502e7183cb00662001b90cad7e6ac1200656ae7dab5`  
		Last Modified: Tue, 09 Sep 2025 01:03:43 GMT  
		Size: 17.2 MB (17207047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9150a97148a8943bad12961e6cb8b10a9ecae26f2d412e39d3c30e7420b912`  
		Last Modified: Tue, 09 Sep 2025 01:03:44 GMT  
		Size: 10.5 KB (10505 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5bc8ea6965b0224bfc773e1d437f65ca66e784ff09101ef8018b6470661631fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342776469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5668ee0599ce5c29e10de4381c60b28cb57707888258353efff14537618447d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0096434708f67385cef0fbdd93979f2d8849a82842e1217f692977f3e6600333`  
		Last Modified: Mon, 29 Sep 2025 23:34:22 GMT  
		Size: 47.4 MB (47448480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465ab5ce2f6d84d807e4534e3dcd0b62e1a1f4c158895b4c7b3539c651a1fd9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 24.3 MB (24341544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cab31d748b7b8f9f94774a6883d028265fd21b230de80c9e3380a4eb4afc67`  
		Last Modified: Tue, 30 Sep 2025 02:18:18 GMT  
		Size: 65.3 MB (65317483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79018456490ca5855115540fba19e6d714903041ad69448e3f7fc7b7c07af4b`  
		Last Modified: Tue, 30 Sep 2025 04:14:28 GMT  
		Size: 205.7 MB (205668962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc45d2f63b92b4b0d973fc349f2dac1a73c742868aa498f03f9a4ec6485fd9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16979822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6957e98b57ad265652ccf1ef24f28d340c8e0623ce5248e8a5fc20e5583307b`

```dockerfile
```

-	Layers:
	-	`sha256:7dabc1b11ff14f4e8e9b6c3434e838fe8f46d13e5983a9c99b0511f618b3e879`  
		Last Modified: Tue, 30 Sep 2025 06:36:43 GMT  
		Size: 17.0 MB (16969245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0850f46423fb74848b1f765f80def5fe917f9ee8dac21ad4b7fabb4109324b`  
		Last Modified: Tue, 30 Sep 2025 06:36:44 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:561f160beab710090a23f780aaa13788599f45636f2e8de3e8b0995faf0349cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.2 MB (325243696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96ab8c97c92b83b6a81394041b806fb8cb60702be53b0f1b0016ebf2f608d6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847685b749ce0208c0ad2a407e89f30279b1c8515c5c33f13a9c9b4c5e3da02`  
		Last Modified: Tue, 09 Sep 2025 06:20:22 GMT  
		Size: 62.7 MB (62719599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2036348658d5c1e73dc60e26a597693c7bfe4c2a1637ccf355bd7a79033ee2e`  
		Last Modified: Tue, 09 Sep 2025 07:22:34 GMT  
		Size: 193.2 MB (193198347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa519adfc6d389ec616f688b1fd6240dcf05834a3c85addf1daa2139a8b045d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16985612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8defa019181955a5f15aeb4c883c12e418ef26a1d185334f6dd10f88fa761482`

```dockerfile
```

-	Layers:
	-	`sha256:2de03440b9c14c061ac846a9759c15c7a3dd57d125a8e63fe2d979726ae39305`  
		Last Modified: Tue, 09 Sep 2025 07:20:35 GMT  
		Size: 17.0 MB (16975035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548ea28ae3854838e13c245ae756a7d67730d61229975cd744e644accfd2ae5d`  
		Last Modified: Tue, 09 Sep 2025 07:20:36 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

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

### `buildpack-deps:stable` - unknown; unknown

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

### `buildpack-deps:stable` - linux; 386

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

### `buildpack-deps:stable` - unknown; unknown

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

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1a55472eeea212da4af9f0a351dc9c8b5f3aa78fbfa4989682a15dd0247e903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384186016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2519608c7f011abcc0a9d8439593326b34499a0e9ad7c1f37655e955719de5f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf3914a916f37a54163b2eb02b685f6e0d654680e02a5e51b78387e81e4077`  
		Last Modified: Tue, 09 Sep 2025 06:02:47 GMT  
		Size: 27.0 MB (26993871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31355a04af67dd51f580585ba523dfd2b5ad7d91e873cb7213748a572df48bb6`  
		Last Modified: Tue, 09 Sep 2025 15:30:51 GMT  
		Size: 73.0 MB (73033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edecae95b05fd90248eadb0963fee10d4821b177931231ae243c72138252bf33`  
		Last Modified: Tue, 09 Sep 2025 23:16:12 GMT  
		Size: 231.1 MB (231054084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c450c295546a30aad7e0848181a2f330084fbbe454ad0fff0fe89bc76dbd287f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f673336e408e3722887216019bf3a1201efe477496b4b4ec6b9e037e564a193`

```dockerfile
```

-	Layers:
	-	`sha256:9db7d945de3c6b2b696aa4ac783091522d748da06a97431e410109e3ba205163`  
		Last Modified: Tue, 09 Sep 2025 22:21:03 GMT  
		Size: 17.2 MB (17192596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2122224a806e88be027fe0a6c4f7a7e3092b3c68c85e95c620f01512eb3af8ae`  
		Last Modified: Tue, 09 Sep 2025 22:21:04 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:27bd0126a134b25678b6961d820345d97fd6504c5b25fd92a01e51fd3acf6745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.2 MB (462193534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e62929c27369755bd63801569a10687a12800c42536e7250841ddded3f693f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1afb27b72dabce7ba373ba8319bd1ccd2205d7724f23909527bd3da7476b1`  
		Last Modified: Thu, 11 Sep 2025 01:43:59 GMT  
		Size: 25.0 MB (24952790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32856986223852ec3f854d1a7c152bc97555c3c9e06114ce074d65dc96a8dee`  
		Last Modified: Fri, 12 Sep 2025 02:24:28 GMT  
		Size: 66.7 MB (66660361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1a88d1459daf3018e7ed94125667851fcd959cf06455a19bbd26188b7bf595`  
		Last Modified: Mon, 15 Sep 2025 05:48:59 GMT  
		Size: 322.8 MB (322814936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2efd051ecb0918b9c2b903b4d813ec3b53e8ed9d7d984e9ce21bdae41db8640b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4494a2446da6e4f388b3e09ef802308055742c75c47ed52b389d1d1fe46a3b81`

```dockerfile
```

-	Layers:
	-	`sha256:4790b902afeb504efb0683f6147da701270a4ca58f1ca5f24d803fe6b3fb4fd9`  
		Last Modified: Mon, 15 Sep 2025 07:20:49 GMT  
		Size: 17.3 MB (17263185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6214570783f2e63b719218ad996c725d27232979c90d038ae99aea55566b7f4d`  
		Last Modified: Mon, 15 Sep 2025 07:20:50 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ba86cdccf2352f2787b3f0cc6eeafae7a7aedda33f204b2ab02c4d7e0cc4ed0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351197160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd76ecb3a651eb8e355ba727d861ab2e333a567b96db9dd449bbb64d7b6eb1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e7868b319a235eef909d5a12163c48c579e84d18d78ed794653cb126a0`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 26.8 MB (26780367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76c2286bf1bfe1b0d2250435d28c0af55c645ac84ddeac003b9da9b68c9c87`  
		Last Modified: Tue, 09 Sep 2025 12:08:32 GMT  
		Size: 68.6 MB (68636032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306840f46ff169a4a8d6b52d2078cfa9ec81edfd3ada29db24f34dacc219b6cd`  
		Last Modified: Tue, 09 Sep 2025 20:08:03 GMT  
		Size: 206.4 MB (206434434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca2e6e45deacb4c132c75397202f29675789a6d85b44285808fcb5b5d48b3f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67ea6d07b84419c4544b385e8eac706a877dc0a564420cbfafc0a35341177e`

```dockerfile
```

-	Layers:
	-	`sha256:b1e24f45e9e621a1320d681ca6f69523d305d1979469f927d6eaa1ea3cea6d6a`  
		Last Modified: Tue, 09 Sep 2025 19:21:34 GMT  
		Size: 17.0 MB (16984280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9894b0c87d24bc486982176afce1ad8c428c576a1f6a8d6c4f7e93f6f054aa00`  
		Last Modified: Tue, 09 Sep 2025 19:21:35 GMT  
		Size: 10.5 KB (10503 bytes)  
		MIME: application/vnd.in-toto+json
