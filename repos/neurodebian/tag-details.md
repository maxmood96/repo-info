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
$ docker pull neurodebian@sha256:e51b766fc2dbd8bf25107130d3d134404fd4a306caea28dd723d29d720ad0ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:9408c6458846d7c42a21b7c302a322ef199d8344ae1c519c81e970aa329d45f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c705dc58062c3ff83585879d84a591b8da0f602fbc704b07b8eaea2c6d025e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0363adf9305a6b41761d438d2a99d852e8ff75744469ba09ffb36630191c6a2`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 11.5 MB (11462689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9217394c3a8c00efd3ed3df63117ff1d5235d1493d0d9927ece4457ad9643c1`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697199bf9c91bfcc1d3bc1cfcd2bcd5a643b7976d86981f5a8e6c72a1cb97dd0`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82f7b82921a5b3474b30a4c42596d5eb0025120b94f4c4c9f9019497651ac7`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 286.3 KB (286275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c1f16cbc7d1bcc96dabf3be292b695386d113dd9f6641ac53d6214dd474525e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61287919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b927c43cfa476937ffa3952f9fe68f9896e10dd2c6a3e57330b2c9fb455a52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861df767d9558c0b849a1f9d8e7152ef4412cc9cd8d7779f02887e1482df404d`  
		Last Modified: Tue, 04 Jul 2023 04:06:36 GMT  
		Size: 11.4 MB (11426584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf1db022c44ac364b74d3dc15420bbfd4234ce595f93aa6e88357d7764831c`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fb2908699cc879f5983cad2800da4109b3863df1907fbcc836091a72b1c54b`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64c88df5b726c53838a6567c16434972a07a424384ad17628e12ae7e3966db`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 286.5 KB (286542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:17edf5fdb1c9340b0c3b8dd9b9d5729f25efcdca520ce97f7a4b4a064a126617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62739643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7a09275b1d385cec55b03cbf72e51cd4daaf767538b94fa3e70765781b2462`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d955a37bc16f78384964e9fe3eaea19c7ce73126226143d91ad06904f88f6c`  
		Last Modified: Fri, 28 Jul 2023 00:28:21 GMT  
		Size: 11.9 MB (11883326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffc2e83e61fafba4c775d5e49f245f6c41fec6fb974344eba3e8413a9efe79`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982312586fa3fb6b226464fdb7d7012bd3b791fd5861afdf90710edd6eadce`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77d2ebb426ec21ab46e2606841ee798e7cb0ac271b2c9496e806d0796628983`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 286.4 KB (286430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:b30bda47e6eb1ff8c88035abfd72918561ea3376e301b0f83f956fa4a92b48d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:858cd4251e5ccd3fbb654f024e79fe6d3786b31324d61bb2832d6eb00071df8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797808e1fb4f66aa79fb78e8df33ba10bd6cf5312edeefb5670e3937854d6ecf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0363adf9305a6b41761d438d2a99d852e8ff75744469ba09ffb36630191c6a2`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 11.5 MB (11462689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9217394c3a8c00efd3ed3df63117ff1d5235d1493d0d9927ece4457ad9643c1`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697199bf9c91bfcc1d3bc1cfcd2bcd5a643b7976d86981f5a8e6c72a1cb97dd0`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82f7b82921a5b3474b30a4c42596d5eb0025120b94f4c4c9f9019497651ac7`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 286.3 KB (286275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a06c5cf996db9fe8ee9a4f77e2915465281718a38555d47d2a777d5c47be3c`  
		Last Modified: Tue, 04 Jul 2023 13:15:02 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d5edae74ae1b942b9502023f23837e250589e2d6207ea008ffcccacd2a3bddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a893555b6a968518c5160f8448e510094af5263207b10262bad8add5ec68801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861df767d9558c0b849a1f9d8e7152ef4412cc9cd8d7779f02887e1482df404d`  
		Last Modified: Tue, 04 Jul 2023 04:06:36 GMT  
		Size: 11.4 MB (11426584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf1db022c44ac364b74d3dc15420bbfd4234ce595f93aa6e88357d7764831c`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fb2908699cc879f5983cad2800da4109b3863df1907fbcc836091a72b1c54b`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64c88df5b726c53838a6567c16434972a07a424384ad17628e12ae7e3966db`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 286.5 KB (286542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daedea9b78dacce29febd8344cde1d29ea62c63bcf4282f8ca56f870c9892af`  
		Last Modified: Tue, 04 Jul 2023 04:06:44 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e93626359a36a48bcc52dafc8f06c0314f34e2363d5222491aca6992aec03a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfc1e630f7cf429a188bd3ae4877ca5fe4084dec8cbdfb63969279c8e6a03e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d955a37bc16f78384964e9fe3eaea19c7ce73126226143d91ad06904f88f6c`  
		Last Modified: Fri, 28 Jul 2023 00:28:21 GMT  
		Size: 11.9 MB (11883326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffc2e83e61fafba4c775d5e49f245f6c41fec6fb974344eba3e8413a9efe79`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982312586fa3fb6b226464fdb7d7012bd3b791fd5861afdf90710edd6eadce`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77d2ebb426ec21ab46e2606841ee798e7cb0ac271b2c9496e806d0796628983`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 286.4 KB (286430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7712c30fa50f50f5023f34c834fc38657c999b4b7016a15b5456d677e8b50d3d`  
		Last Modified: Fri, 28 Jul 2023 00:28:29 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:dfc9034c40e65e2ef4f7e1e61c897801775326158ff9fd8c5581ecbe54bba8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:17e40ae48b08927ad9f929ce109cd9675c01790b7e6b2fcd9208814796a740d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a8ea646425187442f92e3340a19547676384636a5473b1c73f4a6f80103730`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d223c0d22bd6d70d7de2b9162c0bd070e394cc82d487fc2a3cfc74027821147b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5376d00c3f4c268b392f6ec0525de3ae605083ccb61ad56ac6e05245697a4666`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:904deac4d3c48e2a034f547b054c5f3a78bdd19c1f294559802f88db89107a1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c5dd0312e6960237633d471619e956d6e2cdad37b9664db832df9a44c78c4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:8619e94863a7e6120b37060f2e45d4a3e6b1ecc47f30e5418cccbb58bc5419c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a3664b64f74716206ce118015164b4e83c8e03236dd79d6d6b5dda5ca4df692f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc8ae09bd086d04e8614e6632e92cb0040ca7d7d53995afa40f6ddcc2dc8cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead5308361a9d838b9d3e134bcfa5c09b2c664c755ddeff7d08096c61ae8edf`  
		Last Modified: Tue, 04 Jul 2023 13:14:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c79f16dd43a41a53551f24e44bcab68f7e25aae050b34270b4b6d9d4fdf6c8df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45d0d53778ee619fe21002c84a503535d661328def02ebceb9889ffad4bedc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115fb106a48cee105f8bc705681ef1cd600e4ae858f2f6f1f40215cad7c61e37`  
		Last Modified: Tue, 04 Jul 2023 04:06:25 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:024bac8c6bfc8fc3756ad87e1bd83504396ccb407abcbcb13247b75d4e1cfba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68063188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867cccb166e3bf525588dee87b37cd135772a137c84008d25278eb29cdc5c08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98dfa587a22d76f618fe45988114cfa1854794cb5b7c2f39f42e05b491466b`  
		Last Modified: Fri, 28 Jul 2023 00:28:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:ad5dee6ca3803ad8587cf6e057ecff1e7851b8f12ef03147b9b6469362f514e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:deb93f3307d27c4de1500e2337a2a4caf22660c9690a45f2ab7fdae7aac64bdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05a4895e0373b829bab24adb3aa689651e14f8fddace44ec76f40a59dfb8e50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51501b2dee2f897cc32e530eff98a547dfd01a8079f04a202ef8264e6b457765`  
		Last Modified: Tue, 04 Jul 2023 13:14:15 GMT  
		Size: 10.5 MB (10504493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17e41e68dcc386b939fa71d4bf957ea44f5852396c9b08aba9f99855b080a55`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f610d075a131b52d3ec952ea5a91a9ceef4812f2e5ae485b766b22fadbaa205`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9102b0aceadfee304d5111cc55897e204d7b8a6e7c93990b1b02004a9fcb74b`  
		Last Modified: Tue, 04 Jul 2023 13:14:14 GMT  
		Size: 304.4 KB (304418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7e51082265a3937a16d07b925552350453ca7571100b093c6b66a3a57decc4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60055385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec2246abc1bd36aa1deb09f3f9098174d3eec4c5b7ac90d0f76fac8e0652923`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:59 GMT
ADD file:a61276f534601d7b193af24e35c16b73a2913511d2b1ad997c9a8cb907685257 in / 
# Tue, 04 Jul 2023 01:58:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:03:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5e2555ae6edde2e7933c533234cb224b6d7ef3a3c90041851e31fe29ab7197c9`  
		Last Modified: Tue, 04 Jul 2023 02:02:18 GMT  
		Size: 49.2 MB (49238644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d25790825e41444bb69f0bb17e2b5df75a15de0298dcf3989655d6eb7b75`  
		Last Modified: Tue, 04 Jul 2023 04:05:58 GMT  
		Size: 10.5 MB (10510379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461e85bf7126aee3bc32065bc89583822e1a8475ec7944d58970c9680985d399`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11727db7413c0797ab3185cc121327037478eeadfd63bc1b28ca6dd4e4c61d32`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949944ffb995b80048a3b556a86dc236acadcc632d995a23e76d0665b23d402f`  
		Last Modified: Tue, 04 Jul 2023 04:05:57 GMT  
		Size: 304.4 KB (304351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:72904dedb6d4a2d924e34eede70dfacb3a70e5fab24b283c4db67261e4ee6cec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b99350bc621c055021846aaeb1b5dfdcb2998d8abf1f01164c012bfa36f82e4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:29 GMT
ADD file:a4caa39d69b463e1f2628cb32f33763655fd873129cf98dd26c431183c53b6d6 in / 
# Thu, 27 Jul 2023 23:39:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b5eb5e3691ae17e5aaa83c175523a7a17d58c9c61698ed6bba826d9acc809ec`  
		Last Modified: Thu, 27 Jul 2023 23:44:34 GMT  
		Size: 51.3 MB (51255427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9546696cfc41507830169b067ee13ec325fe6700c48dd0cbc5305fc2e7ca5`  
		Last Modified: Fri, 28 Jul 2023 00:27:38 GMT  
		Size: 10.9 MB (10868456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248c8a0326f730ee26d03c9b5aa23067f9422968d77aba57711075b6255677b0`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b42292c3c0cc2f12375716e1845d09e94189548afab4c0355ab61f7475c862`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50994e1702ad118d42ed1c2ed85ff7a2cf5a158ca8cbd886ee714d44efa66a7`  
		Last Modified: Fri, 28 Jul 2023 00:27:37 GMT  
		Size: 304.5 KB (304539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:700a098f6f3ea0f94862e9f1d30256406f1f95ad40e42874b329e63fc39e583b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e7d437647ec774cca69b084a8d516096651f7044bc554b9abb8bae3bc52afa89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da056298eb82b97c4a326187bd9c36a3fecb79dede9ca259230347bda2271e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51501b2dee2f897cc32e530eff98a547dfd01a8079f04a202ef8264e6b457765`  
		Last Modified: Tue, 04 Jul 2023 13:14:15 GMT  
		Size: 10.5 MB (10504493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17e41e68dcc386b939fa71d4bf957ea44f5852396c9b08aba9f99855b080a55`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f610d075a131b52d3ec952ea5a91a9ceef4812f2e5ae485b766b22fadbaa205`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9102b0aceadfee304d5111cc55897e204d7b8a6e7c93990b1b02004a9fcb74b`  
		Last Modified: Tue, 04 Jul 2023 13:14:14 GMT  
		Size: 304.4 KB (304418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828c12709f45803586fd2e5271c553f3132d49e98d2d7011cd1e0236bea25d29`  
		Last Modified: Tue, 04 Jul 2023 13:14:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a0252cd512d037e3053d4cf4e540ee0f877b320a5079e0e861ae03254d2e19da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60055743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4010dc112ef79880088a91a195ab5203a453d5ce5506868767a836459b270`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:59 GMT
ADD file:a61276f534601d7b193af24e35c16b73a2913511d2b1ad997c9a8cb907685257 in / 
# Tue, 04 Jul 2023 01:58:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:03:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5e2555ae6edde2e7933c533234cb224b6d7ef3a3c90041851e31fe29ab7197c9`  
		Last Modified: Tue, 04 Jul 2023 02:02:18 GMT  
		Size: 49.2 MB (49238644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d25790825e41444bb69f0bb17e2b5df75a15de0298dcf3989655d6eb7b75`  
		Last Modified: Tue, 04 Jul 2023 04:05:58 GMT  
		Size: 10.5 MB (10510379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461e85bf7126aee3bc32065bc89583822e1a8475ec7944d58970c9680985d399`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11727db7413c0797ab3185cc121327037478eeadfd63bc1b28ca6dd4e4c61d32`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949944ffb995b80048a3b556a86dc236acadcc632d995a23e76d0665b23d402f`  
		Last Modified: Tue, 04 Jul 2023 04:05:57 GMT  
		Size: 304.4 KB (304351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a954847d698dbc608e12c380f76e1b5aa3f1f166e792278130cd6bec8eef7e1`  
		Last Modified: Tue, 04 Jul 2023 04:06:06 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:154a6e8bf757c2a56521e555e827e8fae62e40bf29faf9ddb9394675c5121665
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075469979bba1f5bb176d7fd582c03fd8e81905fe4f61b9db283c17dd2a6825e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:29 GMT
ADD file:a4caa39d69b463e1f2628cb32f33763655fd873129cf98dd26c431183c53b6d6 in / 
# Thu, 27 Jul 2023 23:39:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4b5eb5e3691ae17e5aaa83c175523a7a17d58c9c61698ed6bba826d9acc809ec`  
		Last Modified: Thu, 27 Jul 2023 23:44:34 GMT  
		Size: 51.3 MB (51255427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9546696cfc41507830169b067ee13ec325fe6700c48dd0cbc5305fc2e7ca5`  
		Last Modified: Fri, 28 Jul 2023 00:27:38 GMT  
		Size: 10.9 MB (10868456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248c8a0326f730ee26d03c9b5aa23067f9422968d77aba57711075b6255677b0`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b42292c3c0cc2f12375716e1845d09e94189548afab4c0355ab61f7475c862`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50994e1702ad118d42ed1c2ed85ff7a2cf5a158ca8cbd886ee714d44efa66a7`  
		Last Modified: Fri, 28 Jul 2023 00:27:37 GMT  
		Size: 304.5 KB (304539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c3b2bb602d2b7f4c6da3126c6bbbf3940a26e98c1aeb3045a3fb2f218da43d`  
		Last Modified: Fri, 28 Jul 2023 00:27:47 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:d702c4ef3b26b10c78a4c77d637b399f2744a44e85d7d1e95acf992ca60c2799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:1c43aa6f4d4b16647b59a440068e1fb169a90f807f60c7f5406e9460e1bf925e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34315846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67417a0b461fbea4a9c9f18a4543a5ecc99d8bc74d268879607cdf1050c923f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a302d555069890ebb36b070cd326cac9483fa7cb0be84d036adc6d9cafaef1f`  
		Last Modified: Tue, 04 Jul 2023 13:13:40 GMT  
		Size: 5.5 MB (5494700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82e637645e32971a8fadb64831e8be1e58872cc0a856f5c3bc1d0e9645f688e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029aea76fbed8bf5fd4b30bfb395d8fad60024fa01b46c2eabe7407427e51cea`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525085905b04c4b6c0016c54ce9bf5ff65b825548d8627f965637feb66affa5e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 239.1 KB (239121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cb1408d965364bde6b5e3515ee76bbebecc189b1237db6eec1c485c397e3d965
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32915183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d4b0e079fc0de2d459067e9c935f4ece4cab4eb81c2602f4c1566b1eb47fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:02:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:02:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:02:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02bddd63143ca4ce20f8dd8832f98797baa25ce22f7e19532c5f43b95a6903d`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 5.5 MB (5475129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d569cdc258fb1dfe7b8edec6fc4ea0a13c5218c8d485f2b00eb2231a05adb5a`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80dab06bbbea579a049caebec835872a366b6f05eae4a088d0894534dde1d98`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f259a30976e0cc7a20d3bad8fa982bae4253b72be2fc66b4e5e24aa6998f64`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 239.7 KB (239710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:389fcc32f094ed06518a9416306f5dfc3b8a5057dcf56eb334c022420e726be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1020aff8a2b05abc2c4b91235f346f33da55dfffbc978210adc2427791e8d5df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd914ec98278af185c21b30a911ab26e016f999df4b594eff8b8e854581b2703`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a302d555069890ebb36b070cd326cac9483fa7cb0be84d036adc6d9cafaef1f`  
		Last Modified: Tue, 04 Jul 2023 13:13:40 GMT  
		Size: 5.5 MB (5494700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82e637645e32971a8fadb64831e8be1e58872cc0a856f5c3bc1d0e9645f688e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029aea76fbed8bf5fd4b30bfb395d8fad60024fa01b46c2eabe7407427e51cea`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525085905b04c4b6c0016c54ce9bf5ff65b825548d8627f965637feb66affa5e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 239.1 KB (239121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17414e278d1d2b6ee5faad416671884e44cf76a0b766820af26f97a386241d7`  
		Last Modified: Tue, 04 Jul 2023 13:13:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f57a51064310824edf3301b7d9a77a465fadcfdb81158255a7efdd643223b748
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32915438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61681f5228478c2a28043ef7811d57357acb86748737342e39805e877b730f73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:02:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:02:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:02:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:02:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02bddd63143ca4ce20f8dd8832f98797baa25ce22f7e19532c5f43b95a6903d`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 5.5 MB (5475129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d569cdc258fb1dfe7b8edec6fc4ea0a13c5218c8d485f2b00eb2231a05adb5a`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80dab06bbbea579a049caebec835872a366b6f05eae4a088d0894534dde1d98`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f259a30976e0cc7a20d3bad8fa982bae4253b72be2fc66b4e5e24aa6998f64`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 239.7 KB (239710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ca9babba4cd0309d441b839e5c62a5d57be6537e0138d8738759b89ea752be`  
		Last Modified: Tue, 04 Jul 2023 04:05:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:191fec3216a692f829a5014024649eaf52df8b851c33a1e240c776a1242bc7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:0dddb9c58d26e4c5aa1381b60d6c956a658957bcb6d45ec8dc71a41d86fb4983
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5b16817fd6ac863f72c4d1879ef8fb975ce97de3d4453db80f3052f97a288`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3084125742d0581ee9ff82c21a6b489f43cf4e3e26117810ab2889ab6a4f00`  
		Last Modified: Tue, 04 Jul 2023 13:13:57 GMT  
		Size: 3.8 MB (3766304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255c4d0a7a145ca1ed2a4ccd12bd5680381a2e29a3b26c58b3527a9f992de3cd`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1321fcfa793b7d739b03fc0d89858434cab1ac41dfd2b170fc21b3240aad3b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ee1bf3076f23c0c8acdc198cad12b7da1546abc2a7a4e33e2766342714bf6b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 258.8 KB (258840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b2af04eaa6241fdc0f627b88d040ec44f5a082c3c94fa23b91a3fdc1c9dd5969
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32393179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63bd08b7cebbaf9f01a44f2e743023b2d443987282b377f237bc468596bd59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:03:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e82ac260be4046395c46fca73c81e7092d5db44e0639a55cd7f078bc67892`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 3.7 MB (3739904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b7c5d8a744c2070daee97b2d73e804013e8c69cdbcd8a57771d63851935f4`  
		Last Modified: Tue, 04 Jul 2023 04:05:37 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f7a318245f4a1cf0358726cf34dd020c5ebedb50206075beebb0d370760bb`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33822f30aabf33f7963ace371532a97547b3eddcc696ebc78b4b79649f746787`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 260.3 KB (260256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:35c1ea3ea35f91c1a474f2fd78f107b7739c49dc69cd1ae62ac78bf05b53c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c7f3c031b0c94e4c82d058a79999b2422c7306a5fcaa72e0caa692e7f326113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07082726d621d0dccb475a0da0b40ade8eda0efc77872c6ca318ae813182f1f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3084125742d0581ee9ff82c21a6b489f43cf4e3e26117810ab2889ab6a4f00`  
		Last Modified: Tue, 04 Jul 2023 13:13:57 GMT  
		Size: 3.8 MB (3766304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255c4d0a7a145ca1ed2a4ccd12bd5680381a2e29a3b26c58b3527a9f992de3cd`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1321fcfa793b7d739b03fc0d89858434cab1ac41dfd2b170fc21b3240aad3b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ee1bf3076f23c0c8acdc198cad12b7da1546abc2a7a4e33e2766342714bf6b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 258.8 KB (258840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170816573dbaf7412a7c85c1e23777dbab9104015b2beeddc9203e7ca964dff3`  
		Last Modified: Tue, 04 Jul 2023 13:14:05 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e176b3b6e55f9aa5b34103e5922f9fb86ace9f918cc8cb88dc4ae1e6f9458dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32393436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c18e0d7d850ab58b32a4ee7ceb4e5b7ec49e2e7f1de7a255ac070dac688a30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:03:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e82ac260be4046395c46fca73c81e7092d5db44e0639a55cd7f078bc67892`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 3.7 MB (3739904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b7c5d8a744c2070daee97b2d73e804013e8c69cdbcd8a57771d63851935f4`  
		Last Modified: Tue, 04 Jul 2023 04:05:37 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f7a318245f4a1cf0358726cf34dd020c5ebedb50206075beebb0d370760bb`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33822f30aabf33f7963ace371532a97547b3eddcc696ebc78b4b79649f746787`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 260.3 KB (260256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9674aaca2237100d14c918077fc864d6cd4bc5d584a967f5eb3286a8e891fd`  
		Last Modified: Tue, 04 Jul 2023 04:05:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:dfc9034c40e65e2ef4f7e1e61c897801775326158ff9fd8c5581ecbe54bba8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:17e40ae48b08927ad9f929ce109cd9675c01790b7e6b2fcd9208814796a740d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a8ea646425187442f92e3340a19547676384636a5473b1c73f4a6f80103730`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d223c0d22bd6d70d7de2b9162c0bd070e394cc82d487fc2a3cfc74027821147b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5376d00c3f4c268b392f6ec0525de3ae605083ccb61ad56ac6e05245697a4666`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:904deac4d3c48e2a034f547b054c5f3a78bdd19c1f294559802f88db89107a1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c5dd0312e6960237633d471619e956d6e2cdad37b9664db832df9a44c78c4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:623666c0822d330a48f6a9f89e6b6bc6abf8602ae7b2a8cb474642a4e6605f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:8ff70d7e6535a394265e18711bf2bed554d01f814616d3594576fe4b9db44b0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61239793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fadf68870c491b08605f0009960823d4a0a85e1092c69e82faed8c6326acffc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:13:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:13:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:13:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb16e254dc465c5893d6aeff18369662c8044c54f5c83bf08e442d3d0e121f9`  
		Last Modified: Tue, 04 Jul 2023 13:15:12 GMT  
		Size: 11.5 MB (11475625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b603511d97f2386a8ab3b1db7d9dee4088d3d7c6ffb7a26eac6df5aecbbbee9a`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0aabc1a8108a3a7a5ff6a06688362f7e3ef8a054d2681c47f391601395823`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b7ca55d70bd6c3371f54cd1a75a9fb89ba8e8dbbe6ccbd1edefcc58a520464`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 286.2 KB (286218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:26c493c1871d1cc2caeea5e545e5b2c631929abafb545ecf4957f7b83bf1d0fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61210069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed1e107f267b91f3daa33a4eda91c308b6f77e77317ed626441ad1586d6f3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:49 GMT
ADD file:2c2c0588b93f9af7d93f19033795edf9e61a692ff56e65d9e9500915276782c9 in / 
# Tue, 04 Jul 2023 01:58:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1b52151d5bb774f3680f8697c343bae1b64b7308354db57dc6bbeb7d65d0964`  
		Last Modified: Tue, 04 Jul 2023 02:03:59 GMT  
		Size: 49.5 MB (49482570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5339efefb62ae359de57f76cc7c3abcddcabc209998c1163785b6d94dc057f0`  
		Last Modified: Tue, 04 Jul 2023 04:06:54 GMT  
		Size: 11.4 MB (11438867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178be8dad69d8c80854a04cb17b21e471f0bbf2ae4a86464ff32e9970e33378`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58976cca48524ce8dd67a80e399d538d3fbef3d3f6162f96d5178183a1549de`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2da580b40ebc70f119ee6e12f89303261f8bdc03a02215e3d987f228e3067b`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 286.6 KB (286624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:8de06f8e3299736ad3ce983e2f9ef19372787757135eb8387320d7ddd052b938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62861896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edec188a835e550ecca1cd7eacd796bc31389979e13e512a9f4cdd132aede9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:29 GMT
ADD file:f80411b5104f2db2a54b08d2fb1755fdc31ca042be72f3b3165979726a335a02 in / 
# Thu, 27 Jul 2023 23:40:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:27:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:27:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:27:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0cecd19dc43936e99574e6dd27db4982f7645bc158ab590b29cfc15e2c4f23a`  
		Last Modified: Thu, 27 Jul 2023 23:46:36 GMT  
		Size: 50.5 MB (50473688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c7f2e1cde6914fe23854b6902ae0a8fff8f1f0a5d8ba072e01d078cdfdeec8`  
		Last Modified: Fri, 28 Jul 2023 00:28:39 GMT  
		Size: 12.1 MB (12099954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aabb1338e505c29ec6fa33c90e2e7459a0587bb0bb0975ecdf310f2e15df2f7`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153131614253cf9252fcb4ccf05b60ad52afc2fb119dd115527e601b2b76d46`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd2ce3714afd4b50e39cf699cef7cd43812425d907d1160bc9bbf94b9c9d10`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 286.2 KB (286244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:1ae453421a71699345e895c1129a8fb503daf7982c5fec4c51523c11d229034a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:62820e5ff8aec5ab9d872ccc3e1f5a64ec85fc4849ebeae73e58d54b61c3ba95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8d8a0b6900a2051209904878057de68e54caff42553a1ff3f8b4ddf27c7b22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:13:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:13:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:13:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb16e254dc465c5893d6aeff18369662c8044c54f5c83bf08e442d3d0e121f9`  
		Last Modified: Tue, 04 Jul 2023 13:15:12 GMT  
		Size: 11.5 MB (11475625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b603511d97f2386a8ab3b1db7d9dee4088d3d7c6ffb7a26eac6df5aecbbbee9a`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0aabc1a8108a3a7a5ff6a06688362f7e3ef8a054d2681c47f391601395823`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b7ca55d70bd6c3371f54cd1a75a9fb89ba8e8dbbe6ccbd1edefcc58a520464`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 286.2 KB (286218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df3a10e230ea51013bab8caba261407bfa609c9c15f5f03018a2b73e96d410`  
		Last Modified: Tue, 04 Jul 2023 13:15:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6b94c90aadb2c204e7bd6394e5985e1770861ea491ebc26338ad53013efbabbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61210466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb194f65a1b70c1548887e06ca9e554d24f961aa84bb8e8e8af92a8eb54eba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:49 GMT
ADD file:2c2c0588b93f9af7d93f19033795edf9e61a692ff56e65d9e9500915276782c9 in / 
# Tue, 04 Jul 2023 01:58:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d1b52151d5bb774f3680f8697c343bae1b64b7308354db57dc6bbeb7d65d0964`  
		Last Modified: Tue, 04 Jul 2023 02:03:59 GMT  
		Size: 49.5 MB (49482570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5339efefb62ae359de57f76cc7c3abcddcabc209998c1163785b6d94dc057f0`  
		Last Modified: Tue, 04 Jul 2023 04:06:54 GMT  
		Size: 11.4 MB (11438867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178be8dad69d8c80854a04cb17b21e471f0bbf2ae4a86464ff32e9970e33378`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58976cca48524ce8dd67a80e399d538d3fbef3d3f6162f96d5178183a1549de`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2da580b40ebc70f119ee6e12f89303261f8bdc03a02215e3d987f228e3067b`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 286.6 KB (286624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c5b6175ba7c9e5a7370cd8b462ba718539b94f4b43ee91c28ceb2d38e0d95d`  
		Last Modified: Tue, 04 Jul 2023 04:07:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1f39faf94344b4725d91ca24cea26a9ce1a6a1a21cabe07df459db3cb190efc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62862289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a609a69a151edf20931cdebcdde41828431bb1b08d618a64071dcec52cfe0adc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:29 GMT
ADD file:f80411b5104f2db2a54b08d2fb1755fdc31ca042be72f3b3165979726a335a02 in / 
# Thu, 27 Jul 2023 23:40:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:27:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:27:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:27:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0cecd19dc43936e99574e6dd27db4982f7645bc158ab590b29cfc15e2c4f23a`  
		Last Modified: Thu, 27 Jul 2023 23:46:36 GMT  
		Size: 50.5 MB (50473688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c7f2e1cde6914fe23854b6902ae0a8fff8f1f0a5d8ba072e01d078cdfdeec8`  
		Last Modified: Fri, 28 Jul 2023 00:28:39 GMT  
		Size: 12.1 MB (12099954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aabb1338e505c29ec6fa33c90e2e7459a0587bb0bb0975ecdf310f2e15df2f7`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153131614253cf9252fcb4ccf05b60ad52afc2fb119dd115527e601b2b76d46`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd2ce3714afd4b50e39cf699cef7cd43812425d907d1160bc9bbf94b9c9d10`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 286.2 KB (286244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd05bf720bdf0a12d29d89a095980633f86f45b748e8ec46dfa8715f06ce9ba5`  
		Last Modified: Fri, 28 Jul 2023 00:28:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:ad5dee6ca3803ad8587cf6e057ecff1e7851b8f12ef03147b9b6469362f514e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:deb93f3307d27c4de1500e2337a2a4caf22660c9690a45f2ab7fdae7aac64bdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05a4895e0373b829bab24adb3aa689651e14f8fddace44ec76f40a59dfb8e50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51501b2dee2f897cc32e530eff98a547dfd01a8079f04a202ef8264e6b457765`  
		Last Modified: Tue, 04 Jul 2023 13:14:15 GMT  
		Size: 10.5 MB (10504493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17e41e68dcc386b939fa71d4bf957ea44f5852396c9b08aba9f99855b080a55`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f610d075a131b52d3ec952ea5a91a9ceef4812f2e5ae485b766b22fadbaa205`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9102b0aceadfee304d5111cc55897e204d7b8a6e7c93990b1b02004a9fcb74b`  
		Last Modified: Tue, 04 Jul 2023 13:14:14 GMT  
		Size: 304.4 KB (304418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7e51082265a3937a16d07b925552350453ca7571100b093c6b66a3a57decc4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60055385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec2246abc1bd36aa1deb09f3f9098174d3eec4c5b7ac90d0f76fac8e0652923`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:59 GMT
ADD file:a61276f534601d7b193af24e35c16b73a2913511d2b1ad997c9a8cb907685257 in / 
# Tue, 04 Jul 2023 01:58:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:03:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5e2555ae6edde2e7933c533234cb224b6d7ef3a3c90041851e31fe29ab7197c9`  
		Last Modified: Tue, 04 Jul 2023 02:02:18 GMT  
		Size: 49.2 MB (49238644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d25790825e41444bb69f0bb17e2b5df75a15de0298dcf3989655d6eb7b75`  
		Last Modified: Tue, 04 Jul 2023 04:05:58 GMT  
		Size: 10.5 MB (10510379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461e85bf7126aee3bc32065bc89583822e1a8475ec7944d58970c9680985d399`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11727db7413c0797ab3185cc121327037478eeadfd63bc1b28ca6dd4e4c61d32`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949944ffb995b80048a3b556a86dc236acadcc632d995a23e76d0665b23d402f`  
		Last Modified: Tue, 04 Jul 2023 04:05:57 GMT  
		Size: 304.4 KB (304351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:72904dedb6d4a2d924e34eede70dfacb3a70e5fab24b283c4db67261e4ee6cec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b99350bc621c055021846aaeb1b5dfdcb2998d8abf1f01164c012bfa36f82e4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:29 GMT
ADD file:a4caa39d69b463e1f2628cb32f33763655fd873129cf98dd26c431183c53b6d6 in / 
# Thu, 27 Jul 2023 23:39:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b5eb5e3691ae17e5aaa83c175523a7a17d58c9c61698ed6bba826d9acc809ec`  
		Last Modified: Thu, 27 Jul 2023 23:44:34 GMT  
		Size: 51.3 MB (51255427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9546696cfc41507830169b067ee13ec325fe6700c48dd0cbc5305fc2e7ca5`  
		Last Modified: Fri, 28 Jul 2023 00:27:38 GMT  
		Size: 10.9 MB (10868456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248c8a0326f730ee26d03c9b5aa23067f9422968d77aba57711075b6255677b0`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b42292c3c0cc2f12375716e1845d09e94189548afab4c0355ab61f7475c862`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50994e1702ad118d42ed1c2ed85ff7a2cf5a158ca8cbd886ee714d44efa66a7`  
		Last Modified: Fri, 28 Jul 2023 00:27:37 GMT  
		Size: 304.5 KB (304539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:700a098f6f3ea0f94862e9f1d30256406f1f95ad40e42874b329e63fc39e583b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e7d437647ec774cca69b084a8d516096651f7044bc554b9abb8bae3bc52afa89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da056298eb82b97c4a326187bd9c36a3fecb79dede9ca259230347bda2271e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51501b2dee2f897cc32e530eff98a547dfd01a8079f04a202ef8264e6b457765`  
		Last Modified: Tue, 04 Jul 2023 13:14:15 GMT  
		Size: 10.5 MB (10504493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17e41e68dcc386b939fa71d4bf957ea44f5852396c9b08aba9f99855b080a55`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f610d075a131b52d3ec952ea5a91a9ceef4812f2e5ae485b766b22fadbaa205`  
		Last Modified: Tue, 04 Jul 2023 13:14:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9102b0aceadfee304d5111cc55897e204d7b8a6e7c93990b1b02004a9fcb74b`  
		Last Modified: Tue, 04 Jul 2023 13:14:14 GMT  
		Size: 304.4 KB (304418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828c12709f45803586fd2e5271c553f3132d49e98d2d7011cd1e0236bea25d29`  
		Last Modified: Tue, 04 Jul 2023 13:14:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a0252cd512d037e3053d4cf4e540ee0f877b320a5079e0e861ae03254d2e19da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60055743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4010dc112ef79880088a91a195ab5203a453d5ce5506868767a836459b270`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:59 GMT
ADD file:a61276f534601d7b193af24e35c16b73a2913511d2b1ad997c9a8cb907685257 in / 
# Tue, 04 Jul 2023 01:58:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:03:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5e2555ae6edde2e7933c533234cb224b6d7ef3a3c90041851e31fe29ab7197c9`  
		Last Modified: Tue, 04 Jul 2023 02:02:18 GMT  
		Size: 49.2 MB (49238644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d25790825e41444bb69f0bb17e2b5df75a15de0298dcf3989655d6eb7b75`  
		Last Modified: Tue, 04 Jul 2023 04:05:58 GMT  
		Size: 10.5 MB (10510379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461e85bf7126aee3bc32065bc89583822e1a8475ec7944d58970c9680985d399`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11727db7413c0797ab3185cc121327037478eeadfd63bc1b28ca6dd4e4c61d32`  
		Last Modified: Tue, 04 Jul 2023 04:05:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949944ffb995b80048a3b556a86dc236acadcc632d995a23e76d0665b23d402f`  
		Last Modified: Tue, 04 Jul 2023 04:05:57 GMT  
		Size: 304.4 KB (304351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a954847d698dbc608e12c380f76e1b5aa3f1f166e792278130cd6bec8eef7e1`  
		Last Modified: Tue, 04 Jul 2023 04:06:06 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:154a6e8bf757c2a56521e555e827e8fae62e40bf29faf9ddb9394675c5121665
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075469979bba1f5bb176d7fd582c03fd8e81905fe4f61b9db283c17dd2a6825e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:29 GMT
ADD file:a4caa39d69b463e1f2628cb32f33763655fd873129cf98dd26c431183c53b6d6 in / 
# Thu, 27 Jul 2023 23:39:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4b5eb5e3691ae17e5aaa83c175523a7a17d58c9c61698ed6bba826d9acc809ec`  
		Last Modified: Thu, 27 Jul 2023 23:44:34 GMT  
		Size: 51.3 MB (51255427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9546696cfc41507830169b067ee13ec325fe6700c48dd0cbc5305fc2e7ca5`  
		Last Modified: Fri, 28 Jul 2023 00:27:38 GMT  
		Size: 10.9 MB (10868456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248c8a0326f730ee26d03c9b5aa23067f9422968d77aba57711075b6255677b0`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b42292c3c0cc2f12375716e1845d09e94189548afab4c0355ab61f7475c862`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50994e1702ad118d42ed1c2ed85ff7a2cf5a158ca8cbd886ee714d44efa66a7`  
		Last Modified: Fri, 28 Jul 2023 00:27:37 GMT  
		Size: 304.5 KB (304539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c3b2bb602d2b7f4c6da3126c6bbbf3940a26e98c1aeb3045a3fb2f218da43d`  
		Last Modified: Fri, 28 Jul 2023 00:27:47 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:dfc9034c40e65e2ef4f7e1e61c897801775326158ff9fd8c5581ecbe54bba8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:17e40ae48b08927ad9f929ce109cd9675c01790b7e6b2fcd9208814796a740d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a8ea646425187442f92e3340a19547676384636a5473b1c73f4a6f80103730`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d223c0d22bd6d70d7de2b9162c0bd070e394cc82d487fc2a3cfc74027821147b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5376d00c3f4c268b392f6ec0525de3ae605083ccb61ad56ac6e05245697a4666`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:904deac4d3c48e2a034f547b054c5f3a78bdd19c1f294559802f88db89107a1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68062828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c5dd0312e6960237633d471619e956d6e2cdad37b9664db832df9a44c78c4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:8619e94863a7e6120b37060f2e45d4a3e6b1ecc47f30e5418cccbb58bc5419c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a3664b64f74716206ce118015164b4e83c8e03236dd79d6d6b5dda5ca4df692f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc8ae09bd086d04e8614e6632e92cb0040ca7d7d53995afa40f6ddcc2dc8cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead5308361a9d838b9d3e134bcfa5c09b2c664c755ddeff7d08096c61ae8edf`  
		Last Modified: Tue, 04 Jul 2023 13:14:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c79f16dd43a41a53551f24e44bcab68f7e25aae050b34270b4b6d9d4fdf6c8df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45d0d53778ee619fe21002c84a503535d661328def02ebceb9889ffad4bedc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115fb106a48cee105f8bc705681ef1cd600e4ae858f2f6f1f40215cad7c61e37`  
		Last Modified: Tue, 04 Jul 2023 04:06:25 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:024bac8c6bfc8fc3756ad87e1bd83504396ccb407abcbcb13247b75d4e1cfba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68063188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867cccb166e3bf525588dee87b37cd135772a137c84008d25278eb29cdc5c08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98dfa587a22d76f618fe45988114cfa1854794cb5b7c2f39f42e05b491466b`  
		Last Modified: Fri, 28 Jul 2023 00:28:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:e51b766fc2dbd8bf25107130d3d134404fd4a306caea28dd723d29d720ad0ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:9408c6458846d7c42a21b7c302a322ef199d8344ae1c519c81e970aa329d45f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c705dc58062c3ff83585879d84a591b8da0f602fbc704b07b8eaea2c6d025e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0363adf9305a6b41761d438d2a99d852e8ff75744469ba09ffb36630191c6a2`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 11.5 MB (11462689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9217394c3a8c00efd3ed3df63117ff1d5235d1493d0d9927ece4457ad9643c1`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697199bf9c91bfcc1d3bc1cfcd2bcd5a643b7976d86981f5a8e6c72a1cb97dd0`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82f7b82921a5b3474b30a4c42596d5eb0025120b94f4c4c9f9019497651ac7`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 286.3 KB (286275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c1f16cbc7d1bcc96dabf3be292b695386d113dd9f6641ac53d6214dd474525e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61287919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b927c43cfa476937ffa3952f9fe68f9896e10dd2c6a3e57330b2c9fb455a52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861df767d9558c0b849a1f9d8e7152ef4412cc9cd8d7779f02887e1482df404d`  
		Last Modified: Tue, 04 Jul 2023 04:06:36 GMT  
		Size: 11.4 MB (11426584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf1db022c44ac364b74d3dc15420bbfd4234ce595f93aa6e88357d7764831c`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fb2908699cc879f5983cad2800da4109b3863df1907fbcc836091a72b1c54b`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64c88df5b726c53838a6567c16434972a07a424384ad17628e12ae7e3966db`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 286.5 KB (286542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:17edf5fdb1c9340b0c3b8dd9b9d5729f25efcdca520ce97f7a4b4a064a126617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62739643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7a09275b1d385cec55b03cbf72e51cd4daaf767538b94fa3e70765781b2462`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d955a37bc16f78384964e9fe3eaea19c7ce73126226143d91ad06904f88f6c`  
		Last Modified: Fri, 28 Jul 2023 00:28:21 GMT  
		Size: 11.9 MB (11883326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffc2e83e61fafba4c775d5e49f245f6c41fec6fb974344eba3e8413a9efe79`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982312586fa3fb6b226464fdb7d7012bd3b791fd5861afdf90710edd6eadce`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77d2ebb426ec21ab46e2606841ee798e7cb0ac271b2c9496e806d0796628983`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 286.4 KB (286430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:b30bda47e6eb1ff8c88035abfd72918561ea3376e301b0f83f956fa4a92b48d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:858cd4251e5ccd3fbb654f024e79fe6d3786b31324d61bb2832d6eb00071df8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797808e1fb4f66aa79fb78e8df33ba10bd6cf5312edeefb5670e3937854d6ecf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0363adf9305a6b41761d438d2a99d852e8ff75744469ba09ffb36630191c6a2`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 11.5 MB (11462689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9217394c3a8c00efd3ed3df63117ff1d5235d1493d0d9927ece4457ad9643c1`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697199bf9c91bfcc1d3bc1cfcd2bcd5a643b7976d86981f5a8e6c72a1cb97dd0`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82f7b82921a5b3474b30a4c42596d5eb0025120b94f4c4c9f9019497651ac7`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 286.3 KB (286275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a06c5cf996db9fe8ee9a4f77e2915465281718a38555d47d2a777d5c47be3c`  
		Last Modified: Tue, 04 Jul 2023 13:15:02 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d5edae74ae1b942b9502023f23837e250589e2d6207ea008ffcccacd2a3bddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a893555b6a968518c5160f8448e510094af5263207b10262bad8add5ec68801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861df767d9558c0b849a1f9d8e7152ef4412cc9cd8d7779f02887e1482df404d`  
		Last Modified: Tue, 04 Jul 2023 04:06:36 GMT  
		Size: 11.4 MB (11426584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf1db022c44ac364b74d3dc15420bbfd4234ce595f93aa6e88357d7764831c`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fb2908699cc879f5983cad2800da4109b3863df1907fbcc836091a72b1c54b`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64c88df5b726c53838a6567c16434972a07a424384ad17628e12ae7e3966db`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 286.5 KB (286542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daedea9b78dacce29febd8344cde1d29ea62c63bcf4282f8ca56f870c9892af`  
		Last Modified: Tue, 04 Jul 2023 04:06:44 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e93626359a36a48bcc52dafc8f06c0314f34e2363d5222491aca6992aec03a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfc1e630f7cf429a188bd3ae4877ca5fe4084dec8cbdfb63969279c8e6a03e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d955a37bc16f78384964e9fe3eaea19c7ce73126226143d91ad06904f88f6c`  
		Last Modified: Fri, 28 Jul 2023 00:28:21 GMT  
		Size: 11.9 MB (11883326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffc2e83e61fafba4c775d5e49f245f6c41fec6fb974344eba3e8413a9efe79`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982312586fa3fb6b226464fdb7d7012bd3b791fd5861afdf90710edd6eadce`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77d2ebb426ec21ab46e2606841ee798e7cb0ac271b2c9496e806d0796628983`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 286.4 KB (286430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7712c30fa50f50f5023f34c834fc38657c999b4b7016a15b5456d677e8b50d3d`  
		Last Modified: Fri, 28 Jul 2023 00:28:29 GMT  
		Size: 431.0 B  
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
$ docker pull neurodebian@sha256:d702c4ef3b26b10c78a4c77d637b399f2744a44e85d7d1e95acf992ca60c2799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:1c43aa6f4d4b16647b59a440068e1fb169a90f807f60c7f5406e9460e1bf925e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34315846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67417a0b461fbea4a9c9f18a4543a5ecc99d8bc74d268879607cdf1050c923f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a302d555069890ebb36b070cd326cac9483fa7cb0be84d036adc6d9cafaef1f`  
		Last Modified: Tue, 04 Jul 2023 13:13:40 GMT  
		Size: 5.5 MB (5494700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82e637645e32971a8fadb64831e8be1e58872cc0a856f5c3bc1d0e9645f688e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029aea76fbed8bf5fd4b30bfb395d8fad60024fa01b46c2eabe7407427e51cea`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525085905b04c4b6c0016c54ce9bf5ff65b825548d8627f965637feb66affa5e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 239.1 KB (239121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cb1408d965364bde6b5e3515ee76bbebecc189b1237db6eec1c485c397e3d965
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32915183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d4b0e079fc0de2d459067e9c935f4ece4cab4eb81c2602f4c1566b1eb47fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:02:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:02:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:02:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02bddd63143ca4ce20f8dd8832f98797baa25ce22f7e19532c5f43b95a6903d`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 5.5 MB (5475129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d569cdc258fb1dfe7b8edec6fc4ea0a13c5218c8d485f2b00eb2231a05adb5a`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80dab06bbbea579a049caebec835872a366b6f05eae4a088d0894534dde1d98`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f259a30976e0cc7a20d3bad8fa982bae4253b72be2fc66b4e5e24aa6998f64`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 239.7 KB (239710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:389fcc32f094ed06518a9416306f5dfc3b8a5057dcf56eb334c022420e726be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1020aff8a2b05abc2c4b91235f346f33da55dfffbc978210adc2427791e8d5df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd914ec98278af185c21b30a911ab26e016f999df4b594eff8b8e854581b2703`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a302d555069890ebb36b070cd326cac9483fa7cb0be84d036adc6d9cafaef1f`  
		Last Modified: Tue, 04 Jul 2023 13:13:40 GMT  
		Size: 5.5 MB (5494700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82e637645e32971a8fadb64831e8be1e58872cc0a856f5c3bc1d0e9645f688e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029aea76fbed8bf5fd4b30bfb395d8fad60024fa01b46c2eabe7407427e51cea`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525085905b04c4b6c0016c54ce9bf5ff65b825548d8627f965637feb66affa5e`  
		Last Modified: Tue, 04 Jul 2023 13:13:39 GMT  
		Size: 239.1 KB (239121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17414e278d1d2b6ee5faad416671884e44cf76a0b766820af26f97a386241d7`  
		Last Modified: Tue, 04 Jul 2023 13:13:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f57a51064310824edf3301b7d9a77a465fadcfdb81158255a7efdd643223b748
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32915438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61681f5228478c2a28043ef7811d57357acb86748737342e39805e877b730f73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:02:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:02:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:02:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:02:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02bddd63143ca4ce20f8dd8832f98797baa25ce22f7e19532c5f43b95a6903d`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 5.5 MB (5475129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d569cdc258fb1dfe7b8edec6fc4ea0a13c5218c8d485f2b00eb2231a05adb5a`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80dab06bbbea579a049caebec835872a366b6f05eae4a088d0894534dde1d98`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f259a30976e0cc7a20d3bad8fa982bae4253b72be2fc66b4e5e24aa6998f64`  
		Last Modified: Tue, 04 Jul 2023 04:05:19 GMT  
		Size: 239.7 KB (239710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ca9babba4cd0309d441b839e5c62a5d57be6537e0138d8738759b89ea752be`  
		Last Modified: Tue, 04 Jul 2023 04:05:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:191fec3216a692f829a5014024649eaf52df8b851c33a1e240c776a1242bc7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:0dddb9c58d26e4c5aa1381b60d6c956a658957bcb6d45ec8dc71a41d86fb4983
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5b16817fd6ac863f72c4d1879ef8fb975ce97de3d4453db80f3052f97a288`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3084125742d0581ee9ff82c21a6b489f43cf4e3e26117810ab2889ab6a4f00`  
		Last Modified: Tue, 04 Jul 2023 13:13:57 GMT  
		Size: 3.8 MB (3766304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255c4d0a7a145ca1ed2a4ccd12bd5680381a2e29a3b26c58b3527a9f992de3cd`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1321fcfa793b7d739b03fc0d89858434cab1ac41dfd2b170fc21b3240aad3b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ee1bf3076f23c0c8acdc198cad12b7da1546abc2a7a4e33e2766342714bf6b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 258.8 KB (258840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b2af04eaa6241fdc0f627b88d040ec44f5a082c3c94fa23b91a3fdc1c9dd5969
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32393179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63bd08b7cebbaf9f01a44f2e743023b2d443987282b377f237bc468596bd59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:03:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e82ac260be4046395c46fca73c81e7092d5db44e0639a55cd7f078bc67892`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 3.7 MB (3739904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b7c5d8a744c2070daee97b2d73e804013e8c69cdbcd8a57771d63851935f4`  
		Last Modified: Tue, 04 Jul 2023 04:05:37 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f7a318245f4a1cf0358726cf34dd020c5ebedb50206075beebb0d370760bb`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33822f30aabf33f7963ace371532a97547b3eddcc696ebc78b4b79649f746787`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 260.3 KB (260256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:35c1ea3ea35f91c1a474f2fd78f107b7739c49dc69cd1ae62ac78bf05b53c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c7f3c031b0c94e4c82d058a79999b2422c7306a5fcaa72e0caa692e7f326113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07082726d621d0dccb475a0da0b40ade8eda0efc77872c6ca318ae813182f1f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 13:11:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:11:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:11:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:11:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3084125742d0581ee9ff82c21a6b489f43cf4e3e26117810ab2889ab6a4f00`  
		Last Modified: Tue, 04 Jul 2023 13:13:57 GMT  
		Size: 3.8 MB (3766304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255c4d0a7a145ca1ed2a4ccd12bd5680381a2e29a3b26c58b3527a9f992de3cd`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1321fcfa793b7d739b03fc0d89858434cab1ac41dfd2b170fc21b3240aad3b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ee1bf3076f23c0c8acdc198cad12b7da1546abc2a7a4e33e2766342714bf6b`  
		Last Modified: Tue, 04 Jul 2023 13:13:56 GMT  
		Size: 258.8 KB (258840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170816573dbaf7412a7c85c1e23777dbab9104015b2beeddc9203e7ca964dff3`  
		Last Modified: Tue, 04 Jul 2023 13:14:05 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e176b3b6e55f9aa5b34103e5922f9fb86ace9f918cc8cb88dc4ae1e6f9458dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32393436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c18e0d7d850ab58b32a4ee7ceb4e5b7ec49e2e7f1de7a255ac070dac688a30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:03:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:03:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:03:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e82ac260be4046395c46fca73c81e7092d5db44e0639a55cd7f078bc67892`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 3.7 MB (3739904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b7c5d8a744c2070daee97b2d73e804013e8c69cdbcd8a57771d63851935f4`  
		Last Modified: Tue, 04 Jul 2023 04:05:37 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f7a318245f4a1cf0358726cf34dd020c5ebedb50206075beebb0d370760bb`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33822f30aabf33f7963ace371532a97547b3eddcc696ebc78b4b79649f746787`  
		Last Modified: Tue, 04 Jul 2023 04:05:38 GMT  
		Size: 260.3 KB (260256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9674aaca2237100d14c918077fc864d6cd4bc5d584a967f5eb3286a8e891fd`  
		Last Modified: Tue, 04 Jul 2023 04:05:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:8619e94863a7e6120b37060f2e45d4a3e6b1ecc47f30e5418cccbb58bc5419c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a3664b64f74716206ce118015164b4e83c8e03236dd79d6d6b5dda5ca4df692f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc8ae09bd086d04e8614e6632e92cb0040ca7d7d53995afa40f6ddcc2dc8cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead5308361a9d838b9d3e134bcfa5c09b2c664c755ddeff7d08096c61ae8edf`  
		Last Modified: Tue, 04 Jul 2023 13:14:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c79f16dd43a41a53551f24e44bcab68f7e25aae050b34270b4b6d9d4fdf6c8df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45d0d53778ee619fe21002c84a503535d661328def02ebceb9889ffad4bedc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115fb106a48cee105f8bc705681ef1cd600e4ae858f2f6f1f40215cad7c61e37`  
		Last Modified: Tue, 04 Jul 2023 04:06:25 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:024bac8c6bfc8fc3756ad87e1bd83504396ccb407abcbcb13247b75d4e1cfba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68063188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867cccb166e3bf525588dee87b37cd135772a137c84008d25278eb29cdc5c08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98dfa587a22d76f618fe45988114cfa1854794cb5b7c2f39f42e05b491466b`  
		Last Modified: Fri, 28 Jul 2023 00:28:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:623666c0822d330a48f6a9f89e6b6bc6abf8602ae7b2a8cb474642a4e6605f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:8ff70d7e6535a394265e18711bf2bed554d01f814616d3594576fe4b9db44b0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61239793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fadf68870c491b08605f0009960823d4a0a85e1092c69e82faed8c6326acffc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:13:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:13:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:13:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb16e254dc465c5893d6aeff18369662c8044c54f5c83bf08e442d3d0e121f9`  
		Last Modified: Tue, 04 Jul 2023 13:15:12 GMT  
		Size: 11.5 MB (11475625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b603511d97f2386a8ab3b1db7d9dee4088d3d7c6ffb7a26eac6df5aecbbbee9a`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0aabc1a8108a3a7a5ff6a06688362f7e3ef8a054d2681c47f391601395823`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b7ca55d70bd6c3371f54cd1a75a9fb89ba8e8dbbe6ccbd1edefcc58a520464`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 286.2 KB (286218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:26c493c1871d1cc2caeea5e545e5b2c631929abafb545ecf4957f7b83bf1d0fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61210069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed1e107f267b91f3daa33a4eda91c308b6f77e77317ed626441ad1586d6f3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:49 GMT
ADD file:2c2c0588b93f9af7d93f19033795edf9e61a692ff56e65d9e9500915276782c9 in / 
# Tue, 04 Jul 2023 01:58:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1b52151d5bb774f3680f8697c343bae1b64b7308354db57dc6bbeb7d65d0964`  
		Last Modified: Tue, 04 Jul 2023 02:03:59 GMT  
		Size: 49.5 MB (49482570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5339efefb62ae359de57f76cc7c3abcddcabc209998c1163785b6d94dc057f0`  
		Last Modified: Tue, 04 Jul 2023 04:06:54 GMT  
		Size: 11.4 MB (11438867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178be8dad69d8c80854a04cb17b21e471f0bbf2ae4a86464ff32e9970e33378`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58976cca48524ce8dd67a80e399d538d3fbef3d3f6162f96d5178183a1549de`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2da580b40ebc70f119ee6e12f89303261f8bdc03a02215e3d987f228e3067b`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 286.6 KB (286624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8de06f8e3299736ad3ce983e2f9ef19372787757135eb8387320d7ddd052b938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62861896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edec188a835e550ecca1cd7eacd796bc31389979e13e512a9f4cdd132aede9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:29 GMT
ADD file:f80411b5104f2db2a54b08d2fb1755fdc31ca042be72f3b3165979726a335a02 in / 
# Thu, 27 Jul 2023 23:40:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:27:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:27:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:27:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0cecd19dc43936e99574e6dd27db4982f7645bc158ab590b29cfc15e2c4f23a`  
		Last Modified: Thu, 27 Jul 2023 23:46:36 GMT  
		Size: 50.5 MB (50473688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c7f2e1cde6914fe23854b6902ae0a8fff8f1f0a5d8ba072e01d078cdfdeec8`  
		Last Modified: Fri, 28 Jul 2023 00:28:39 GMT  
		Size: 12.1 MB (12099954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aabb1338e505c29ec6fa33c90e2e7459a0587bb0bb0975ecdf310f2e15df2f7`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153131614253cf9252fcb4ccf05b60ad52afc2fb119dd115527e601b2b76d46`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd2ce3714afd4b50e39cf699cef7cd43812425d907d1160bc9bbf94b9c9d10`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 286.2 KB (286244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:1ae453421a71699345e895c1129a8fb503daf7982c5fec4c51523c11d229034a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:62820e5ff8aec5ab9d872ccc3e1f5a64ec85fc4849ebeae73e58d54b61c3ba95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8d8a0b6900a2051209904878057de68e54caff42553a1ff3f8b4ddf27c7b22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:13:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:13:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:13:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb16e254dc465c5893d6aeff18369662c8044c54f5c83bf08e442d3d0e121f9`  
		Last Modified: Tue, 04 Jul 2023 13:15:12 GMT  
		Size: 11.5 MB (11475625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b603511d97f2386a8ab3b1db7d9dee4088d3d7c6ffb7a26eac6df5aecbbbee9a`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0aabc1a8108a3a7a5ff6a06688362f7e3ef8a054d2681c47f391601395823`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b7ca55d70bd6c3371f54cd1a75a9fb89ba8e8dbbe6ccbd1edefcc58a520464`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 286.2 KB (286218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df3a10e230ea51013bab8caba261407bfa609c9c15f5f03018a2b73e96d410`  
		Last Modified: Tue, 04 Jul 2023 13:15:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6b94c90aadb2c204e7bd6394e5985e1770861ea491ebc26338ad53013efbabbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61210466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb194f65a1b70c1548887e06ca9e554d24f961aa84bb8e8e8af92a8eb54eba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:49 GMT
ADD file:2c2c0588b93f9af7d93f19033795edf9e61a692ff56e65d9e9500915276782c9 in / 
# Tue, 04 Jul 2023 01:58:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d1b52151d5bb774f3680f8697c343bae1b64b7308354db57dc6bbeb7d65d0964`  
		Last Modified: Tue, 04 Jul 2023 02:03:59 GMT  
		Size: 49.5 MB (49482570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5339efefb62ae359de57f76cc7c3abcddcabc209998c1163785b6d94dc057f0`  
		Last Modified: Tue, 04 Jul 2023 04:06:54 GMT  
		Size: 11.4 MB (11438867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178be8dad69d8c80854a04cb17b21e471f0bbf2ae4a86464ff32e9970e33378`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58976cca48524ce8dd67a80e399d538d3fbef3d3f6162f96d5178183a1549de`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2da580b40ebc70f119ee6e12f89303261f8bdc03a02215e3d987f228e3067b`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 286.6 KB (286624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c5b6175ba7c9e5a7370cd8b462ba718539b94f4b43ee91c28ceb2d38e0d95d`  
		Last Modified: Tue, 04 Jul 2023 04:07:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1f39faf94344b4725d91ca24cea26a9ce1a6a1a21cabe07df459db3cb190efc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62862289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a609a69a151edf20931cdebcdde41828431bb1b08d618a64071dcec52cfe0adc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:29 GMT
ADD file:f80411b5104f2db2a54b08d2fb1755fdc31ca042be72f3b3165979726a335a02 in / 
# Thu, 27 Jul 2023 23:40:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:27:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:27:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:27:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0cecd19dc43936e99574e6dd27db4982f7645bc158ab590b29cfc15e2c4f23a`  
		Last Modified: Thu, 27 Jul 2023 23:46:36 GMT  
		Size: 50.5 MB (50473688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c7f2e1cde6914fe23854b6902ae0a8fff8f1f0a5d8ba072e01d078cdfdeec8`  
		Last Modified: Fri, 28 Jul 2023 00:28:39 GMT  
		Size: 12.1 MB (12099954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aabb1338e505c29ec6fa33c90e2e7459a0587bb0bb0975ecdf310f2e15df2f7`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153131614253cf9252fcb4ccf05b60ad52afc2fb119dd115527e601b2b76d46`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd2ce3714afd4b50e39cf699cef7cd43812425d907d1160bc9bbf94b9c9d10`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 286.2 KB (286244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd05bf720bdf0a12d29d89a095980633f86f45b748e8ec46dfa8715f06ce9ba5`  
		Last Modified: Fri, 28 Jul 2023 00:28:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
