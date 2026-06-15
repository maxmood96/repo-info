## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:c349d8a4de32e2021a2106dc1b5cda0d2f2734ef36adab662ace6ccb87258715
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1f5cff44330996444e25679daded98ca38179dcb0312fdf687bae304a9cd41be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352921996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138114bc1e79083eec493ee667cf8a6994b2a34a869cd5587792c09a8e3876d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250af42f2a097a32d106444385fc18ff806e3b5890910b0e364be8e50256f63d`  
		Last Modified: Thu, 11 Jun 2026 00:42:46 GMT  
		Size: 27.9 MB (27921945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe07d3f4abc5d03b2d2858f1ba1c7420683bb86a466dddaaaedcbd7924b07e6`  
		Last Modified: Thu, 11 Jun 2026 02:25:02 GMT  
		Size: 77.4 MB (77443662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05765fe547c197c881954d9909682851237d680152ffb271cf1b9eafaa119e0`  
		Last Modified: Thu, 11 Jun 2026 03:17:12 GMT  
		Size: 198.8 MB (198755177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83f1279f1d40c4e2cd9e8e01d4b6ea9964273817ec479bf25e2b92b4be44b062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16863116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ed56ccb3e4fa41d6f018f197edaa71d6ac4ee5b01239abecdc490b25fd5abc`

```dockerfile
```

-	Layers:
	-	`sha256:5d499516851b2f510436c536cae124ea5673252370873b5074da893968d3b424`  
		Last Modified: Thu, 11 Jun 2026 03:17:08 GMT  
		Size: 16.9 MB (16852983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28092760f9e584588b1252b6baf03dd4d659c0636a8c94c5ec72dcf5c2c11b91`  
		Last Modified: Thu, 11 Jun 2026 03:17:07 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d5bbb5a4c7e0638f4ba9eeabb86154ede7f3b8a99f9c74d05747ee3fcc7ef14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298561847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395ba5ccb7a11ab9693b24e1307d4f822e420a622279537f5dcc2b5de385fcd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:20:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dddbc4e0b590efd809489171b20c0c05ae23facbf49b0dac491dc8f542364ec`  
		Last Modified: Wed, 10 Jun 2026 23:42:26 GMT  
		Size: 45.7 MB (45703240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86724da0b6362c0867d62fcf26f2b64559186172953570f5baa9b4fad9928363`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 25.3 MB (25312845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db452c0bb423225c4a3bd143fc60d5a1dfd43be7a750053460623b4d219b8bbe`  
		Last Modified: Thu, 11 Jun 2026 02:44:48 GMT  
		Size: 71.9 MB (71862939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26a8b68a15ff8565f805f1a8cbae50945c7c154d3d2222020cbeb0b36c25e20`  
		Last Modified: Thu, 11 Jun 2026 03:21:27 GMT  
		Size: 155.7 MB (155682823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c14fcf9ec1faa6bd21fafb4c5691b7e82460962dd0b2ab600a7b9d3821eb8ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16644801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db46ad6bffc4cd81ab2853614897b89e04e1db6b71c1b510c07270de74303e7`

```dockerfile
```

-	Layers:
	-	`sha256:6f90bc95f0302237d3bd0d17c5c91624534169eb67e615452cc1f6d7a5d599fc`  
		Last Modified: Thu, 11 Jun 2026 03:21:17 GMT  
		Size: 16.6 MB (16634604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6dd90e17893ab9c82074fbb216e793245d877c557e3c75aa91b2e03e79bb06d`  
		Last Modified: Thu, 11 Jun 2026 03:21:09 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aa11f51ec60dbf5792bff1c6c69040fd91968192918f7f90bdfabfa8d5b48dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341402666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86797154582c8743322bceb75a2f8dfa95e94ab6c55f26604eb2b823112cd474`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bde100970346a8633eb293a95aaa718b901d789108bd4e63e4f66d9d3771ea`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 27.1 MB (27124297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4cd7a68975013932751dfea9f2948b3d26def5e08e10b642c93f54033e1e2a`  
		Last Modified: Thu, 11 Jun 2026 02:25:15 GMT  
		Size: 76.6 MB (76571859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8b14370d37b7442fbcf3981445dd2548487cc599907de2ee4e3d68642b5c65`  
		Last Modified: Thu, 11 Jun 2026 03:17:25 GMT  
		Size: 188.9 MB (188887953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:139d8e908958dbcc29eec101c41af7167e505e455379d7b147876519bb42d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16969353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa171f48b1642c79c9c40e0d9c9979ed4b5b120f032f9291fd784d3224b186`

```dockerfile
```

-	Layers:
	-	`sha256:72044d7f4ab66208087526f0eeb3557218e3c9b6fa2a9331a77e052b92057f59`  
		Last Modified: Thu, 11 Jun 2026 03:17:18 GMT  
		Size: 17.0 MB (16959140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff29e63984ea85483da1ffdae884fefe17b4b3f620f02c843b26b64b6a78344`  
		Last Modified: Thu, 11 Jun 2026 03:17:17 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bca3d28b3409f55bef92a4e6d8c3c35519352930e5a7d7112a04ca2a2b764ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360629501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac606de3faf24135b64fea0f704e1bffce751ff29aa2f89719452db21b46ad96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:17:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6776bc9208fe6e23886fcebb117107385c0d62bb58b598a5be9aff86230bd6cf`  
		Last Modified: Thu, 11 Jun 2026 00:45:19 GMT  
		Size: 29.0 MB (29046245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307963f270d1b61f7485c87a06ce39b78dcb16c03a58803cde22b17a8b7d56e`  
		Last Modified: Thu, 11 Jun 2026 02:25:11 GMT  
		Size: 79.5 MB (79541253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5187766c18684774771c9ff30c737a4ee6af77e2b12e03ccb3db86b9101eb3cb`  
		Last Modified: Thu, 11 Jun 2026 03:17:44 GMT  
		Size: 201.9 MB (201936604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:005a13eb68eedb5dbcd673338dc95411dc5d7b941e60bcca142816568a508fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603abf46ab2603c1e5273cfa5471b256c7c874fb0c5a8ca26d1f8f3cfbc80eb4`

```dockerfile
```

-	Layers:
	-	`sha256:ece9c82f3e9ed5dd1102dd076286d1ee3c9b6e1a754a1e446c65743adedf0d2e`  
		Last Modified: Thu, 11 Jun 2026 03:17:39 GMT  
		Size: 16.8 MB (16822124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d8c4126427d2c40935eeb666b631d9f97a7626c04514b56b5973ce3cf8fcf3`  
		Last Modified: Thu, 11 Jun 2026 03:17:39 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a721da21fc7cd9a5b3749589deafe17577211d5a42ae9598c43e7040c58666ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361171239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc455938506f9e8feda12bd0b386e949ee72705422c9f6492d4c89ba4f482e64`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e0ce2460747d14df6cfd1da4b61c0c9b7caf034c9fddf19fabbcba65c2416ba`  
		Last Modified: Thu, 11 Jun 2026 00:23:09 GMT  
		Size: 54.1 MB (54132513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f91ba1bf8c0d9e7dee82b12886a4f7ee70c339c3778c5cf99a230830c8d7b`  
		Last Modified: Thu, 11 Jun 2026 04:44:58 GMT  
		Size: 30.1 MB (30117465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0b6bed36d53f6ece4654f5cea50eb41e560afbf8d24b742882a59a9592eec`  
		Last Modified: Thu, 11 Jun 2026 10:28:41 GMT  
		Size: 84.0 MB (83984627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba12de2554a5ddb9fbc56a08ad185dbffc092d30c70044c2475ab3603a1daf3`  
		Last Modified: Thu, 11 Jun 2026 12:49:56 GMT  
		Size: 192.9 MB (192936634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c27841898a13045cfa04fb21cbbb186c810d658dd785062afe24e43162bc424f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16835082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0b1660429354559e28ccb7ecf0d613f90ee489ada6a6d4b346f861f28d2e90`

```dockerfile
```

-	Layers:
	-	`sha256:3821c289038144501bb038851e03118c3a27467fbdb588bbf211f21bbd3b4fd0`  
		Last Modified: Thu, 11 Jun 2026 12:49:53 GMT  
		Size: 16.8 MB (16824917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9551896eed9386eba47bb4d950b692c25bc19b8951c38c8e6185e475f3a429eb`  
		Last Modified: Thu, 11 Jun 2026 12:49:52 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0825c93837cb195b8aca355b19b6a72d66d8e12b3c8b8ae0ecbeb486bcac0775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489673273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9808707c3a484a341b65df98146ac319c2e0b8488e0ac725d606335026aa3b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1781049600'
# Sat, 13 Jun 2026 04:41:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 16:58:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 19:08:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2efc7e0091930e45ea6218e0e9380e67d07fe2085c100b1d3d74190636f5938`  
		Last Modified: Thu, 11 Jun 2026 02:48:51 GMT  
		Size: 46.9 MB (46911636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b18596f8f629861877fe419ef9028caff67b10f2dba8a160480c551f8733fcc`  
		Last Modified: Sat, 13 Jun 2026 04:43:12 GMT  
		Size: 27.2 MB (27238456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbc93acbb612bc5718255bceb11979ccddc1f5a211420ca842ecd80d9a0dd40`  
		Last Modified: Sun, 14 Jun 2026 17:02:53 GMT  
		Size: 76.6 MB (76647225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2158d3b51dd02900f3609fa255cbb58890c4ccfeb7b988bdba1af078751ed549`  
		Last Modified: Mon, 15 Jun 2026 19:24:19 GMT  
		Size: 338.9 MB (338875956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62e508866289b3ccd2d054a61a677d13c0e1328230a046d046bc1b4c7d1242f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16930138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de4c15504ba7356be08e30723af3f3be5bfc0417502e7c06eed5d476b279675`

```dockerfile
```

-	Layers:
	-	`sha256:3d8f1903298d998b087276834b1523006bbb0ad200596fdfdc84fb2176882fa7`  
		Last Modified: Mon, 15 Jun 2026 19:23:31 GMT  
		Size: 16.9 MB (16919973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd590be3bc045f459198c8b0710ed4381e5970b47d3a6b8b3d39e0097c312ff6`  
		Last Modified: Mon, 15 Jun 2026 19:23:26 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:68525ec284fe9568b34f9289601e027ed9f600170878dc3ec36957d1b94b16b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326211872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ed4681b988ffeb5ef4ae1c574b2de344919ad27a6e6c12d490410a525b203f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:15:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb23912042361f66d2c3fed63550770682f92117280cb0cf2a2611ef14ea13e4`  
		Last Modified: Wed, 10 Jun 2026 23:41:42 GMT  
		Size: 48.5 MB (48541819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdb3735386433a0b206e3395692138596ad8486bc9cf1339bdb4dc651cae241`  
		Last Modified: Thu, 11 Jun 2026 01:44:48 GMT  
		Size: 27.5 MB (27516492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c93fa43c64e99f6e508916e89876e16992649f171cc918b2100f0106656d2`  
		Last Modified: Thu, 11 Jun 2026 03:27:12 GMT  
		Size: 78.0 MB (77981246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99884cb2820e61eb374697205c1413d83e75f6f1084452bb20acbf4bb4fe9cd`  
		Last Modified: Thu, 11 Jun 2026 04:16:44 GMT  
		Size: 172.2 MB (172172315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:038643f113ad2cd6c3756f04b1a220266955f221e26b99d837913cc65fa75032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16639135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231d0e15faae92374ea2adfe38974c24edf76426ac3f8797a0b5038dfbca787d`

```dockerfile
```

-	Layers:
	-	`sha256:e5a1c3520ad415fe6362ee9b5b7d002d68a773852b2119091f5f38944d1d2e9d`  
		Last Modified: Thu, 11 Jun 2026 04:16:40 GMT  
		Size: 16.6 MB (16629002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4deddfd299095fe87e39543e455f153efa6d4df496089909d8291f28c718febd`  
		Last Modified: Thu, 11 Jun 2026 04:16:40 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
