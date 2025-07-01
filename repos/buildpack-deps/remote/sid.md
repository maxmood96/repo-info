## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:8f175611cb3281465dd8580d93d6b1bde91ed219ea614ae93f5984fcec75960c
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
$ docker pull buildpack-deps@sha256:c4164a88e5d9d0c29a9455813c35d6442e0be8884948a1c334e1b006156ca0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334764099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea577f8b0051e5868605c3778231bb4a5bfda5b8c733aca84e7e8fdec3229af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:603de70df79137e44ed9b8e9d2eec3a1b8eb889b8a8650df1a6bfc2ba9798f72`  
		Last Modified: Tue, 01 Jul 2025 01:14:45 GMT  
		Size: 49.3 MB (49267699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b752883ea09044589f48c52df49289712f416806e7b67e6d3b283e6c96ac266`  
		Last Modified: Tue, 01 Jul 2025 02:25:34 GMT  
		Size: 25.6 MB (25619155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14a16253ea0df4ebeb77b1db25ac37e73812925ccf4de831d1f7bc411f2c38`  
		Last Modified: Tue, 01 Jul 2025 04:11:59 GMT  
		Size: 68.2 MB (68209103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a7e6712aba6de069b3bb66c090c22b9c48d12c91f5125d308722d20000d452`  
		Last Modified: Tue, 01 Jul 2025 04:13:04 GMT  
		Size: 191.7 MB (191668142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:179fe3fee18d736ef5451ef970f7f83369690992bdd922c6543b9c4e266cc390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16325075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2415d21f10d0419f78786da88908449bec3477c20cf2aa40769e8fc78589e2bd`

```dockerfile
```

-	Layers:
	-	`sha256:69fad41b22438173645da091585cbc19b78c9005c587bd0612eb3ccd89413f5a`  
		Last Modified: Tue, 01 Jul 2025 07:20:53 GMT  
		Size: 16.3 MB (16314900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12da18078ce36f0258c7c011197fc80817829ae9ceff763d34cd032dab998388`  
		Last Modified: Tue, 01 Jul 2025 07:20:54 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7f1c8fa4d15ce5a71703cdb0924ede66bde31c60fb1c354bca651e0e3bb61030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299719569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e2b8b561df5a7771e37fc228d404544208d42aac4cfad0f8d0b811964c9385`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8344b2028cc05a08f8b0b577cc9430fd30421d98f7302a20cc79a7392635ca51`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 47.4 MB (47435203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8ec6927bc0cb7d56e990391b853ec23d7d3eb74a5f1f9500df8d5cf23ea4d`  
		Last Modified: Wed, 11 Jun 2025 03:13:46 GMT  
		Size: 24.3 MB (24328621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085f136199cc5a804201375aeae18b933264b5486014fd2d2c46cfb68e131fc`  
		Last Modified: Wed, 11 Jun 2025 12:21:44 GMT  
		Size: 65.6 MB (65640755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e204187b29a43e4ec106f4ad6c42a78478cdf09f7ab0ba5d8e27c8151c087e`  
		Last Modified: Fri, 13 Jun 2025 16:50:05 GMT  
		Size: 162.3 MB (162314990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b21303a657b816d65c5263c412f255a390099185975b10380173d9bf98c1f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16093223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d204d4905184e5ee7c1e755b4deb5111287485f061f8e7e1e4c9c3f111986323`

```dockerfile
```

-	Layers:
	-	`sha256:b675300656ddb88f39d9241e4f5c3747e64f5e8fa9c0b1d619fbdabc94eac2f8`  
		Last Modified: Wed, 11 Jun 2025 13:20:43 GMT  
		Size: 16.1 MB (16082987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5315cb718648785f3f1ad5894c2bcabbd95026f0f38c90becc8385e6a2739593`  
		Last Modified: Wed, 11 Jun 2025 13:20:45 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8b8fd75c6ddb76e7b6881b9c175217bc3a5ce876a69d29e9baa9d16e333dfdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282940363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c319a7e8cf2224dd89f312ee6607fcd89ac713d094d8409954c4d63d15fea165`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ceacdda8a07413d9c26c141b0f4894fae020e6ab65ff0188cce0bfe5e0c66eb`  
		Last Modified: Wed, 11 Jun 2025 01:10:03 GMT  
		Size: 45.7 MB (45707825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b841f0ab46f7d7bc86d75d499d470af27c2315d80feaa41746c1f9e6d995ef`  
		Last Modified: Fri, 13 Jun 2025 17:03:18 GMT  
		Size: 23.6 MB (23601456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b703c4341425792b641192b1633584b31d3164c5bde6219fcbd37175e45bb2`  
		Last Modified: Wed, 11 Jun 2025 13:14:31 GMT  
		Size: 63.0 MB (63015556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85b69e87c980f17dd8f84b28e8ed63351b861562111262841aadfece81db21`  
		Last Modified: Fri, 13 Jun 2025 17:00:32 GMT  
		Size: 150.6 MB (150615526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b991eace02c5615fdcc2952969649857e81e11b254db148210b239655e3033d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16089514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71f877033c49e07c0bb438fd522ecbf82836fdca41306e8d94daea3773c998`

```dockerfile
```

-	Layers:
	-	`sha256:e22d8be388602630f8bf1e2c168126766d2da5e743944f08176826043604b2a6`  
		Last Modified: Wed, 11 Jun 2025 19:20:49 GMT  
		Size: 16.1 MB (16079278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9175abc5f34b57c60dee48d2014d51039d08acacf328f3aeb52ccc42d6f59af`  
		Last Modified: Wed, 11 Jun 2025 19:20:50 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:36cd5d886223ad0244c348bdfb7fb39b3903261824a40c868a0655499f756e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324443256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e059b179e8903cd6d253c5b824cb9f3470ae69199397a38c9c6b347ef84ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b10e85b1b46df396d3cb4118de7b2483607b89bcd163318c9756c711f9a3ef9`  
		Last Modified: Wed, 11 Jun 2025 00:37:10 GMT  
		Size: 49.6 MB (49629348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae44e59140036c47291ca98d6f5cbe09bbc2c6ff2f7067e6ed8f93f2a9ed0b71`  
		Last Modified: Wed, 11 Jun 2025 08:13:09 GMT  
		Size: 25.0 MB (24998868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1842d0d17df930326b268986cae23d9f266eff7b38d9a7a69d040cf74bd3fa`  
		Last Modified: Wed, 11 Jun 2025 15:10:50 GMT  
		Size: 67.9 MB (67901215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ae760546480e2453321a26fc6dcd7c752fa657059171a38f48610465648727`  
		Last Modified: Thu, 12 Jun 2025 04:48:58 GMT  
		Size: 181.9 MB (181913825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b09284e54963b7549251fad2e9ee20afc2fe3636bec66f924f607104d194105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16406082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5900153655dc6bba17d6c667f0688789256c46642a4ebe02170621e40c1c144`

```dockerfile
```

-	Layers:
	-	`sha256:d314350ae1e0c9f056d82c8c7de3429deb936164a01bdc3ad30a225e3b11f091`  
		Last Modified: Wed, 11 Jun 2025 19:21:02 GMT  
		Size: 16.4 MB (16395826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59835d3f84b9f5d5710097a36114bdd56d15d34a5abaf46379e13ad065b4059f`  
		Last Modified: Wed, 11 Jun 2025 19:21:04 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4fc103f996e35de2cd316f75bcadbe42304eebf2596bb401aaf65f3631d12fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343056822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc34ec94a13f524654d76addf8be866b252892eb47e36311b5d8a6e811ffa2e9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41ea081e29dc4034ec31a49ac48ddbf738b840fd4d226f5678cb63f00b10ab33`  
		Last Modified: Tue, 01 Jul 2025 01:15:01 GMT  
		Size: 50.8 MB (50790707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d224078a83c5498b9115edbeec34eecaddc04a9e2e47f0e71d34a7e780a2059`  
		Last Modified: Tue, 01 Jul 2025 02:24:36 GMT  
		Size: 26.8 MB (26773974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6014d1af113edbca3a63a8a8aff65bf03bbb831dcab023e346303a638c1250`  
		Last Modified: Tue, 01 Jul 2025 03:19:59 GMT  
		Size: 70.3 MB (70286001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3b4b6aef8ffc726b6e5209bdf37883d83d71e08f64c1f66f265682fb1d8c35`  
		Last Modified: Tue, 01 Jul 2025 04:13:16 GMT  
		Size: 195.2 MB (195206140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8ea4ded8436acf53fef42176583fa4f6f170d064452512baf566721e06c02ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16294914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55f9eaefa62c700b72769806dae70408791a9342eb47681e5f0ea8b9c6c1f22`

```dockerfile
```

-	Layers:
	-	`sha256:3920cbaa88391d7c35b068c7acd34712cab409cd37404f397cc39e021fbeb313`  
		Last Modified: Tue, 01 Jul 2025 07:21:43 GMT  
		Size: 16.3 MB (16284760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c958c7f547e5d5876de665c59af41c37ae2d1e9c6d9ae6a10bbc04b3d1bcb296`  
		Last Modified: Tue, 01 Jul 2025 07:21:44 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6d01c567bb16df88fc5122452179444291b271126f62189fe965656a8fab5df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313950586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5051cb5a5ab58f4824e0e420e7742cc16d4b0b7b1dda316d083c6c3bbddcc6a8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54a8735d26fa76df64dcf3824b7f78b58d44ea01ab0788f2fc33afa2bac4f1ad`  
		Last Modified: Tue, 10 Jun 2025 22:48:52 GMT  
		Size: 49.6 MB (49553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ee97fbcbae75cf1777c40791b1a1c25100c4b6ad8a9ed9323cceb66a38ba5`  
		Last Modified: Wed, 11 Jun 2025 13:02:36 GMT  
		Size: 25.7 MB (25652069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd97199828602994822322c66b6b3a65083d16ea25127f0a48c6b159108cd4`  
		Last Modified: Wed, 11 Jun 2025 22:23:25 GMT  
		Size: 67.1 MB (67072610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0870155614264814890e54a8cb3796604707e92918a524a16a2b3c9198cb976`  
		Last Modified: Thu, 12 Jun 2025 07:23:03 GMT  
		Size: 171.7 MB (171672652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2e3c6d5a41f6932884d552b0b2f81bff40b48067a29dc3826c62586dacbf0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea1e26f971bdb9d3f4431086fec8f49096400a1122d71cac27a778dfcd22adc`

```dockerfile
```

-	Layers:
	-	`sha256:0ef860f332fba2152991b0c2090ca64df71eb5f14b7a7c7ed19934d3178e97f9`  
		Last Modified: Thu, 12 Jun 2025 07:21:03 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:405ebfacc917de4974d7f2bee2168e041b4f7738724e757daa105d13b7a63102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338824891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f63b539aa4e5f6616c7ae054c091bfac68d5af5e9a0073797b8f60e35fb0d02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f34e3f5941a9b9d7f66cc62bea1f477c727df8c87b640bd63d443c8cb4c08203`  
		Last Modified: Wed, 11 Jun 2025 00:27:42 GMT  
		Size: 53.1 MB (53098680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f227a2066e39def58b490c6183c1c743b3db44ed881ae2f1d7f6c8febfbc6b1`  
		Last Modified: Wed, 11 Jun 2025 17:42:13 GMT  
		Size: 27.0 MB (26983625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fa176b0ee9b3a9a511ef65649d379d0d0d4e1a342fc2d3e54b6d5e65171edc`  
		Last Modified: Wed, 11 Jun 2025 19:14:57 GMT  
		Size: 73.3 MB (73341809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f7364d6157bebbce38c131919d7b9d1b2f458adde75b9ad55512c9af3ba4d9`  
		Last Modified: Fri, 13 Jun 2025 16:40:54 GMT  
		Size: 185.4 MB (185400777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70980a08aa1394c1ebbcdf93aa5f8310c84228c38bdd4efd50775d0927a74201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16315853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24c36116feb0b1ca72b8ee5d5f675a01addb6a76f91bfd759bc2288eaabdac7`

```dockerfile
```

-	Layers:
	-	`sha256:aac84d0e21e0f647666340ab9ca753cd12e18258cb16630550fec6fa535d0b4b`  
		Last Modified: Wed, 11 Jun 2025 22:21:00 GMT  
		Size: 16.3 MB (16305646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefb0ce04c7ad2cbabaddb8c380d197d24ec3474c557b623aae2c824600309de`  
		Last Modified: Wed, 11 Jun 2025 22:21:01 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:29cd3278281f582ad5cd57b939d1284ad99df3eebae2c7fbabed6de117c7722f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.8 MB (408765791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bfeaee9d71d7bc1888562d29e9a9a29bfee53216b4996013e45c07038e848`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:42f7c08d656e09c01f14d35a847143f84e881d1ac3f16f3ba511348bbbaa7d82`  
		Last Modified: Tue, 01 Jul 2025 03:27:03 GMT  
		Size: 47.8 MB (47756066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4ef3bea202b6f661456b37f5106a6a6e0acda6439394bd6618c6150a35c24`  
		Last Modified: Tue, 01 Jul 2025 02:22:42 GMT  
		Size: 25.0 MB (24954336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f59f94fee11898b889be78db1b26357b77690be8753df91b533098e18b75eb`  
		Last Modified: Tue, 01 Jul 2025 03:58:27 GMT  
		Size: 67.1 MB (67092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5105cd5e447d85c1f29b081d53f831277bf3fc355a0e4055af207a99f0da902c`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 269.0 MB (268963197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b1d1a3cc531f6c108f69dfa48143d509611ec16681a646d1ec09711bfb253bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16380929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db7e11bd3c98961708bd002af9351c178ac22039c3d2c0bd71a41d65f0dd571`

```dockerfile
```

-	Layers:
	-	`sha256:3810125539ce82c0d26a080afe93db147515d71940cf1be0198ec978a2a2e08a`  
		Last Modified: Tue, 01 Jul 2025 07:22:11 GMT  
		Size: 16.4 MB (16370721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4529d741b7463f6429cd17e4d2f240111d3a5dcfb5ee905cb362c1329b230eb`  
		Last Modified: Tue, 01 Jul 2025 07:22:12 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d57c7ad545bc0c38ab2758c2c2a06f75a1e06b4a728a32366c81218428670ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306499661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8026cba8778485ddeea5c4b6f063f257ccefd75c9b722f137f829ea2e8a2aa3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a52b4c8ce9959e1107790b0cf878188904eecb5b1ccf411d93d6ab16036dc160`  
		Last Modified: Wed, 11 Jun 2025 02:03:33 GMT  
		Size: 49.3 MB (49343092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0965e23eb9d70e72f15582a2cb686bcf1857eb924b4d704542fc37d206146`  
		Last Modified: Wed, 11 Jun 2025 02:51:24 GMT  
		Size: 26.8 MB (26769281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc44cd2b9aa97b3fbb56995ed62a657167162e1278b818c7bc6bd60f13d1e12`  
		Last Modified: Fri, 13 Jun 2025 17:13:35 GMT  
		Size: 68.7 MB (68689048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a662117a21d6756827011b9a9ab400fa9db860df9a5da8d3d1a1a8597172c7`  
		Last Modified: Fri, 13 Jun 2025 16:51:50 GMT  
		Size: 161.7 MB (161698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98a10f6e1cacddf487ba9d6cc84e03a9aa69ff01ad2c3ae1f7e6689ac2f67da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16088768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38867d0847e9aa3cc7858d65dbb7277cecac6ea10846276e2eeea3f0070a6a87`

```dockerfile
```

-	Layers:
	-	`sha256:6c5a5481488bbe4a9be4f7f0a03b2001cca8feeeb6e48826bf380c6b6bcc2649`  
		Last Modified: Wed, 11 Jun 2025 13:22:04 GMT  
		Size: 16.1 MB (16078592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922e6e6f9518f191e7921c07bad9fcfd114eb50637eb14e095a971de69370ca0`  
		Last Modified: Wed, 11 Jun 2025 13:22:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
