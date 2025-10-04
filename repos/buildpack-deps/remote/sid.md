## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:572a544ef4a8531738439658e43b150f7c619219539e56911ec0dd05997e0230
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
$ docker pull buildpack-deps@sha256:89c9b65c1704d52b05344d60b783b57f6c495a033b80e409dc1731a496b9a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.0 MB (678991858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51a69e0dbf94be6c9193557f4e4d276a635cf64d71305b8871019f38392bc50`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:410e9863388c7a21d38fa0364bd31feaac4d5fae5c51ecfcc10007da8077b744`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 44.9 MB (44858795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eeddc4fd7915f74eff81bac7a518e5a7fecd59b3a04c00f06c47816cda9300`  
		Last Modified: Tue, 30 Sep 2025 01:08:10 GMT  
		Size: 24.7 MB (24743855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d489a9efad7dba1ba6693a0ea8aa439b3802b4fec6bf9dd4cd2a8d50b521bc8`  
		Last Modified: Tue, 30 Sep 2025 02:39:33 GMT  
		Size: 63.3 MB (63312060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95aa455bcfd87d3541d1c3583fa4e05a6ffd255602d9694ad0787507d509e2a4`  
		Last Modified: Sat, 04 Oct 2025 09:23:26 GMT  
		Size: 546.1 MB (546077148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51f5f8373115bb4c2a235cbb93b3faeb0930fbb73a9a4bd6e191405bff3e3ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16013029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d2efb5fbd4880426178579f657e2760b69780770457767a5d72aa8f5e9c033`

```dockerfile
```

-	Layers:
	-	`sha256:3a9f7a2c554e6d1f0d04afb6c8667b958bbe26fdc16de5709e76f28d786688d5`  
		Last Modified: Wed, 01 Oct 2025 22:21:59 GMT  
		Size: 16.0 MB (16002789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ad3d119dcf292170356579196c40204c546f6b984cf159d008960ed57dbee4`  
		Last Modified: Wed, 01 Oct 2025 22:22:00 GMT  
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
$ docker pull buildpack-deps@sha256:643e20d3c78e382812fa7f8e19931651dbe5c754b57e10c263e34e5f69ad9b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698586420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af33aa40f9fdec34a3955fa64896cfa9d73a64a842231a4b6e884b36f56c5afd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:77c8b650eb6fce09ed4263c2e250af93b45ee5839eef29ca2155317e0945bc1e`  
		Last Modified: Mon, 29 Sep 2025 23:37:42 GMT  
		Size: 53.2 MB (53152155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111aaffc2c801bff609a6e02c9de336f2bc1ea5c09d43a29d51e58997b20a73`  
		Last Modified: Tue, 30 Sep 2025 19:07:37 GMT  
		Size: 28.5 MB (28522160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984a3c965c22954420e5fc5d6d364efb5b25cb9467e9ee7553350dc94f4ffb93`  
		Last Modified: Tue, 30 Sep 2025 09:23:36 GMT  
		Size: 73.7 MB (73720279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94190c2cacb1fe5eedca0d37327174e55ac461832cc8679c8f42b332933f30ce`  
		Last Modified: Sat, 04 Oct 2025 09:23:08 GMT  
		Size: 543.2 MB (543191826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fa969484877915c6ffa657bace90aa42ec0aae56a986ea18f8afe8e9d6b55d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16229363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb4d966cff5504cd1c8ad2e59e0187ce6a6fc8c7b5fda481b3264c61de0548`

```dockerfile
```

-	Layers:
	-	`sha256:f3d9a82a0cb171fe808276ff6013f7c2a8fdad2a79140f7b548506313ca856e6`  
		Last Modified: Wed, 01 Oct 2025 22:22:30 GMT  
		Size: 16.2 MB (16219155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4ba4e4b3964fab91b4044fa09a705ca4ddc3cb1fb77eddb703cb8bdad39394`  
		Last Modified: Wed, 01 Oct 2025 22:22:31 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4c5b86d60c2a47b18f9568df30aade15edc1e03f26778fbeb21ec94094ae6418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1074829384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d93c586aa6c6c26245d0a082e6f566bfffe7e0d3c175899876618afc0aa65d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5296fd171b043d9adeac427b668a2c333e09261704a2befe2a2593421c6da9fd`  
		Last Modified: Tue, 30 Sep 2025 00:53:09 GMT  
		Size: 46.7 MB (46680971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d995bc0710c59defc3b6e948b5fec04402ad900b4af1204d7420bb8e2736886a`  
		Last Modified: Wed, 01 Oct 2025 18:09:27 GMT  
		Size: 29.3 MB (29334857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5342a4415df6cfdfa16b453bdb12523178508b905f6d7a7425c52c9dbe807e2`  
		Last Modified: Sat, 04 Oct 2025 09:26:31 GMT  
		Size: 68.1 MB (68132570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8a911f0e9103cc9cbc648070539f00433c38f8d75702cd3a96e2c3edd1bedb`  
		Last Modified: Sat, 04 Oct 2025 20:53:02 GMT  
		Size: 930.7 MB (930680986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d69ef1261c90835189151876e1109c6425dd9e941d2523f54337a6dbc5351017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16329653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adb5022c94b327f59781054b93dceaa314ddeba37aa0b70d8cd01d61905d0bf`

```dockerfile
```

-	Layers:
	-	`sha256:ef5019874f895c7a4d57db5a7552fb6f610e776524fbac8b904acf96fd3da587`  
		Last Modified: Sat, 04 Oct 2025 13:21:44 GMT  
		Size: 16.3 MB (16319445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26da5cc02d10e245991309b0c864a8bb1d9becdd73fab10594bfe86b4f3f929f`  
		Last Modified: Sat, 04 Oct 2025 13:21:45 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:780c0ee56d5a8f411786dd6089e5a1cfe69b53edf322bcbd974459b3aec78b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.1 MB (650137851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd713317b507386e536f25801d3c2d80b17afc9e3f22b5267e81a8b1bea007c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d997811a60a9b9144b07fdb085fc1feb6f43f5adf62ec1daf292a386279413a0`  
		Last Modified: Mon, 29 Sep 2025 23:37:26 GMT  
		Size: 48.2 MB (48234517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263fee109e376d69cd8ab45eebe497b85f6bb9dab4d00421e46048f3b05dbc2`  
		Last Modified: Tue, 30 Sep 2025 03:10:36 GMT  
		Size: 28.2 MB (28155087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1c052f36ed7138d27ebb7e300cd8fe66223f9064d8cb89d721192113efa6f0`  
		Last Modified: Sat, 04 Oct 2025 09:22:53 GMT  
		Size: 69.3 MB (69261597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4701bc7ece704ca33a82d3d3f7b7676bef048ab18a728870be4e9a59f82a996`  
		Last Modified: Sat, 04 Oct 2025 09:23:59 GMT  
		Size: 504.5 MB (504486650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5fc51cbc7688a442ef8da313d453d7e649e2df7b942b5138376acb5ba440b556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16021893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63be267f112976b1a6dbebc2c8227deb2fdbe09d35bc869d23e07e62c5fe3c5c`

```dockerfile
```

-	Layers:
	-	`sha256:aa112cbc9624b3b7ca0e63e368e3052d052292d3c9797154c0d926a95330a005`  
		Last Modified: Wed, 01 Oct 2025 22:22:53 GMT  
		Size: 16.0 MB (16011717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b69f017155bababf4148bbc77624a745c0d1a383efb6e54659f0c14e7e8e9b`  
		Last Modified: Wed, 01 Oct 2025 22:22:53 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
