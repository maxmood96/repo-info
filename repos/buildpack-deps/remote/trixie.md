## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:85b34559ae71686a42f39eb7935ddb733485a5b3feadf5da9d0e74065cb6f8bd
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea48770f60f8253d76816ba51dc2c45761969ad719afa9bbcf51d97b8afa20db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379522391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86afab738cdab5d117fbac5e1f2e0f1fdd2f2be5222deea5b1aba5d0c44394d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:692a22a94aa33126be6870a35a1980ffe9de71c0099f51ae704bd57260a9fc1b`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 47.5 MB (47471280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119cdb265769f912819a0900d5eb7385b02b7a4a1f5220c788c3497c9f3670b0`  
		Last Modified: Tue, 25 Feb 2025 02:12:43 GMT  
		Size: 27.4 MB (27431156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba4fa7d8fdc56ce202984a19f0913c41ba64b96758e5cadfe4d2a5d6dd09f29`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 67.5 MB (67516172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdd9c26f40ba8f781faefb721014da5253ffe38f234d19b1b66c714d76d80c3`  
		Last Modified: Tue, 25 Feb 2025 04:18:02 GMT  
		Size: 237.1 MB (237103783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa0c0fc82bd18d90908eecaac489a7356944e9611831c496fc37ae41286c3a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16865645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5dac154f0182f8570ccf57401cb70bd3d3aa0976ba40ae0b0d77289c5d421a`

```dockerfile
```

-	Layers:
	-	`sha256:84749bff8da6eefd6d86fe27fc1c2601d90b037a5b1a0b8c09ab0a368a42baeb`  
		Last Modified: Tue, 25 Feb 2025 04:17:58 GMT  
		Size: 16.9 MB (16855452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0a41db4f4cc78ed2eff6274be3208c195f0dcc1bfbf17ed2edb492f7676fc`  
		Last Modified: Tue, 25 Feb 2025 04:17:58 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:865defa61fa2613cad8601f5ebc893b90b78a38724958affca0e63b9f36d2d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343745859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7613d03b19fbd40cb9de166ab5dbd953b4dd9c485c07786565216c98e99ecfa8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:131ae520a4eaed5ef3f8bfb62695032fc5b0cf09159cb958245abf1bbddef3b8`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 45.7 MB (45706841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cfbb99d11f866136a1de25d46d555105f60a1f7b061aaf7d89155339ee129`  
		Last Modified: Tue, 25 Feb 2025 05:17:32 GMT  
		Size: 26.1 MB (26127258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb7a39b0019bff7c7c84e047f3e1f583a04358b1f598c468c944216bf4311bf`  
		Last Modified: Tue, 25 Feb 2025 08:39:03 GMT  
		Size: 65.1 MB (65143611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60237d957f53ae60bd3916e6ad8c4604caad9c2bbf8d78ff4906450ef90d1d38`  
		Last Modified: Tue, 25 Feb 2025 10:18:55 GMT  
		Size: 206.8 MB (206768149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25b4c5c1a4b9fa437d095141481a063242750032f39203252fcc4bfcd27e231f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16635094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc527e83936bef6f826ff3f72926a4a4e2e3d5feae5fa2fe352126f230130d`

```dockerfile
```

-	Layers:
	-	`sha256:e162587b3cf78d66751cf23cd7cd16414e67c9bc5eec90f74853f6a080a9f61e`  
		Last Modified: Tue, 25 Feb 2025 10:18:49 GMT  
		Size: 16.6 MB (16624841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c462b668af31d9a76c9146a96545d7324c03341bb37af1ddb852aa65529cef6`  
		Last Modified: Tue, 25 Feb 2025 10:18:48 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bd6da6e60ea23c1a5f489593637ccdd1bdd215a380e34e2d12faec42ade4af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327631135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757cf038f22f0f86988d656f343533b7c5012217c706f316208e77ac2d1675a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e33ebdd9205b4932e0915a58ae82fa3919bb7ba65980ba80c0f55146637007ef`  
		Last Modified: Tue, 04 Feb 2025 01:41:14 GMT  
		Size: 44.6 MB (44632834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b579f9683272f3a08c4aea06231a8e2c1bb0d003cd712e88bfd308809a74d5`  
		Last Modified: Tue, 04 Feb 2025 22:18:45 GMT  
		Size: 23.9 MB (23893022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8433f727fdc7ab38c5833ce7296a33e709d29dfcce93ccb57257c21adc2e131d`  
		Last Modified: Wed, 05 Feb 2025 05:01:34 GMT  
		Size: 62.6 MB (62561130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d403f0575dba08e82802fdd09737d2819850d01120ae3b232c8d2c38688813ab`  
		Last Modified: Wed, 05 Feb 2025 11:55:37 GMT  
		Size: 196.5 MB (196544149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32f5842f0363be79d9c89cfe46347ab530ddee39c0475410eb9d2de1d8f91ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16711952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4532cc6f1eedbf88406855f3486030a674509e227ba413c82bea4f3352b4bdf5`

```dockerfile
```

-	Layers:
	-	`sha256:acbaacdd8e6e6382413d099eac35ff6b795f9c73d7b15499883a5b6ff247c483`  
		Last Modified: Wed, 05 Feb 2025 11:55:33 GMT  
		Size: 16.7 MB (16701700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53051de34e3c5e577ff215b4a20d1cba9949b5398632c44859981dd73e157bb6`  
		Last Modified: Wed, 05 Feb 2025 11:55:32 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b9de5d2b6b716a0011e22c989a546ea4ca512c532a2e968f36a426efea1e4c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371621902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf51fe60c39f18a533a7ce3309fcff633e68dd43fc3ea21d0903c11a0ec1e04b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5e40a2b9fe32b2158c946023b700f61f57f567701b6be2e04192bbcc68fb32d`  
		Last Modified: Tue, 04 Feb 2025 01:40:49 GMT  
		Size: 48.7 MB (48735381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7a097e6822ff46406de4794f79cc58a671b1cf4aca2e12e0e5d75f3e88af8`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 25.5 MB (25503719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2170d1913f7fa1e873c1ee369893d0954947e899c3a86eb221ad1345da5303`  
		Last Modified: Tue, 04 Feb 2025 19:04:01 GMT  
		Size: 67.5 MB (67509562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abca9d1e86268c1e133ec774ecb84fd04c0ba5f7cd7e4f274cce8aff313fe59`  
		Last Modified: Wed, 05 Feb 2025 01:43:38 GMT  
		Size: 229.9 MB (229873240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87b6e7d46a899f4a7a003ac58f05647af127e79175476c9a04a137aac5eab579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17027898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bc36f83d6ecf9777e6bed4218254d36c027a804a727c253ef931146a52a3dd`

```dockerfile
```

-	Layers:
	-	`sha256:34cdc201731b7d4114e801e7bdb98a18d64cda142fcf085a1b226ed72e289506`  
		Last Modified: Wed, 05 Feb 2025 01:43:34 GMT  
		Size: 17.0 MB (17017625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224400fd4d3458e852c0e1d09fc6926bac81e3fe1e306f8365fdda9edb61d758`  
		Last Modified: Wed, 05 Feb 2025 01:43:33 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e6d87d4e2d0b1909c78dfae8482a9e5efe0fd692134c47496d16228b7c50a5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387918693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c646865cd1447c5795dae14566ddd4a93fec9cbff308d65e08054569241d028`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dcb935698360f1bab29ac55f866f04fa900325b5fd7cc453717787a10e4c3537`  
		Last Modified: Tue, 25 Feb 2025 01:29:53 GMT  
		Size: 48.8 MB (48768687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d32c316fc3ccb64f40c6d0195841a31fb8d71e5cc812824cf157a401090b0a3`  
		Last Modified: Tue, 25 Feb 2025 02:24:52 GMT  
		Size: 28.6 MB (28569292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa72fa9c3e348de2475feab504d12e1c7e8277a121ac1989fd7f7c0161b081d`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 69.5 MB (69473471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d984e782e48d9f873af047a4d59170903642b7d26efbab04c7b3588e244bc732`  
		Last Modified: Tue, 25 Feb 2025 04:18:07 GMT  
		Size: 241.1 MB (241107243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eda4dbbd8face00a60985247703fe0117754c2bd074f2fcce796290cb72e61dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16834480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba97f3e48d95021ab0b57b9f5337d5988f6b671d8d1336048015540ebad7a84a`

```dockerfile
```

-	Layers:
	-	`sha256:76e42aad2436f4cb04eb0a7f17f8258b80e486f6f6eb76f7e3730cc65294c534`  
		Last Modified: Tue, 25 Feb 2025 04:18:02 GMT  
		Size: 16.8 MB (16824309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e9d0f99d89714b8100ced34b15d319e0ceed1defebf7223094986307f5a446`  
		Last Modified: Tue, 25 Feb 2025 04:18:01 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c6ff7364be5680f38d13b892dfc510ef6b7fea19ffd14e2946c9fb6fdccc8fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358210820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88d5889ef8d61e64cc2bb25b42f6f2b72a17c0453a1cc2cd1b47901ce15bbf5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7826127ebc82b4ee7746953f0d6a69270e61dcbbf770239c14d7990a9a75f3f7`  
		Last Modified: Tue, 04 Feb 2025 01:41:04 GMT  
		Size: 48.5 MB (48512402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1db1bb102af1e1e6cc9344b3dc0fe8a2eacb41e418cb6879c409441345ea5e`  
		Last Modified: Tue, 04 Feb 2025 19:29:29 GMT  
		Size: 26.1 MB (26065581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ddad714b4d53955dc18a1aeba118edf8c418c35d77183888fcf175b9f62c0`  
		Last Modified: Wed, 05 Feb 2025 03:00:07 GMT  
		Size: 66.6 MB (66627729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda9e66a22c3aead80d0f53a6fbb19e67110206dfe108d51142f77e4d056edf`  
		Last Modified: Wed, 05 Feb 2025 08:09:12 GMT  
		Size: 217.0 MB (217005108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a7fac358d054776a689ffb57af956d838f254b318c5bc35a3547759695f8819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f87451bb4ae0587776976a205cd32d3b16072cf584710704c0908eb09ca466`

```dockerfile
```

-	Layers:
	-	`sha256:c115eea164794d5c7387dd3280c49301a53ed72b7d1596403e4df73c146544de`  
		Last Modified: Wed, 05 Feb 2025 08:08:53 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dbdb3935fc73e886dbad52d87770d957cbd7b3da319e52ce60b2cefcec3bae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (386010995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fba81901c03186a5e748c4da8f475c05b55c9ec495b47a53e65d539be72f5a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ea3e230c71f31965fdc8d0bdc4e71749c73ddb97789439e708ba01bec0516b7`  
		Last Modified: Tue, 25 Feb 2025 01:34:02 GMT  
		Size: 51.1 MB (51131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b138a9fbadd117790fd6473b3c1516b6ff1b1b1e5e321ff71f2a2c4c08c6`  
		Last Modified: Tue, 25 Feb 2025 04:34:33 GMT  
		Size: 29.0 MB (29016584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7bb81cdfac8e52fedda82eb71511b491bce0161320904fa9a6cf3542f360d`  
		Last Modified: Tue, 25 Feb 2025 08:22:16 GMT  
		Size: 72.8 MB (72849870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b9193155e6433be9c72a79a072384c8d9c994e3a46f363cea47d85fe4057f4`  
		Last Modified: Tue, 25 Feb 2025 11:57:05 GMT  
		Size: 233.0 MB (233013250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:48fd5fa468890d51856d7aff2e9a851b53564b542061cffa5cb937f395acf140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16856443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8a483835c66bb279c4c3c9d4c677d206b0c669dfde44cbd35fca6c0f140895`

```dockerfile
```

-	Layers:
	-	`sha256:2597092f65f219e1017531f65960cadade51c3e614910854a2debc90d3389932`  
		Last Modified: Tue, 25 Feb 2025 11:56:57 GMT  
		Size: 16.8 MB (16846218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61ff43ae01014d70b7c430e3452a9a00f8aed1b4b057d9cdfe31fcbbc86bba8`  
		Last Modified: Tue, 25 Feb 2025 11:56:56 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75a08081b54d2e72741a8dcc56634fe810b65b5c49af6d14164dd89f53e77798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352454019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0e746b391e6be1f516c21aa919b96d45adca4252a5ed707ed7d7734a10da80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab0460cfb129d20515573ff27552b94c41a5822739be2d7bf548df5315225ee2`  
		Last Modified: Tue, 25 Feb 2025 01:34:35 GMT  
		Size: 47.5 MB (47508261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec199ac309750ebc4bdf20cce23eb64ef847d0a7c63d2075c1e80b9a8017dc`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 28.6 MB (28608136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971e21f8d766abab097575a50fb382c4f9461b5b1c49e9167693254a56cb32e`  
		Last Modified: Tue, 25 Feb 2025 07:19:01 GMT  
		Size: 68.5 MB (68498289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d0b6a464804002fbaa4678001a519c5385071e63d3bd4b4e7858cdde7a3f3e`  
		Last Modified: Tue, 25 Feb 2025 09:27:04 GMT  
		Size: 207.8 MB (207839333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16daf362086a893af19dddbf51277bb30758181aeae9b7b4dfee8cfc60e32c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16650068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011a61c624e103ec4a28e6055ef330a76c3b4134fb9ff34804f002b54dd56f58`

```dockerfile
```

-	Layers:
	-	`sha256:f112b533cb3db1e1b06faf1a3b4297d9b6925022230049af57923235606d1eee`  
		Last Modified: Tue, 25 Feb 2025 09:27:02 GMT  
		Size: 16.6 MB (16639876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19418062cdc7e6cc001edf19870d3e1ccb3fc76b54f1765599a3e89a793ba0b9`  
		Last Modified: Tue, 25 Feb 2025 09:27:00 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json
