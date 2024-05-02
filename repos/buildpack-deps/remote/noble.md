## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:9f0ee57d23e685061dc449030e76ed9c72633c26bd4867c424cb8ecafa2beca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4f663c4643392e5195af8e569708fcc3c770bab0cdbe0ab8387a5df4f1272440
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53c764fa76f7c831ed6460fd62c5d2f2d952b08169f27d457b22b2e798360e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:07:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:10:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea5bac13515fdc1a8104c4b6ea8a3b1a95b23c5aca6d0d4c9678d4dbd51f787`  
		Last Modified: Thu, 02 May 2024 02:14:27 GMT  
		Size: 14.3 MB (14304582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b344ba15a0c144e3d4a9437b4151d3ffd6f5909cb07f246e840e7969545a8`  
		Last Modified: Thu, 02 May 2024 02:14:43 GMT  
		Size: 45.3 MB (45302143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb741e38dbe0ead13e584560b0a1f53de6ff52bb88eb9340740f1507b4c41e`  
		Last Modified: Thu, 02 May 2024 02:15:16 GMT  
		Size: 189.8 MB (189845924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77c6c0f3f77a5f66aede3520f063cb67fba6aaee9861ed58a106f286b7e21658
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239418192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55a2e73609832235742b4d10dc90119c431ee69f208a795708d89eb875fd7f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 17:03:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 17:03:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 17:03:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 17:03:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 17:03:38 GMT
ADD file:7b9ebeed2b8df3ae6b4ff0b90cb86423ff21019cca623cd8f5ffaeedebc50bef in / 
# Mon, 29 Apr 2024 17:03:38 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:03:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65b0f107a3b2a3765c847470cc1b37265cdb4ec78f1b5b17b6936546f15e2381`  
		Last Modified: Thu, 02 May 2024 02:12:18 GMT  
		Size: 27.0 MB (26956922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2009af8124e8bc3b99916b5796900bb049316889c95b2415fd0546099a15fbac`  
		Last Modified: Thu, 02 May 2024 02:12:17 GMT  
		Size: 13.3 MB (13326268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb16b7cf87a88247a81a97d34c7cd63d20e837352f087543a76695f6b699b531`  
		Last Modified: Thu, 02 May 2024 02:12:36 GMT  
		Size: 48.8 MB (48844639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872f2bea34cc929ad83fb7323b61b2897232ddc40bcb30f791a4c1a0ce4ae14c`  
		Last Modified: Thu, 02 May 2024 02:13:04 GMT  
		Size: 150.3 MB (150290363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9b109ccd1d3c83fb4418f721ec04c5c47e6e96afea7008aa44a81f45ae6afe10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270278149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f11c24268accc13db331490860e08aea044b831b35ce23ee3a1b9623930bf9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:25:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:30:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad3cd85790125fac89e6d0bad52d855bbc174d8152dffce3feb2aff28367973`  
		Last Modified: Thu, 02 May 2024 03:33:41 GMT  
		Size: 14.1 MB (14135675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c4a0ba36acd16ac34cf3b63622e2f16de3bac3e7babfbf4e5088a4948fd7e8`  
		Last Modified: Thu, 02 May 2024 03:33:54 GMT  
		Size: 45.3 MB (45261248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80fa78c16903501f446d2a6187a81222a84664d608f2718e6f29a68f7105fb4`  
		Last Modified: Thu, 02 May 2024 03:34:19 GMT  
		Size: 181.8 MB (181842556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e002b9f401fa2b7cb26fed4eed5638c7369145d2343a7be87299766380bb8874
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298493165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3431db431d3ba66773f622dfe434728a0a9399c3d93be697aa473657832af550`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:36:39 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:36:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:36:42 GMT
ADD file:c915ac180ad59faba89e9e3f73473adedd3ac5b7024bea2fe61b266b3efc1267 in / 
# Mon, 29 Apr 2024 16:36:42 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:29:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bcb8c42b2752babcd7ef1c98e380f22f0fe7f25521a416951d4cd54bb4cb300`  
		Last Modified: Thu, 02 May 2024 02:33:48 GMT  
		Size: 34.6 MB (34579045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311118f71d2a44d1b56b9473b56c32fdfc1087ec55036a3248875324836f0765`  
		Last Modified: Thu, 02 May 2024 02:33:40 GMT  
		Size: 16.9 MB (16871085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a14005ff03cc724a59a3a332b2bf29f2c02bcaba9aa43ac57f20a425e3ba6f`  
		Last Modified: Thu, 02 May 2024 02:34:05 GMT  
		Size: 50.5 MB (50514990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d0e6429813060b3c7bdfc1c7b32b46b417e0b8163a76c65f01809a33706887`  
		Last Modified: Thu, 02 May 2024 02:34:43 GMT  
		Size: 196.5 MB (196528045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d5de8ecde9fb182409202db6a976897e9762850c730a9c90f598e026db3fefb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261611373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee16dfb9d748fec9d94cc2c353b18d64edd19ff867c2f2de05d18a028465058`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:31:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68e0be12c8304c831d669224097b6db6b2c5123796652f8911f2245c0f955227`  
		Last Modified: Thu, 02 May 2024 01:35:40 GMT  
		Size: 29.8 MB (29782463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a326658ec81d60132e0e611daac8eae9a8b5a44e3daf1e55494e0fd34099b201`  
		Last Modified: Thu, 02 May 2024 01:35:38 GMT  
		Size: 15.7 MB (15722305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0689cef181cf02068879a4bbf1cd4b32359780c1c88816b5a66771d3a1e333`  
		Last Modified: Thu, 02 May 2024 01:35:55 GMT  
		Size: 46.9 MB (46945323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8bde3e487eced2f7695f0d6e9482b3aab8eed76c0c304c1d0261c10fc66527`  
		Last Modified: Thu, 02 May 2024 01:36:23 GMT  
		Size: 169.2 MB (169161282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
