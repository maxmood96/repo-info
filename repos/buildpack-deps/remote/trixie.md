## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:a866e54fbc1651e799948568c804db2267879213d8bf18354736e768fa3f797e
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
$ docker pull buildpack-deps@sha256:ba095bb649386b16b9fc040a78d3178a0517fca394dcd6a794ac9edc2ed63c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345661913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ea7e4b70bf69715291cdd7917f482d0acfa53e0ac45ba3034532d2360631a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d054220a6a95da9f3d586a2f3758d12b834db5f03df5446b2303636b5e04ce3a`  
		Last Modified: Tue, 04 Feb 2025 11:48:13 GMT  
		Size: 209.3 MB (209312786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:421e412642e50cc48434133d8fc62f191432878ad160c9067bad7a3999f6eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16712372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617465c67c203784a67272318700e60f7d05912337ea5b12e0c42892846c4a81`

```dockerfile
```

-	Layers:
	-	`sha256:43cb58f621a1a135d73938e960d782544b1e1f86a646f1457e362731c292633d`  
		Last Modified: Tue, 04 Feb 2025 11:48:08 GMT  
		Size: 16.7 MB (16702119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041297f6ef05786d56a6380863e85430c242c49e3901190b100bd6269cae8f43`  
		Last Modified: Tue, 04 Feb 2025 11:48:07 GMT  
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
$ docker pull buildpack-deps@sha256:152852cfff14bc437a7287e5859d939681a5c6e9a96c70227ba8d24f425c8e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388175447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94631a8261439570a602b04ba53bfa0e7dfbdc5a47b36031bd1be0769b4c3a5c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f8f4c2cf61c41cc250d2e87b5eba96ba3e64ef3a295453812dac1f66ba73216`  
		Last Modified: Tue, 04 Feb 2025 01:41:20 GMT  
		Size: 52.1 MB (52139243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7e1fce86863c28c734873936872848b6798972c915ef83ac0ef8757fcc152`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 27.6 MB (27596205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d5b75b14bc48f5cc9ed4250816b6c4c64a25a407024363029abe470236b5c7`  
		Last Modified: Tue, 04 Feb 2025 15:49:45 GMT  
		Size: 72.9 MB (72895536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3111d721719b367a41c04aea9d4ca3f134173acb02b4e328384b9335ca6c9220`  
		Last Modified: Tue, 04 Feb 2025 22:04:23 GMT  
		Size: 235.5 MB (235544463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94a87135974e8a3ceeacceabb479631ee4b6a6e8c0bb8ccf26e6c0add5ca1a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16933795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429e304bbaff466f62f0c6caccef8643225d716d2d0a9cd4b6e5ff357a5004a0`

```dockerfile
```

-	Layers:
	-	`sha256:bd7473dc1ccaf313d20f9856d5e7efadf102c6ea87b70d4251b6cc3876e0f151`  
		Last Modified: Tue, 04 Feb 2025 22:04:16 GMT  
		Size: 16.9 MB (16923570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b554005c7192fa9b624c559364f8230dabb378cd46a9d77accf1e479cdb300d7`  
		Last Modified: Tue, 04 Feb 2025 22:04:13 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8a193a73a1c36a407b2bd644b834c0afdc6fadc39439eec0f68045e7ab18584c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.7 MB (353653435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc12deedcbe8fa72abaa6a18c604fc957559d49267733fa5d1125898bb88dcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371642bbb4f2496e43eaeaa75efac59f54344b0c0beee1184503290cbf7343a`  
		Last Modified: Tue, 04 Feb 2025 11:38:14 GMT  
		Size: 68.6 MB (68552428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398f4fe2e4f51ccd9b7296baef872519fe359656284a911f15e9eeeebfeaca4a`  
		Last Modified: Tue, 04 Feb 2025 18:01:00 GMT  
		Size: 209.5 MB (209470061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cdd2970b265bc3108a931d0a6a43af9f3ec937aab68e03c4033ad571f535e094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16727327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d46aa5b714de97083a97265cf7cac8605c4be967c3d15b9b59dc47fcda3dfe`

```dockerfile
```

-	Layers:
	-	`sha256:2c4808a04df6dd60cd733169775798a94f7d4e091503687d0e0fc88ebbc23438`  
		Last Modified: Tue, 04 Feb 2025 18:00:56 GMT  
		Size: 16.7 MB (16717134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80172605fc9fe32f238c754acb56f450e6d73bd3f157b9254ab55ba57f3970ee`  
		Last Modified: Tue, 04 Feb 2025 18:00:56 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
