## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:06c4b5532064752a74c385f80e94dbab84043607ea73c158c56e16f543f89dd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4855f0d999f6de65077dca105ffde39748a3d1f570b42bbf84e6767563bfc54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249473048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cefe47586b35e03c26c8486718fe32e06a44574936b92b300ba295059b49cb0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:26:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e4958bba254d5b20b93d40bc57b4d2e5d5db9d885840d5f7405d3da91fb59`  
		Last Modified: Wed, 15 Apr 2026 21:27:09 GMT  
		Size: 39.5 MB (39487893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f1f5c0cd77b5a3fb7e80dcfcf4a7aad992e30ca95d28ce6221d930a68ebc5`  
		Last Modified: Wed, 15 Apr 2026 22:13:37 GMT  
		Size: 173.1 MB (173142267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:80d4204730ec4eac2a10a7cc1d7bfe8d6438c689cc33b4c194a7b6f9e21a6f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11850542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559f9692c93b6b7c407d8150b81679db82d94b6ddd4145debe021b4c0e33032`

```dockerfile
```

-	Layers:
	-	`sha256:b48a6490589ceb7f8d8bd21947462fa8290be6169820b41aa2def05dfb65c588`  
		Last Modified: Wed, 15 Apr 2026 22:13:34 GMT  
		Size: 11.8 MB (11840382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b380547d340a742db038b77f1503fd285526027d8ad3ffb0690e92137223dcf0`  
		Last Modified: Wed, 15 Apr 2026 22:13:33 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:225fa43b6539c36529ecd2a8c43d6a3ed66bd8677d64fb82e02847ab877cd5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216729350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef7ada333d9246e1be73dda93c854f1cf6a17f48fe324f222b3fbe955918e19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:44:44 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:44:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:44:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:44:47 GMT
ADD file:cf79b3b81bc9aa60d93ec4cfb803894aca6ed3d1e7c9ed02435158c6c0de400b in / 
# Fri, 10 Apr 2026 09:44:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:32:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:49:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c61368409f262f2b51173bb83056489f63f356da65ec1d7227c4451afc7ff0`  
		Last Modified: Fri, 10 Apr 2026 11:01:03 GMT  
		Size: 26.8 MB (26841687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ea175a59e4f7f510d8b43574403d0483cfe07a859f9c54ff97760dc3b0b09e`  
		Last Modified: Wed, 15 Apr 2026 20:31:20 GMT  
		Size: 7.0 MB (7010549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03bc9e8dd1d1fa48ff01cdf2bcc6457fb722e8d6ec9fc5d5681fe7bb742fba`  
		Last Modified: Wed, 15 Apr 2026 21:32:27 GMT  
		Size: 42.3 MB (42269424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d465447be136f472c6395a3d4e78c5ac12db016d2062808703aa67d708bb5ef7`  
		Last Modified: Wed, 15 Apr 2026 21:49:31 GMT  
		Size: 140.6 MB (140607690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:31aa635adfdce0ba3fa51b77aaf6915cec729f7445315f05daf581a345689842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11639815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc4838d06795ab25c2d380bdd1630d0d35d792d94423db7ef5322cb4cdf4c83`

```dockerfile
```

-	Layers:
	-	`sha256:38ec4de41a1a51a83acb8132b17b3647092e620e351b945df5f7adbd27bea31b`  
		Last Modified: Wed, 15 Apr 2026 21:49:28 GMT  
		Size: 11.6 MB (11629591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef484a10510934348b0d771807846a04b185bc950a798500a8c19aa38ebecb6f`  
		Last Modified: Wed, 15 Apr 2026 21:49:27 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b59eb88c13803fa55a2e8a593cad96ce2ccb99a898e0fe74e72a229b3051428e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240794814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca3922b2ba2fad71924838a7eb2bc8c3fdfef338d9eb61f40b6ebf043b69e52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:40:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:25:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbcb8f28dc46ee2582e5ed090a59d48662855ba06861fbb05e006c6efc2f612`  
		Last Modified: Wed, 15 Apr 2026 21:40:17 GMT  
		Size: 39.4 MB (39411137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08e75f88afadcdf28969da8041071c3a233a8e749485711afb9d26ece170bd`  
		Last Modified: Wed, 15 Apr 2026 22:25:42 GMT  
		Size: 166.7 MB (166716007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e8b7b476b21a8e5719407ed9168f918f929b746e2c1d44c506fe083e5fc10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11846289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924af5f9eb30d52747e8d9632d1039b5084355d75403011d0a1b0db6be3c11f7`

```dockerfile
```

-	Layers:
	-	`sha256:e0a34ef6cd999cf04f0e53ad140dee616a63aa439a251dcab43eff5a48c4203c`  
		Last Modified: Wed, 15 Apr 2026 22:25:38 GMT  
		Size: 11.8 MB (11836049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b2d2988c18d67570795c1a343c6953814589bc8428ef57ef067de2a125fb37`  
		Last Modified: Wed, 15 Apr 2026 22:25:37 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6d5d4de8bd3edce980d77fa98d2bf36cbbbf3a350d63685ab15feb35c3ac4c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270200295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3978175045dbbeea665bf6481da8ba41168adf8e92b6f0b10ed75b18dc7ec15a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 00:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 03:43:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934dcd0d71e03d90a927f281153e6d3ea266863de69f95adc0ac8dc3ddc9e4e`  
		Last Modified: Wed, 15 Apr 2026 21:11:30 GMT  
		Size: 8.2 MB (8186214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d1ad4a4ff321f644d76bbef785a0d592a87d54674d9faa63d42df9d16e983`  
		Last Modified: Thu, 16 Apr 2026 00:11:00 GMT  
		Size: 43.8 MB (43776297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7122709282e898cf070d5b2d0995264981308f9a2ca69dd2377087fb78a984`  
		Last Modified: Thu, 16 Apr 2026 03:44:48 GMT  
		Size: 183.6 MB (183589386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7714d22915ec2cc8cd8a4695a0bdf400b63b794ece0c8a99ce1f57d373b94799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b0efee7b58f2938c573db10f66b0a150e7cf35030a900810af8f070227d0b1`

```dockerfile
```

-	Layers:
	-	`sha256:0e076d0264f915f01f0a55998a7cf76ab0874e4107b69650dcf7393159e296f4`  
		Last Modified: Thu, 16 Apr 2026 03:44:44 GMT  
		Size: 11.8 MB (11799747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac80dab467aceb900c375b451a915f5ad60abc8b3c6900a12eea7a30842b0e8`  
		Last Modified: Thu, 16 Apr 2026 03:44:43 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3107648809ce059d133fb9eed37def4ddcade13fa274b001905c5e060acffaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274710141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a66893a5c07ceb31d799fc2932e1ff357754de090cf34cce1b5e27b32b34bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 10:46:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 10:46:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 10:46:31 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 10:47:09 GMT
ADD file:7ae2692e9ead2e53576d53cdb893209a70fe6f0a62ff35308c9fe5c855c10e94 in / 
# Fri, 10 Apr 2026 10:47:13 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Apr 2026 15:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 19 Apr 2026 03:49:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:116177a8ef78c1de97a5262550388dc00d9881fcb4c367e06e4e52bbdb5a832b`  
		Last Modified: Fri, 10 Apr 2026 11:01:22 GMT  
		Size: 27.2 MB (27240349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ddabbfbd66006e6d36799950a3c7e93532654f0837cde6fe2521d8c52ee83`  
		Last Modified: Thu, 16 Apr 2026 16:41:28 GMT  
		Size: 7.1 MB (7118338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144adc2ee8321b5f81e7424187eca2a7ced16978dd9f89b2dca14b113fd47f46`  
		Last Modified: Fri, 17 Apr 2026 15:20:34 GMT  
		Size: 42.3 MB (42308226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb8ffd50f5e32d66c7eb25fbcee5b0b4d32e9fd0b83deb18009e7ad0ed6316f`  
		Last Modified: Sun, 19 Apr 2026 03:59:07 GMT  
		Size: 198.0 MB (198043228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a69499834e137e50f036a1d5af5c16748ef60c7d830bfcdb55bd1aa6afd303b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75eece980e99475735d226344409d5a18400141d956a97dc6ab8583ed20a43`

```dockerfile
```

-	Layers:
	-	`sha256:ca8b15ade417809c42f14cacdee7e7ea2a5ee574fb71d4c18ad931e390bf7c47`  
		Last Modified: Sun, 19 Apr 2026 03:58:40 GMT  
		Size: 11.8 MB (11780731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed146cd514c446c70cfd6cbffcacff8ab42eb1ab426888838346146e7ce3464`  
		Last Modified: Sun, 19 Apr 2026 03:58:36 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2441610aa53ec29044a50752e89c1ed4ebae99fdb8f34e1a685ac2d5d5214e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223440803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e052dfebc7c11170dc59805e479e979c9d779bb6f5bb16f3ef0c7201d355ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 00:57:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb2def34f87e70db8ee4787df628a5479c6cdb42d140cd23cb1cfc202317d9`  
		Last Modified: Wed, 15 Apr 2026 20:43:23 GMT  
		Size: 7.0 MB (7019135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f2f17fa2aa4d3f3d7ffad88a6e820e36144fc3f9f9de46504012f45065a9d8`  
		Last Modified: Wed, 15 Apr 2026 23:51:03 GMT  
		Size: 39.4 MB (39414408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2203621968957d7231c9c1616df61125de04a6ec534060338e0942425ef946a`  
		Last Modified: Thu, 16 Apr 2026 00:58:26 GMT  
		Size: 148.8 MB (148804961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:121a7b9207a6b7263131ac8d0f78c8ff0bace98dcdc243b8edc0f076d75e59fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11664419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16813f51ae1bfdec918c10c4fa9c0e3f1fc81753ffa5498f619b9e42f25162f6`

```dockerfile
```

-	Layers:
	-	`sha256:b313609cf60a28748b98e8c24c2f6bf483d388d1e2ddbd18161d435a4db5466f`  
		Last Modified: Thu, 16 Apr 2026 00:58:22 GMT  
		Size: 11.7 MB (11654259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7af98b61152f41cc689b4c50ce761fe1b274576879eb86a4b83a7df0b8e5c3e`  
		Last Modified: Thu, 16 Apr 2026 00:58:22 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
