## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:5b6f6100bf0f492d51da4ee88ace8c2aca11852b45f196b362c0b8262fa2efa5
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e8e0a69af531b03890c5d7f7b79dc1efb1bd4e752b43e699139bab0851698a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378860259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2fb49f11106b54a837a4122c90d2944098ca55d46c88a43f150ceee850e65e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:18:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5470790761244112ed0b9ea9218282e5185dc7fd1e91840e855a32550e2ecd73`  
		Last Modified: Fri, 08 May 2026 21:18:48 GMT  
		Size: 236.1 MB (236145627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9de7643947ed54820d035ff5f43f1809924085db37bdca2faae303e8b04d8a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17219282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2aadb36bf63b24d9a566a1ecb3313526e98063d67b4625fb4a8ba932d691a9c`

```dockerfile
```

-	Layers:
	-	`sha256:967660fe690cf85f089b72e37765b55457234a13b7b53791a58be6884c169360`  
		Last Modified: Fri, 08 May 2026 21:18:43 GMT  
		Size: 17.2 MB (17208820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c037c9f373c90d8061a1118234909cf858b7d41bc4eebb97a1b6bb70f47cd97a`  
		Last Modified: Fri, 08 May 2026 21:18:42 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1b2cd4d1fec14e55ce21765ad3bddbb54d6546afe162405bcc53fba652632e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (343001465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b113f65408dfb7573a2d5fe15194d1b532f48f7f7911e06540ba9ca2ed46b19e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2782236aac3a37777665c4737690456903e8f45d5d8a06d88dfd8fdb29da5876`  
		Last Modified: Fri, 08 May 2026 20:57:34 GMT  
		Size: 24.4 MB (24363654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768a28224fae77f3965cdd69933693d2e36af26e730f0f75e576bd8b5e516d41`  
		Last Modified: Fri, 08 May 2026 21:56:37 GMT  
		Size: 65.3 MB (65318209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b43951eb50fbbec798a98a0d5e3979bc819241fd4dcdb56f1db4886771d88`  
		Last Modified: Fri, 08 May 2026 22:13:57 GMT  
		Size: 205.9 MB (205853310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50697ec36776ceb52fff6476c697773b7f18cf3961aca08b63bf29d364d144c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16981552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eab44ba133edd4264846b0d0f89cc902237ddd30f4a0092b2afb215de62708`

```dockerfile
```

-	Layers:
	-	`sha256:24c81a46c775a065f51912b80d8d038db7bd027d076e01d57d48f2c04223bc66`  
		Last Modified: Fri, 08 May 2026 22:13:53 GMT  
		Size: 17.0 MB (16971018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd59ec7b591e9964de409a0e1c89b2111e4ce385c5fa36297575d202c62b902f`  
		Last Modified: Fri, 08 May 2026 22:13:52 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:371f5dbaf1f5948705573252013c3064108c9b38575df95c66d5e2a441caa546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325564396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8182fff6ea4b726b34966731f7585d386bc0ca9024844de709738cb1e036f02d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6753753dc173af6d2d0689a1eccd6337abda3fd742e649454b834a7d6c6afc`  
		Last Modified: Fri, 08 May 2026 21:35:45 GMT  
		Size: 62.7 MB (62728028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c66f6797abbefc309d6193205f793cea64fedf67e46f6f6933d96ecdcb0436`  
		Last Modified: Fri, 08 May 2026 22:13:45 GMT  
		Size: 193.5 MB (193461530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:df2b3e7f01227db089a9e0865ebe03a94881801b2ee08bd1146fa867e9420aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be8fc58aa4025b84f5fb240d75100690a784be814109aace2bee4d04b143a8a`

```dockerfile
```

-	Layers:
	-	`sha256:bdd9ee56fd187469b2c93ca51d38f74ad9d02250275b003867361c562a03b8bc`  
		Last Modified: Fri, 08 May 2026 22:13:41 GMT  
		Size: 17.0 MB (16976808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc17bb485cc7b3ec5a2c773ad2e3f06fd94a681ef2d4350a45a16a84bb1e46d6`  
		Last Modified: Fri, 08 May 2026 22:13:40 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d62634dff550cac03a00088156076097bbe420ce40ece73fad1a5dbd14b1f1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368558450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9724175eca139410f560f92dbcd70fc4f5cdbfd447910493a859a118971914a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:18:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335e8e024cb0fa8e07cb848bdae282ce9861dd9255063fc58f55ccdf85a6f08`  
		Last Modified: Fri, 08 May 2026 21:19:23 GMT  
		Size: 226.3 MB (226273474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49806a6ec3279520cbbb0a11b158c273c9fe5d77ca81e91ae30dbc8bebde180e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17303668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3e0507956ef9b2088680b144c80bb9ec650dd5593e1acf82cbcb1a94be8730`

```dockerfile
```

-	Layers:
	-	`sha256:dee38f62880b01f8675ff5c7b6ca9ba12935993f526490d598bde14cdbd6f617`  
		Last Modified: Fri, 08 May 2026 21:19:19 GMT  
		Size: 17.3 MB (17293114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3f2bfa4285eac5e17ff63689825310d1cfc6af5838f7ed58103356a8a504a1`  
		Last Modified: Fri, 08 May 2026 21:19:18 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dea633402395783965dcb2969bb95f3bdd9b4ceb9b2ef85c72091894f60845ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387670308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bbd8c1540ee905d08116487b145d3fb6d58f20bff28e7c505e72c0771226b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 02:26:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3633f2ad7dfa64f7e00b07a5405063f2d661e1f1a5e715c57ad65aaaf0f60d5`  
		Last Modified: Fri, 08 May 2026 23:05:42 GMT  
		Size: 69.8 MB (69815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfce016012aae1811a31b56f808d3457fa3b5556823afa341bd018e63864905d`  
		Last Modified: Sat, 09 May 2026 02:27:17 GMT  
		Size: 240.2 MB (240244203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75604de4bab282d04f7f5b1277e41969a9e7ad2e357ea935fb585ad3be7a02f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17188847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c92531676ce0d0e41bc285099e54be0331687201c6b9b466301ac87db74ffc1`

```dockerfile
```

-	Layers:
	-	`sha256:9337feef28dcfbebd7a5616e185e1cbf471b94a35601fe89a02ca8e9cbd4e483`  
		Last Modified: Sat, 09 May 2026 02:27:13 GMT  
		Size: 17.2 MB (17178412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20cb62165924ddf129c52dd66b79a28ba5c7ca7275114fae5baf7c5fa38016e3`  
		Last Modified: Sat, 09 May 2026 02:27:12 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b9335fc474f4629e6b23b9605464f1dd5a243c8510aba7ad798db67de63eac2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384387111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb06264073546ca49c03a589d30fa5bce863233239a3dd1f0cb25a7f353749f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:17:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee24d1527042fdf5416c0f176e46ee07a4162716bc3c579e21e2b5b37cf0dc3`  
		Last Modified: Wed, 22 Apr 2026 12:18:28 GMT  
		Size: 231.2 MB (231209822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ed70909b9e74631f9da210fa61c333d10fde9dbdd6ad267afcbb4663cdc0eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17204871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6921d5ff5e0e65957a29c9f049c3b4342eed103b5782b3555769922c7cbfdc55`

```dockerfile
```

-	Layers:
	-	`sha256:e5a8c793af33a0245870710077dae9ca5e47747fa3d981fd629c382b3f152976`  
		Last Modified: Wed, 22 Apr 2026 12:18:24 GMT  
		Size: 17.2 MB (17194371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8413a70963606d62a3a222e1b2513a353581dceda9cc85e0fc3f2908f86e3b36`  
		Last Modified: Wed, 22 Apr 2026 12:18:23 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d901a5e0f5d7a950a054cf3660fb6298125aa34207e5bd21e10d5494c8b0d2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.4 MB (462427650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fba636082f21446a0bd411c85a02dbb3ef6b7204ed1e0712a1b396d87a8ac94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:13:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375b0ab5684a2ec8ed31b820ba37fcb1bdf59a507240c61d57d8e8abbf2c70e2`  
		Last Modified: Sun, 26 Apr 2026 20:29:22 GMT  
		Size: 323.0 MB (323025554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a3cc59c990582be6ba52bf15bb5e1d2881af6684b5bc7bc7c0ebf2d4888c605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17275460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9662f9c352ffdb3ebdbcf3fcd64595a2b08ea7a4a5d380df6a0f9c0e47d8c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:7a735deab0fb4eebbed6169f678f25be20fc2d2f54338183d45de20a6665ac8d`  
		Last Modified: Sun, 26 Apr 2026 20:28:36 GMT  
		Size: 17.3 MB (17264960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920d3036737980ac069abfc80d276f26ad2243e58e5c50133ed0c7216a900893`  
		Last Modified: Sun, 26 Apr 2026 20:28:32 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:819d60ec10fe68c4dbfe18149b9d0b7e34ac202218dba1ca05c6fac80d632855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351476578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea374f454d40e0ba5d69b340ef43377aaeb595cb496f8a5d976fce62787c99a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 00:14:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0445f3803885031cb22352d4abf0c173876f6316acd6230b59fe9c5654bfec7`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 26.8 MB (26802639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3bbdd2fc257950c611fd6795ac67747b411ad1789b54a283e0cb1bb22d4b2`  
		Last Modified: Fri, 08 May 2026 22:34:34 GMT  
		Size: 68.6 MB (68627825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03310278784aa9433f5e9518d7a38a810f4dc05b175ca1c33c9f49594f0d0d`  
		Last Modified: Sat, 09 May 2026 00:15:37 GMT  
		Size: 206.7 MB (206673810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b18ded5d6dc34428c55fd14418260edd54d3b7562166dcb9f1c0a9e6c3e84570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16996515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9c9aae08737aceaa8c0b1c92c56ae1c6548c444f06217222190310445ff39a`

```dockerfile
```

-	Layers:
	-	`sha256:eb43ee2f71f8c327f6a08a46f7724e8bf11be774853b30d8337e523cc040f912`  
		Last Modified: Sat, 09 May 2026 00:15:30 GMT  
		Size: 17.0 MB (16986053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3ede8ab3b423d3d717c5df95e81710c532e7bb896e82bda7f26ed775bac9dd`  
		Last Modified: Sat, 09 May 2026 00:15:29 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json
