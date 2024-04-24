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
$ docker pull neurodebian@sha256:540f9f0378eaed7b99ff0f393aeca5b85d21bf20e3e6dec2cf4d58592780f9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:8af16353c0e9c11925a2d06e84f94ee6622dd1311e0782cb31e5ef0ff06b1715
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61333615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18094a9b7cd4c5c88c1b8b234d5aa269e23a631cfac99a6b4c2f9e1b93082c60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db8dc93c243437c267d9050d41579b2c1da9361a99099c87d1e73bce54f380`  
		Last Modified: Wed, 24 Apr 2024 08:10:21 GMT  
		Size: 11.5 MB (11465651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0289cdd63d0b79750c9280dcb3e17b718cccae3e27dc5e4bb33b22e348aef4`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53e5a3f047b2db762be2c81e3c782ad0484dd786c84dfc865e483ce7d6feed2`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5894ce1634f7ae09fa800521db0b96625dee18aaf578129cf1c85c4d3d71dd`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 289.7 KB (289668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:328530398d63ae3d3e39ec8963b2e6684137933d17e5ccd2a7a96852632e7ad6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b26e0fb52826d601a222c22d359229200170ea7d482d1593aa83d6d1d044921`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b7b4f0f0785407b52c5ab62c03c68b16d48dbff6f85628b50a8d5a783d0`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 11.4 MB (11429751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19eb2c60eedda2f4cf1976f0c806b310292a7d55e3b1ea15f8cf76d6ba2f`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759585282845c3252db14d8ddcc2c4e2bf59648949ad6c9625a6afad359e0120`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd085a612fc52502e17d38291e29478c6f400c15e4685dcc925cd3a9e8894833`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:d6cc2081f62e9a58884bfe9572da7d59ecd928df1ef64d6c1f0ccf0c8ec48bda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62761437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacfdcfc79711a900e6a2f09ac39c947c81b63ff08add3173d5232b8392d1006`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16eee48bd91b78b72210da4efa0fdcdc5e71fb772596cd8c0572336b1af8524`  
		Last Modified: Wed, 10 Apr 2024 07:25:16 GMT  
		Size: 11.9 MB (11883988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8527804a98939baaadec8983fdae4ab5ce88aa38dbc3fd98b78784b8adf96f`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cf72b2080e40e991ec5c9aa98d3348e202aa424b986a2e0677e824d2ed8b5`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a12e51afe8bf6ee26dfa29de12a2bfdb63e53df2d3b1a18bf795e95cbfd1c`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 288.2 KB (288202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:701a0207c477f7dd36e5cb582c3bc35c4a54491ab07b65c572cdceab30c3c045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff1c57557b768aa811a215238e09ead288334a413535c7eda58be0d7b3cf594f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e937042ce9e2bf7644e822b90ee21b6dc37dbe41760c77d141e62a053225a47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db8dc93c243437c267d9050d41579b2c1da9361a99099c87d1e73bce54f380`  
		Last Modified: Wed, 24 Apr 2024 08:10:21 GMT  
		Size: 11.5 MB (11465651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0289cdd63d0b79750c9280dcb3e17b718cccae3e27dc5e4bb33b22e348aef4`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53e5a3f047b2db762be2c81e3c782ad0484dd786c84dfc865e483ce7d6feed2`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5894ce1634f7ae09fa800521db0b96625dee18aaf578129cf1c85c4d3d71dd`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 289.7 KB (289668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83b404241090c98faa330d0592a4adcdad8e26eb2f8a5710370e279ec21f40f`  
		Last Modified: Wed, 24 Apr 2024 08:10:28 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:91337a1e94def592bbd01d137c15beec06f770224a7e4e9916021ac4807c8bee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c4ce701f20e6ed13ecd243e1db2046bbfda06bb0838d4af3ce89407cc28f9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b7b4f0f0785407b52c5ab62c03c68b16d48dbff6f85628b50a8d5a783d0`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 11.4 MB (11429751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19eb2c60eedda2f4cf1976f0c806b310292a7d55e3b1ea15f8cf76d6ba2f`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759585282845c3252db14d8ddcc2c4e2bf59648949ad6c9625a6afad359e0120`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd085a612fc52502e17d38291e29478c6f400c15e4685dcc925cd3a9e8894833`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78819c7f738132280c3305dbdd627bf20b4edb2a9e149e3d73a85d826f5f5c84`  
		Last Modified: Wed, 24 Apr 2024 04:43:10 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f21d2a2c52896cec8a69d3dc10c93c6c968e9f56549952f76a86f2e580095aa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62761866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a01d8364920a2d50bd720b72856ddedd63634184e1e4603b9df00479321dbef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16eee48bd91b78b72210da4efa0fdcdc5e71fb772596cd8c0572336b1af8524`  
		Last Modified: Wed, 10 Apr 2024 07:25:16 GMT  
		Size: 11.9 MB (11883988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8527804a98939baaadec8983fdae4ab5ce88aa38dbc3fd98b78784b8adf96f`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cf72b2080e40e991ec5c9aa98d3348e202aa424b986a2e0677e824d2ed8b5`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a12e51afe8bf6ee26dfa29de12a2bfdb63e53df2d3b1a18bf795e95cbfd1c`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 288.2 KB (288202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc6b13c79af4260e1e39014af8e2ab2fd06ce9b0f16e73635d2eabac48e32a4`  
		Last Modified: Wed, 10 Apr 2024 07:25:32 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:5d25ff74ca5efad474ede142f04a122e3fdfdabc671d15f35a48963b95d5947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:2320f4fdbffba27f42e311af32288d59b2bfa7b132c7aa9b1feb20779a5373d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78901287c3396aa5f431afc9e8cf59f5737377a719f5ba1f7d5b47bf3a28c6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3aa55f66293a278b78670a2f2f2d792b19de4177447661cb34602064c86f80e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7434120237e5c825cea47d3e2542d57b598fefb9c6375f9dfe7948806ee4dbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:2c9e756b383c9cdfad4fd8299e6bab8e0d272187594873902e380b13b42f55e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5753bf3a806b1f2d120800853aec731cc6f767ed7ac6c68358ab0608ed5cc8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:00c4982170e8781a27233d2e2a75d62a89c127ab27ef28de9274a0f1bfa2e36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3ae4cecce765fb1e419ef28e56adbe542743625480bed78a6f59471004cb855
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cbced98ae2907bea19c536757d93411ece53976a1629f42df91b5baa50d1f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269bbc6aa8eea32220fd696f924348d95431a0f432cff2d9c00f3748988b164`  
		Last Modified: Wed, 24 Apr 2024 08:10:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b8ce5dbb664dce1f56363f6b83b4a1976383ad0c34da0d8614af4c3a9d53c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b7159593c55cd9beb5394aa1d4d97239c292a286413e4e239e8bd32a25f81b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9717652fb5e910c228b0dae069d356eb298967cc6440b73745668a420aa2e2a`  
		Last Modified: Wed, 24 Apr 2024 04:42:47 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b0864a7383d8c68c8b1237062b619ecce06878f1742e656c75ee017a823f2905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a96f942a67cc85ef7cb701a6b443e8871de980aa20c777fc7f91299880c742d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120b7317a3b37952c50216ba072c4c503b22262cb884b3866f9fef9b2f40bc05`  
		Last Modified: Wed, 10 Apr 2024 07:25:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:3eaa3634e6d1292ad0bc85d7c70412129c5783bd534aca65da49e04bb3a522ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:07c73a4958240d229123ef1a97377e465332fa97080f5b67ee97d4eb4f2c4a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61463382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5191584db3372a79f7ffbd98b96e3c67d4be2b5522de23cb70f014d5de1f98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:41 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
# Wed, 24 Apr 2024 03:28:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5a97dfd108ff40ee8c22fb1b674c4b0fa71d4728a7c957f5ec3c7bf3f211f`  
		Last Modified: Wed, 24 Apr 2024 08:09:45 GMT  
		Size: 10.5 MB (10504543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc0aa6e5f908abc21bcc432f37a7616080de8f05aed4a053d5e4c2748186e3e`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d835973a558f188c0dea4ef504782eb743c56e14bef9e753f423a4a44bbab7`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355de9ffe679fe4300a0e38c273cd79b40a5912cbd8af4058d63704daff83b13`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 299.3 KB (299325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:56efdc6d4802c96908131c14deb23f2091fde8ce61a5e6331c8c9f09aafe132e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60264995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d172ac6a5fef3c1e4e17c078c2daf5df51d43e0f1e5d08080ddaac12778ce2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:40:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:40:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:40:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:40:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecc8a5ac86b486903737291255556b77f7a90a8e214ec345d700fc1c8f18878`  
		Last Modified: Wed, 24 Apr 2024 04:42:21 GMT  
		Size: 10.5 MB (10510475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e0aabb024a919a3d450e2a440658372daba5388e7b50bddfd1365d0115436`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ea48749b49637a0ef75c50e94c555ac928984662b3635dfee7ca5f0b81a922`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e36e1e3c24b698699ab9452390385c45b992d86280ca886ae53e44fa113e7`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 299.3 KB (299348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:df8d03c48e83e5849a8fd395a81f6a24395968e77bb2c98d032044ead1c64962
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9966b92f65077c736ffdee2928aef16b1a12949a00c6670f6bbde84d1f147b13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:45 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Wed, 10 Apr 2024 00:57:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:22:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:22:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:22:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8784b17322d3d4a6b07cd237ba7efe07278b1e0c9664aeb2629fb4549a858a9`  
		Last Modified: Wed, 10 Apr 2024 07:24:35 GMT  
		Size: 10.9 MB (10868462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af86fdf824835b62c3d8705ea2f6349a655a9d7694f6d4db4c9457ee449df8f`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83b62197ab09a16810d259602f4d31d648b49ae6f812ffbe3a4534056145bf2`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4c400e7b23507419bdb5153ffe01fa0ce304a6f128930f4809da6f69701d1b`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 299.4 KB (299396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:408a796d1064bd35b48fba62951ca39ca9daaa9f939c3c7200618eea9fce1e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4b091c009dc24d7be992ee1c6109c8716479fdfe17d61066dfd4983b77acf165
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61463743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527f37e21fba42ac823635c60be1750c6c653a66270b196d848d525d58751e8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:41 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
# Wed, 24 Apr 2024 03:28:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5a97dfd108ff40ee8c22fb1b674c4b0fa71d4728a7c957f5ec3c7bf3f211f`  
		Last Modified: Wed, 24 Apr 2024 08:09:45 GMT  
		Size: 10.5 MB (10504543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc0aa6e5f908abc21bcc432f37a7616080de8f05aed4a053d5e4c2748186e3e`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d835973a558f188c0dea4ef504782eb743c56e14bef9e753f423a4a44bbab7`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355de9ffe679fe4300a0e38c273cd79b40a5912cbd8af4058d63704daff83b13`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 299.3 KB (299325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d20dc516f901becb966e456841d1a6c9c9ca61dc07e02c333eff55b439fc1f`  
		Last Modified: Wed, 24 Apr 2024 08:09:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:88a242bbefe2114d7a0d414a1a87c65d47dd3778150637c354b8613a07eb24d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60265352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2471a63b1f2c98d58e22ead1ec9ebc131bc0dcf927a4a26d9c4676a3701a15d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:40:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:40:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:40:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:40:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecc8a5ac86b486903737291255556b77f7a90a8e214ec345d700fc1c8f18878`  
		Last Modified: Wed, 24 Apr 2024 04:42:21 GMT  
		Size: 10.5 MB (10510475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e0aabb024a919a3d450e2a440658372daba5388e7b50bddfd1365d0115436`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ea48749b49637a0ef75c50e94c555ac928984662b3635dfee7ca5f0b81a922`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e36e1e3c24b698699ab9452390385c45b992d86280ca886ae53e44fa113e7`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 299.3 KB (299348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7af1f9b164792dd8923f97b651ff98e17795691dde122adea7406e9c63aa2`  
		Last Modified: Wed, 24 Apr 2024 04:42:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1e087e0531fce17fec3203a4fd3db9132ac8d0c52841365772e1d34f11240896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1050ab7f1f273d04e2de05d45259b5682c474d7e8e6e169e125a43ecfd38c5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:45 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Wed, 10 Apr 2024 00:57:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:22:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:22:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:22:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8784b17322d3d4a6b07cd237ba7efe07278b1e0c9664aeb2629fb4549a858a9`  
		Last Modified: Wed, 10 Apr 2024 07:24:35 GMT  
		Size: 10.9 MB (10868462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af86fdf824835b62c3d8705ea2f6349a655a9d7694f6d4db4c9457ee449df8f`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83b62197ab09a16810d259602f4d31d648b49ae6f812ffbe3a4534056145bf2`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4c400e7b23507419bdb5153ffe01fa0ce304a6f128930f4809da6f69701d1b`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 299.4 KB (299396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c99c77dd89a66b028c71d03c07e750f68bfa1381a67c00d6f99b44569556ed`  
		Last Modified: Wed, 10 Apr 2024 07:24:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:d5afe5aa50b490160f2376a1231feaa1aa5062a746656bfa50c79ca1d5624e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3ee033ce6ba8e7c820a28018f3cdc6271c3f394ff6995fc4ec5a12f8d783eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6734241f3a76dedaef5b4ac32077e106efac5d37ba35a36076eb9c88296707`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f252c279c1245ea47a44d3326988bd3f7aa7e271da8117a505e57f0d5756a010`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 5.5 MB (5494626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ff0f44046e789e0d0b70a8e3fac28f4ae1bbb0e337f66aa29fb6c09c3a9a11`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f617399291fd7fb8a39fa4320a06e71ef72b24bd247a304a0cd591c57ef016f7`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea265c293a70b71c7b25449c823f937f648eaaf482a07495e803b665a2e5f4f`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 239.5 KB (239492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:03529a596fef23fb8c67f4f0a1a0725fec4aeb871d999ad0096c8940ec992f7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32921858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39031c4227a6069e7098f1080bbddd97e16de31f80b7056965cd75122d9f1f73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:37:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:37:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:37:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:37:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced7a6d3abbe464bf762a82a656eac696cb8a1f016f460c22962aaec7f7bcaa1`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 5.5 MB (5474948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf585fd20b0200e660a0939d16828fd20434131110b6dfd0a3f9f3ea1a960d4`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063e9b1fd3a1b1fcdb78293f09bfdb6873198075c722be20837cb3f757a0b726`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebedb6467515c983f418b9c4af883e13a130480463f372b64fbfdb609c065c`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 239.9 KB (239916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:2c90171350ba7245623727a4df9e3b596c078b2faaf6ca0b82a52b540a0bdde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:def9ca98be8ba4b69562593d869320a43a86c351396ca2e33652cf14b3820a32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb9721979d47090721d09e59e0a40dc85f12c8853416d10f154f85aab5bb6f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f252c279c1245ea47a44d3326988bd3f7aa7e271da8117a505e57f0d5756a010`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 5.5 MB (5494626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ff0f44046e789e0d0b70a8e3fac28f4ae1bbb0e337f66aa29fb6c09c3a9a11`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f617399291fd7fb8a39fa4320a06e71ef72b24bd247a304a0cd591c57ef016f7`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea265c293a70b71c7b25449c823f937f648eaaf482a07495e803b665a2e5f4f`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 239.5 KB (239492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40162089408f601135275d7d1ff64ffe86d88e12b207a669d1c98053029ca9a`  
		Last Modified: Tue, 16 Apr 2024 05:21:51 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eeb80a3de7d834bac56076aa31e003892ea2357f64a46fd8842e665f9a0f98a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32922113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc0678e65eaed5a11dea215f50e2bd20771e67f59607b1f7c0dfb50425db9e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:37:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:37:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:37:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:37:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced7a6d3abbe464bf762a82a656eac696cb8a1f016f460c22962aaec7f7bcaa1`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 5.5 MB (5474948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf585fd20b0200e660a0939d16828fd20434131110b6dfd0a3f9f3ea1a960d4`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063e9b1fd3a1b1fcdb78293f09bfdb6873198075c722be20837cb3f757a0b726`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebedb6467515c983f418b9c4af883e13a130480463f372b64fbfdb609c065c`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 239.9 KB (239916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729a8551f3f028911c9fe65b02dc5db64a086b156b178bfbb701fd7608ae789`  
		Last Modified: Tue, 16 Apr 2024 03:39:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:dd28b549dcc0c965c39774c71ab0ee9a245d447e041ff5fa4ececa7f5ee7fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:aacb4187c645fc1181ff2e54d164f05e728d4d07e755274d8abf41558faca7b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34462647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947839795e4e9f44c063cdf65a0a04d1b8535a0815bff651873ae6caa3d4f578`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94664be31c2336989672810e8eae41ae9173296afe40c7a279d0eeff5c886f29`  
		Last Modified: Tue, 16 Apr 2024 05:22:01 GMT  
		Size: 3.8 MB (3767400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350ca5cbbb3e541640b66df0df99da12f628da133fe276d06bf8ffcb5a4cc3a`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bd6793c31737e55e00ab7f914f32a745f2bee1f0f323805b4455e10f289034`  
		Last Modified: Tue, 16 Apr 2024 05:21:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c140cba835ae5b3bae411148fb2e651573b8a9daa82f24a08d99856c66da57f3`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 253.5 KB (253456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d2deebd91609fd76d3275f708bb8b8e76d06648395b462e66b7c5dbbc25ad109
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32395640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580e4117cae9b62176898970adbe2dfd2e0bed789bb52036ec29518cf9608285`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:38:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:38:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:38:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09775ad9e72d75fdb01bd2481e64506d36bd752927db1e12238d48c9ee2ed459`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 3.7 MB (3739473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40afa244e52805c09919d20b2552941cff429b665223738a4114e74b637711f`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49e08caeafc57ea01b64b800cb267d7ae4d8ec5c54975c0e92f6499082888ad`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868a05d69fda4fb84b11fe2d42740101a5cdb3ac6ae6b4217b32871c522b8817`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 253.9 KB (253852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:f84c3060cf4fe27309a30e524a7d58b1b9bc785811140d8773b68360f61cb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f959e102c7e1ca44ef5a659df3638e7df765c0deda408695e5165f87bdf1ada7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34462906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a53656ee1d9a157bb9547425b0a26f146aadfdef634c8a5a3d1ded63cc03b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94664be31c2336989672810e8eae41ae9173296afe40c7a279d0eeff5c886f29`  
		Last Modified: Tue, 16 Apr 2024 05:22:01 GMT  
		Size: 3.8 MB (3767400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350ca5cbbb3e541640b66df0df99da12f628da133fe276d06bf8ffcb5a4cc3a`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bd6793c31737e55e00ab7f914f32a745f2bee1f0f323805b4455e10f289034`  
		Last Modified: Tue, 16 Apr 2024 05:21:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c140cba835ae5b3bae411148fb2e651573b8a9daa82f24a08d99856c66da57f3`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 253.5 KB (253456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5ef2f7826ab3c5a8775ae04f85996abfcc0124d3cd6b3a452cbbd5445f5ced`  
		Last Modified: Tue, 16 Apr 2024 05:22:09 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:824be41a6a3f95926b5ad440687b448bf469a6ab0dc80b49a234121b7b484cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32395897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114b6dfcb1c1445f64f371dcad07f7f59020924cccdd7e5662251fe4c8094578`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:38:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:38:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:38:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09775ad9e72d75fdb01bd2481e64506d36bd752927db1e12238d48c9ee2ed459`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 3.7 MB (3739473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40afa244e52805c09919d20b2552941cff429b665223738a4114e74b637711f`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49e08caeafc57ea01b64b800cb267d7ae4d8ec5c54975c0e92f6499082888ad`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868a05d69fda4fb84b11fe2d42740101a5cdb3ac6ae6b4217b32871c522b8817`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 253.9 KB (253852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8377980bff32d6794f1d33e92bd7b0075d35e8348ee9d4d13e03d49f2facd6`  
		Last Modified: Tue, 16 Apr 2024 03:39:28 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:5d25ff74ca5efad474ede142f04a122e3fdfdabc671d15f35a48963b95d5947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:2320f4fdbffba27f42e311af32288d59b2bfa7b132c7aa9b1feb20779a5373d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78901287c3396aa5f431afc9e8cf59f5737377a719f5ba1f7d5b47bf3a28c6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3aa55f66293a278b78670a2f2f2d792b19de4177447661cb34602064c86f80e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7434120237e5c825cea47d3e2542d57b598fefb9c6375f9dfe7948806ee4dbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:2c9e756b383c9cdfad4fd8299e6bab8e0d272187594873902e380b13b42f55e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5753bf3a806b1f2d120800853aec731cc6f767ed7ac6c68358ab0608ed5cc8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:c23e7183f6e52b4e2de181ef64309ab1f08225385dbbc8bc146279fe540dc39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:d6f23bd21819674b163ecf6d32924d910d225448ff3518022e6e4517ff0a2a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c9900b40f363d586167e78d0a9a1b29ca4e78d2add419fce9711a1e87c18d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:09:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:09:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c7dfd06437e02fff0de53af99dc1c00f1276fbb8de9e98d2df6028c40b2335`  
		Last Modified: Wed, 24 Apr 2024 08:10:36 GMT  
		Size: 11.7 MB (11743087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd26b6c5d7f38213336fea92572312ac1832834e19f0645d8013bef455f1c5a`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ebb65957e8e94ec9c3a1b4f90b48587b350b1a5d2e066e0d8870c6438a93ed`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77527b91c07d267eb02ab1842c5fecf2250bc80f9a3071ca1c62fa510ce8a020`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 287.8 KB (287843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:af6c719ace34f312b6740f86c4488f80d6561be1cd851a7308819a050b342097
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64889517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9721214a287b0669996f8064877b5cb2c777c2ca39d4cfe9e1ceeb180e2d343b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:40 GMT
ADD file:58d167eb75df26d368d9ef63173440fad7973e18049ffb23841be9cf507ee614 in / 
# Wed, 24 Apr 2024 04:11:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9914f5e7b79b9a6b9b6b7b39565cb50b06e8e20c51fa6732d67575dc53227762`  
		Last Modified: Wed, 24 Apr 2024 04:16:38 GMT  
		Size: 52.9 MB (52860803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d837feebd2f839b2c1f963eea7ebc9e63d698a5493a5a0400ac20b7f43a2071c`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 11.7 MB (11738112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09977deff1fff17d1ef335ccaf490538bd16ff4a539f9e12bb7c0c3eb4cb0c82`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b96de0d76100592b8310f330c37dad1a727ec9bf5e76ad94c35d9f20a35bc2`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2df9bddff64eec380d895f9b9009fc18c563afecbc57fd1c443e6dbc7820ee`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 288.6 KB (288594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:40f257d65c33a3ca4bac3d5a8dd73fe5f681a38e847a622336bc25777511e50b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65963214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9414f1ef791b35f0e53ec296123bbf56fce785fd4afadd1a5b8dcba95f79646`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fd105449905a0a94707b3cba942d456bf9fe38526a79f7b341be509fb6708`  
		Last Modified: Wed, 10 Apr 2024 07:25:43 GMT  
		Size: 13.1 MB (13128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2827d9b3036a22fee78ea17382d6ba1f730c8c763ef24312843fcaf186c8cc69`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc53f67a234b9e433bd5bc4d7b7c4fe1e787931568ce54d0eb27900e207d2095`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068b92b06f0afc1e120d97fe37e9366d8729e90600f03c95d7ccdbca3a3fd8b8`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 287.8 KB (287757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:b8bbce806a0a49eb1358850b02d5841437015b411a81ecc80519953fa5e712ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:da4dfb4fd57feb809612292068b88cf45248d914f7dbf20b188d1c12dc854a75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998ff6a3fd8de4cba074e06a09d1adb79793ed5a0627c455c9056d68b55e6e10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:09:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:09:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c7dfd06437e02fff0de53af99dc1c00f1276fbb8de9e98d2df6028c40b2335`  
		Last Modified: Wed, 24 Apr 2024 08:10:36 GMT  
		Size: 11.7 MB (11743087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd26b6c5d7f38213336fea92572312ac1832834e19f0645d8013bef455f1c5a`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ebb65957e8e94ec9c3a1b4f90b48587b350b1a5d2e066e0d8870c6438a93ed`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77527b91c07d267eb02ab1842c5fecf2250bc80f9a3071ca1c62fa510ce8a020`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 287.8 KB (287843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1eb88e765e63782a59d495ea7f9b1079764f27094a1479608f41455b5c7f9ef`  
		Last Modified: Wed, 24 Apr 2024 08:10:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8eed19e43fe455a4467dc0964ea15c6a2527e735a32b26147778c5d4e98ba806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64889916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbddc970b69155e7710675b1470b74121ed4abae73cdad8df3316e0680cf6ed9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:40 GMT
ADD file:58d167eb75df26d368d9ef63173440fad7973e18049ffb23841be9cf507ee614 in / 
# Wed, 24 Apr 2024 04:11:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:55 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9914f5e7b79b9a6b9b6b7b39565cb50b06e8e20c51fa6732d67575dc53227762`  
		Last Modified: Wed, 24 Apr 2024 04:16:38 GMT  
		Size: 52.9 MB (52860803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d837feebd2f839b2c1f963eea7ebc9e63d698a5493a5a0400ac20b7f43a2071c`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 11.7 MB (11738112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09977deff1fff17d1ef335ccaf490538bd16ff4a539f9e12bb7c0c3eb4cb0c82`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b96de0d76100592b8310f330c37dad1a727ec9bf5e76ad94c35d9f20a35bc2`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2df9bddff64eec380d895f9b9009fc18c563afecbc57fd1c443e6dbc7820ee`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 288.6 KB (288594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec7a4c6962d047c0b07c813ee90ae3364131902545f2ce9a30b3453030562f8`  
		Last Modified: Wed, 24 Apr 2024 04:43:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d720fce2bfbba32832cc2bf799dd698e43bb233d4a37c2cd4d197b0cb4193b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65963609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f46f2052a62716fe2561cd94f0df4bc0d16574b334e2a01e5d8736e1808ac0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fd105449905a0a94707b3cba942d456bf9fe38526a79f7b341be509fb6708`  
		Last Modified: Wed, 10 Apr 2024 07:25:43 GMT  
		Size: 13.1 MB (13128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2827d9b3036a22fee78ea17382d6ba1f730c8c763ef24312843fcaf186c8cc69`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc53f67a234b9e433bd5bc4d7b7c4fe1e787931568ce54d0eb27900e207d2095`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068b92b06f0afc1e120d97fe37e9366d8729e90600f03c95d7ccdbca3a3fd8b8`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 287.8 KB (287757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a446d0e0f4843ac41fcb1c976e2e429b405f2dc9841ac6c22095f1b59139e6`  
		Last Modified: Wed, 10 Apr 2024 07:25:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:3eaa3634e6d1292ad0bc85d7c70412129c5783bd534aca65da49e04bb3a522ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:07c73a4958240d229123ef1a97377e465332fa97080f5b67ee97d4eb4f2c4a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61463382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5191584db3372a79f7ffbd98b96e3c67d4be2b5522de23cb70f014d5de1f98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:41 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
# Wed, 24 Apr 2024 03:28:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5a97dfd108ff40ee8c22fb1b674c4b0fa71d4728a7c957f5ec3c7bf3f211f`  
		Last Modified: Wed, 24 Apr 2024 08:09:45 GMT  
		Size: 10.5 MB (10504543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc0aa6e5f908abc21bcc432f37a7616080de8f05aed4a053d5e4c2748186e3e`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d835973a558f188c0dea4ef504782eb743c56e14bef9e753f423a4a44bbab7`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355de9ffe679fe4300a0e38c273cd79b40a5912cbd8af4058d63704daff83b13`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 299.3 KB (299325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:56efdc6d4802c96908131c14deb23f2091fde8ce61a5e6331c8c9f09aafe132e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60264995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d172ac6a5fef3c1e4e17c078c2daf5df51d43e0f1e5d08080ddaac12778ce2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:40:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:40:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:40:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:40:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecc8a5ac86b486903737291255556b77f7a90a8e214ec345d700fc1c8f18878`  
		Last Modified: Wed, 24 Apr 2024 04:42:21 GMT  
		Size: 10.5 MB (10510475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e0aabb024a919a3d450e2a440658372daba5388e7b50bddfd1365d0115436`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ea48749b49637a0ef75c50e94c555ac928984662b3635dfee7ca5f0b81a922`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e36e1e3c24b698699ab9452390385c45b992d86280ca886ae53e44fa113e7`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 299.3 KB (299348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:df8d03c48e83e5849a8fd395a81f6a24395968e77bb2c98d032044ead1c64962
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9966b92f65077c736ffdee2928aef16b1a12949a00c6670f6bbde84d1f147b13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:45 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Wed, 10 Apr 2024 00:57:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:22:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:22:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:22:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8784b17322d3d4a6b07cd237ba7efe07278b1e0c9664aeb2629fb4549a858a9`  
		Last Modified: Wed, 10 Apr 2024 07:24:35 GMT  
		Size: 10.9 MB (10868462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af86fdf824835b62c3d8705ea2f6349a655a9d7694f6d4db4c9457ee449df8f`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83b62197ab09a16810d259602f4d31d648b49ae6f812ffbe3a4534056145bf2`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4c400e7b23507419bdb5153ffe01fa0ce304a6f128930f4809da6f69701d1b`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 299.4 KB (299396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:408a796d1064bd35b48fba62951ca39ca9daaa9f939c3c7200618eea9fce1e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4b091c009dc24d7be992ee1c6109c8716479fdfe17d61066dfd4983b77acf165
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61463743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527f37e21fba42ac823635c60be1750c6c653a66270b196d848d525d58751e8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:41 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
# Wed, 24 Apr 2024 03:28:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5a97dfd108ff40ee8c22fb1b674c4b0fa71d4728a7c957f5ec3c7bf3f211f`  
		Last Modified: Wed, 24 Apr 2024 08:09:45 GMT  
		Size: 10.5 MB (10504543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc0aa6e5f908abc21bcc432f37a7616080de8f05aed4a053d5e4c2748186e3e`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d835973a558f188c0dea4ef504782eb743c56e14bef9e753f423a4a44bbab7`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355de9ffe679fe4300a0e38c273cd79b40a5912cbd8af4058d63704daff83b13`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 299.3 KB (299325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d20dc516f901becb966e456841d1a6c9c9ca61dc07e02c333eff55b439fc1f`  
		Last Modified: Wed, 24 Apr 2024 08:09:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:88a242bbefe2114d7a0d414a1a87c65d47dd3778150637c354b8613a07eb24d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60265352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2471a63b1f2c98d58e22ead1ec9ebc131bc0dcf927a4a26d9c4676a3701a15d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:40:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:40:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:40:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:40:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecc8a5ac86b486903737291255556b77f7a90a8e214ec345d700fc1c8f18878`  
		Last Modified: Wed, 24 Apr 2024 04:42:21 GMT  
		Size: 10.5 MB (10510475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e0aabb024a919a3d450e2a440658372daba5388e7b50bddfd1365d0115436`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ea48749b49637a0ef75c50e94c555ac928984662b3635dfee7ca5f0b81a922`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e36e1e3c24b698699ab9452390385c45b992d86280ca886ae53e44fa113e7`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 299.3 KB (299348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7af1f9b164792dd8923f97b651ff98e17795691dde122adea7406e9c63aa2`  
		Last Modified: Wed, 24 Apr 2024 04:42:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1e087e0531fce17fec3203a4fd3db9132ac8d0c52841365772e1d34f11240896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1050ab7f1f273d04e2de05d45259b5682c474d7e8e6e169e125a43ecfd38c5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:45 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Wed, 10 Apr 2024 00:57:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:22:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:22:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:22:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8784b17322d3d4a6b07cd237ba7efe07278b1e0c9664aeb2629fb4549a858a9`  
		Last Modified: Wed, 10 Apr 2024 07:24:35 GMT  
		Size: 10.9 MB (10868462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af86fdf824835b62c3d8705ea2f6349a655a9d7694f6d4db4c9457ee449df8f`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83b62197ab09a16810d259602f4d31d648b49ae6f812ffbe3a4534056145bf2`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4c400e7b23507419bdb5153ffe01fa0ce304a6f128930f4809da6f69701d1b`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 299.4 KB (299396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c99c77dd89a66b028c71d03c07e750f68bfa1381a67c00d6f99b44569556ed`  
		Last Modified: Wed, 10 Apr 2024 07:24:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:5d25ff74ca5efad474ede142f04a122e3fdfdabc671d15f35a48963b95d5947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:2320f4fdbffba27f42e311af32288d59b2bfa7b132c7aa9b1feb20779a5373d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78901287c3396aa5f431afc9e8cf59f5737377a719f5ba1f7d5b47bf3a28c6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3aa55f66293a278b78670a2f2f2d792b19de4177447661cb34602064c86f80e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7434120237e5c825cea47d3e2542d57b598fefb9c6375f9dfe7948806ee4dbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:2c9e756b383c9cdfad4fd8299e6bab8e0d272187594873902e380b13b42f55e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5753bf3a806b1f2d120800853aec731cc6f767ed7ac6c68358ab0608ed5cc8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:00c4982170e8781a27233d2e2a75d62a89c127ab27ef28de9274a0f1bfa2e36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3ae4cecce765fb1e419ef28e56adbe542743625480bed78a6f59471004cb855
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cbced98ae2907bea19c536757d93411ece53976a1629f42df91b5baa50d1f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269bbc6aa8eea32220fd696f924348d95431a0f432cff2d9c00f3748988b164`  
		Last Modified: Wed, 24 Apr 2024 08:10:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b8ce5dbb664dce1f56363f6b83b4a1976383ad0c34da0d8614af4c3a9d53c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b7159593c55cd9beb5394aa1d4d97239c292a286413e4e239e8bd32a25f81b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9717652fb5e910c228b0dae069d356eb298967cc6440b73745668a420aa2e2a`  
		Last Modified: Wed, 24 Apr 2024 04:42:47 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b0864a7383d8c68c8b1237062b619ecce06878f1742e656c75ee017a823f2905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a96f942a67cc85ef7cb701a6b443e8871de980aa20c777fc7f91299880c742d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120b7317a3b37952c50216ba072c4c503b22262cb884b3866f9fef9b2f40bc05`  
		Last Modified: Wed, 10 Apr 2024 07:25:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:540f9f0378eaed7b99ff0f393aeca5b85d21bf20e3e6dec2cf4d58592780f9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:8af16353c0e9c11925a2d06e84f94ee6622dd1311e0782cb31e5ef0ff06b1715
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61333615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18094a9b7cd4c5c88c1b8b234d5aa269e23a631cfac99a6b4c2f9e1b93082c60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db8dc93c243437c267d9050d41579b2c1da9361a99099c87d1e73bce54f380`  
		Last Modified: Wed, 24 Apr 2024 08:10:21 GMT  
		Size: 11.5 MB (11465651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0289cdd63d0b79750c9280dcb3e17b718cccae3e27dc5e4bb33b22e348aef4`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53e5a3f047b2db762be2c81e3c782ad0484dd786c84dfc865e483ce7d6feed2`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5894ce1634f7ae09fa800521db0b96625dee18aaf578129cf1c85c4d3d71dd`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 289.7 KB (289668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:328530398d63ae3d3e39ec8963b2e6684137933d17e5ccd2a7a96852632e7ad6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b26e0fb52826d601a222c22d359229200170ea7d482d1593aa83d6d1d044921`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b7b4f0f0785407b52c5ab62c03c68b16d48dbff6f85628b50a8d5a783d0`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 11.4 MB (11429751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19eb2c60eedda2f4cf1976f0c806b310292a7d55e3b1ea15f8cf76d6ba2f`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759585282845c3252db14d8ddcc2c4e2bf59648949ad6c9625a6afad359e0120`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd085a612fc52502e17d38291e29478c6f400c15e4685dcc925cd3a9e8894833`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:d6cc2081f62e9a58884bfe9572da7d59ecd928df1ef64d6c1f0ccf0c8ec48bda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62761437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacfdcfc79711a900e6a2f09ac39c947c81b63ff08add3173d5232b8392d1006`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16eee48bd91b78b72210da4efa0fdcdc5e71fb772596cd8c0572336b1af8524`  
		Last Modified: Wed, 10 Apr 2024 07:25:16 GMT  
		Size: 11.9 MB (11883988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8527804a98939baaadec8983fdae4ab5ce88aa38dbc3fd98b78784b8adf96f`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cf72b2080e40e991ec5c9aa98d3348e202aa424b986a2e0677e824d2ed8b5`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a12e51afe8bf6ee26dfa29de12a2bfdb63e53df2d3b1a18bf795e95cbfd1c`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 288.2 KB (288202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:701a0207c477f7dd36e5cb582c3bc35c4a54491ab07b65c572cdceab30c3c045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff1c57557b768aa811a215238e09ead288334a413535c7eda58be0d7b3cf594f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e937042ce9e2bf7644e822b90ee21b6dc37dbe41760c77d141e62a053225a47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db8dc93c243437c267d9050d41579b2c1da9361a99099c87d1e73bce54f380`  
		Last Modified: Wed, 24 Apr 2024 08:10:21 GMT  
		Size: 11.5 MB (11465651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0289cdd63d0b79750c9280dcb3e17b718cccae3e27dc5e4bb33b22e348aef4`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53e5a3f047b2db762be2c81e3c782ad0484dd786c84dfc865e483ce7d6feed2`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5894ce1634f7ae09fa800521db0b96625dee18aaf578129cf1c85c4d3d71dd`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 289.7 KB (289668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83b404241090c98faa330d0592a4adcdad8e26eb2f8a5710370e279ec21f40f`  
		Last Modified: Wed, 24 Apr 2024 08:10:28 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:91337a1e94def592bbd01d137c15beec06f770224a7e4e9916021ac4807c8bee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c4ce701f20e6ed13ecd243e1db2046bbfda06bb0838d4af3ce89407cc28f9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b7b4f0f0785407b52c5ab62c03c68b16d48dbff6f85628b50a8d5a783d0`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 11.4 MB (11429751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19eb2c60eedda2f4cf1976f0c806b310292a7d55e3b1ea15f8cf76d6ba2f`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759585282845c3252db14d8ddcc2c4e2bf59648949ad6c9625a6afad359e0120`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd085a612fc52502e17d38291e29478c6f400c15e4685dcc925cd3a9e8894833`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78819c7f738132280c3305dbdd627bf20b4edb2a9e149e3d73a85d826f5f5c84`  
		Last Modified: Wed, 24 Apr 2024 04:43:10 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f21d2a2c52896cec8a69d3dc10c93c6c968e9f56549952f76a86f2e580095aa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62761866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a01d8364920a2d50bd720b72856ddedd63634184e1e4603b9df00479321dbef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16eee48bd91b78b72210da4efa0fdcdc5e71fb772596cd8c0572336b1af8524`  
		Last Modified: Wed, 10 Apr 2024 07:25:16 GMT  
		Size: 11.9 MB (11883988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8527804a98939baaadec8983fdae4ab5ce88aa38dbc3fd98b78784b8adf96f`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cf72b2080e40e991ec5c9aa98d3348e202aa424b986a2e0677e824d2ed8b5`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a12e51afe8bf6ee26dfa29de12a2bfdb63e53df2d3b1a18bf795e95cbfd1c`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 288.2 KB (288202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc6b13c79af4260e1e39014af8e2ab2fd06ce9b0f16e73635d2eabac48e32a4`  
		Last Modified: Wed, 10 Apr 2024 07:25:32 GMT  
		Size: 429.0 B  
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
$ docker pull neurodebian@sha256:d5afe5aa50b490160f2376a1231feaa1aa5062a746656bfa50c79ca1d5624e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3ee033ce6ba8e7c820a28018f3cdc6271c3f394ff6995fc4ec5a12f8d783eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6734241f3a76dedaef5b4ac32077e106efac5d37ba35a36076eb9c88296707`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f252c279c1245ea47a44d3326988bd3f7aa7e271da8117a505e57f0d5756a010`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 5.5 MB (5494626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ff0f44046e789e0d0b70a8e3fac28f4ae1bbb0e337f66aa29fb6c09c3a9a11`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f617399291fd7fb8a39fa4320a06e71ef72b24bd247a304a0cd591c57ef016f7`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea265c293a70b71c7b25449c823f937f648eaaf482a07495e803b665a2e5f4f`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 239.5 KB (239492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:03529a596fef23fb8c67f4f0a1a0725fec4aeb871d999ad0096c8940ec992f7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32921858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39031c4227a6069e7098f1080bbddd97e16de31f80b7056965cd75122d9f1f73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:37:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:37:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:37:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:37:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced7a6d3abbe464bf762a82a656eac696cb8a1f016f460c22962aaec7f7bcaa1`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 5.5 MB (5474948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf585fd20b0200e660a0939d16828fd20434131110b6dfd0a3f9f3ea1a960d4`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063e9b1fd3a1b1fcdb78293f09bfdb6873198075c722be20837cb3f757a0b726`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebedb6467515c983f418b9c4af883e13a130480463f372b64fbfdb609c065c`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 239.9 KB (239916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:2c90171350ba7245623727a4df9e3b596c078b2faaf6ca0b82a52b540a0bdde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:def9ca98be8ba4b69562593d869320a43a86c351396ca2e33652cf14b3820a32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb9721979d47090721d09e59e0a40dc85f12c8853416d10f154f85aab5bb6f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f252c279c1245ea47a44d3326988bd3f7aa7e271da8117a505e57f0d5756a010`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 5.5 MB (5494626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ff0f44046e789e0d0b70a8e3fac28f4ae1bbb0e337f66aa29fb6c09c3a9a11`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f617399291fd7fb8a39fa4320a06e71ef72b24bd247a304a0cd591c57ef016f7`  
		Last Modified: Tue, 16 Apr 2024 05:21:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea265c293a70b71c7b25449c823f937f648eaaf482a07495e803b665a2e5f4f`  
		Last Modified: Tue, 16 Apr 2024 05:21:43 GMT  
		Size: 239.5 KB (239492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40162089408f601135275d7d1ff64ffe86d88e12b207a669d1c98053029ca9a`  
		Last Modified: Tue, 16 Apr 2024 05:21:51 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eeb80a3de7d834bac56076aa31e003892ea2357f64a46fd8842e665f9a0f98a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32922113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc0678e65eaed5a11dea215f50e2bd20771e67f59607b1f7c0dfb50425db9e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:37:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:37:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:37:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:37:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced7a6d3abbe464bf762a82a656eac696cb8a1f016f460c22962aaec7f7bcaa1`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 5.5 MB (5474948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf585fd20b0200e660a0939d16828fd20434131110b6dfd0a3f9f3ea1a960d4`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063e9b1fd3a1b1fcdb78293f09bfdb6873198075c722be20837cb3f757a0b726`  
		Last Modified: Tue, 16 Apr 2024 03:39:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebedb6467515c983f418b9c4af883e13a130480463f372b64fbfdb609c065c`  
		Last Modified: Tue, 16 Apr 2024 03:39:02 GMT  
		Size: 239.9 KB (239916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729a8551f3f028911c9fe65b02dc5db64a086b156b178bfbb701fd7608ae789`  
		Last Modified: Tue, 16 Apr 2024 03:39:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:dd28b549dcc0c965c39774c71ab0ee9a245d447e041ff5fa4ececa7f5ee7fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:aacb4187c645fc1181ff2e54d164f05e728d4d07e755274d8abf41558faca7b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34462647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947839795e4e9f44c063cdf65a0a04d1b8535a0815bff651873ae6caa3d4f578`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94664be31c2336989672810e8eae41ae9173296afe40c7a279d0eeff5c886f29`  
		Last Modified: Tue, 16 Apr 2024 05:22:01 GMT  
		Size: 3.8 MB (3767400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350ca5cbbb3e541640b66df0df99da12f628da133fe276d06bf8ffcb5a4cc3a`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bd6793c31737e55e00ab7f914f32a745f2bee1f0f323805b4455e10f289034`  
		Last Modified: Tue, 16 Apr 2024 05:21:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c140cba835ae5b3bae411148fb2e651573b8a9daa82f24a08d99856c66da57f3`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 253.5 KB (253456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d2deebd91609fd76d3275f708bb8b8e76d06648395b462e66b7c5dbbc25ad109
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32395640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580e4117cae9b62176898970adbe2dfd2e0bed789bb52036ec29518cf9608285`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:38:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:38:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:38:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09775ad9e72d75fdb01bd2481e64506d36bd752927db1e12238d48c9ee2ed459`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 3.7 MB (3739473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40afa244e52805c09919d20b2552941cff429b665223738a4114e74b637711f`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49e08caeafc57ea01b64b800cb267d7ae4d8ec5c54975c0e92f6499082888ad`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868a05d69fda4fb84b11fe2d42740101a5cdb3ac6ae6b4217b32871c522b8817`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 253.9 KB (253852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:f84c3060cf4fe27309a30e524a7d58b1b9bc785811140d8773b68360f61cb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f959e102c7e1ca44ef5a659df3638e7df765c0deda408695e5165f87bdf1ada7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34462906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a53656ee1d9a157bb9547425b0a26f146aadfdef634c8a5a3d1ded63cc03b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:20:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 05:20:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 05:20:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:20:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94664be31c2336989672810e8eae41ae9173296afe40c7a279d0eeff5c886f29`  
		Last Modified: Tue, 16 Apr 2024 05:22:01 GMT  
		Size: 3.8 MB (3767400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350ca5cbbb3e541640b66df0df99da12f628da133fe276d06bf8ffcb5a4cc3a`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bd6793c31737e55e00ab7f914f32a745f2bee1f0f323805b4455e10f289034`  
		Last Modified: Tue, 16 Apr 2024 05:21:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c140cba835ae5b3bae411148fb2e651573b8a9daa82f24a08d99856c66da57f3`  
		Last Modified: Tue, 16 Apr 2024 05:22:00 GMT  
		Size: 253.5 KB (253456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5ef2f7826ab3c5a8775ae04f85996abfcc0124d3cd6b3a452cbbd5445f5ced`  
		Last Modified: Tue, 16 Apr 2024 05:22:09 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:824be41a6a3f95926b5ad440687b448bf469a6ab0dc80b49a234121b7b484cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32395897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114b6dfcb1c1445f64f371dcad07f7f59020924cccdd7e5662251fe4c8094578`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:38:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 Apr 2024 03:38:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 Apr 2024 03:38:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:38:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09775ad9e72d75fdb01bd2481e64506d36bd752927db1e12238d48c9ee2ed459`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 3.7 MB (3739473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40afa244e52805c09919d20b2552941cff429b665223738a4114e74b637711f`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49e08caeafc57ea01b64b800cb267d7ae4d8ec5c54975c0e92f6499082888ad`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868a05d69fda4fb84b11fe2d42740101a5cdb3ac6ae6b4217b32871c522b8817`  
		Last Modified: Tue, 16 Apr 2024 03:39:20 GMT  
		Size: 253.9 KB (253852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8377980bff32d6794f1d33e92bd7b0075d35e8348ee9d4d13e03d49f2facd6`  
		Last Modified: Tue, 16 Apr 2024 03:39:28 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:00c4982170e8781a27233d2e2a75d62a89c127ab27ef28de9274a0f1bfa2e36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3ae4cecce765fb1e419ef28e56adbe542743625480bed78a6f59471004cb855
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cbced98ae2907bea19c536757d93411ece53976a1629f42df91b5baa50d1f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269bbc6aa8eea32220fd696f924348d95431a0f432cff2d9c00f3748988b164`  
		Last Modified: Wed, 24 Apr 2024 08:10:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b8ce5dbb664dce1f56363f6b83b4a1976383ad0c34da0d8614af4c3a9d53c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b7159593c55cd9beb5394aa1d4d97239c292a286413e4e239e8bd32a25f81b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9717652fb5e910c228b0dae069d356eb298967cc6440b73745668a420aa2e2a`  
		Last Modified: Wed, 24 Apr 2024 04:42:47 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b0864a7383d8c68c8b1237062b619ecce06878f1742e656c75ee017a823f2905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a96f942a67cc85ef7cb701a6b443e8871de980aa20c777fc7f91299880c742d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120b7317a3b37952c50216ba072c4c503b22262cb884b3866f9fef9b2f40bc05`  
		Last Modified: Wed, 10 Apr 2024 07:25:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:c23e7183f6e52b4e2de181ef64309ab1f08225385dbbc8bc146279fe540dc39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:d6f23bd21819674b163ecf6d32924d910d225448ff3518022e6e4517ff0a2a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c9900b40f363d586167e78d0a9a1b29ca4e78d2add419fce9711a1e87c18d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:09:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:09:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c7dfd06437e02fff0de53af99dc1c00f1276fbb8de9e98d2df6028c40b2335`  
		Last Modified: Wed, 24 Apr 2024 08:10:36 GMT  
		Size: 11.7 MB (11743087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd26b6c5d7f38213336fea92572312ac1832834e19f0645d8013bef455f1c5a`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ebb65957e8e94ec9c3a1b4f90b48587b350b1a5d2e066e0d8870c6438a93ed`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77527b91c07d267eb02ab1842c5fecf2250bc80f9a3071ca1c62fa510ce8a020`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 287.8 KB (287843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:af6c719ace34f312b6740f86c4488f80d6561be1cd851a7308819a050b342097
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64889517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9721214a287b0669996f8064877b5cb2c777c2ca39d4cfe9e1ceeb180e2d343b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:40 GMT
ADD file:58d167eb75df26d368d9ef63173440fad7973e18049ffb23841be9cf507ee614 in / 
# Wed, 24 Apr 2024 04:11:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9914f5e7b79b9a6b9b6b7b39565cb50b06e8e20c51fa6732d67575dc53227762`  
		Last Modified: Wed, 24 Apr 2024 04:16:38 GMT  
		Size: 52.9 MB (52860803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d837feebd2f839b2c1f963eea7ebc9e63d698a5493a5a0400ac20b7f43a2071c`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 11.7 MB (11738112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09977deff1fff17d1ef335ccaf490538bd16ff4a539f9e12bb7c0c3eb4cb0c82`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b96de0d76100592b8310f330c37dad1a727ec9bf5e76ad94c35d9f20a35bc2`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2df9bddff64eec380d895f9b9009fc18c563afecbc57fd1c443e6dbc7820ee`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 288.6 KB (288594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:40f257d65c33a3ca4bac3d5a8dd73fe5f681a38e847a622336bc25777511e50b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65963214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9414f1ef791b35f0e53ec296123bbf56fce785fd4afadd1a5b8dcba95f79646`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fd105449905a0a94707b3cba942d456bf9fe38526a79f7b341be509fb6708`  
		Last Modified: Wed, 10 Apr 2024 07:25:43 GMT  
		Size: 13.1 MB (13128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2827d9b3036a22fee78ea17382d6ba1f730c8c763ef24312843fcaf186c8cc69`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc53f67a234b9e433bd5bc4d7b7c4fe1e787931568ce54d0eb27900e207d2095`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068b92b06f0afc1e120d97fe37e9366d8729e90600f03c95d7ccdbca3a3fd8b8`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 287.8 KB (287757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:b8bbce806a0a49eb1358850b02d5841437015b411a81ecc80519953fa5e712ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:da4dfb4fd57feb809612292068b88cf45248d914f7dbf20b188d1c12dc854a75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998ff6a3fd8de4cba074e06a09d1adb79793ed5a0627c455c9056d68b55e6e10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:09:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:09:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c7dfd06437e02fff0de53af99dc1c00f1276fbb8de9e98d2df6028c40b2335`  
		Last Modified: Wed, 24 Apr 2024 08:10:36 GMT  
		Size: 11.7 MB (11743087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd26b6c5d7f38213336fea92572312ac1832834e19f0645d8013bef455f1c5a`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ebb65957e8e94ec9c3a1b4f90b48587b350b1a5d2e066e0d8870c6438a93ed`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77527b91c07d267eb02ab1842c5fecf2250bc80f9a3071ca1c62fa510ce8a020`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 287.8 KB (287843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1eb88e765e63782a59d495ea7f9b1079764f27094a1479608f41455b5c7f9ef`  
		Last Modified: Wed, 24 Apr 2024 08:10:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8eed19e43fe455a4467dc0964ea15c6a2527e735a32b26147778c5d4e98ba806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64889916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbddc970b69155e7710675b1470b74121ed4abae73cdad8df3316e0680cf6ed9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:40 GMT
ADD file:58d167eb75df26d368d9ef63173440fad7973e18049ffb23841be9cf507ee614 in / 
# Wed, 24 Apr 2024 04:11:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:55 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9914f5e7b79b9a6b9b6b7b39565cb50b06e8e20c51fa6732d67575dc53227762`  
		Last Modified: Wed, 24 Apr 2024 04:16:38 GMT  
		Size: 52.9 MB (52860803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d837feebd2f839b2c1f963eea7ebc9e63d698a5493a5a0400ac20b7f43a2071c`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 11.7 MB (11738112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09977deff1fff17d1ef335ccaf490538bd16ff4a539f9e12bb7c0c3eb4cb0c82`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b96de0d76100592b8310f330c37dad1a727ec9bf5e76ad94c35d9f20a35bc2`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2df9bddff64eec380d895f9b9009fc18c563afecbc57fd1c443e6dbc7820ee`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 288.6 KB (288594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec7a4c6962d047c0b07c813ee90ae3364131902545f2ce9a30b3453030562f8`  
		Last Modified: Wed, 24 Apr 2024 04:43:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d720fce2bfbba32832cc2bf799dd698e43bb233d4a37c2cd4d197b0cb4193b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65963609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f46f2052a62716fe2561cd94f0df4bc0d16574b334e2a01e5d8736e1808ac0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fd105449905a0a94707b3cba942d456bf9fe38526a79f7b341be509fb6708`  
		Last Modified: Wed, 10 Apr 2024 07:25:43 GMT  
		Size: 13.1 MB (13128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2827d9b3036a22fee78ea17382d6ba1f730c8c763ef24312843fcaf186c8cc69`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc53f67a234b9e433bd5bc4d7b7c4fe1e787931568ce54d0eb27900e207d2095`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068b92b06f0afc1e120d97fe37e9366d8729e90600f03c95d7ccdbca3a3fd8b8`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 287.8 KB (287757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a446d0e0f4843ac41fcb1c976e2e429b405f2dc9841ac6c22095f1b59139e6`  
		Last Modified: Wed, 10 Apr 2024 07:25:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
