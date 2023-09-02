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
$ docker pull neurodebian@sha256:0dc0c6379aa9de4c7beb314a77836296ed1b9ecec52b6e370d7d1d8fb37e8c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:436d0f91b2596d1a67587f416d172e20ea63d2ba9fab4064134e658283be40b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54202678ffa323cabbfa7d9142d688755ff6767f3a44607c1eb821edd05ac91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:be402681584b912cb441771e9a7e1b039e2da347fe7ebf2d1cd9f3736c2e5b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364f14a0ddb6cdd1d2222f8d8d1cd397a7334c3eb47c91b89028ee7a7e491380`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:c6e4772e5c601ede7ccf289927f339f34eab81e04942d3e803f285f931926a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:137b909d0e4c4e1c4300fa4479a22b15c053df24cbbef0f13fce395100eafa77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226a853426c1d4b6bd2f86d099a28d4c4db35b9d83d9a7021c549f5386248a11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e158a3949abb4a78460b0321777ca278a50c79ac290966e5d6a7f027b04e3dd`  
		Last Modified: Fri, 02 Jun 2023 01:35:57 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edc6bddeb118195088c3f1948fdc52cc913d453e5f543927c7c89c015fe7bd6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d966d5bec6e766760870e6f4674ca17b3fe69617f78ade07c2a7b6b3154ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:46:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350adb1f8b3dcaa1835899b2dc84ec2f5a997c31b87aa8e76470a92bc742bc7f`  
		Last Modified: Thu, 01 Jun 2023 23:46:55 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:0d130609fbb2188edc7ee683677321dd930d20c9f45d9ae659e0d8f0883c81ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:21894431e3a16dc7f171d76066a7122a135676a9b505e1816e10b550c4139951
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61308980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6172b4009d06e533acd67e84f4542e78aae2f19fad619f3ac124985e2b6f68fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:30 GMT
ADD file:3a6d159d80cb8abfacda5873c243a6ae635ff603708febc4df51f8eec26d3de7 in / 
# Wed, 16 Aug 2023 00:59:31 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de4cac68b6165c40cf6f8b30417948c31be03a968e233e55ee40221553a5e570`  
		Last Modified: Wed, 16 Aug 2023 01:04:06 GMT  
		Size: 49.6 MB (49557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d6403b214041d209839a70f25dbd8a74ca35b340cd505a7beab4a170cca7f5`  
		Last Modified: Wed, 16 Aug 2023 10:15:49 GMT  
		Size: 11.5 MB (11463261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98032d4a249856d7aabaa3af9134cd443eeee95627f4b4826f18d3dfd3dc4331`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871fc39cb100ac4f417725f892c0e7d1fe64fd283c71f47da0babe29d87271f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b37d2551f1ac4bf700870ba04cc161179be2c0f688406c9dbe1d6cf58cd24f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7058e215cde4c1022622e829cb6e4e526d3738afd710b707481395e7c12fce25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b38f7ddb07b4861aa264cce463468a311f6727d5b67388b3bce2b990ba30a5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2702582abd923413cfef5d91b723dd4d2a9fa9c89a6e68e42fa66876db7f4`  
		Last Modified: Wed, 16 Aug 2023 03:52:57 GMT  
		Size: 11.4 MB (11426893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a3cbd38cab59e99577e9251a79dd45edcbd8cd11619d83a9ca0b2ef51eee8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd89b2b4d95679b6e5bbe98ee70a0ffea9d1e8884e0fc4f90e9fd57a6b3465d8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d717c54d750af9ef25aea7e73cbecf3d063ba7e3ba6c9e05fceafc40f519cd8f`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 286.6 KB (286586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:01332eb612c9330b3a3c3dc2dbe5d3aca14928caeef3e6b07858395da9469f27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62739862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2184b9c8fc56b5e43afc8a24637c675b5f63fccf9e2243ccc39946b305bbf8dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:38:49 GMT
ADD file:3f0a4d6b18b22088d0785bc2e351d829ad1ed6f154058017035842bdbe2a8d1e in / 
# Tue, 15 Aug 2023 23:38:51 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dc6cc826af02d533745c4612f635e028f3471e46f50422fd20a6dc913b60574`  
		Last Modified: Tue, 15 Aug 2023 23:43:02 GMT  
		Size: 50.6 MB (50568054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646efa09d31a3e9a9508a47906e753a78732c68c3d19f31a5f2e7c01492dae9`  
		Last Modified: Wed, 16 Aug 2023 03:43:21 GMT  
		Size: 11.9 MB (11883338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4995daa45aaed4dd28725edeca185c0aa766cfb40924d40620cf18f750436eb3`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee4413c37e9b5ccb7f7a6083b10b9405a8597b97a4d0b633e59f3c8e20ca22`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e05db3d06057f7b8dc58d17ceeb8083288c9bb6af96b2195da0956e89022b`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 286.5 KB (286453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:6ec9fb7baaac405ef37bb93de693eda1cbd8c72332c5fb0150783f2b8a3c42c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2d3b719f4ae2a0197538c37d7ce91900fd5c99c816b356f209e863500f6d8f82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae7c41266f3afec454933bceaf2ab670697ef86c81b79e42883defee230e2bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:30 GMT
ADD file:3a6d159d80cb8abfacda5873c243a6ae635ff603708febc4df51f8eec26d3de7 in / 
# Wed, 16 Aug 2023 00:59:31 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:de4cac68b6165c40cf6f8b30417948c31be03a968e233e55ee40221553a5e570`  
		Last Modified: Wed, 16 Aug 2023 01:04:06 GMT  
		Size: 49.6 MB (49557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d6403b214041d209839a70f25dbd8a74ca35b340cd505a7beab4a170cca7f5`  
		Last Modified: Wed, 16 Aug 2023 10:15:49 GMT  
		Size: 11.5 MB (11463261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98032d4a249856d7aabaa3af9134cd443eeee95627f4b4826f18d3dfd3dc4331`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871fc39cb100ac4f417725f892c0e7d1fe64fd283c71f47da0babe29d87271f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b37d2551f1ac4bf700870ba04cc161179be2c0f688406c9dbe1d6cf58cd24f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24ad0c9c7a55acb043200edd44eb47f0b650a545a0fb69f6f7fe9a081a52ee`  
		Last Modified: Wed, 16 Aug 2023 10:15:57 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:974160c65245412290cbf8d1b12115acc678d7dcb6a63096e384ed6100818161
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61307231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e451defa12b04fc9f56455eb9346a4ce0260a78a1e7f3aaffb312a09aaebc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2702582abd923413cfef5d91b723dd4d2a9fa9c89a6e68e42fa66876db7f4`  
		Last Modified: Wed, 16 Aug 2023 03:52:57 GMT  
		Size: 11.4 MB (11426893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a3cbd38cab59e99577e9251a79dd45edcbd8cd11619d83a9ca0b2ef51eee8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd89b2b4d95679b6e5bbe98ee70a0ffea9d1e8884e0fc4f90e9fd57a6b3465d8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d717c54d750af9ef25aea7e73cbecf3d063ba7e3ba6c9e05fceafc40f519cd8f`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 286.6 KB (286586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ac2213dbcf824403a3cbfe97c9c9a16d189471fcd448f71e496940768214d2`  
		Last Modified: Wed, 16 Aug 2023 03:53:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c4af6957f74e19b0093bbb86c0180a4088e66fb3fcda0dc11ea6069983a24ba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856eaaeb40cd76eb168df229d318ec8dbe29c8d82a0e95c8be449ce04610390e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:38:49 GMT
ADD file:3f0a4d6b18b22088d0785bc2e351d829ad1ed6f154058017035842bdbe2a8d1e in / 
# Tue, 15 Aug 2023 23:38:51 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1dc6cc826af02d533745c4612f635e028f3471e46f50422fd20a6dc913b60574`  
		Last Modified: Tue, 15 Aug 2023 23:43:02 GMT  
		Size: 50.6 MB (50568054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646efa09d31a3e9a9508a47906e753a78732c68c3d19f31a5f2e7c01492dae9`  
		Last Modified: Wed, 16 Aug 2023 03:43:21 GMT  
		Size: 11.9 MB (11883338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4995daa45aaed4dd28725edeca185c0aa766cfb40924d40620cf18f750436eb3`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee4413c37e9b5ccb7f7a6083b10b9405a8597b97a4d0b633e59f3c8e20ca22`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e05db3d06057f7b8dc58d17ceeb8083288c9bb6af96b2195da0956e89022b`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 286.5 KB (286453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05abbd3aff72718cfe7c0f7690be327e1ea516e52d433760875df5973c7f033`  
		Last Modified: Wed, 16 Aug 2023 03:43:28 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:2556feb52625ee39aa8b09b9e4420232b231f4b5e46c2a251e7923ca35a3c4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:b88dc1cd32373ceb3e8b6f1e29816b95c677f084126a968ae9afddd9f8ed0664
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66681560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfaf8983cbc172d7a70de973c76fbdc94ac97fa240ec66a4d59d647e09d071a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277dc632d247999fb7a6cd0bd5baec2171b343c20b37144154ee00b5f16c33c`  
		Last Modified: Wed, 16 Aug 2023 10:15:27 GMT  
		Size: 11.3 MB (11310931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d86ff81e5b660e03eeeee9621aaaa20e5f489179d72d578cdda7d70ee2c5d`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447f2ea93014e7d1c7b07289e423184f36439a89ad19283eccdc016b42cf9fe`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea88abaf68b1bb7c8399a5458e6ebe8cd32f9ac34e4b05a1832fc4930135d6ac`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 312.0 KB (311993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a97004bec5c1281f8fcb08fb6b26e6db2c5c7df3a8d26b06d111c6e6d995937f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c8b34682450722533d0edc8ce1ceb00f1cfd30e01d638633504ed9c3fa126`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f617cf8ad2e2c41398a2e69ee56490ac9f8d5c1dbd0ab7b36b10a0efa3144`  
		Last Modified: Wed, 16 Aug 2023 03:52:36 GMT  
		Size: 11.3 MB (11313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ac930639ae5b54a166c044aded05a4158b2d09535fc1db3b615f2b1de7e9a`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88e6bdea4ca56ad8afce5b3316f65de09d3e4065a741716fab48052a8f317e`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee859683358f1930f92f8c516715068cfe671ec72b49a97ef92b6d13ea709a1`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 311.9 KB (311918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:cb2e82e795b75e1888216025391b0f6889a76daf64e07f90caf70b5201802ddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da46703ed660e2ab9b62b1d5edd3e9f7e39c1a946be608bca549c6393b5efcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5750deeda7e20aa3970ce752bfae0fd6c1a830d267498576eaf6ccf81b775bef`  
		Last Modified: Wed, 16 Aug 2023 03:42:59 GMT  
		Size: 11.7 MB (11707953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55328912e9ff34ca1f686e3fd42e1daf0949cf81967f6f81902e62a18486b506`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc32ee8ff65662d5091b2e4e952394e383e9fe418d81477718c164b03ae4198`  
		Last Modified: Wed, 16 Aug 2023 03:42:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f976114f832664b48a08c50da76cf92bff2e7820d61f534a002c298b7c5b7b3`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 311.8 KB (311849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:741af06694a1c55f2da8b4abab79e407527a0e4d2c4517e9dcae27b02c6d8d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6b4fa7b4b9fefa395a00e816d280df65e27ee7b431f2e725849cb8b4038875fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66681919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7147d37d98a4b3ae2e7db97d368c8e94816f766a5d3e788041cb4066dff406c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277dc632d247999fb7a6cd0bd5baec2171b343c20b37144154ee00b5f16c33c`  
		Last Modified: Wed, 16 Aug 2023 10:15:27 GMT  
		Size: 11.3 MB (11310931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d86ff81e5b660e03eeeee9621aaaa20e5f489179d72d578cdda7d70ee2c5d`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447f2ea93014e7d1c7b07289e423184f36439a89ad19283eccdc016b42cf9fe`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea88abaf68b1bb7c8399a5458e6ebe8cd32f9ac34e4b05a1832fc4930135d6ac`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 312.0 KB (311993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80aaa9ab5b22adbd516f80deac4bd772aeaf624108aa2939fcdf90c8d812f8`  
		Last Modified: Wed, 16 Aug 2023 10:15:38 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1c1f04b90f03ee0e3630f0e38ed6b61157285c4dc89d73719fd52ccb0634a2d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2b570139c1bae4983d5f7477cfca3bb1df62880b79682017a23b16ebc0929a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f617cf8ad2e2c41398a2e69ee56490ac9f8d5c1dbd0ab7b36b10a0efa3144`  
		Last Modified: Wed, 16 Aug 2023 03:52:36 GMT  
		Size: 11.3 MB (11313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ac930639ae5b54a166c044aded05a4158b2d09535fc1db3b615f2b1de7e9a`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88e6bdea4ca56ad8afce5b3316f65de09d3e4065a741716fab48052a8f317e`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee859683358f1930f92f8c516715068cfe671ec72b49a97ef92b6d13ea709a1`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 311.9 KB (311918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803acde4b75dbb93b203e9432ccc3755a95eaca94114e6ecc54fc98e921b2a6`  
		Last Modified: Wed, 16 Aug 2023 03:52:46 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3bdd99a51d92fecffae8ab6c9199e8c39f7e10a059050d0c7c7bd9528e2dbb88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07866f611e3e3217fa93a66044867c874391cbc9bf56019524b580601674b67a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5750deeda7e20aa3970ce752bfae0fd6c1a830d267498576eaf6ccf81b775bef`  
		Last Modified: Wed, 16 Aug 2023 03:42:59 GMT  
		Size: 11.7 MB (11707953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55328912e9ff34ca1f686e3fd42e1daf0949cf81967f6f81902e62a18486b506`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc32ee8ff65662d5091b2e4e952394e383e9fe418d81477718c164b03ae4198`  
		Last Modified: Wed, 16 Aug 2023 03:42:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f976114f832664b48a08c50da76cf92bff2e7820d61f534a002c298b7c5b7b3`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 311.8 KB (311849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3e8b052baa4381b554e9dbc07893559e3acdaab1f7b9bbb525937b3b1a47d`  
		Last Modified: Wed, 16 Aug 2023 03:43:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:8da30a13d55f682cb7b5abcb1ba4ec1948a418aa379db648ccb706ee46032350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:0da68b4aca50e778ac715c49714c6bba2209cfc37cdb1444b03fb7fa7558b3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea452dff405f01f746e680cb1dc3b4c1457238a9405245d4c2d0774760300ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:19 GMT
ADD file:30ed10904e3533aa50c332544532891f0dcf06cce020988e07af9afa6b2f5df4 in / 
# Wed, 16 Aug 2023 01:00:20 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6b7393fb4f375905c31c483d81ce2a2905f88aba8cb198874da2b54035bc41d`  
		Last Modified: Wed, 16 Aug 2023 01:05:31 GMT  
		Size: 50.5 MB (50498099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d786e39fbdde08da5ac21348797106a8e48f83ec4f16eb988bae3d24b3d1f`  
		Last Modified: Wed, 16 Aug 2023 10:15:09 GMT  
		Size: 10.5 MB (10504726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067e4a986b67fcae5368b79e01f6f2bfa8c41b745cb020fcb702b8dec9ce0a8c`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b10d61fb6b2b77af47566a04fb2f10162c788281459e74630ceeb4b713c2a`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e9b94a4b05fa98315a44b00a103167cea1a667dccf6483a4eb9f6201bac3b`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 304.6 KB (304619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5c066f0b95d700c7c3bbb02258c68faf30f73bd15cbcb5c5faffeb0222bb1468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17ce73f54623eae40a7273f88ce32130e6ee13f6b8397d25ffef4cf59444673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:50:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:50:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff548e71e5e2b2825cca5159e38ac0f04f9ea241d05e88b8df6c827bcc66890e`  
		Last Modified: Wed, 16 Aug 2023 03:52:19 GMT  
		Size: 10.5 MB (10510675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd3c3a2153366ee917527815d07c3d6084923d4377d36a0fb26dde691b7b20`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dfdfdf86764a28629c52c3bcdfdad862c754d940385bbb1f38e6f03b18d8f3`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a825c8e8bc1a402e4fe8ab17fe0f155a3a9025417cb24bf4d2a2637170e57`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 304.5 KB (304542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:62ca31b62277e996a6e5bc4002e25e2d0e4341dd8e20e7341d0209219f7f4ec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff2c883e44081a3fcbf67700e217756905f3b28e33ba79d31601bbd3e9cbf14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c33de8dd8d88404193f8d100efd13ecaafbc18e3391f3688ce0c41b269c813`  
		Last Modified: Wed, 16 Aug 2023 03:42:41 GMT  
		Size: 10.9 MB (10868493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690636d1fbf114a0d369abbe65be2cbc0237d8715c0e8ef4b4226c1fb32cb310`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6912fa3cbe68256fbe65f857e365c177f93957e7048c96c4ff7ad44e3350b18`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76675ef82d7692108de74c45d4c734a1277e8a1ad34a2383ba8e0cc3247c34`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 304.5 KB (304516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:bc20e10a5af1bc7ca8e59d8b30f28268d6d29323ee7590649b3a27c27245d829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:93f8d0afac93b903b63fa9359774326e1a25be96eb932e6b0f630d1247528fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5382eed41a72f0ff3b74550ad076459631f1d6d308c29f7b51c91db65318e484`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:19 GMT
ADD file:30ed10904e3533aa50c332544532891f0dcf06cce020988e07af9afa6b2f5df4 in / 
# Wed, 16 Aug 2023 01:00:20 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d6b7393fb4f375905c31c483d81ce2a2905f88aba8cb198874da2b54035bc41d`  
		Last Modified: Wed, 16 Aug 2023 01:05:31 GMT  
		Size: 50.5 MB (50498099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d786e39fbdde08da5ac21348797106a8e48f83ec4f16eb988bae3d24b3d1f`  
		Last Modified: Wed, 16 Aug 2023 10:15:09 GMT  
		Size: 10.5 MB (10504726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067e4a986b67fcae5368b79e01f6f2bfa8c41b745cb020fcb702b8dec9ce0a8c`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b10d61fb6b2b77af47566a04fb2f10162c788281459e74630ceeb4b713c2a`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e9b94a4b05fa98315a44b00a103167cea1a667dccf6483a4eb9f6201bac3b`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 304.6 KB (304619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffc707d6bc130465732198e61ac65ec3f1b7d04c28b3bf6d86a3286ca18869`  
		Last Modified: Wed, 16 Aug 2023 10:15:17 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:88f4b1a84b6f01382b277f7d3bf39f72a8b94b2548b554238fc77253f3ceb7b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7543797664e4133d57ddbb8a7a093b86e7323dfaa8a15c3327ab452d1a7db5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:50:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:50:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff548e71e5e2b2825cca5159e38ac0f04f9ea241d05e88b8df6c827bcc66890e`  
		Last Modified: Wed, 16 Aug 2023 03:52:19 GMT  
		Size: 10.5 MB (10510675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd3c3a2153366ee917527815d07c3d6084923d4377d36a0fb26dde691b7b20`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dfdfdf86764a28629c52c3bcdfdad862c754d940385bbb1f38e6f03b18d8f3`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a825c8e8bc1a402e4fe8ab17fe0f155a3a9025417cb24bf4d2a2637170e57`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 304.5 KB (304542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96918ab91a1c0ba75a677c85f091ac5a0d073d76bf8a1bc4f90cbdfc63f97c23`  
		Last Modified: Wed, 16 Aug 2023 03:52:27 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d9dafca1013a713ff6fca9a964b8c9b56a92988935dfc370e02e1ab1693b1645
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bcd09ce9224a3e6205d4c33853d71f22d8c18f63259a4e7d8121b89ad39573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c33de8dd8d88404193f8d100efd13ecaafbc18e3391f3688ce0c41b269c813`  
		Last Modified: Wed, 16 Aug 2023 03:42:41 GMT  
		Size: 10.9 MB (10868493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690636d1fbf114a0d369abbe65be2cbc0237d8715c0e8ef4b4226c1fb32cb310`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6912fa3cbe68256fbe65f857e365c177f93957e7048c96c4ff7ad44e3350b18`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76675ef82d7692108de74c45d4c734a1277e8a1ad34a2383ba8e0cc3247c34`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 304.5 KB (304516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9df965a7d01865ff78ea9517c27a9ca66828c8a0b44728b69854d721a577c5`  
		Last Modified: Wed, 16 Aug 2023 03:42:49 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:78fa09eede785e42fa6669b1938c227e2859bfd70fcacf8cbc31b99dc92f819e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3fd6957df1609400f9344e8de9d2ed14a3ac1b047cb1a3be17e55715c905017
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcb6cbd73caade03201b228e77ba48521f114ae2675c53ef89b7b2d84cc073c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:48:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:48:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 03:48:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 03:48:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996de8d1cedbbc569fa7dfdd5fd018d3e463c2e41c043ecf211e64bc390d566c`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 5.5 MB (5494586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb39f69622ecc6a477deaca425f31a38fad22551b28285389073ee054ee63252`  
		Last Modified: Thu, 03 Aug 2023 03:48:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2edb53cbd14f656021446f9b9f351e5852b7a97993bf84a7c97f43442cadac`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1713824f3e3261919583589793966986d23d737e5214e28bdf9e783c9ef94e91`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 239.0 KB (239034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4fd89521f0dcdb0f495790500aedf47ae05dbb2e34757fd56a4c9cbe884531b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32918902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e28a184eb3c1bf9ad917c9ea6b0eb607a6a3a06d07783394bcf02da6df996`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:30:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 01:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 01:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63c5faaf7c554994559ed54ecb9f84a82adfbacb4383b8518aaa4faba59424`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 5.5 MB (5475860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3162aef2e0e6d6032786a78a889a521993ac708ba7506179b22fe53102a79`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8134c9fede462311ab098bc16b5b9b1bf50089fce796a8b35277261ce2be826`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922aea672c964eb686faf77e05d42b42976cfbd3ed8277c8e99006613a5e094`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 240.5 KB (240451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:d4e1d0ce4646fd92a60b64c42e2a4c72081d88a3133a35b654fc284b1f273166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6f30bc52211eb7670c2a6246d0c8cedc6981a050bbf0ae28246e367a7e788aeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d0779b1ff01d9dfd563a80f22a94adea9e91dfcfa6fc0d03a4c203873b27e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:48:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:48:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 03:48:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 03:48:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:48:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996de8d1cedbbc569fa7dfdd5fd018d3e463c2e41c043ecf211e64bc390d566c`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 5.5 MB (5494586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb39f69622ecc6a477deaca425f31a38fad22551b28285389073ee054ee63252`  
		Last Modified: Thu, 03 Aug 2023 03:48:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2edb53cbd14f656021446f9b9f351e5852b7a97993bf84a7c97f43442cadac`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1713824f3e3261919583589793966986d23d737e5214e28bdf9e783c9ef94e91`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 239.0 KB (239034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d0b8d19f78648bb2b61cc78769969fd8786e3d8e570b760153c2a06d490469`  
		Last Modified: Thu, 03 Aug 2023 03:49:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ab117e5aea14f21f28b8814dca5d695f0f6b4209605db72d1a226894a62837b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32919157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960367c533f54a716dcf7f5e6b4855dd5f1d24ae005ced662e079d6bd99c98c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:30:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 01:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 01:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:30:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63c5faaf7c554994559ed54ecb9f84a82adfbacb4383b8518aaa4faba59424`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 5.5 MB (5475860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3162aef2e0e6d6032786a78a889a521993ac708ba7506179b22fe53102a79`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8134c9fede462311ab098bc16b5b9b1bf50089fce796a8b35277261ce2be826`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922aea672c964eb686faf77e05d42b42976cfbd3ed8277c8e99006613a5e094`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 240.5 KB (240451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecb54b393650c5e82de82f477b5c07540f83a3a6a9021f46cc1be84cd0e1fe2`  
		Last Modified: Thu, 03 Aug 2023 01:31:45 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:5a928ba189304f359eb0dbf2c7e25b2dc4f2316e98d966f89ab0c6f91931877f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:8b4a05e18e650221a18e5144786310a304eba507b814f365481e9010ace9250e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34459391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82459abc98ed3482c86b6a5d476fa37916587ac7f18313213de9323e328cd028`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:05:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:05:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 02 Sep 2023 01:05:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 02 Sep 2023 01:05:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c6df981bf8e714c3119d4d1e33079c5a968c033963bd99451423487557e909`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 3.8 MB (3766306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed08637fe3c5e56cc458dab0b57242e504c98dc4f266bbcc2dd0b8bb08afebe7`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0a296b76bc799e69e4749412aa44af53e835b9fb8e2b4ddfff7a9d9e14081`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79990fbc25130cbe31e916a2d269c550c61608f6e33991097b73d5f6d2ab643e`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 252.1 KB (252091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:be7132784be260e212cf3adfa3dbcfad197e3b374d64199b6ad7f9437824f973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32390261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5819c0679db7f841fb420fd9ed07ea428431cc581593137c403c2fba5e753a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:50:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:50:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 01 Sep 2023 23:50:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 01 Sep 2023 23:50:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e4672cc8070664195f1b1ad06e121588c135ab993990718d524b8edc7363d`  
		Last Modified: Fri, 01 Sep 2023 23:51:22 GMT  
		Size: 3.7 MB (3740889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7466094bc82120783a482512f89f7f642266c71264b9dd14cf711668b6fca7`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa10a35bc86a246abbdf8410135721cca29a57836e09eee999e9805848e09`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ff8bc2397bd0434a4fab33cde29ae79b7c8c774cf9d5dc43a5c1b061c82933`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 254.4 KB (254388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:0c61115424db63491c0c4fe4feede362863e2c06633cedb0dcae76c4e4f8bb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d5736abdd06248482c2adfe0aa07e229e1b948717c07586c40528fc00e01a91a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34459649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec93b39a9f52def22b989488297035df452645c7043e5bd618b208fe8c054b8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:05:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:05:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 02 Sep 2023 01:05:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 02 Sep 2023 01:05:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:05:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c6df981bf8e714c3119d4d1e33079c5a968c033963bd99451423487557e909`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 3.8 MB (3766306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed08637fe3c5e56cc458dab0b57242e504c98dc4f266bbcc2dd0b8bb08afebe7`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0a296b76bc799e69e4749412aa44af53e835b9fb8e2b4ddfff7a9d9e14081`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79990fbc25130cbe31e916a2d269c550c61608f6e33991097b73d5f6d2ab643e`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 252.1 KB (252091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac2a6c1ebf8830122f752f8e25c5be5d9feb297d739e8c1637662b71580fe74`  
		Last Modified: Sat, 02 Sep 2023 01:06:37 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c818e9a42c8d30afee0055e13ec269621e7ef9cb47dbebc3dba60e4cc68f54b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32390518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617e11d1a4d7e09daaa5118de6c117eb48dd06ff4a69d8166ad7f0bfc0590cf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:50:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:50:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 01 Sep 2023 23:50:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 01 Sep 2023 23:50:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:50:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e4672cc8070664195f1b1ad06e121588c135ab993990718d524b8edc7363d`  
		Last Modified: Fri, 01 Sep 2023 23:51:22 GMT  
		Size: 3.7 MB (3740889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7466094bc82120783a482512f89f7f642266c71264b9dd14cf711668b6fca7`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa10a35bc86a246abbdf8410135721cca29a57836e09eee999e9805848e09`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ff8bc2397bd0434a4fab33cde29ae79b7c8c774cf9d5dc43a5c1b061c82933`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 254.4 KB (254388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9f183231cabed309619ffd623fd2c71eee3b3bed618d088bbefa9eacb0eae7`  
		Last Modified: Fri, 01 Sep 2023 23:51:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:2556feb52625ee39aa8b09b9e4420232b231f4b5e46c2a251e7923ca35a3c4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:b88dc1cd32373ceb3e8b6f1e29816b95c677f084126a968ae9afddd9f8ed0664
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66681560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfaf8983cbc172d7a70de973c76fbdc94ac97fa240ec66a4d59d647e09d071a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277dc632d247999fb7a6cd0bd5baec2171b343c20b37144154ee00b5f16c33c`  
		Last Modified: Wed, 16 Aug 2023 10:15:27 GMT  
		Size: 11.3 MB (11310931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d86ff81e5b660e03eeeee9621aaaa20e5f489179d72d578cdda7d70ee2c5d`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447f2ea93014e7d1c7b07289e423184f36439a89ad19283eccdc016b42cf9fe`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea88abaf68b1bb7c8399a5458e6ebe8cd32f9ac34e4b05a1832fc4930135d6ac`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 312.0 KB (311993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a97004bec5c1281f8fcb08fb6b26e6db2c5c7df3a8d26b06d111c6e6d995937f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c8b34682450722533d0edc8ce1ceb00f1cfd30e01d638633504ed9c3fa126`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f617cf8ad2e2c41398a2e69ee56490ac9f8d5c1dbd0ab7b36b10a0efa3144`  
		Last Modified: Wed, 16 Aug 2023 03:52:36 GMT  
		Size: 11.3 MB (11313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ac930639ae5b54a166c044aded05a4158b2d09535fc1db3b615f2b1de7e9a`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88e6bdea4ca56ad8afce5b3316f65de09d3e4065a741716fab48052a8f317e`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee859683358f1930f92f8c516715068cfe671ec72b49a97ef92b6d13ea709a1`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 311.9 KB (311918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:cb2e82e795b75e1888216025391b0f6889a76daf64e07f90caf70b5201802ddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da46703ed660e2ab9b62b1d5edd3e9f7e39c1a946be608bca549c6393b5efcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5750deeda7e20aa3970ce752bfae0fd6c1a830d267498576eaf6ccf81b775bef`  
		Last Modified: Wed, 16 Aug 2023 03:42:59 GMT  
		Size: 11.7 MB (11707953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55328912e9ff34ca1f686e3fd42e1daf0949cf81967f6f81902e62a18486b506`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc32ee8ff65662d5091b2e4e952394e383e9fe418d81477718c164b03ae4198`  
		Last Modified: Wed, 16 Aug 2023 03:42:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f976114f832664b48a08c50da76cf92bff2e7820d61f534a002c298b7c5b7b3`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 311.8 KB (311849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:26858837455717ccc343466334900923140e3e516132dd65fbc9e4db5c6ea17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:1abd2e1a3efc31c1d4a28c94d69ee07797e433f7e60a93119ffb9e9140672844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64168717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed6491eea8d1c1077623c4d8e1aa506e169aa01fa3bd38502677c90ad14dc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1753a4167c634c5010550a1f4f417b282f2e72009c2a83a24d3d670c294ad`  
		Last Modified: Wed, 16 Aug 2023 10:16:07 GMT  
		Size: 14.3 MB (14264309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6425f36a7f840361853d24139d567df7ebcdf25533add46ae9b71a1b58899`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffee644b7121bfa1a75452287f0ec6760aca7d2443b5b40ab08d661983c822`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d34f1a1b9fad277ce6fab6fb5714ff0e477efdacb71481b1a19571270f5c72`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 285.1 KB (285086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:246c4c73759d44ead4c3dfd373311b79df3a25a2dbe53f4c1a2213fe3808763c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63890308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578bda0b0f3ca70f20c661d6af97b9d167a5523ff67cf5fe386467ac94f3cc80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:01 GMT
ADD file:8064072457ccf7b4072e08095fa84f96b0fe3387ec8f302afde022186aa3eab5 in / 
# Tue, 15 Aug 2023 23:41:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4513653e4d749342b34f60c592adaf0ef4af993e76a913a1c086a4229a0e3afe`  
		Last Modified: Tue, 15 Aug 2023 23:45:54 GMT  
		Size: 49.5 MB (49531730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce812d7af41ad795cf945688ee3fc47de3e52c7d41f9096865b42621b207cd11`  
		Last Modified: Wed, 16 Aug 2023 03:53:14 GMT  
		Size: 14.1 MB (14070959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd452a3a5eb5d5aa0bca4af1ec0aac980e7024c2886cf99489c75ffb8812530`  
		Last Modified: Wed, 16 Aug 2023 03:53:12 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145fd67a5c34a7ec4d6b4fae9664abcb6c8022c8819ede55397b8fd285ed35cf`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32c90e7cd03d64125341b0f6c1fe0d8b720900a58bda65b7dc130b02ae1c4b`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 285.6 KB (285607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:8c02d9e2b2428d501c06b75f1b296231a48040fc4ce123472d2fad97d8ad6574
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65590266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f522dc2f4c7a47c6c5d24ec3af0d697e00ef975d898004c45c535ff685ddbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:34 GMT
ADD file:d86f66385d3993c597ac040a976cd8a826b097d014cc4f3b69d8ebfaa5aa6eff in / 
# Tue, 15 Aug 2023 23:40:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:42:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e41394c7daa90fb4aae0f67d43af5ee9838fb125e249fc0002bfdc3b90bb6c05`  
		Last Modified: Tue, 15 Aug 2023 23:46:33 GMT  
		Size: 50.6 MB (50631355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b86fa75275b3360f0cabc05723d0926928e895a32997b0045ad1a4b87c6d7a`  
		Last Modified: Wed, 16 Aug 2023 03:43:39 GMT  
		Size: 14.7 MB (14671551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31ed6d29a83b27add317575ac2bad9081baaa869afd0edad2f462982c52e652`  
		Last Modified: Wed, 16 Aug 2023 03:43:36 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94acc54b4e308d89fb245806d56517510569b98017639228cbf03c46350a9a2a`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda7bfdd1b15918713a3b6dec980d78af341813470a5ae7d6b3fb016ea4410e`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 285.4 KB (285352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:4568eb3c4efa41029b9b23a9d9e0d7556d84ad92ccbf959ad157e314465f4d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b771ee3290efa1a6c265af138725a8950240a5a9719d1dcaa90107df4c9a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64169110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad7b8bc81b61754cc3c0c2924d41f86ea94e73418d0115e3bfc254be913040`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1753a4167c634c5010550a1f4f417b282f2e72009c2a83a24d3d670c294ad`  
		Last Modified: Wed, 16 Aug 2023 10:16:07 GMT  
		Size: 14.3 MB (14264309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6425f36a7f840361853d24139d567df7ebcdf25533add46ae9b71a1b58899`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffee644b7121bfa1a75452287f0ec6760aca7d2443b5b40ab08d661983c822`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d34f1a1b9fad277ce6fab6fb5714ff0e477efdacb71481b1a19571270f5c72`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 285.1 KB (285086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83e062af1b4b3ed0bbe171920540cba07de2a176984b2dd9c1b9896a8146bf`  
		Last Modified: Wed, 16 Aug 2023 10:16:16 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82d15489b6aee0b568dd46d4e5b0cb7ddac18eac77d323eb4119da8bb7c948e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63890703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5546961801efcaa72e4d88940f4ffb803f8739ca577c52b16045bf536cb61`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:01 GMT
ADD file:8064072457ccf7b4072e08095fa84f96b0fe3387ec8f302afde022186aa3eab5 in / 
# Tue, 15 Aug 2023 23:41:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4513653e4d749342b34f60c592adaf0ef4af993e76a913a1c086a4229a0e3afe`  
		Last Modified: Tue, 15 Aug 2023 23:45:54 GMT  
		Size: 49.5 MB (49531730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce812d7af41ad795cf945688ee3fc47de3e52c7d41f9096865b42621b207cd11`  
		Last Modified: Wed, 16 Aug 2023 03:53:14 GMT  
		Size: 14.1 MB (14070959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd452a3a5eb5d5aa0bca4af1ec0aac980e7024c2886cf99489c75ffb8812530`  
		Last Modified: Wed, 16 Aug 2023 03:53:12 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145fd67a5c34a7ec4d6b4fae9664abcb6c8022c8819ede55397b8fd285ed35cf`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32c90e7cd03d64125341b0f6c1fe0d8b720900a58bda65b7dc130b02ae1c4b`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 285.6 KB (285607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c944cd14cc6be34b10a12d49005ad43d5b49a84f08569b3f28e0cad958ec6fe`  
		Last Modified: Wed, 16 Aug 2023 03:53:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:81e4bc1dbf529ee19748f7a61381d73524921abfa86227b39e29b8644cad239d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65590666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74f18d42edd9c73b33bfb5f14d0bc6a7959b339e05f785c52da1338719aa94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:34 GMT
ADD file:d86f66385d3993c597ac040a976cd8a826b097d014cc4f3b69d8ebfaa5aa6eff in / 
# Tue, 15 Aug 2023 23:40:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:42:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e41394c7daa90fb4aae0f67d43af5ee9838fb125e249fc0002bfdc3b90bb6c05`  
		Last Modified: Tue, 15 Aug 2023 23:46:33 GMT  
		Size: 50.6 MB (50631355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b86fa75275b3360f0cabc05723d0926928e895a32997b0045ad1a4b87c6d7a`  
		Last Modified: Wed, 16 Aug 2023 03:43:39 GMT  
		Size: 14.7 MB (14671551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31ed6d29a83b27add317575ac2bad9081baaa869afd0edad2f462982c52e652`  
		Last Modified: Wed, 16 Aug 2023 03:43:36 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94acc54b4e308d89fb245806d56517510569b98017639228cbf03c46350a9a2a`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda7bfdd1b15918713a3b6dec980d78af341813470a5ae7d6b3fb016ea4410e`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 285.4 KB (285352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512567c2c7d4e968f00b68682cfea6da66ea4783d9da51af2905c8173196709`  
		Last Modified: Wed, 16 Aug 2023 03:43:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:8da30a13d55f682cb7b5abcb1ba4ec1948a418aa379db648ccb706ee46032350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:0da68b4aca50e778ac715c49714c6bba2209cfc37cdb1444b03fb7fa7558b3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea452dff405f01f746e680cb1dc3b4c1457238a9405245d4c2d0774760300ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:19 GMT
ADD file:30ed10904e3533aa50c332544532891f0dcf06cce020988e07af9afa6b2f5df4 in / 
# Wed, 16 Aug 2023 01:00:20 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6b7393fb4f375905c31c483d81ce2a2905f88aba8cb198874da2b54035bc41d`  
		Last Modified: Wed, 16 Aug 2023 01:05:31 GMT  
		Size: 50.5 MB (50498099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d786e39fbdde08da5ac21348797106a8e48f83ec4f16eb988bae3d24b3d1f`  
		Last Modified: Wed, 16 Aug 2023 10:15:09 GMT  
		Size: 10.5 MB (10504726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067e4a986b67fcae5368b79e01f6f2bfa8c41b745cb020fcb702b8dec9ce0a8c`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b10d61fb6b2b77af47566a04fb2f10162c788281459e74630ceeb4b713c2a`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e9b94a4b05fa98315a44b00a103167cea1a667dccf6483a4eb9f6201bac3b`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 304.6 KB (304619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5c066f0b95d700c7c3bbb02258c68faf30f73bd15cbcb5c5faffeb0222bb1468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17ce73f54623eae40a7273f88ce32130e6ee13f6b8397d25ffef4cf59444673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:50:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:50:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff548e71e5e2b2825cca5159e38ac0f04f9ea241d05e88b8df6c827bcc66890e`  
		Last Modified: Wed, 16 Aug 2023 03:52:19 GMT  
		Size: 10.5 MB (10510675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd3c3a2153366ee917527815d07c3d6084923d4377d36a0fb26dde691b7b20`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dfdfdf86764a28629c52c3bcdfdad862c754d940385bbb1f38e6f03b18d8f3`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a825c8e8bc1a402e4fe8ab17fe0f155a3a9025417cb24bf4d2a2637170e57`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 304.5 KB (304542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:62ca31b62277e996a6e5bc4002e25e2d0e4341dd8e20e7341d0209219f7f4ec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff2c883e44081a3fcbf67700e217756905f3b28e33ba79d31601bbd3e9cbf14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c33de8dd8d88404193f8d100efd13ecaafbc18e3391f3688ce0c41b269c813`  
		Last Modified: Wed, 16 Aug 2023 03:42:41 GMT  
		Size: 10.9 MB (10868493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690636d1fbf114a0d369abbe65be2cbc0237d8715c0e8ef4b4226c1fb32cb310`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6912fa3cbe68256fbe65f857e365c177f93957e7048c96c4ff7ad44e3350b18`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76675ef82d7692108de74c45d4c734a1277e8a1ad34a2383ba8e0cc3247c34`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 304.5 KB (304516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:bc20e10a5af1bc7ca8e59d8b30f28268d6d29323ee7590649b3a27c27245d829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:93f8d0afac93b903b63fa9359774326e1a25be96eb932e6b0f630d1247528fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5382eed41a72f0ff3b74550ad076459631f1d6d308c29f7b51c91db65318e484`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:19 GMT
ADD file:30ed10904e3533aa50c332544532891f0dcf06cce020988e07af9afa6b2f5df4 in / 
# Wed, 16 Aug 2023 01:00:20 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d6b7393fb4f375905c31c483d81ce2a2905f88aba8cb198874da2b54035bc41d`  
		Last Modified: Wed, 16 Aug 2023 01:05:31 GMT  
		Size: 50.5 MB (50498099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d786e39fbdde08da5ac21348797106a8e48f83ec4f16eb988bae3d24b3d1f`  
		Last Modified: Wed, 16 Aug 2023 10:15:09 GMT  
		Size: 10.5 MB (10504726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067e4a986b67fcae5368b79e01f6f2bfa8c41b745cb020fcb702b8dec9ce0a8c`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b10d61fb6b2b77af47566a04fb2f10162c788281459e74630ceeb4b713c2a`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e9b94a4b05fa98315a44b00a103167cea1a667dccf6483a4eb9f6201bac3b`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 304.6 KB (304619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffc707d6bc130465732198e61ac65ec3f1b7d04c28b3bf6d86a3286ca18869`  
		Last Modified: Wed, 16 Aug 2023 10:15:17 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:88f4b1a84b6f01382b277f7d3bf39f72a8b94b2548b554238fc77253f3ceb7b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7543797664e4133d57ddbb8a7a093b86e7323dfaa8a15c3327ab452d1a7db5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:50:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:50:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff548e71e5e2b2825cca5159e38ac0f04f9ea241d05e88b8df6c827bcc66890e`  
		Last Modified: Wed, 16 Aug 2023 03:52:19 GMT  
		Size: 10.5 MB (10510675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd3c3a2153366ee917527815d07c3d6084923d4377d36a0fb26dde691b7b20`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dfdfdf86764a28629c52c3bcdfdad862c754d940385bbb1f38e6f03b18d8f3`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a825c8e8bc1a402e4fe8ab17fe0f155a3a9025417cb24bf4d2a2637170e57`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 304.5 KB (304542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96918ab91a1c0ba75a677c85f091ac5a0d073d76bf8a1bc4f90cbdfc63f97c23`  
		Last Modified: Wed, 16 Aug 2023 03:52:27 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d9dafca1013a713ff6fca9a964b8c9b56a92988935dfc370e02e1ab1693b1645
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bcd09ce9224a3e6205d4c33853d71f22d8c18f63259a4e7d8121b89ad39573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c33de8dd8d88404193f8d100efd13ecaafbc18e3391f3688ce0c41b269c813`  
		Last Modified: Wed, 16 Aug 2023 03:42:41 GMT  
		Size: 10.9 MB (10868493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690636d1fbf114a0d369abbe65be2cbc0237d8715c0e8ef4b4226c1fb32cb310`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6912fa3cbe68256fbe65f857e365c177f93957e7048c96c4ff7ad44e3350b18`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76675ef82d7692108de74c45d4c734a1277e8a1ad34a2383ba8e0cc3247c34`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 304.5 KB (304516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9df965a7d01865ff78ea9517c27a9ca66828c8a0b44728b69854d721a577c5`  
		Last Modified: Wed, 16 Aug 2023 03:42:49 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:2556feb52625ee39aa8b09b9e4420232b231f4b5e46c2a251e7923ca35a3c4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:b88dc1cd32373ceb3e8b6f1e29816b95c677f084126a968ae9afddd9f8ed0664
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66681560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfaf8983cbc172d7a70de973c76fbdc94ac97fa240ec66a4d59d647e09d071a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277dc632d247999fb7a6cd0bd5baec2171b343c20b37144154ee00b5f16c33c`  
		Last Modified: Wed, 16 Aug 2023 10:15:27 GMT  
		Size: 11.3 MB (11310931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d86ff81e5b660e03eeeee9621aaaa20e5f489179d72d578cdda7d70ee2c5d`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447f2ea93014e7d1c7b07289e423184f36439a89ad19283eccdc016b42cf9fe`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea88abaf68b1bb7c8399a5458e6ebe8cd32f9ac34e4b05a1832fc4930135d6ac`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 312.0 KB (311993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a97004bec5c1281f8fcb08fb6b26e6db2c5c7df3a8d26b06d111c6e6d995937f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c8b34682450722533d0edc8ce1ceb00f1cfd30e01d638633504ed9c3fa126`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f617cf8ad2e2c41398a2e69ee56490ac9f8d5c1dbd0ab7b36b10a0efa3144`  
		Last Modified: Wed, 16 Aug 2023 03:52:36 GMT  
		Size: 11.3 MB (11313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ac930639ae5b54a166c044aded05a4158b2d09535fc1db3b615f2b1de7e9a`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88e6bdea4ca56ad8afce5b3316f65de09d3e4065a741716fab48052a8f317e`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee859683358f1930f92f8c516715068cfe671ec72b49a97ef92b6d13ea709a1`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 311.9 KB (311918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:cb2e82e795b75e1888216025391b0f6889a76daf64e07f90caf70b5201802ddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da46703ed660e2ab9b62b1d5edd3e9f7e39c1a946be608bca549c6393b5efcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5750deeda7e20aa3970ce752bfae0fd6c1a830d267498576eaf6ccf81b775bef`  
		Last Modified: Wed, 16 Aug 2023 03:42:59 GMT  
		Size: 11.7 MB (11707953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55328912e9ff34ca1f686e3fd42e1daf0949cf81967f6f81902e62a18486b506`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc32ee8ff65662d5091b2e4e952394e383e9fe418d81477718c164b03ae4198`  
		Last Modified: Wed, 16 Aug 2023 03:42:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f976114f832664b48a08c50da76cf92bff2e7820d61f534a002c298b7c5b7b3`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 311.8 KB (311849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:741af06694a1c55f2da8b4abab79e407527a0e4d2c4517e9dcae27b02c6d8d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6b4fa7b4b9fefa395a00e816d280df65e27ee7b431f2e725849cb8b4038875fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66681919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7147d37d98a4b3ae2e7db97d368c8e94816f766a5d3e788041cb4066dff406c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277dc632d247999fb7a6cd0bd5baec2171b343c20b37144154ee00b5f16c33c`  
		Last Modified: Wed, 16 Aug 2023 10:15:27 GMT  
		Size: 11.3 MB (11310931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d86ff81e5b660e03eeeee9621aaaa20e5f489179d72d578cdda7d70ee2c5d`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447f2ea93014e7d1c7b07289e423184f36439a89ad19283eccdc016b42cf9fe`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea88abaf68b1bb7c8399a5458e6ebe8cd32f9ac34e4b05a1832fc4930135d6ac`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 312.0 KB (311993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80aaa9ab5b22adbd516f80deac4bd772aeaf624108aa2939fcdf90c8d812f8`  
		Last Modified: Wed, 16 Aug 2023 10:15:38 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1c1f04b90f03ee0e3630f0e38ed6b61157285c4dc89d73719fd52ccb0634a2d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2b570139c1bae4983d5f7477cfca3bb1df62880b79682017a23b16ebc0929a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f617cf8ad2e2c41398a2e69ee56490ac9f8d5c1dbd0ab7b36b10a0efa3144`  
		Last Modified: Wed, 16 Aug 2023 03:52:36 GMT  
		Size: 11.3 MB (11313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ac930639ae5b54a166c044aded05a4158b2d09535fc1db3b615f2b1de7e9a`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88e6bdea4ca56ad8afce5b3316f65de09d3e4065a741716fab48052a8f317e`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee859683358f1930f92f8c516715068cfe671ec72b49a97ef92b6d13ea709a1`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 311.9 KB (311918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803acde4b75dbb93b203e9432ccc3755a95eaca94114e6ecc54fc98e921b2a6`  
		Last Modified: Wed, 16 Aug 2023 03:52:46 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3bdd99a51d92fecffae8ab6c9199e8c39f7e10a059050d0c7c7bd9528e2dbb88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07866f611e3e3217fa93a66044867c874391cbc9bf56019524b580601674b67a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5750deeda7e20aa3970ce752bfae0fd6c1a830d267498576eaf6ccf81b775bef`  
		Last Modified: Wed, 16 Aug 2023 03:42:59 GMT  
		Size: 11.7 MB (11707953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55328912e9ff34ca1f686e3fd42e1daf0949cf81967f6f81902e62a18486b506`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc32ee8ff65662d5091b2e4e952394e383e9fe418d81477718c164b03ae4198`  
		Last Modified: Wed, 16 Aug 2023 03:42:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f976114f832664b48a08c50da76cf92bff2e7820d61f534a002c298b7c5b7b3`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 311.8 KB (311849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3e8b052baa4381b554e9dbc07893559e3acdaab1f7b9bbb525937b3b1a47d`  
		Last Modified: Wed, 16 Aug 2023 03:43:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:0d130609fbb2188edc7ee683677321dd930d20c9f45d9ae659e0d8f0883c81ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:21894431e3a16dc7f171d76066a7122a135676a9b505e1816e10b550c4139951
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61308980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6172b4009d06e533acd67e84f4542e78aae2f19fad619f3ac124985e2b6f68fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:30 GMT
ADD file:3a6d159d80cb8abfacda5873c243a6ae635ff603708febc4df51f8eec26d3de7 in / 
# Wed, 16 Aug 2023 00:59:31 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de4cac68b6165c40cf6f8b30417948c31be03a968e233e55ee40221553a5e570`  
		Last Modified: Wed, 16 Aug 2023 01:04:06 GMT  
		Size: 49.6 MB (49557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d6403b214041d209839a70f25dbd8a74ca35b340cd505a7beab4a170cca7f5`  
		Last Modified: Wed, 16 Aug 2023 10:15:49 GMT  
		Size: 11.5 MB (11463261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98032d4a249856d7aabaa3af9134cd443eeee95627f4b4826f18d3dfd3dc4331`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871fc39cb100ac4f417725f892c0e7d1fe64fd283c71f47da0babe29d87271f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b37d2551f1ac4bf700870ba04cc161179be2c0f688406c9dbe1d6cf58cd24f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7058e215cde4c1022622e829cb6e4e526d3738afd710b707481395e7c12fce25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b38f7ddb07b4861aa264cce463468a311f6727d5b67388b3bce2b990ba30a5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2702582abd923413cfef5d91b723dd4d2a9fa9c89a6e68e42fa66876db7f4`  
		Last Modified: Wed, 16 Aug 2023 03:52:57 GMT  
		Size: 11.4 MB (11426893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a3cbd38cab59e99577e9251a79dd45edcbd8cd11619d83a9ca0b2ef51eee8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd89b2b4d95679b6e5bbe98ee70a0ffea9d1e8884e0fc4f90e9fd57a6b3465d8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d717c54d750af9ef25aea7e73cbecf3d063ba7e3ba6c9e05fceafc40f519cd8f`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 286.6 KB (286586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:01332eb612c9330b3a3c3dc2dbe5d3aca14928caeef3e6b07858395da9469f27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62739862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2184b9c8fc56b5e43afc8a24637c675b5f63fccf9e2243ccc39946b305bbf8dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:38:49 GMT
ADD file:3f0a4d6b18b22088d0785bc2e351d829ad1ed6f154058017035842bdbe2a8d1e in / 
# Tue, 15 Aug 2023 23:38:51 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dc6cc826af02d533745c4612f635e028f3471e46f50422fd20a6dc913b60574`  
		Last Modified: Tue, 15 Aug 2023 23:43:02 GMT  
		Size: 50.6 MB (50568054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646efa09d31a3e9a9508a47906e753a78732c68c3d19f31a5f2e7c01492dae9`  
		Last Modified: Wed, 16 Aug 2023 03:43:21 GMT  
		Size: 11.9 MB (11883338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4995daa45aaed4dd28725edeca185c0aa766cfb40924d40620cf18f750436eb3`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee4413c37e9b5ccb7f7a6083b10b9405a8597b97a4d0b633e59f3c8e20ca22`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e05db3d06057f7b8dc58d17ceeb8083288c9bb6af96b2195da0956e89022b`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 286.5 KB (286453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:6ec9fb7baaac405ef37bb93de693eda1cbd8c72332c5fb0150783f2b8a3c42c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2d3b719f4ae2a0197538c37d7ce91900fd5c99c816b356f209e863500f6d8f82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae7c41266f3afec454933bceaf2ab670697ef86c81b79e42883defee230e2bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:30 GMT
ADD file:3a6d159d80cb8abfacda5873c243a6ae635ff603708febc4df51f8eec26d3de7 in / 
# Wed, 16 Aug 2023 00:59:31 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:de4cac68b6165c40cf6f8b30417948c31be03a968e233e55ee40221553a5e570`  
		Last Modified: Wed, 16 Aug 2023 01:04:06 GMT  
		Size: 49.6 MB (49557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d6403b214041d209839a70f25dbd8a74ca35b340cd505a7beab4a170cca7f5`  
		Last Modified: Wed, 16 Aug 2023 10:15:49 GMT  
		Size: 11.5 MB (11463261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98032d4a249856d7aabaa3af9134cd443eeee95627f4b4826f18d3dfd3dc4331`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871fc39cb100ac4f417725f892c0e7d1fe64fd283c71f47da0babe29d87271f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b37d2551f1ac4bf700870ba04cc161179be2c0f688406c9dbe1d6cf58cd24f`  
		Last Modified: Wed, 16 Aug 2023 10:15:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24ad0c9c7a55acb043200edd44eb47f0b650a545a0fb69f6f7fe9a081a52ee`  
		Last Modified: Wed, 16 Aug 2023 10:15:57 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:974160c65245412290cbf8d1b12115acc678d7dcb6a63096e384ed6100818161
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61307231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e451defa12b04fc9f56455eb9346a4ce0260a78a1e7f3aaffb312a09aaebc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2702582abd923413cfef5d91b723dd4d2a9fa9c89a6e68e42fa66876db7f4`  
		Last Modified: Wed, 16 Aug 2023 03:52:57 GMT  
		Size: 11.4 MB (11426893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a3cbd38cab59e99577e9251a79dd45edcbd8cd11619d83a9ca0b2ef51eee8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd89b2b4d95679b6e5bbe98ee70a0ffea9d1e8884e0fc4f90e9fd57a6b3465d8`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d717c54d750af9ef25aea7e73cbecf3d063ba7e3ba6c9e05fceafc40f519cd8f`  
		Last Modified: Wed, 16 Aug 2023 03:52:56 GMT  
		Size: 286.6 KB (286586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ac2213dbcf824403a3cbfe97c9c9a16d189471fcd448f71e496940768214d2`  
		Last Modified: Wed, 16 Aug 2023 03:53:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c4af6957f74e19b0093bbb86c0180a4088e66fb3fcda0dc11ea6069983a24ba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856eaaeb40cd76eb168df229d318ec8dbe29c8d82a0e95c8be449ce04610390e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:38:49 GMT
ADD file:3f0a4d6b18b22088d0785bc2e351d829ad1ed6f154058017035842bdbe2a8d1e in / 
# Tue, 15 Aug 2023 23:38:51 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1dc6cc826af02d533745c4612f635e028f3471e46f50422fd20a6dc913b60574`  
		Last Modified: Tue, 15 Aug 2023 23:43:02 GMT  
		Size: 50.6 MB (50568054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646efa09d31a3e9a9508a47906e753a78732c68c3d19f31a5f2e7c01492dae9`  
		Last Modified: Wed, 16 Aug 2023 03:43:21 GMT  
		Size: 11.9 MB (11883338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4995daa45aaed4dd28725edeca185c0aa766cfb40924d40620cf18f750436eb3`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee4413c37e9b5ccb7f7a6083b10b9405a8597b97a4d0b633e59f3c8e20ca22`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e05db3d06057f7b8dc58d17ceeb8083288c9bb6af96b2195da0956e89022b`  
		Last Modified: Wed, 16 Aug 2023 03:43:19 GMT  
		Size: 286.5 KB (286453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05abbd3aff72718cfe7c0f7690be327e1ea516e52d433760875df5973c7f033`  
		Last Modified: Wed, 16 Aug 2023 03:43:28 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:0dc0c6379aa9de4c7beb314a77836296ed1b9ecec52b6e370d7d1d8fb37e8c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:436d0f91b2596d1a67587f416d172e20ea63d2ba9fab4064134e658283be40b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54202678ffa323cabbfa7d9142d688755ff6767f3a44607c1eb821edd05ac91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:be402681584b912cb441771e9a7e1b039e2da347fe7ebf2d1cd9f3736c2e5b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364f14a0ddb6cdd1d2222f8d8d1cd397a7334c3eb47c91b89028ee7a7e491380`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:c6e4772e5c601ede7ccf289927f339f34eab81e04942d3e803f285f931926a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:137b909d0e4c4e1c4300fa4479a22b15c053df24cbbef0f13fce395100eafa77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226a853426c1d4b6bd2f86d099a28d4c4db35b9d83d9a7021c549f5386248a11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e158a3949abb4a78460b0321777ca278a50c79ac290966e5d6a7f027b04e3dd`  
		Last Modified: Fri, 02 Jun 2023 01:35:57 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edc6bddeb118195088c3f1948fdc52cc913d453e5f543927c7c89c015fe7bd6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d966d5bec6e766760870e6f4674ca17b3fe69617f78ade07c2a7b6b3154ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:46:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350adb1f8b3dcaa1835899b2dc84ec2f5a997c31b87aa8e76470a92bc742bc7f`  
		Last Modified: Thu, 01 Jun 2023 23:46:55 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:78fa09eede785e42fa6669b1938c227e2859bfd70fcacf8cbc31b99dc92f819e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3fd6957df1609400f9344e8de9d2ed14a3ac1b047cb1a3be17e55715c905017
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcb6cbd73caade03201b228e77ba48521f114ae2675c53ef89b7b2d84cc073c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:48:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:48:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 03:48:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 03:48:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996de8d1cedbbc569fa7dfdd5fd018d3e463c2e41c043ecf211e64bc390d566c`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 5.5 MB (5494586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb39f69622ecc6a477deaca425f31a38fad22551b28285389073ee054ee63252`  
		Last Modified: Thu, 03 Aug 2023 03:48:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2edb53cbd14f656021446f9b9f351e5852b7a97993bf84a7c97f43442cadac`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1713824f3e3261919583589793966986d23d737e5214e28bdf9e783c9ef94e91`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 239.0 KB (239034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4fd89521f0dcdb0f495790500aedf47ae05dbb2e34757fd56a4c9cbe884531b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32918902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e28a184eb3c1bf9ad917c9ea6b0eb607a6a3a06d07783394bcf02da6df996`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:30:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 01:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 01:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63c5faaf7c554994559ed54ecb9f84a82adfbacb4383b8518aaa4faba59424`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 5.5 MB (5475860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3162aef2e0e6d6032786a78a889a521993ac708ba7506179b22fe53102a79`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8134c9fede462311ab098bc16b5b9b1bf50089fce796a8b35277261ce2be826`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922aea672c964eb686faf77e05d42b42976cfbd3ed8277c8e99006613a5e094`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 240.5 KB (240451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:d4e1d0ce4646fd92a60b64c42e2a4c72081d88a3133a35b654fc284b1f273166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6f30bc52211eb7670c2a6246d0c8cedc6981a050bbf0ae28246e367a7e788aeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d0779b1ff01d9dfd563a80f22a94adea9e91dfcfa6fc0d03a4c203873b27e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:48:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:48:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 03:48:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 03:48:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:48:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996de8d1cedbbc569fa7dfdd5fd018d3e463c2e41c043ecf211e64bc390d566c`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 5.5 MB (5494586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb39f69622ecc6a477deaca425f31a38fad22551b28285389073ee054ee63252`  
		Last Modified: Thu, 03 Aug 2023 03:48:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2edb53cbd14f656021446f9b9f351e5852b7a97993bf84a7c97f43442cadac`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1713824f3e3261919583589793966986d23d737e5214e28bdf9e783c9ef94e91`  
		Last Modified: Thu, 03 Aug 2023 03:48:57 GMT  
		Size: 239.0 KB (239034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d0b8d19f78648bb2b61cc78769969fd8786e3d8e570b760153c2a06d490469`  
		Last Modified: Thu, 03 Aug 2023 03:49:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ab117e5aea14f21f28b8814dca5d695f0f6b4209605db72d1a226894a62837b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32919157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960367c533f54a716dcf7f5e6b4855dd5f1d24ae005ced662e079d6bd99c98c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:30:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 03 Aug 2023 01:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 03 Aug 2023 01:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:30:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63c5faaf7c554994559ed54ecb9f84a82adfbacb4383b8518aaa4faba59424`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 5.5 MB (5475860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3162aef2e0e6d6032786a78a889a521993ac708ba7506179b22fe53102a79`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8134c9fede462311ab098bc16b5b9b1bf50089fce796a8b35277261ce2be826`  
		Last Modified: Thu, 03 Aug 2023 01:31:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922aea672c964eb686faf77e05d42b42976cfbd3ed8277c8e99006613a5e094`  
		Last Modified: Thu, 03 Aug 2023 01:31:37 GMT  
		Size: 240.5 KB (240451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecb54b393650c5e82de82f477b5c07540f83a3a6a9021f46cc1be84cd0e1fe2`  
		Last Modified: Thu, 03 Aug 2023 01:31:45 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:5a928ba189304f359eb0dbf2c7e25b2dc4f2316e98d966f89ab0c6f91931877f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:8b4a05e18e650221a18e5144786310a304eba507b814f365481e9010ace9250e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34459391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82459abc98ed3482c86b6a5d476fa37916587ac7f18313213de9323e328cd028`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:05:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:05:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 02 Sep 2023 01:05:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 02 Sep 2023 01:05:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c6df981bf8e714c3119d4d1e33079c5a968c033963bd99451423487557e909`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 3.8 MB (3766306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed08637fe3c5e56cc458dab0b57242e504c98dc4f266bbcc2dd0b8bb08afebe7`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0a296b76bc799e69e4749412aa44af53e835b9fb8e2b4ddfff7a9d9e14081`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79990fbc25130cbe31e916a2d269c550c61608f6e33991097b73d5f6d2ab643e`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 252.1 KB (252091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:be7132784be260e212cf3adfa3dbcfad197e3b374d64199b6ad7f9437824f973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32390261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5819c0679db7f841fb420fd9ed07ea428431cc581593137c403c2fba5e753a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:50:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:50:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 01 Sep 2023 23:50:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 01 Sep 2023 23:50:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e4672cc8070664195f1b1ad06e121588c135ab993990718d524b8edc7363d`  
		Last Modified: Fri, 01 Sep 2023 23:51:22 GMT  
		Size: 3.7 MB (3740889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7466094bc82120783a482512f89f7f642266c71264b9dd14cf711668b6fca7`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa10a35bc86a246abbdf8410135721cca29a57836e09eee999e9805848e09`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ff8bc2397bd0434a4fab33cde29ae79b7c8c774cf9d5dc43a5c1b061c82933`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 254.4 KB (254388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:0c61115424db63491c0c4fe4feede362863e2c06633cedb0dcae76c4e4f8bb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d5736abdd06248482c2adfe0aa07e229e1b948717c07586c40528fc00e01a91a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34459649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec93b39a9f52def22b989488297035df452645c7043e5bd618b208fe8c054b8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:05:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:05:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 02 Sep 2023 01:05:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 02 Sep 2023 01:05:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:05:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c6df981bf8e714c3119d4d1e33079c5a968c033963bd99451423487557e909`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 3.8 MB (3766306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed08637fe3c5e56cc458dab0b57242e504c98dc4f266bbcc2dd0b8bb08afebe7`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0a296b76bc799e69e4749412aa44af53e835b9fb8e2b4ddfff7a9d9e14081`  
		Last Modified: Sat, 02 Sep 2023 01:06:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79990fbc25130cbe31e916a2d269c550c61608f6e33991097b73d5f6d2ab643e`  
		Last Modified: Sat, 02 Sep 2023 01:06:29 GMT  
		Size: 252.1 KB (252091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac2a6c1ebf8830122f752f8e25c5be5d9feb297d739e8c1637662b71580fe74`  
		Last Modified: Sat, 02 Sep 2023 01:06:37 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c818e9a42c8d30afee0055e13ec269621e7ef9cb47dbebc3dba60e4cc68f54b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32390518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617e11d1a4d7e09daaa5118de6c117eb48dd06ff4a69d8166ad7f0bfc0590cf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:50:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:50:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 01 Sep 2023 23:50:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 01 Sep 2023 23:50:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:50:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e4672cc8070664195f1b1ad06e121588c135ab993990718d524b8edc7363d`  
		Last Modified: Fri, 01 Sep 2023 23:51:22 GMT  
		Size: 3.7 MB (3740889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7466094bc82120783a482512f89f7f642266c71264b9dd14cf711668b6fca7`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa10a35bc86a246abbdf8410135721cca29a57836e09eee999e9805848e09`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ff8bc2397bd0434a4fab33cde29ae79b7c8c774cf9d5dc43a5c1b061c82933`  
		Last Modified: Fri, 01 Sep 2023 23:51:21 GMT  
		Size: 254.4 KB (254388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9f183231cabed309619ffd623fd2c71eee3b3bed618d088bbefa9eacb0eae7`  
		Last Modified: Fri, 01 Sep 2023 23:51:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:741af06694a1c55f2da8b4abab79e407527a0e4d2c4517e9dcae27b02c6d8d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6b4fa7b4b9fefa395a00e816d280df65e27ee7b431f2e725849cb8b4038875fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66681919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7147d37d98a4b3ae2e7db97d368c8e94816f766a5d3e788041cb4066dff406c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277dc632d247999fb7a6cd0bd5baec2171b343c20b37144154ee00b5f16c33c`  
		Last Modified: Wed, 16 Aug 2023 10:15:27 GMT  
		Size: 11.3 MB (11310931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d86ff81e5b660e03eeeee9621aaaa20e5f489179d72d578cdda7d70ee2c5d`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447f2ea93014e7d1c7b07289e423184f36439a89ad19283eccdc016b42cf9fe`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea88abaf68b1bb7c8399a5458e6ebe8cd32f9ac34e4b05a1832fc4930135d6ac`  
		Last Modified: Wed, 16 Aug 2023 10:15:26 GMT  
		Size: 312.0 KB (311993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80aaa9ab5b22adbd516f80deac4bd772aeaf624108aa2939fcdf90c8d812f8`  
		Last Modified: Wed, 16 Aug 2023 10:15:38 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1c1f04b90f03ee0e3630f0e38ed6b61157285c4dc89d73719fd52ccb0634a2d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2b570139c1bae4983d5f7477cfca3bb1df62880b79682017a23b16ebc0929a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f617cf8ad2e2c41398a2e69ee56490ac9f8d5c1dbd0ab7b36b10a0efa3144`  
		Last Modified: Wed, 16 Aug 2023 03:52:36 GMT  
		Size: 11.3 MB (11313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ac930639ae5b54a166c044aded05a4158b2d09535fc1db3b615f2b1de7e9a`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88e6bdea4ca56ad8afce5b3316f65de09d3e4065a741716fab48052a8f317e`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee859683358f1930f92f8c516715068cfe671ec72b49a97ef92b6d13ea709a1`  
		Last Modified: Wed, 16 Aug 2023 03:52:35 GMT  
		Size: 311.9 KB (311918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803acde4b75dbb93b203e9432ccc3755a95eaca94114e6ecc54fc98e921b2a6`  
		Last Modified: Wed, 16 Aug 2023 03:52:46 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3bdd99a51d92fecffae8ab6c9199e8c39f7e10a059050d0c7c7bd9528e2dbb88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07866f611e3e3217fa93a66044867c874391cbc9bf56019524b580601674b67a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5750deeda7e20aa3970ce752bfae0fd6c1a830d267498576eaf6ccf81b775bef`  
		Last Modified: Wed, 16 Aug 2023 03:42:59 GMT  
		Size: 11.7 MB (11707953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55328912e9ff34ca1f686e3fd42e1daf0949cf81967f6f81902e62a18486b506`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc32ee8ff65662d5091b2e4e952394e383e9fe418d81477718c164b03ae4198`  
		Last Modified: Wed, 16 Aug 2023 03:42:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f976114f832664b48a08c50da76cf92bff2e7820d61f534a002c298b7c5b7b3`  
		Last Modified: Wed, 16 Aug 2023 03:42:58 GMT  
		Size: 311.8 KB (311849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3e8b052baa4381b554e9dbc07893559e3acdaab1f7b9bbb525937b3b1a47d`  
		Last Modified: Wed, 16 Aug 2023 03:43:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:26858837455717ccc343466334900923140e3e516132dd65fbc9e4db5c6ea17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:1abd2e1a3efc31c1d4a28c94d69ee07797e433f7e60a93119ffb9e9140672844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64168717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed6491eea8d1c1077623c4d8e1aa506e169aa01fa3bd38502677c90ad14dc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1753a4167c634c5010550a1f4f417b282f2e72009c2a83a24d3d670c294ad`  
		Last Modified: Wed, 16 Aug 2023 10:16:07 GMT  
		Size: 14.3 MB (14264309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6425f36a7f840361853d24139d567df7ebcdf25533add46ae9b71a1b58899`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffee644b7121bfa1a75452287f0ec6760aca7d2443b5b40ab08d661983c822`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d34f1a1b9fad277ce6fab6fb5714ff0e477efdacb71481b1a19571270f5c72`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 285.1 KB (285086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:246c4c73759d44ead4c3dfd373311b79df3a25a2dbe53f4c1a2213fe3808763c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63890308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578bda0b0f3ca70f20c661d6af97b9d167a5523ff67cf5fe386467ac94f3cc80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:01 GMT
ADD file:8064072457ccf7b4072e08095fa84f96b0fe3387ec8f302afde022186aa3eab5 in / 
# Tue, 15 Aug 2023 23:41:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4513653e4d749342b34f60c592adaf0ef4af993e76a913a1c086a4229a0e3afe`  
		Last Modified: Tue, 15 Aug 2023 23:45:54 GMT  
		Size: 49.5 MB (49531730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce812d7af41ad795cf945688ee3fc47de3e52c7d41f9096865b42621b207cd11`  
		Last Modified: Wed, 16 Aug 2023 03:53:14 GMT  
		Size: 14.1 MB (14070959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd452a3a5eb5d5aa0bca4af1ec0aac980e7024c2886cf99489c75ffb8812530`  
		Last Modified: Wed, 16 Aug 2023 03:53:12 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145fd67a5c34a7ec4d6b4fae9664abcb6c8022c8819ede55397b8fd285ed35cf`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32c90e7cd03d64125341b0f6c1fe0d8b720900a58bda65b7dc130b02ae1c4b`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 285.6 KB (285607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8c02d9e2b2428d501c06b75f1b296231a48040fc4ce123472d2fad97d8ad6574
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65590266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f522dc2f4c7a47c6c5d24ec3af0d697e00ef975d898004c45c535ff685ddbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:34 GMT
ADD file:d86f66385d3993c597ac040a976cd8a826b097d014cc4f3b69d8ebfaa5aa6eff in / 
# Tue, 15 Aug 2023 23:40:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:42:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e41394c7daa90fb4aae0f67d43af5ee9838fb125e249fc0002bfdc3b90bb6c05`  
		Last Modified: Tue, 15 Aug 2023 23:46:33 GMT  
		Size: 50.6 MB (50631355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b86fa75275b3360f0cabc05723d0926928e895a32997b0045ad1a4b87c6d7a`  
		Last Modified: Wed, 16 Aug 2023 03:43:39 GMT  
		Size: 14.7 MB (14671551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31ed6d29a83b27add317575ac2bad9081baaa869afd0edad2f462982c52e652`  
		Last Modified: Wed, 16 Aug 2023 03:43:36 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94acc54b4e308d89fb245806d56517510569b98017639228cbf03c46350a9a2a`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda7bfdd1b15918713a3b6dec980d78af341813470a5ae7d6b3fb016ea4410e`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 285.4 KB (285352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:4568eb3c4efa41029b9b23a9d9e0d7556d84ad92ccbf959ad157e314465f4d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b771ee3290efa1a6c265af138725a8950240a5a9719d1dcaa90107df4c9a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64169110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad7b8bc81b61754cc3c0c2924d41f86ea94e73418d0115e3bfc254be913040`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1753a4167c634c5010550a1f4f417b282f2e72009c2a83a24d3d670c294ad`  
		Last Modified: Wed, 16 Aug 2023 10:16:07 GMT  
		Size: 14.3 MB (14264309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6425f36a7f840361853d24139d567df7ebcdf25533add46ae9b71a1b58899`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffee644b7121bfa1a75452287f0ec6760aca7d2443b5b40ab08d661983c822`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d34f1a1b9fad277ce6fab6fb5714ff0e477efdacb71481b1a19571270f5c72`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 285.1 KB (285086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83e062af1b4b3ed0bbe171920540cba07de2a176984b2dd9c1b9896a8146bf`  
		Last Modified: Wed, 16 Aug 2023 10:16:16 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82d15489b6aee0b568dd46d4e5b0cb7ddac18eac77d323eb4119da8bb7c948e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63890703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5546961801efcaa72e4d88940f4ffb803f8739ca577c52b16045bf536cb61`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:01 GMT
ADD file:8064072457ccf7b4072e08095fa84f96b0fe3387ec8f302afde022186aa3eab5 in / 
# Tue, 15 Aug 2023 23:41:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4513653e4d749342b34f60c592adaf0ef4af993e76a913a1c086a4229a0e3afe`  
		Last Modified: Tue, 15 Aug 2023 23:45:54 GMT  
		Size: 49.5 MB (49531730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce812d7af41ad795cf945688ee3fc47de3e52c7d41f9096865b42621b207cd11`  
		Last Modified: Wed, 16 Aug 2023 03:53:14 GMT  
		Size: 14.1 MB (14070959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd452a3a5eb5d5aa0bca4af1ec0aac980e7024c2886cf99489c75ffb8812530`  
		Last Modified: Wed, 16 Aug 2023 03:53:12 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145fd67a5c34a7ec4d6b4fae9664abcb6c8022c8819ede55397b8fd285ed35cf`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32c90e7cd03d64125341b0f6c1fe0d8b720900a58bda65b7dc130b02ae1c4b`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 285.6 KB (285607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c944cd14cc6be34b10a12d49005ad43d5b49a84f08569b3f28e0cad958ec6fe`  
		Last Modified: Wed, 16 Aug 2023 03:53:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:81e4bc1dbf529ee19748f7a61381d73524921abfa86227b39e29b8644cad239d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65590666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74f18d42edd9c73b33bfb5f14d0bc6a7959b339e05f785c52da1338719aa94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:34 GMT
ADD file:d86f66385d3993c597ac040a976cd8a826b097d014cc4f3b69d8ebfaa5aa6eff in / 
# Tue, 15 Aug 2023 23:40:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:42:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e41394c7daa90fb4aae0f67d43af5ee9838fb125e249fc0002bfdc3b90bb6c05`  
		Last Modified: Tue, 15 Aug 2023 23:46:33 GMT  
		Size: 50.6 MB (50631355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b86fa75275b3360f0cabc05723d0926928e895a32997b0045ad1a4b87c6d7a`  
		Last Modified: Wed, 16 Aug 2023 03:43:39 GMT  
		Size: 14.7 MB (14671551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31ed6d29a83b27add317575ac2bad9081baaa869afd0edad2f462982c52e652`  
		Last Modified: Wed, 16 Aug 2023 03:43:36 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94acc54b4e308d89fb245806d56517510569b98017639228cbf03c46350a9a2a`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda7bfdd1b15918713a3b6dec980d78af341813470a5ae7d6b3fb016ea4410e`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 285.4 KB (285352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512567c2c7d4e968f00b68682cfea6da66ea4783d9da51af2905c8173196709`  
		Last Modified: Wed, 16 Aug 2023 03:43:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
