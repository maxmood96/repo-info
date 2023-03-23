<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:2429604df643c021ff2cab3dac991a0fa74772bf0b83861bd2ecd784fe0da05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:ada092c3a0c585f13d5f793e7205070600af63e45981298386e2dababa1d738a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97eecada419163ee3c517ac6705ef6e5dfa59771e40d23b94dfc828b9d1d62c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2a4b5dc9653f9c297b655b999a18dc419aa1de140d5f0922e669d63ba8f81e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d4d01492647633a3360a913f3e312b6b59ea3c99348fb6c59efd5147552260`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:088603ff4edc4022b00300092617e96a8049eeb012b4171c88cb69e1deaed5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9e8ffa5a31ecac0fc53ac08f758b6f3acd6aa33812e5f0d0527472b9b881dfa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bb7a8f0e8135403e8e485b1e329938addf81ddadf3098c440a8e59666b9b66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da88f82f719637c6eaba4b8175eda88b088da7adfc3952ff2732a42ed676775e`  
		Last Modified: Thu, 16 Mar 2023 05:58:04 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f9f953e47a67b48292e1ce793d31c3c7189d274b938ad5449b46e116d25a8a6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072b8fb76cb79a0ce80d413e95024a3f0fc969a9404af11cc642f6fc269db7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505f3caedc8772916ffde5305b38400b1745044ad55838322de25760fb04dc4a`  
		Last Modified: Thu, 16 Mar 2023 02:42:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:22dea449602d8560942c7b84d9e3bd0813eb0acc4a17fd39ef115e38023819be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:aaf4ace714149fbbd4aa37702ef9a418e815693769d5d6948d9680a098d95065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea11c1f6a6a05aaedd47a751c5820a89bd89707b688187f4ba1a74e6f4642f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:29:51 GMT
ADD file:98917c081507795b8ce084d09f5df75e959c5365882d73ca7a52da226c93fdcf in / 
# Thu, 23 Mar 2023 01:29:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15c60aea1a8c926f00ec7713f9ae1fcd349591095bddcc01ee5a6027b8a3998`  
		Last Modified: Thu, 23 Mar 2023 01:33:26 GMT  
		Size: 49.3 MB (49278011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9208dbea1384f0435290a314a68b9e6ad71ba2b9dbc0e8e2e4852875066ddf`  
		Last Modified: Thu, 23 Mar 2023 15:58:27 GMT  
		Size: 11.7 MB (11700942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a15d3deea27d74ff209b653b645539f94afc9c3199da23c2809f8d280b1b3f`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e406df43edaf35d7a6bc4cea702f54397cf137a9d3fc0019407820d04ef31`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a7fbeae0fd84e72219aeeee22cdbe3cb20cc7a557f566b2f22aaf19d9b50e`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 281.8 KB (281820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0ce04cb955ac097770a113bfbf6a31a982f9b257a46d81310f207bbd3e5a1817
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61274170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a17a3b7a5e2f272625f4110217f17c95e107be31ca369b7f03707d564374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a5450317480d94cb3403d7cde2e56b05a48f2729e28a94049e38b55e2c549`  
		Last Modified: Thu, 23 Mar 2023 09:32:07 GMT  
		Size: 11.7 MB (11661617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedde67f6e600aa9b9a11df48f5d1062eb19dddf30cc6e3692edcaf48930293`  
		Last Modified: Thu, 23 Mar 2023 09:32:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0b4d2410468a43678d43b81648e033fa5a8ddf3a801c9d297f60d0a31d8f2`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd75676c2211f19e7b64fb9984b6e1bf632dcd2caea07507d60c7effb2eb465c`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 282.3 KB (282259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e5113fd09171ab576c1d16b344acf0e917e04d98112db25425b0d5728ea300e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557d46a191412276903630954b271d01ce46d04c01a44e474ff3e6e2c21a8419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:863174a23d498b858cb76312989a2a59b8824c5675a61db6d927694fdaac8985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0237ee6a22e7705b99f1bbed529f9a219ea3fbe5eff0bae93e7fdd431523e6a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61263207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b0d2074eceb83419b21ce55ebd3311ee6c49a01e4bde2965538596e1f2605b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:29:51 GMT
ADD file:98917c081507795b8ce084d09f5df75e959c5365882d73ca7a52da226c93fdcf in / 
# Thu, 23 Mar 2023 01:29:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c15c60aea1a8c926f00ec7713f9ae1fcd349591095bddcc01ee5a6027b8a3998`  
		Last Modified: Thu, 23 Mar 2023 01:33:26 GMT  
		Size: 49.3 MB (49278011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9208dbea1384f0435290a314a68b9e6ad71ba2b9dbc0e8e2e4852875066ddf`  
		Last Modified: Thu, 23 Mar 2023 15:58:27 GMT  
		Size: 11.7 MB (11700942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a15d3deea27d74ff209b653b645539f94afc9c3199da23c2809f8d280b1b3f`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e406df43edaf35d7a6bc4cea702f54397cf137a9d3fc0019407820d04ef31`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a7fbeae0fd84e72219aeeee22cdbe3cb20cc7a557f566b2f22aaf19d9b50e`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 281.8 KB (281820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941509578d336ae727d7fe0d4c3761b4a2a7a1ce6df64c7b1fb2e3f4616beacc`  
		Last Modified: Thu, 23 Mar 2023 15:58:35 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a2c5e1cfb2814edb23bd6065569664d16e86693f6f514e76dbc163682bbfc6fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61274598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6da4b4fdf067a7776172d7f1f60446aa9567a46f13b4c63b53325eba4a8489`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a5450317480d94cb3403d7cde2e56b05a48f2729e28a94049e38b55e2c549`  
		Last Modified: Thu, 23 Mar 2023 09:32:07 GMT  
		Size: 11.7 MB (11661617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedde67f6e600aa9b9a11df48f5d1062eb19dddf30cc6e3692edcaf48930293`  
		Last Modified: Thu, 23 Mar 2023 09:32:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0b4d2410468a43678d43b81648e033fa5a8ddf3a801c9d297f60d0a31d8f2`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd75676c2211f19e7b64fb9984b6e1bf632dcd2caea07507d60c7effb2eb465c`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 282.3 KB (282259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c013b8973b114670d57c5a9a234343c9cd9199af17a900bf60083c001ee0d0`  
		Last Modified: Thu, 23 Mar 2023 09:32:14 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f5fb222c99bb60ec1873ec12109f2100cc2f7c0c0c4c49ebb862931a40cdd778
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09e3e4c39734921aa13a5fdf12088049ecffc7f768a939e9d66a1f34b502ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81dfd8e9fbdde88d17ac8708e298dfcd7fdad09eda77db2790d4525ee1b50c3`  
		Last Modified: Wed, 01 Mar 2023 14:04:58 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:00f4eabfcf6450382882359397323f5ce0ee1fb0cb6bb978eb328b6c33cd210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:731d9416c74576d5a00e1e625dfb2f62359eb4424e53824e1c0c3587875911da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5671c8387d65e53e56174bc8c57a79128a786b69655ff42f370ba344b7311ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92868460c6fd1adf5b17efda71fe04f9a3f942b0d2207e5e896d945691c34f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65329803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b09d7a97a033bde4a7708e836cf6e5e08c5f34d0e8bb9491dce8a4f1d87b51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:23ceabfead07bc794a3b911ec139f354023a29726b2104d031763c0e4ef80842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ffaf0534f22237b26e31bebacbe1ebc34cd0de0dfebcdc0c8e8b326335f5052f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa0c96870ed0a018d382afba1c0ba37f6c631858137d15d7140e96bc6231760`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563217d06ceffa980bd11353e01edde1aaa6630b9ec105205bb408b3413223e0`  
		Last Modified: Thu, 23 Mar 2023 15:58:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:295ddab89857cef0356935333a55df2ba7b26c6b53d402b293ff3f5c27e953d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f273b679fbf05cd298c531d890064262b449d3d7ac94283da3408f650ac4bfc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b84876434546224a0b3486b5afd43e5f2e02d867d6595aa8aea5dab4980ff`  
		Last Modified: Thu, 23 Mar 2023 09:31:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:60f0cbf3c9adcc42cffaa350f90a04cc21e30f190344386b844341df97c990b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:c4d51165f1892b56219b96998bc1020132f45310d639ec24d1eff26cc960f4e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a173c6a4606354e919d95d1c34b15c70261a567994dc7ca2f8d6231a6e5f84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b178d3e9f240e77488752e765509042c03f2bc17a3eab0e5f5a62b7b67c966`  
		Last Modified: Thu, 23 Mar 2023 15:57:49 GMT  
		Size: 10.5 MB (10504479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f9a76e2eac0f9a3dc42a01f95d1c280aa08207634cb8df83dd30a27f97959`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d9d3002cfeef01f97b0d184b0e841bfdf021850df4b0f6a88c2861c3bab41`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19bb407c9c70c6a8f88ceebbd19e3dde631a527d767bd8d13445707f3ab191f`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 304.3 KB (304269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b32bcd4cafaf47cf6c24e67da7b40242813e58d933b86dc54759c6084f759505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5526c79bfe19500886e549b52f3ec14113f2dd8a20a0dc87f2f627d67413642`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23969bd0deb154819623454501293274ed5d84a2980ddfab4a06aa292e2a8c2`  
		Last Modified: Thu, 23 Mar 2023 09:31:32 GMT  
		Size: 10.5 MB (10510313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbd5727c34bbfbac27263abe66d340203b862be36b5956a8a7a1be2e808287f`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9105f78f42f3a9a4b9f358a6913d438e595c68c00a3ca058316341700981f2`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e54dd992daca6739d936bec0393525b37f84ce18f86441110e7748352193d7`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 304.3 KB (304287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:96124b0d939cd9453d1f5bd48eaf28f9604b813af5f93a0ee05a6e5e9843f7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513b02edc7b5e1bfa4491c5259504ada968aaf72d7088609818f6f63a6d4e73c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:d5c8df09d1a6dd4914125eb9673a1f36809dd1aa4e6604538420c4890c57ed6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:90af1451f53e1c6742109e4d54dbad70fc89cdb8adb6ef0abdc245c335bb66ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0a64f9a25c419b96996656c710c481d3a87486d7fa0118a379379009f8e88f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b178d3e9f240e77488752e765509042c03f2bc17a3eab0e5f5a62b7b67c966`  
		Last Modified: Thu, 23 Mar 2023 15:57:49 GMT  
		Size: 10.5 MB (10504479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f9a76e2eac0f9a3dc42a01f95d1c280aa08207634cb8df83dd30a27f97959`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d9d3002cfeef01f97b0d184b0e841bfdf021850df4b0f6a88c2861c3bab41`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19bb407c9c70c6a8f88ceebbd19e3dde631a527d767bd8d13445707f3ab191f`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 304.3 KB (304269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e1b98b76491914cf926697dac13d6b087f7d6d5abac8dc4e43f32f2361f611`  
		Last Modified: Thu, 23 Mar 2023 15:57:57 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:707b6b7ee753feff9c0e77fd533fbed40ad0de825780d2e8b0882c058f587dcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b48cfaa3525f6d38ee12012c95842484629f74e01fb847be0310142622e9698`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23969bd0deb154819623454501293274ed5d84a2980ddfab4a06aa292e2a8c2`  
		Last Modified: Thu, 23 Mar 2023 09:31:32 GMT  
		Size: 10.5 MB (10510313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbd5727c34bbfbac27263abe66d340203b862be36b5956a8a7a1be2e808287f`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9105f78f42f3a9a4b9f358a6913d438e595c68c00a3ca058316341700981f2`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e54dd992daca6739d936bec0393525b37f84ce18f86441110e7748352193d7`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 304.3 KB (304287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3932c847bad7a644ef61688a39fe7e6985622bfae24224db72ebfbe22916aab`  
		Last Modified: Thu, 23 Mar 2023 09:31:40 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3317c07eda65fb456e1fb7372dcf45379845b3fabd59aaf6cb390fabed893fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf32adb5752d709797e0414a4d9b854663dcd211fd8f990390d1a6356b2cbd7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a7ebbf20b05aa1bc459f99a4e5299be2866f5a1f1c10119f96e417677ce6f9`  
		Last Modified: Wed, 01 Mar 2023 14:04:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:cf735919f0a9cc5aea3daf7ab80d7f93ad8ca2afba62bb55c07f2a0bcefa9780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:a99108bea9d07e5335225edd6ed83221e8408f2f0ea1c91a9bb60567127f65d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff0277e3ae878c0028f0d36cd89f9a1e74128f131914a395ce680396e7e671`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:da7229782d5fba3c8438c2b2de88bd3c6099ae476b1703fa26e86395a7562083
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563d61ed1e782e4a6aaa7a5d76b241ebd72621b74a11f862ab60ded47aa82b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:1b211a877b07ea4e1af7555214e58aeb850488ae2bca0bdd37c08ed013fe615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc97612a4116bab9949b583fb9c895b6a057a55ff0eb6fd8272d87a1d152cbea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d48b1adf7bba169d225b2bd8b8edcb1ad2c286e8ca68520b5174d3a18b7d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bf30130b0e476fe071e98d9ab2c3175b52a7508cb1e62517a27f3e948ca612`  
		Last Modified: Thu, 16 Mar 2023 05:58:21 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:546a886a46534eb07c9d82a7390048541674fc3b5d15c1d5905dbdb9a3263de5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f67aad37e1f08a1df26e7dc3fbeeec841d3e9dd70921d5dc3d40493fa9dd07c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61d991a58959ac33992a13de9a8889e155ffb794facc83d7bd5d7727080bc7`  
		Last Modified: Thu, 16 Mar 2023 02:43:10 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:43553d3ebc3be2e84e9750c76af18f59fcc1cae78f4d4886fdaa6b3bda22a8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:73c2f226b9d41a6ca475169b8a89e70fc0d8a921923c02d8afcb664afd8d8f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7191d88ea89379c7d8e2774cec92200333c8a7c2f3451a3cc48413f526dee25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c95488ad407602f3428cc2f1ca2a18fae5d6a574d08748cb496395700cf21a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db42a4a163de92fa05e1a55401762179cf3d028caf4e35c98f0f3914c62b0448`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:befaa46361e4cdf5e51af9449a8b44252a0de82fcffdfc01ec72fa2dca2db88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:52c45e356c8aa65f0195280d10137325b7079ffdaa1d264f97c21d6af24e6078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c7a0db011b4f391a443a7124397742ff9157869a66ae55e6e7f191966c5ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:57:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab5940b1d2c038782f17a50acc9126268be50075871c55afb2186fbc68e4bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4ac76a3c541cd78be3cddc5ff62f5665c6431aba800889e736786318e40285e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f25d7769d9cd3afa3b69a5e1309559b4abf92742d07f0f98b6f70396fb197`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338595f61a4f73430e7935e55fd6a4e9ed2ab7cab265310c9c90f41b00b94686`  
		Last Modified: Thu, 16 Mar 2023 02:43:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:00f4eabfcf6450382882359397323f5ce0ee1fb0cb6bb978eb328b6c33cd210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:731d9416c74576d5a00e1e625dfb2f62359eb4424e53824e1c0c3587875911da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5671c8387d65e53e56174bc8c57a79128a786b69655ff42f370ba344b7311ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92868460c6fd1adf5b17efda71fe04f9a3f942b0d2207e5e896d945691c34f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65329803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b09d7a97a033bde4a7708e836cf6e5e08c5f34d0e8bb9491dce8a4f1d87b51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:30e13475d409ec3f81d0614340f6cf87eda78738d1d7d653ea63c11976cabb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:3b6236836430a9b600ad6c23ee170bdab5cb7e8c8f57d92e1c75768e7ddc1b20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61293213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a271e0a7fcc73c4874a05deda7640915a38454a568ef348851239c8350e67185`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:57:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87854b612208107946dc34f8b2c307f8d327dd5e9d9bb230c589e38e39517b7e`  
		Last Modified: Thu, 23 Mar 2023 15:58:44 GMT  
		Size: 11.7 MB (11717776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dd62393e4e67f3515e1db58edc190f05b10d96684fe588165e9439c22b14fe`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44bc4b8083e27ff5a00477a6d71a509254fa7e50d77b8d41a3c0fc9fd99460`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a35ecff7e273194d23bd146df1031b1d5d40f9ec29f6cefba4f2ba45a67b4`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 281.8 KB (281792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:24c740bc59d10d0dc004696bc623404ab79f733bec1e1db0e0d6ce7c10066ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca4d0aeba7e98c3dba66e436fb1b58c135a1997e9b831276d8554516354fb5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:31:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0e8bba10f3b5b2432a2b1218e1c8025aa37e5b2848aba78cb30b14c96d48b`  
		Last Modified: Thu, 23 Mar 2023 09:32:22 GMT  
		Size: 11.7 MB (11677082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c996676719d71c02efc60656700e2212d3ad2c4aad1f607c5baa5644790eaad`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f354b2c84f012c8699569e7416cc07ba57b26ed0f605ae146d61586a3dbc579b`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89a260248440979723f69655c586df9a7be34913dc586e4ccf4a675c842b5d`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 282.2 KB (282220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:f528b19cc612f1d1444e5a4e3a3acf883bfca110b57d86b7f6f1e244c844f371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62722827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5387b36ce2af622c1e0eba8fe0b4347ccf401180723bdcb1bd9eee565933a3a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:1488f17cf02ffdc4fc658b91e1a4d259aebb0a2346095a40f2efbe2ac72c8f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:11aeabfc80c2ef7343d1ac7d4bc2a8183114f070c7bb6dd6f537ae889336cb4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61293606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4872da7f998dd349c6545f0f848f2f3ce3d0e1e9c1980e1d9c5d7188be4ad9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:57:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87854b612208107946dc34f8b2c307f8d327dd5e9d9bb230c589e38e39517b7e`  
		Last Modified: Thu, 23 Mar 2023 15:58:44 GMT  
		Size: 11.7 MB (11717776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dd62393e4e67f3515e1db58edc190f05b10d96684fe588165e9439c22b14fe`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44bc4b8083e27ff5a00477a6d71a509254fa7e50d77b8d41a3c0fc9fd99460`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a35ecff7e273194d23bd146df1031b1d5d40f9ec29f6cefba4f2ba45a67b4`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 281.8 KB (281792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092c12a90f6b1431a4546b33232e967f2126636ceff47cd7cf15bf42e71a9f2`  
		Last Modified: Thu, 23 Mar 2023 15:58:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:342c0311e4a3e51c8b6d2ba51cc2626c535413d7bb71b5e0427e14142a2cc3c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1704113e9c945898a8a0d7a241be127649f1269ff7fd5df9e088f5c8510fa74e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:31:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0e8bba10f3b5b2432a2b1218e1c8025aa37e5b2848aba78cb30b14c96d48b`  
		Last Modified: Thu, 23 Mar 2023 09:32:22 GMT  
		Size: 11.7 MB (11677082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c996676719d71c02efc60656700e2212d3ad2c4aad1f607c5baa5644790eaad`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f354b2c84f012c8699569e7416cc07ba57b26ed0f605ae146d61586a3dbc579b`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89a260248440979723f69655c586df9a7be34913dc586e4ccf4a675c842b5d`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 282.2 KB (282220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd26fafda5fed39ec26a8d1eec81c16dbb9f31c1a4593db76820237bb36856`  
		Last Modified: Thu, 23 Mar 2023 09:32:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf1388217fc75201eec1764ecf9ccc9d84becbc1a5c2fff97de123176d113bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62723225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5280e2b5efae98def7467cf9eecfc70f505f631e134aee484003dfdb9202f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61643c2ab05c90ffcc0f8e261d002b4cd8d654267ceadef7f14d5b5f46a05348`  
		Last Modified: Wed, 01 Mar 2023 14:25:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:60f0cbf3c9adcc42cffaa350f90a04cc21e30f190344386b844341df97c990b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:c4d51165f1892b56219b96998bc1020132f45310d639ec24d1eff26cc960f4e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a173c6a4606354e919d95d1c34b15c70261a567994dc7ca2f8d6231a6e5f84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b178d3e9f240e77488752e765509042c03f2bc17a3eab0e5f5a62b7b67c966`  
		Last Modified: Thu, 23 Mar 2023 15:57:49 GMT  
		Size: 10.5 MB (10504479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f9a76e2eac0f9a3dc42a01f95d1c280aa08207634cb8df83dd30a27f97959`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d9d3002cfeef01f97b0d184b0e841bfdf021850df4b0f6a88c2861c3bab41`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19bb407c9c70c6a8f88ceebbd19e3dde631a527d767bd8d13445707f3ab191f`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 304.3 KB (304269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b32bcd4cafaf47cf6c24e67da7b40242813e58d933b86dc54759c6084f759505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5526c79bfe19500886e549b52f3ec14113f2dd8a20a0dc87f2f627d67413642`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23969bd0deb154819623454501293274ed5d84a2980ddfab4a06aa292e2a8c2`  
		Last Modified: Thu, 23 Mar 2023 09:31:32 GMT  
		Size: 10.5 MB (10510313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbd5727c34bbfbac27263abe66d340203b862be36b5956a8a7a1be2e808287f`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9105f78f42f3a9a4b9f358a6913d438e595c68c00a3ca058316341700981f2`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e54dd992daca6739d936bec0393525b37f84ce18f86441110e7748352193d7`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 304.3 KB (304287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:96124b0d939cd9453d1f5bd48eaf28f9604b813af5f93a0ee05a6e5e9843f7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513b02edc7b5e1bfa4491c5259504ada968aaf72d7088609818f6f63a6d4e73c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:d5c8df09d1a6dd4914125eb9673a1f36809dd1aa4e6604538420c4890c57ed6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:90af1451f53e1c6742109e4d54dbad70fc89cdb8adb6ef0abdc245c335bb66ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0a64f9a25c419b96996656c710c481d3a87486d7fa0118a379379009f8e88f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b178d3e9f240e77488752e765509042c03f2bc17a3eab0e5f5a62b7b67c966`  
		Last Modified: Thu, 23 Mar 2023 15:57:49 GMT  
		Size: 10.5 MB (10504479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f9a76e2eac0f9a3dc42a01f95d1c280aa08207634cb8df83dd30a27f97959`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d9d3002cfeef01f97b0d184b0e841bfdf021850df4b0f6a88c2861c3bab41`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19bb407c9c70c6a8f88ceebbd19e3dde631a527d767bd8d13445707f3ab191f`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 304.3 KB (304269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e1b98b76491914cf926697dac13d6b087f7d6d5abac8dc4e43f32f2361f611`  
		Last Modified: Thu, 23 Mar 2023 15:57:57 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:707b6b7ee753feff9c0e77fd533fbed40ad0de825780d2e8b0882c058f587dcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b48cfaa3525f6d38ee12012c95842484629f74e01fb847be0310142622e9698`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23969bd0deb154819623454501293274ed5d84a2980ddfab4a06aa292e2a8c2`  
		Last Modified: Thu, 23 Mar 2023 09:31:32 GMT  
		Size: 10.5 MB (10510313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbd5727c34bbfbac27263abe66d340203b862be36b5956a8a7a1be2e808287f`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9105f78f42f3a9a4b9f358a6913d438e595c68c00a3ca058316341700981f2`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e54dd992daca6739d936bec0393525b37f84ce18f86441110e7748352193d7`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 304.3 KB (304287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3932c847bad7a644ef61688a39fe7e6985622bfae24224db72ebfbe22916aab`  
		Last Modified: Thu, 23 Mar 2023 09:31:40 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3317c07eda65fb456e1fb7372dcf45379845b3fabd59aaf6cb390fabed893fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf32adb5752d709797e0414a4d9b854663dcd211fd8f990390d1a6356b2cbd7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a7ebbf20b05aa1bc459f99a4e5299be2866f5a1f1c10119f96e417677ce6f9`  
		Last Modified: Wed, 01 Mar 2023 14:04:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:00f4eabfcf6450382882359397323f5ce0ee1fb0cb6bb978eb328b6c33cd210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:731d9416c74576d5a00e1e625dfb2f62359eb4424e53824e1c0c3587875911da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5671c8387d65e53e56174bc8c57a79128a786b69655ff42f370ba344b7311ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92868460c6fd1adf5b17efda71fe04f9a3f942b0d2207e5e896d945691c34f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65329803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b09d7a97a033bde4a7708e836cf6e5e08c5f34d0e8bb9491dce8a4f1d87b51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:23ceabfead07bc794a3b911ec139f354023a29726b2104d031763c0e4ef80842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ffaf0534f22237b26e31bebacbe1ebc34cd0de0dfebcdc0c8e8b326335f5052f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa0c96870ed0a018d382afba1c0ba37f6c631858137d15d7140e96bc6231760`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563217d06ceffa980bd11353e01edde1aaa6630b9ec105205bb408b3413223e0`  
		Last Modified: Thu, 23 Mar 2023 15:58:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:295ddab89857cef0356935333a55df2ba7b26c6b53d402b293ff3f5c27e953d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f273b679fbf05cd298c531d890064262b449d3d7ac94283da3408f650ac4bfc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b84876434546224a0b3486b5afd43e5f2e02d867d6595aa8aea5dab4980ff`  
		Last Modified: Thu, 23 Mar 2023 09:31:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:22dea449602d8560942c7b84d9e3bd0813eb0acc4a17fd39ef115e38023819be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:aaf4ace714149fbbd4aa37702ef9a418e815693769d5d6948d9680a098d95065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea11c1f6a6a05aaedd47a751c5820a89bd89707b688187f4ba1a74e6f4642f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:29:51 GMT
ADD file:98917c081507795b8ce084d09f5df75e959c5365882d73ca7a52da226c93fdcf in / 
# Thu, 23 Mar 2023 01:29:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15c60aea1a8c926f00ec7713f9ae1fcd349591095bddcc01ee5a6027b8a3998`  
		Last Modified: Thu, 23 Mar 2023 01:33:26 GMT  
		Size: 49.3 MB (49278011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9208dbea1384f0435290a314a68b9e6ad71ba2b9dbc0e8e2e4852875066ddf`  
		Last Modified: Thu, 23 Mar 2023 15:58:27 GMT  
		Size: 11.7 MB (11700942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a15d3deea27d74ff209b653b645539f94afc9c3199da23c2809f8d280b1b3f`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e406df43edaf35d7a6bc4cea702f54397cf137a9d3fc0019407820d04ef31`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a7fbeae0fd84e72219aeeee22cdbe3cb20cc7a557f566b2f22aaf19d9b50e`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 281.8 KB (281820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0ce04cb955ac097770a113bfbf6a31a982f9b257a46d81310f207bbd3e5a1817
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61274170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a17a3b7a5e2f272625f4110217f17c95e107be31ca369b7f03707d564374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a5450317480d94cb3403d7cde2e56b05a48f2729e28a94049e38b55e2c549`  
		Last Modified: Thu, 23 Mar 2023 09:32:07 GMT  
		Size: 11.7 MB (11661617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedde67f6e600aa9b9a11df48f5d1062eb19dddf30cc6e3692edcaf48930293`  
		Last Modified: Thu, 23 Mar 2023 09:32:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0b4d2410468a43678d43b81648e033fa5a8ddf3a801c9d297f60d0a31d8f2`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd75676c2211f19e7b64fb9984b6e1bf632dcd2caea07507d60c7effb2eb465c`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 282.3 KB (282259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:e5113fd09171ab576c1d16b344acf0e917e04d98112db25425b0d5728ea300e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557d46a191412276903630954b271d01ce46d04c01a44e474ff3e6e2c21a8419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:863174a23d498b858cb76312989a2a59b8824c5675a61db6d927694fdaac8985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0237ee6a22e7705b99f1bbed529f9a219ea3fbe5eff0bae93e7fdd431523e6a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61263207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b0d2074eceb83419b21ce55ebd3311ee6c49a01e4bde2965538596e1f2605b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:29:51 GMT
ADD file:98917c081507795b8ce084d09f5df75e959c5365882d73ca7a52da226c93fdcf in / 
# Thu, 23 Mar 2023 01:29:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c15c60aea1a8c926f00ec7713f9ae1fcd349591095bddcc01ee5a6027b8a3998`  
		Last Modified: Thu, 23 Mar 2023 01:33:26 GMT  
		Size: 49.3 MB (49278011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9208dbea1384f0435290a314a68b9e6ad71ba2b9dbc0e8e2e4852875066ddf`  
		Last Modified: Thu, 23 Mar 2023 15:58:27 GMT  
		Size: 11.7 MB (11700942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a15d3deea27d74ff209b653b645539f94afc9c3199da23c2809f8d280b1b3f`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e406df43edaf35d7a6bc4cea702f54397cf137a9d3fc0019407820d04ef31`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a7fbeae0fd84e72219aeeee22cdbe3cb20cc7a557f566b2f22aaf19d9b50e`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 281.8 KB (281820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941509578d336ae727d7fe0d4c3761b4a2a7a1ce6df64c7b1fb2e3f4616beacc`  
		Last Modified: Thu, 23 Mar 2023 15:58:35 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a2c5e1cfb2814edb23bd6065569664d16e86693f6f514e76dbc163682bbfc6fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61274598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6da4b4fdf067a7776172d7f1f60446aa9567a46f13b4c63b53325eba4a8489`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a5450317480d94cb3403d7cde2e56b05a48f2729e28a94049e38b55e2c549`  
		Last Modified: Thu, 23 Mar 2023 09:32:07 GMT  
		Size: 11.7 MB (11661617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedde67f6e600aa9b9a11df48f5d1062eb19dddf30cc6e3692edcaf48930293`  
		Last Modified: Thu, 23 Mar 2023 09:32:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0b4d2410468a43678d43b81648e033fa5a8ddf3a801c9d297f60d0a31d8f2`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd75676c2211f19e7b64fb9984b6e1bf632dcd2caea07507d60c7effb2eb465c`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 282.3 KB (282259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c013b8973b114670d57c5a9a234343c9cd9199af17a900bf60083c001ee0d0`  
		Last Modified: Thu, 23 Mar 2023 09:32:14 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f5fb222c99bb60ec1873ec12109f2100cc2f7c0c0c4c49ebb862931a40cdd778
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09e3e4c39734921aa13a5fdf12088049ecffc7f768a939e9d66a1f34b502ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81dfd8e9fbdde88d17ac8708e298dfcd7fdad09eda77db2790d4525ee1b50c3`  
		Last Modified: Wed, 01 Mar 2023 14:04:58 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:2429604df643c021ff2cab3dac991a0fa74772bf0b83861bd2ecd784fe0da05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ada092c3a0c585f13d5f793e7205070600af63e45981298386e2dababa1d738a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97eecada419163ee3c517ac6705ef6e5dfa59771e40d23b94dfc828b9d1d62c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2a4b5dc9653f9c297b655b999a18dc419aa1de140d5f0922e669d63ba8f81e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d4d01492647633a3360a913f3e312b6b59ea3c99348fb6c59efd5147552260`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:088603ff4edc4022b00300092617e96a8049eeb012b4171c88cb69e1deaed5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9e8ffa5a31ecac0fc53ac08f758b6f3acd6aa33812e5f0d0527472b9b881dfa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bb7a8f0e8135403e8e485b1e329938addf81ddadf3098c440a8e59666b9b66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da88f82f719637c6eaba4b8175eda88b088da7adfc3952ff2732a42ed676775e`  
		Last Modified: Thu, 16 Mar 2023 05:58:04 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f9f953e47a67b48292e1ce793d31c3c7189d274b938ad5449b46e116d25a8a6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072b8fb76cb79a0ce80d413e95024a3f0fc969a9404af11cc642f6fc269db7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505f3caedc8772916ffde5305b38400b1745044ad55838322de25760fb04dc4a`  
		Last Modified: Thu, 16 Mar 2023 02:42:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:cf735919f0a9cc5aea3daf7ab80d7f93ad8ca2afba62bb55c07f2a0bcefa9780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:a99108bea9d07e5335225edd6ed83221e8408f2f0ea1c91a9bb60567127f65d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff0277e3ae878c0028f0d36cd89f9a1e74128f131914a395ce680396e7e671`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:da7229782d5fba3c8438c2b2de88bd3c6099ae476b1703fa26e86395a7562083
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563d61ed1e782e4a6aaa7a5d76b241ebd72621b74a11f862ab60ded47aa82b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:1b211a877b07ea4e1af7555214e58aeb850488ae2bca0bdd37c08ed013fe615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc97612a4116bab9949b583fb9c895b6a057a55ff0eb6fd8272d87a1d152cbea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d48b1adf7bba169d225b2bd8b8edcb1ad2c286e8ca68520b5174d3a18b7d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bf30130b0e476fe071e98d9ab2c3175b52a7508cb1e62517a27f3e948ca612`  
		Last Modified: Thu, 16 Mar 2023 05:58:21 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:546a886a46534eb07c9d82a7390048541674fc3b5d15c1d5905dbdb9a3263de5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f67aad37e1f08a1df26e7dc3fbeeec841d3e9dd70921d5dc3d40493fa9dd07c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61d991a58959ac33992a13de9a8889e155ffb794facc83d7bd5d7727080bc7`  
		Last Modified: Thu, 16 Mar 2023 02:43:10 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:43553d3ebc3be2e84e9750c76af18f59fcc1cae78f4d4886fdaa6b3bda22a8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:73c2f226b9d41a6ca475169b8a89e70fc0d8a921923c02d8afcb664afd8d8f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7191d88ea89379c7d8e2774cec92200333c8a7c2f3451a3cc48413f526dee25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c95488ad407602f3428cc2f1ca2a18fae5d6a574d08748cb496395700cf21a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db42a4a163de92fa05e1a55401762179cf3d028caf4e35c98f0f3914c62b0448`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:befaa46361e4cdf5e51af9449a8b44252a0de82fcffdfc01ec72fa2dca2db88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:52c45e356c8aa65f0195280d10137325b7079ffdaa1d264f97c21d6af24e6078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c7a0db011b4f391a443a7124397742ff9157869a66ae55e6e7f191966c5ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:57:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab5940b1d2c038782f17a50acc9126268be50075871c55afb2186fbc68e4bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4ac76a3c541cd78be3cddc5ff62f5665c6431aba800889e736786318e40285e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f25d7769d9cd3afa3b69a5e1309559b4abf92742d07f0f98b6f70396fb197`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338595f61a4f73430e7935e55fd6a4e9ed2ab7cab265310c9c90f41b00b94686`  
		Last Modified: Thu, 16 Mar 2023 02:43:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:23ceabfead07bc794a3b911ec139f354023a29726b2104d031763c0e4ef80842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ffaf0534f22237b26e31bebacbe1ebc34cd0de0dfebcdc0c8e8b326335f5052f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa0c96870ed0a018d382afba1c0ba37f6c631858137d15d7140e96bc6231760`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563217d06ceffa980bd11353e01edde1aaa6630b9ec105205bb408b3413223e0`  
		Last Modified: Thu, 23 Mar 2023 15:58:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:295ddab89857cef0356935333a55df2ba7b26c6b53d402b293ff3f5c27e953d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f273b679fbf05cd298c531d890064262b449d3d7ac94283da3408f650ac4bfc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b84876434546224a0b3486b5afd43e5f2e02d867d6595aa8aea5dab4980ff`  
		Last Modified: Thu, 23 Mar 2023 09:31:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:30e13475d409ec3f81d0614340f6cf87eda78738d1d7d653ea63c11976cabb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:3b6236836430a9b600ad6c23ee170bdab5cb7e8c8f57d92e1c75768e7ddc1b20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61293213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a271e0a7fcc73c4874a05deda7640915a38454a568ef348851239c8350e67185`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:57:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87854b612208107946dc34f8b2c307f8d327dd5e9d9bb230c589e38e39517b7e`  
		Last Modified: Thu, 23 Mar 2023 15:58:44 GMT  
		Size: 11.7 MB (11717776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dd62393e4e67f3515e1db58edc190f05b10d96684fe588165e9439c22b14fe`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44bc4b8083e27ff5a00477a6d71a509254fa7e50d77b8d41a3c0fc9fd99460`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a35ecff7e273194d23bd146df1031b1d5d40f9ec29f6cefba4f2ba45a67b4`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 281.8 KB (281792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:24c740bc59d10d0dc004696bc623404ab79f733bec1e1db0e0d6ce7c10066ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca4d0aeba7e98c3dba66e436fb1b58c135a1997e9b831276d8554516354fb5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:31:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0e8bba10f3b5b2432a2b1218e1c8025aa37e5b2848aba78cb30b14c96d48b`  
		Last Modified: Thu, 23 Mar 2023 09:32:22 GMT  
		Size: 11.7 MB (11677082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c996676719d71c02efc60656700e2212d3ad2c4aad1f607c5baa5644790eaad`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f354b2c84f012c8699569e7416cc07ba57b26ed0f605ae146d61586a3dbc579b`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89a260248440979723f69655c586df9a7be34913dc586e4ccf4a675c842b5d`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 282.2 KB (282220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:f528b19cc612f1d1444e5a4e3a3acf883bfca110b57d86b7f6f1e244c844f371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62722827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5387b36ce2af622c1e0eba8fe0b4347ccf401180723bdcb1bd9eee565933a3a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:1488f17cf02ffdc4fc658b91e1a4d259aebb0a2346095a40f2efbe2ac72c8f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:11aeabfc80c2ef7343d1ac7d4bc2a8183114f070c7bb6dd6f537ae889336cb4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61293606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4872da7f998dd349c6545f0f848f2f3ce3d0e1e9c1980e1d9c5d7188be4ad9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:57:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87854b612208107946dc34f8b2c307f8d327dd5e9d9bb230c589e38e39517b7e`  
		Last Modified: Thu, 23 Mar 2023 15:58:44 GMT  
		Size: 11.7 MB (11717776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dd62393e4e67f3515e1db58edc190f05b10d96684fe588165e9439c22b14fe`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44bc4b8083e27ff5a00477a6d71a509254fa7e50d77b8d41a3c0fc9fd99460`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a35ecff7e273194d23bd146df1031b1d5d40f9ec29f6cefba4f2ba45a67b4`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 281.8 KB (281792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092c12a90f6b1431a4546b33232e967f2126636ceff47cd7cf15bf42e71a9f2`  
		Last Modified: Thu, 23 Mar 2023 15:58:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:342c0311e4a3e51c8b6d2ba51cc2626c535413d7bb71b5e0427e14142a2cc3c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1704113e9c945898a8a0d7a241be127649f1269ff7fd5df9e088f5c8510fa74e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:31:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0e8bba10f3b5b2432a2b1218e1c8025aa37e5b2848aba78cb30b14c96d48b`  
		Last Modified: Thu, 23 Mar 2023 09:32:22 GMT  
		Size: 11.7 MB (11677082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c996676719d71c02efc60656700e2212d3ad2c4aad1f607c5baa5644790eaad`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f354b2c84f012c8699569e7416cc07ba57b26ed0f605ae146d61586a3dbc579b`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89a260248440979723f69655c586df9a7be34913dc586e4ccf4a675c842b5d`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 282.2 KB (282220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd26fafda5fed39ec26a8d1eec81c16dbb9f31c1a4593db76820237bb36856`  
		Last Modified: Thu, 23 Mar 2023 09:32:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf1388217fc75201eec1764ecf9ccc9d84becbc1a5c2fff97de123176d113bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62723225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5280e2b5efae98def7467cf9eecfc70f505f631e134aee484003dfdb9202f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61643c2ab05c90ffcc0f8e261d002b4cd8d654267ceadef7f14d5b5f46a05348`  
		Last Modified: Wed, 01 Mar 2023 14:25:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
