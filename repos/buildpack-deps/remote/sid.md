## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:c20ed50896d759229985e4e004ecd5ee13400dbf31b273d4845c3a9294978301
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6abfcc1d84da81688cf34da195c14d87e18dd27942c8be188d4cf1230bfadb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.1 MB (748127180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fac16fad48f844a4e21ba92a3ec1b36a4d96bd059c51db8c66cbf91f886011`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e26574e4db891d66a1e5b6eea7efe5496bb61e65ab34b6bccfa4228941ecb8`  
		Last Modified: Tue, 30 Sep 2025 03:17:23 GMT  
		Size: 27.1 MB (27050070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86429f6876fb8da0a626753e746ec375d5f24414fad40449bf193e18157416a`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 68.6 MB (68551074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2bc76e4a21ee3e085d88106f5b459e39852370e6d00e7976eba73a14a25903`  
		Last Modified: Wed, 01 Oct 2025 00:56:24 GMT  
		Size: 604.1 MB (604149071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c8c9c01c334ecae0aff3cfa317e0cc29475e5875039947471fc3b7ce03eb2a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16255224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf23370dbc821648b1e81ee6904d928b92de4627b9c8322bc00b90658c4b193`

```dockerfile
```

-	Layers:
	-	`sha256:8f861fff8cc4ab959b5edbbc814f99df35732e32499c6a4c0669cfe33377757a`  
		Last Modified: Tue, 30 Sep 2025 22:36:14 GMT  
		Size: 16.2 MB (16245048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d152fc34ba5a7bff13a4c65560ab707020d92a2f1bd533ea4c244c2c4fd8ca4`  
		Last Modified: Tue, 30 Sep 2025 22:36:15 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bcb4c61b2f025d56e6e22c77ec271d5a63ee13fd2af9b1e2a046096bbb996ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.7 MB (690718004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cf803f3dd44269bd9614ec114187f5eac9b9c37bc0e1fc0a659b228dfc3c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ad1c1ed68f65cb1c94163af3a8f54c7c8b00cfdd4c1c64d4129035587399407`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 46.5 MB (46536602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f466521323edb154d60c581fdb38dbebed8f12bec478faa074c4c81846031`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 25.6 MB (25584742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4855b9d94c21523e35393e46e12e43c1c3dde8d121a86df27935bbd16f5115c`  
		Last Modified: Tue, 30 Sep 2025 02:18:23 GMT  
		Size: 65.9 MB (65897357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04128e1e5652bc71796132a0c3cd6aeb9c92df7aebba51ea6832311de95369`  
		Last Modified: Tue, 30 Sep 2025 20:43:04 GMT  
		Size: 552.7 MB (552699303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca8754161e933d2bc913e4728d44690fa6f082a7704cf28158f8fe11d4bf6efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16007477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c9c6d7bb4f00a2e6d183209e07aea2ab96d3db38dd8b682777ef0ad66855c`

```dockerfile
```

-	Layers:
	-	`sha256:03fd2efb54a04d142d348e619643e31ddc34601faa3a93a1c5b6c29abe1fa687`  
		Last Modified: Tue, 30 Sep 2025 07:21:51 GMT  
		Size: 16.0 MB (15997237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60def5362ef367ff73000c14d3b413defc4f2f85486001023dd8123bb4c8512`  
		Last Modified: Tue, 30 Sep 2025 07:21:52 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b60afe0525708601c4c6161e900d63ada2a732d1d7da423d0bf4a03545152a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676089212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a2e5971b3a57416593b5aed069b5999ead1c3fff6eae6d3041979c6edeca83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d30a0c5c579644a88a894fd0b1f1db229651b30c974b07aef6ab9bcde5b64440`  
		Last Modified: Mon, 08 Sep 2025 21:15:47 GMT  
		Size: 46.0 MB (46006695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf528d0788e249a97adf6d73be0b9ae329c2651a09b55c47f7bfbe9fc96a9cd`  
		Last Modified: Mon, 08 Sep 2025 22:48:40 GMT  
		Size: 23.7 MB (23710180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717220db35946b78b9fb18d38321ad58f2681e6386e6e8368e047874b841311c`  
		Last Modified: Tue, 09 Sep 2025 06:19:30 GMT  
		Size: 63.2 MB (63213996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533570c355fad30283f389efa2203bf589822f15e8001d3aeb0107fe223876b3`  
		Last Modified: Tue, 09 Sep 2025 06:21:56 GMT  
		Size: 543.2 MB (543158341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b1b4f19c09b8f1ea3323bf536ef4d2e38d869c1034b45bc3f0843dc16ab6dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16053053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f164c3e22b58400be25ad55e35587d3d1734a1a6fe8c7669ba2852544698a4e`

```dockerfile
```

-	Layers:
	-	`sha256:7da3c8c563f00599da3b444c11c7f6df723fe44045ecf50cc0f2eb564e453002`  
		Last Modified: Tue, 09 Sep 2025 07:21:07 GMT  
		Size: 16.0 MB (16042813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3c5e838dcd24e731d4be842dc3464fab6e29e6260043965b0d984fcc85205a`  
		Last Modified: Tue, 09 Sep 2025 07:21:08 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2fbfc2820a6a9f1ae0ceabd60e65b8dd52769ec758afc2e15fdf97f717ef3709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.8 MB (751754609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647b5ad9582d718d57b60b70ded348c017d3396aac24804a43e65e5bbb960b4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f20ec06b0e305a026538da296c8990c47be2e5df6951865d9920759cdeaeb5`  
		Last Modified: Tue, 30 Sep 2025 00:14:12 GMT  
		Size: 26.3 MB (26345963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b53826f16396691cd675240f8b08bf70b30d5a527d2aaf12eedd7838ad3b7`  
		Last Modified: Tue, 30 Sep 2025 02:14:02 GMT  
		Size: 68.2 MB (68179555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30251d5875a90bdcdf4cff48de32bb34c1bde266e94e0cd09d80468c6d566ab7`  
		Last Modified: Wed, 01 Oct 2025 13:22:04 GMT  
		Size: 608.7 MB (608741100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:187c1db44fdd90a8cf0ce370448d98b6d0a89b24d63c49193e62cedfb8b7609a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16329848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc994d80901e21767839d97bb0f5348901964412e08f59c832e0feb2db506f8`

```dockerfile
```

-	Layers:
	-	`sha256:42fa2f8b3a17185d36610f594a7da17fff7df7f681c0359afab5979bb6ddab10`  
		Last Modified: Wed, 01 Oct 2025 13:20:36 GMT  
		Size: 16.3 MB (16319592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193f30e14b13fbeed1142a68e2c1bbea5644b23fed37768f9b1198b0c232443d`  
		Last Modified: Wed, 01 Oct 2025 13:20:36 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3af0d643ae3c03999dd9b8bfa817512deae4faa40052fff85e74cf32aa8cf84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.3 MB (748299018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20d09c0c52074e4c13537645580857b0ef0339088b5ce0868c394e8671714e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022e41d633c4affaf1ac4e552e4213448a292b3aff35eb2748ee936cdab8ed6`  
		Last Modified: Tue, 30 Sep 2025 01:19:38 GMT  
		Size: 28.2 MB (28189334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbc4641a87c97f6e9e6e2361254a7f1b45a142ef503068f7c0cf3708f035a44`  
		Last Modified: Tue, 30 Sep 2025 01:20:22 GMT  
		Size: 70.4 MB (70426965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e039924dde5be80dc8faa6ab0c0cd8cc6919498c24d715f0086082f37e75c63`  
		Last Modified: Tue, 30 Sep 2025 20:42:42 GMT  
		Size: 600.0 MB (599996548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4ab8220f0b5738eafe18ce0b0104b1b8887c38a218e59920731b845238f74dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16224993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86241d58cf254c5f80d97af90128e4d55b650773d271b3e5534e7dac5bcaf3a`

```dockerfile
```

-	Layers:
	-	`sha256:ed757ca8752799dfac5f46813cde62dbbd76f6536820ba101d332b9678beb0ba`  
		Last Modified: Tue, 30 Sep 2025 16:38:23 GMT  
		Size: 16.2 MB (16214839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ab21ce3bd31af5271d573085ddcdc67c6faf13e31f3de82cd8adeaad8f4c49`  
		Last Modified: Tue, 30 Sep 2025 16:38:24 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:effaa099e49c53089ddd87f6100d3948021195f073e39521db1c2c7c307f405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.6 MB (704596123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a18c2b2a29473b052629b68e3c12ae35b6ce414beab34915f0cac27d34cf4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4775def833a620dde4f1cc169ae067301bfe3a34dcf5509c22eb227d3468f1ec`  
		Last Modified: Mon, 29 Sep 2025 23:36:30 GMT  
		Size: 48.5 MB (48517068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9e4d8c8e300db469e918627e177662d2c9145c896127a833eae485613de801`  
		Last Modified: Tue, 30 Sep 2025 14:02:31 GMT  
		Size: 26.9 MB (26941858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355dcb4e6f8d4305f466d18918201a1d1987966e7ad83941fc93d52a3f5818a5`  
		Last Modified: Tue, 30 Sep 2025 20:30:18 GMT  
		Size: 67.4 MB (67390921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee46d4ef53fca69838df948d29fb18c713ea0b44c6b9e7f51023792fab32ffed`  
		Last Modified: Wed, 01 Oct 2025 19:23:15 GMT  
		Size: 561.7 MB (561746276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1785e4433ec00819b8ca1549fa98d7e21a76141383a82e702b1fbc32c863f355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bd9fb027f5ad0504f7ca91c9f8e45a75fdc136cd0b4eb1f5839a8cf5207a9c`

```dockerfile
```

-	Layers:
	-	`sha256:badd93ecb9f494d0c44cc33d7bc4448dfd647627ce40097d79dafa74ed67117e`  
		Last Modified: Wed, 01 Oct 2025 19:21:15 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:036b3c66eba3f199cc159e76eb73a1bcc676fa69a4af9e466aa31a120cc502f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.7 MB (698726985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a053e5a4c4ba9a816b2889c1c70aa99f07ff309ed97d5aa6fa6caff3aacbb2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:772eb1186277ef333cc2188830519c27192dac48fb00016f4bed1d6fb65f0e2e`  
		Last Modified: Mon, 08 Sep 2025 22:22:18 GMT  
		Size: 53.5 MB (53458792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383909d767bd90933a41650a2f22af3654b67dad5eb9eb12c8f0c5d5619ec04b`  
		Last Modified: Tue, 09 Sep 2025 03:12:59 GMT  
		Size: 27.1 MB (27099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21675bb5849f4e08ff04ccc490a1604dc152c26899ff15f1b7123fdb165262d2`  
		Last Modified: Tue, 09 Sep 2025 15:27:53 GMT  
		Size: 73.6 MB (73617666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad765ab75d0a6a4c333030e5f3b064803fd117c5339f9dfa354b30257c524dc`  
		Last Modified: Tue, 09 Sep 2025 21:40:18 GMT  
		Size: 544.6 MB (544551403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91063110974a0b3cbe52b193adbe1dd39408197fa51c309e0ef626f05d9627b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16269397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76038cc69c72953a62e1e3771a6f21d428dbcf51b7f7cad129752ba607339576`

```dockerfile
```

-	Layers:
	-	`sha256:4f3e44845fa2378c9a57d210a380cbb6c45080a3f1d4c08c2f4547ee5528b9c4`  
		Last Modified: Tue, 09 Sep 2025 22:21:35 GMT  
		Size: 16.3 MB (16259189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6bc887582d9c817c29a1cd48cb31828e040042b4c4ae5c7d7a91cd728e410e`  
		Last Modified: Tue, 09 Sep 2025 22:21:36 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9d1771dafaec8675a8c047988a0f3d4027c9612c73c699628b084689d307a7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1124032780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2457e96aeafea6680430f666c9bdd305218a5274b2a6b5705d242d56c2f58e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:347be58a551dcf8aa3dd300ae844cdfc6ff2cdec19870bd090fdef86fdd7d393`  
		Last Modified: Mon, 08 Sep 2025 21:38:55 GMT  
		Size: 48.1 MB (48052647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a5a581d6d2c97cf774bc90f07071cf2fb0f1b3c0571346161822b7094bcd3`  
		Last Modified: Tue, 09 Sep 2025 09:13:34 GMT  
		Size: 25.1 MB (25071945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db66c5e84f1e64845f6aff4b1b0ac7d573e0b57248e1ca5ccfaf4eba4dd11ee2`  
		Last Modified: Thu, 11 Sep 2025 19:17:11 GMT  
		Size: 67.2 MB (67219693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5975c784cecbe0f508ec73d74fa0bd717c7ef95c02fef2b17d58176dbe184b`  
		Last Modified: Mon, 22 Sep 2025 17:13:34 GMT  
		Size: 983.7 MB (983688495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba4f420cb44db23c76835b9ae5e7b7360c7e6bd1d97cd5ef8f5fb59e329f4fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c870f4fc516d87fdabad509a56db7ebf8582dadf3f31fffb7b7a623eb4cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:672edda9bc304e53b7f4f6f8e25a7a68c14482516e39396714790b57ee427f3a`  
		Last Modified: Fri, 12 Sep 2025 04:21:16 GMT  
		Size: 16.3 MB (16329390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d685913a2ea01f50085238a48d4dc9c323bd5013a292b680be2e978b797b68`  
		Last Modified: Fri, 12 Sep 2025 04:21:17 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:167dd9489c0ea3ff93351e424da2d2ebee4ceb506b59f5be29ac12621c806a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650377464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5cf25160f5e223cd482835873ff1ad3accb55900e468db4c1ea5b5d7406e36`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75e6f7d74f7a64a858e5c9cdecd19e5f33e99956d1f33d14985ac51b655eba01`  
		Last Modified: Mon, 08 Sep 2025 22:22:23 GMT  
		Size: 49.7 MB (49652038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f495f7a03a882cda8ba1cac3fcd8e67045987237ece386400cab302efabfe1`  
		Last Modified: Tue, 09 Sep 2025 10:20:34 GMT  
		Size: 26.9 MB (26893291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29a0faa66c0d5bc6228e67d1d922c479797207d6a82c57cc284e6c444b5ac1`  
		Last Modified: Tue, 09 Sep 2025 17:57:25 GMT  
		Size: 69.2 MB (69168726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70588f764f63caae860735a5b6598b9b96c443fb133b7ccb3cdd5d0e6d533d7c`  
		Last Modified: Tue, 09 Sep 2025 17:57:25 GMT  
		Size: 504.7 MB (504663409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04470021072f64587be0b3c8635c9ac68e31f5d0ab1e47245596ddbce3260a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16061917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94349f6d8647124a352d103dcbb812a80f91860d27221996a318e8c42659f11f`

```dockerfile
```

-	Layers:
	-	`sha256:6fe45b7bc7476e328d64cfd833f73a3ec37ded12ded649748e473e215ce82b01`  
		Last Modified: Tue, 09 Sep 2025 19:21:45 GMT  
		Size: 16.1 MB (16051741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13fd14b7b4c971d2c518d637418e4d1800b160218f8fbfa5ff38dc7d1dccd243`  
		Last Modified: Tue, 09 Sep 2025 19:21:46 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
