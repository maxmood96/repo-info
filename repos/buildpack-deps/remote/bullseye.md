## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:439e7bd96239a6a8005675f5c8c483b28edb729a5d826c3eb80c7843d4d7452c
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

### `buildpack-deps:bullseye` - linux; amd64

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

### `buildpack-deps:bullseye` - unknown; unknown

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

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:79f5cf9987753894efbed0260efdd3f0066d1c19f3826727485d09d51137ffcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282401087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890635f4f4af426696fb9bac28f947c27ba74317ab360a61d24b7fd60f409930`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:20:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:057662c04791d47966179d44811cec5af4565f7f7a6a4690c7d8e834d0ba3bd2`  
		Last Modified: Wed, 10 Jun 2026 23:40:48 GMT  
		Size: 49.1 MB (49064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa240a68c3059c2e50ee1949050052855111d59f6865103a70421028ec0d924`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 14.9 MB (14905396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c8d826bdbb6b8ffba198124f6ff94c9cf241cbd4761c9ad97d0feb1a0f3333`  
		Last Modified: Thu, 11 Jun 2026 02:43:52 GMT  
		Size: 50.7 MB (50658997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703cd3e4780ac097023e574c5d70d53caf447530af3ef5f584975e25bc356179`  
		Last Modified: Thu, 11 Jun 2026 03:21:15 GMT  
		Size: 167.8 MB (167772690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4a39582683de18263125e88d8a04b27372698af2d321c82216820b8185771f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e436029e3adc5cc69bf67caa26890a62cd3c7d461326f5c62c2c0188b3a7b33`

```dockerfile
```

-	Layers:
	-	`sha256:501167339afb87a31f688ec78cdb1dc2e162cb3c3deef799e8ff44a4a0b7cfaa`  
		Last Modified: Thu, 11 Jun 2026 03:21:12 GMT  
		Size: 15.3 MB (15270903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ed66c3083d0ead2b56d3a8caac2600859467c0b6c70b7b8d251941d034457b`  
		Last Modified: Thu, 11 Jun 2026 03:21:11 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

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

### `buildpack-deps:bullseye` - unknown; unknown

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

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:658a35046770cdb498fb61461129eaa41b7897d9ef3d6758bb7525c5870057b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327282305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e22f56456355f148c9510bcc5f56e89d90fe073015c5171254f8b874da8f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7baf1917f31dc6264a068963cb19f53c4fc1fb3df24b85fb7b1a7235134b9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 16.3 MB (16295657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c66634bc3fa0a0bcd10bde2aef17a8a2d29d8cc303406e191342fab9599745`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 56.0 MB (56047555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680b9a9afe383985f9ac5e211b845598224d8c23f97d9980d6e264b6f15c0345`  
		Last Modified: Thu, 11 Jun 2026 03:17:05 GMT  
		Size: 200.2 MB (200226236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7183299fd5008aa0f969854fd6736b66641116bb4fb8036da68feee6d03821c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f136eb8a9af2872217a33c0ef3bca9b227eb914349497d577faee907a1e7471e`

```dockerfile
```

-	Layers:
	-	`sha256:7dd50882a087f0c99ab8bc00fd2b2bc9a924ade68173cfcb2fd2e9b31f358be3`  
		Last Modified: Thu, 11 Jun 2026 03:17:00 GMT  
		Size: 15.5 MB (15459600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e273d6f97d543790875da38cfdf30e0c94d46433d9f0c57662b18fe2a8d9264`  
		Last Modified: Thu, 11 Jun 2026 03:17:00 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
