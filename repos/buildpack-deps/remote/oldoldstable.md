## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:792277ae89e85f17419cd004722d83f4076354b2365d18ec6c0faa50d9ef23c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:58e4557773304919793094e2c07d2531c8a206b2afb7c1db6c031993d6a92883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321641750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25760206214cf675be876f59712241ad4fa356219f12f153a0d80d5a9a40e781`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:41:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816526a6d4acf81b392ec5a1e6d8d402fbc4bf0460323c5ad45b376b247ca6fc`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 15.8 MB (15790805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3cf50c221acb61e259a7ecd20caf425597eca7d93e329dde2640ca7ec8aaf4`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 54.7 MB (54742897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a160e6d2c8242d5f49a2c1be818ab0f47647e5cc5cf1fcb068e6618846d778`  
		Last Modified: Wed, 24 Jun 2026 03:18:13 GMT  
		Size: 197.3 MB (197335039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:859ec10ff9ece4e5afa2026fe5414bde0abeaedb40cbb4955ea366b1032aaffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123b5aa6a684a1b85dfa65a8c10b1e8d5c9c4b629db2c9ab042aef1e0e781931`

```dockerfile
```

-	Layers:
	-	`sha256:62eb0afa67004b892e10b2b932951b09cc61870238976650454079958edefb2f`  
		Last Modified: Wed, 24 Jun 2026 03:18:08 GMT  
		Size: 15.5 MB (15471585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062f77a6e545f2c918a048c96aaea36d64b2b5ea63be1435e6df93a1a601426c`  
		Last Modified: Wed, 24 Jun 2026 03:18:07 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce74b3b708e790074f680e1d7c4c0c261f06a4674457d5a0959ecdb0997b8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282407921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf02a27274cc9a8c483097b9128a60f95db0324c5973db3879e3cec766dda1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:17:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fc5ae1e57bd12fc3393aea9c4c883b87d2ec58e18ce0892f8effba71fbfcd039`  
		Last Modified: Wed, 24 Jun 2026 00:28:02 GMT  
		Size: 49.1 MB (49064073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354f5593b138af5d5b60d8e82c822aa52fd74f6a603db24886e0573d60561397`  
		Last Modified: Wed, 24 Jun 2026 02:23:28 GMT  
		Size: 14.9 MB (14905363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf4cfcfd51cd63cbc0a86a0ed17f661e5157a3b24f24a750cdb7ac4191f84c2`  
		Last Modified: Wed, 24 Jun 2026 03:55:06 GMT  
		Size: 50.7 MB (50659165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7e6cd4f6193c57c8019ecd8089fc02e4912acb7efee4fe62122766c0d5356`  
		Last Modified: Wed, 24 Jun 2026 04:18:24 GMT  
		Size: 167.8 MB (167779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89f413925bbddfd8f5b200698a0363c8a6b0fc1cb1f20657edfa9deca1804b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041afc5bc5fa36ad2e9e9b1b068f89fa8b429178e20fa0772ec392e0701f2440`

```dockerfile
```

-	Layers:
	-	`sha256:4090b25e489ddcfabc1562f08513e3569f9d0cd33c00ebca6a398f73f37ddc74`  
		Last Modified: Wed, 24 Jun 2026 04:18:21 GMT  
		Size: 15.3 MB (15270903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9d951509d7aefd38563dd5e8d9b4473165d7bcd00faa7c5980ac8063c44c46`  
		Last Modified: Wed, 24 Jun 2026 04:18:20 GMT  
		Size: 10.3 KB (10257 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f47cb2c919c6c97203235b896898598461ce8ab4fe3b6ca69d580b5a37d91d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313141194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbdbdcd0fac59df64f04ffa2efd9d81d51d6de0d0949b5c6f4b40b37bfaab05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf305d6ad7bad47ee0696c3db8b8fed8e9c2a42c53b57d047f8ab32f5d9b546`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 15.8 MB (15774954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f37219bba62c0b4908476dc3cf7f0f98f1c87e8908c188797b1dc1f610c77`  
		Last Modified: Wed, 24 Jun 2026 02:35:29 GMT  
		Size: 54.9 MB (54879567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e939dc6537087193b54cb28550f30706346c9eb7faf3f1da018845a5675ef09`  
		Last Modified: Wed, 24 Jun 2026 03:17:29 GMT  
		Size: 190.2 MB (190229454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f39f84b07fca064d021586fac213b4e157bfcdcadaab895e51ae31f202562f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e567c323910be73c6abc1da574477c254029ed214e0dd4eea4906e57b8541579`

```dockerfile
```

-	Layers:
	-	`sha256:006c1e02fb70beb7a1ede138326b3d0a5bb73ad01083b3938f58857921c5bd2b`  
		Last Modified: Wed, 24 Jun 2026 03:17:25 GMT  
		Size: 15.5 MB (15473530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980d022598b4fab4021ab589890109804dcd11c67ddcd9834a292aadb3a99f52`  
		Last Modified: Wed, 24 Jun 2026 03:17:24 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e73432b9ca5a0e15961c5ab8066e5ec37834811838a5cfd94e73ba13ed7adb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327300029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd99a38ff8a787910c743d5d6beb0d1ab3880b5582f6f4690251e366432ae50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:508ffc251196056212d40e318af0b7425af79fd3069a3f9ab15fd6220917ec75`  
		Last Modified: Wed, 24 Jun 2026 00:28:09 GMT  
		Size: 54.7 MB (54712884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f059b391cd2cd82464a697d38282bb9c5437ac5b83e7b92cde4d9a0644a137f5`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 16.3 MB (16295718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18472033acd6c573e081fc2a3814994e7ab4e4ca2f812052bd6f7c4b0286c5cd`  
		Last Modified: Wed, 24 Jun 2026 02:35:09 GMT  
		Size: 56.0 MB (56047273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6beec4254dd6d9d54bec111217bc6634d6c5d7b5ceaa6029ae996278552695`  
		Last Modified: Wed, 24 Jun 2026 03:18:33 GMT  
		Size: 200.2 MB (200244154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf3abc6879cb5b4fce9407a2be73ad4a5c28e06367e202d200969633756cf921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219021f541005c7c2e19227af3c2449da4b9d3576f5cd1cf82b50de2d27f2b55`

```dockerfile
```

-	Layers:
	-	`sha256:0f75fdb129a77288c88c3184ed5ce9f3820a3415921f4fb5699f2c53e162b0b3`  
		Last Modified: Wed, 24 Jun 2026 03:18:29 GMT  
		Size: 15.5 MB (15459600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b98a3c536810253e59f3bb3e89e8c43e25aea6ce1a5f93e5349b20400a8ba0`  
		Last Modified: Wed, 24 Jun 2026 03:18:28 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
