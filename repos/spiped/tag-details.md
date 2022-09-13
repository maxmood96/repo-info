<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.2`](#spiped162)
-	[`spiped:1.6.2-alpine`](#spiped162-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:ddcd04082be3abfdbe5452e0c278192955c5eb885305e7799abbbfc7e821ab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:317787c5f9c5665704c16b87ffc4224155d783ea0f992ef491850da9c4d399a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37404462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bdb5882e91fb1ae4a790c4740cb19dbb53a2a8684db77272751dcb2fe3acbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:38:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 12:38:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:38:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 12:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 12:38:53 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 12:38:54 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 12:38:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 12:38:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 12:38:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82aa82150b1c93abd6fff58189f411e9cd5669e99e6e09ff9108ae92dface6a`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae1beeecf00d85a0708dfe44241adde7e7976290e97975247baaf1cefc2372`  
		Last Modified: Tue, 13 Sep 2022 12:39:15 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2758bc163bbe99d76e7d182f22932bf6a88923ed82a2eb63a7dce2ed786a2a60`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 6.0 MB (5997085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cf59914bda870dedb72596f24260e5418ddd8459a75eb55127da360fcf204e`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6933f70f8f528137bf3e00ee05e38e58586e90df874f5de39560db7e4bfc406`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bd9a81a856577d66eaf6cfd405bf9c539ff906ce27ae11222a639153c4db8485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33948913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4defe2222797ff5ca89b8588bb9a49be81ce6737b0c9266bf9063a7d0853a57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 06:14:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 06:14:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 06:14:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 06:15:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 06:15:04 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 06:15:05 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 06:15:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 06:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 06:15:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca7ffdeda86ed9df2f347d061a9c5f1387060e845ea61d88b04808805e34147`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8357b564ff8103408646ce2c9c0d1466c58715889adcf374296474e9ea4be2f`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c51133d17bb4905ad2fd6b2a2af4609d3d860514ae110f62a62abb89fc23f8`  
		Last Modified: Tue, 23 Aug 2022 06:15:27 GMT  
		Size: 5.0 MB (5028416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95767529596e0e046a32e1f47de74f17a7e74c694a22f1416f733ae83fbc85c`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1ff78a52a381d96f4aa45a994ae5a3b48c7e69074a9fa747356b23d75af20`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cd7f30dfc79f53306bff898f026da0b3acb41e895bdca3e4e8d4a461af1d02ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31323838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cae80ccead5ae1f3fbc3ff3bb7f77c03d33379b82a83363acd4acf0e1c7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:01 GMT
ADD file:4cd1b4287674228db28402a76aa4f241740585448be48b5b15068d275ee9eb84 in / 
# Tue, 23 Aug 2022 01:43:01 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 04:13:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Aug 2022 04:13:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 04:13:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Aug 2022 04:13:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Aug 2022 04:13:27 GMT
VOLUME [/spiped]
# Wed, 24 Aug 2022 04:13:27 GMT
WORKDIR /spiped
# Wed, 24 Aug 2022 04:13:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Aug 2022 04:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 04:13:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:051ba72559abd0cf65b34b75605580f58636ec3cb994f97de317632a85d82761`  
		Last Modified: Tue, 23 Aug 2022 01:50:05 GMT  
		Size: 26.6 MB (26571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7211db57819091718a1379719cd9dd0680576ab726f68c110c512634db58a41`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f1ffa40647962acf28fffd0bc758f27af32ceab9ade1862834e78d36d3e162`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3a4aeb02b370203246c389d3f401c492facec3fe4b6d1469345cd7000d3d5`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 4.7 MB (4748854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5b9fef849a1f01df12a2523274fa3d03973e09af2f30f5b579c3ae7ba82f94`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328312dedd977c4d32c050796190108d42d2eef8c112310c0d979aa82c9ff017`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:6c24c93a45b59fb50ea46397bea78b6716f1522466bcb8e61b4c9b1ab64ff5ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35338883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9239ed5e15b573ebe5e6d415e128fe156381603fc7d8f787539f20eff91a3a11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:15:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 12:15:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 12:15:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 12:16:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 12:16:16 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 12:16:17 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 12:16:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 12:16:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 12:16:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1de4fdb0951d912e7bc1b85e380a01c3afed4fb95960b876e085ce399af5bb`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475209cde2c820c02a58b7ea087d3b81d27ec9b932049c876d8c33dff7b489b1`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0d1c2438066145aad09d04b34ee2cf519c4d82b080a4d953823ddb46b37b9`  
		Last Modified: Tue, 23 Aug 2022 12:16:52 GMT  
		Size: 5.3 MB (5272117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f54cf5e9c80a511efa854e53a810e694b06372f15bf0b5cd1990080cb7aa775`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aae186f3758daf6d7849bcb60912ba1c31d7189bf9894ab733240379af8d96b`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:080a3ea980d3a0cea9e71e608daac41551810d1d1e864065d09d82c3c71c12f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40275724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdec6799a11241ff8e045278507ad92d1c51719d5d5fab38a06aee9786c347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:38:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 13:38:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:38:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 13:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 13:38:32 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 13:38:33 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 13:38:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:38:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4432e37229888ed10498cbb73a3db7967d321668c0fe3a5ff19544ce4058b`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 1.6 KB (1609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebf7f2aa932c3b1343a7a5582ac1b2615872e7bb6de032c757ff8c82697b9cb`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd929440d2f3ee4d86d6505d860ea41e1afa4ec703c48d3a37bc788e6fa735ba`  
		Last Modified: Tue, 13 Sep 2022 13:39:08 GMT  
		Size: 7.9 MB (7888964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5899589487bc133bfdd2d1e78feb31137bbb2802f6d9c4b9ea3922107efe7ef`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febfe3cf381a26f3297bd9b2623ae878e93eca5772348ca35a0ebc631182724a`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:8d32205618e3d66af5367f472a5dc56e03ed3c925213d57d8038decebadccb85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30470de424b10ca7ffc0e87b80f277b41a9f576626b7fcd1daccd070f764b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 00:11:17 GMT
ADD file:37d58e8a76488fed0f1ebafd3ee993569a3c611b3a5d93400485783112b71386 in / 
# Tue, 23 Aug 2022 00:11:22 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 22:08:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 22:08:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:08:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 22:10:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 22:10:35 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 22:10:38 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 22:10:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:10:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e8d4fbcc8d2fc93de0170727f6e48b6fc7ec8931443fbda8a8cd154dc6f7d36`  
		Last Modified: Tue, 23 Aug 2022 00:19:35 GMT  
		Size: 29.6 MB (29639012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3039e6770ec9eb38b409a4455b2198633f3f42a688197dd0a584b82e0a0ab017`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996d8065e1459dc4aa31f7065ade324545d1e3a8e296790124b4e10bfbb63e9a`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58411fae19d2779901989446665c04634da716480f6181d9ad5cd1cc79890427`  
		Last Modified: Tue, 23 Aug 2022 22:11:10 GMT  
		Size: 5.7 MB (5706203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88986c318699becdad439b466d9025e1a7998cc49fd1d0197a138aa3f725a5f0`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163b344c0c7017792f8bf6d4951736d089c316d372eb92b607cfb3c691ec2771`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:4c582d46893c87c98ccafa957602578635aa15659c90cf8fe139274c6d8161dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41278927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e282a5da0630426f4ac6d354c2b8ce2221cc1567b8f463fbb486b79b829b5e60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:56 GMT
ADD file:8b05dcf5f16a2ae9169b27aa848b812e07cd30414e51e4d53df9a5f01cd4c1a4 in / 
# Tue, 13 Sep 2022 02:07:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:46:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 10:46:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:46:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 10:47:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 10:47:37 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 10:47:37 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 10:47:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 10:47:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9716ed411387b5ba1ec8278e9fb108a44d8a09ffbbbfd1639f06c63f20364b45`  
		Last Modified: Tue, 13 Sep 2022 02:13:40 GMT  
		Size: 35.3 MB (35277392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da9764568c091b695c70f5fb89d4dda9c7013c949db714af9c6dcaa96f4874d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84eaacb9d5368c4448078b023368b11b346b6aece474dd844c8316996dadfb7`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696d9f1c3f308ee0704a1a8ce4fcfbd75277b03bf6fe21c65fa2664f4890aca`  
		Last Modified: Tue, 13 Sep 2022 10:48:16 GMT  
		Size: 6.0 MB (5998275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12947163314fe6f97d5aea93e90e01c81ffbe5b9d5a5998a8d93cfb7f467678d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7523bbddd442a8fda5839b848b7290f044bc50451dffd9615e037a217de270a`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:decfc8601fe96dc6e51d43dd919f0771649cbbc869d79b5cfe6c16cac114707b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34824869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd77c43b80c05ef6493842813dee80b26f6adc3e763b5f69e2efd1e9eef7de8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:31:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 07:31:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:31:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 07:31:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 07:31:25 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 07:31:25 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 07:31:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 07:31:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:31:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04b9fd2ae538f5beed94d613350f72601dd2f3c78b56476ab431781bea81729`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6fe80519eef825419bf59adaa1d52c5e103f3609f3279a282ebf9b5c4fda3`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3280469a228dc957ea3fe90ff2ab7f4365596fc88da3ff3a3a98f69df5c8caa6`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 5.2 MB (5186529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6afc673d5d525b90cd3bb5060a5c41e5d44c9d583e3bbd158d25babee36ccc`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e89edd7ab987b085e5fc553e82d9d132f159e9a3fbb90d31050a3bc43a9fec0`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:07ff0a1ef1a50f0745ee97ebd2e91fd2c55a07e8877639d442a143bcb0c82b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:66b3d848f73df6532c49bb456c441a37691db14797c1288fa9cd5deb9cf9bdb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8fdfbde39b2b89abb4cdfac48560f245fff78fc822e3daac086fd5b29f78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:25:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:25:06 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:25:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:25:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:25:17 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:25:17 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:25:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:25:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:25:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210040c27162008830a83da8ed96f452757ffa50050398230f525b2f22a4541a`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05b54e70388210c7ffd8a9fbb864ca9f878f8ad3dc1613e4b96b107919baadc`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b8ff19a9777e30476c0a48eab4bc4817e9a96226faf7b42870225d69a37ba8`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f71a1b577cfb700f72058dad655d1ec9161da01b7fe6e8bb2b2461d1ddbbe`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c2f8d0b8416d1c553517142cd373249cbbdc3a03229d96604cd32b318a1195`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9bf39d60020a139fa461ebb060df6df01d5164425285c6bfc1b3113ef2242277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88197140375c26dcc5aa5dad079e8343608e24c8a03e91eb5d2fb13c9e09deec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:37:38 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 00:37:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 00:37:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 00:37:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 00:37:47 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 00:37:47 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 00:37:47 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 00:37:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 00:37:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f8a3e1b897eaae3127b4c0c6bf167dc3d7740bbf9596a97a994f1249716538`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa63959f901bfbea0a7da0112a6c04fe32edaaf453bc28bc784d942ef8a1c01`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb53413b98987994a206c07b7c3ba39980d1dd0149f4a1be509beab0c15b75da`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 205.9 KB (205888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12872e965332f5c42d1844aa3dfdbae46eda912838801110e130b89cc181ca`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a33b8651215087c0b9c9d0edc3a3fb9e0d18f0eaf36a0c0bfcddce94e338d57`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:50c8f30f14893fdc35670904e644b7a61a600294dbab4d18238198830510ec5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0a996edc8ef3c7120d02cd6c808d8adca8094539939b1c842bfdc578c3f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 03:46:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 03:46:09 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 03:46:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 03:46:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 03:46:17 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 03:46:17 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 03:46:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 03:46:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 03:46:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d2d1ea22931d8c79f9a9895368cefc8af2039f86e4795ad8e9d3d74ff4f7a6`  
		Last Modified: Thu, 11 Aug 2022 03:46:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b222ded0c4fe977a385f93c4edc434f1284118cb148a13442a3ae08b06718`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 7.7 KB (7731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a524ad23a1be21e15df07159b163bac902d8251f08372a02c998fcbe1f520`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 199.6 KB (199555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004c8029cac2bfb365d7b0a52fdccb5b64e8ae2a2c63bf1f5680b877e914189`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811d9f370333f86cfb5b0fdebf56e3d1d77472e98c127219d4d48584c23d8cb`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:31d9f2978a4900b825028e1c399cd7d0638f75f91f2400f6c6bc1d83d6274fb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031699f5a5efac86682c564a2c655c7eab52ce5aa91a856923d2032ea0517c52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:09:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 06:09:42 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 06:09:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 06:09:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 06:09:55 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 06:09:56 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 06:09:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 06:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:09:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9d3ec407b6270ec79bb3c0552c48d0afd7888773c72f1b25bfc396d4c3eb7`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1183a0c8143435d389abc100d22d7289e4a81f966ca3b9d8301cfb01947b2`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abc3813fe4a6ffebb8bdde4bd9005230c2935072094662e52a3a81cc9a9c3fa`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 214.3 KB (214262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3f496ad70b8f2f8ea93c54500ad75fb9fa4b72d7868ae964cce858765988a4`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46086b9ffd0c9eed5aadecf28229d0ab4532a26add5be2f474ced21cf4f25f7e`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ee4833bbef16308d250de2dac9ad7a6019a6f2e42880ed8eb3dfd4fcecc4ced4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c145e337e061db2f783bf06d6d6b2f1e63cf3e7dedb8ada91bc1744b707620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:02:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 00:02:18 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 00:02:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 00:02:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 00:02:31 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 00:02:32 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 00:02:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 00:02:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:02:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072149e09853327c1921fc351fbf7a93e1056edfefc5daa66cbdc6e48843cd13`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34965b4906426a2b44e36dc3fd455d5da36569c3a0c3de199beecfc03c85244c`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddeae6e8a846e3df57fb016e864191c85342272b8c766aea5b9cd0e001b0332`  
		Last Modified: Wed, 10 Aug 2022 00:03:05 GMT  
		Size: 231.3 KB (231325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463f4e96eadc8d28add083b4c188fcdde9cecb3831b8c5427343441c383e1136`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648573cf3f78bda63b9ea60198dd66926dda5cbd250025fbf6c5c0f08bbbcb4`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:d67f02f9e68884fbd145362c4f490cdfb403437bcf89d1135ad1a15c92052a5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd901b20c0f04f13ac388776797050b3e6a48903ceeccca414c16f53e1c29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:55:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:55:19 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:55:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:55:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:55:34 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:55:35 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:55:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:55:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:55:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8832ea95a37bc42923d861cfefd27ec973fed3564060fce137b8d54f75e02`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab0760cebdd26f5d818b164fe30701e72c6ec6c6c6b97b100ed16bc24fcf653`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cdb874eec093d50ac091467e93cb88955a1ee87db0d0dd84cc6344ad829323`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 220.3 KB (220255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a349e85c23948cd849a1a373c684ee566e0544af2297f9904d664dbb41dc8a6`  
		Last Modified: Wed, 10 Aug 2022 02:56:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd274005021e79dbc526fb1fd7ad0d420d2e5c10abf68e3c7ae46021ae45cbf`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:936312a4e0595fc377ed5e910f12d52cfc4fae63a6190fe388481f204758a480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa6705ab1cc71e7aa223e1b9c9ba81f85eacacdba00737aa34a7014d8d94163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 05:46:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 05:46:34 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 05:46:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 05:46:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 05:46:39 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 05:46:39 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 05:46:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 05:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 05:46:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997054cff6af24fce535516fc4358eabc7dace5f52f427e6a19340c04f6adfe`  
		Last Modified: Wed, 10 Aug 2022 05:47:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78da263b8c9f381935ae64289597db6f2e0d7e77fa388ce819ba7afecd17ef1`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 7.7 KB (7742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acce323c9898120275bb4b4763b7a8971f71720bf7cafb55201dc313247560c`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 208.4 KB (208429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b550d52792a92d7c50d7e5102763598d59d41f0c34d5bd928fbd55e16de8f8`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130443af95b4efa2ff2d4d039066967531a4e10357d515888d55082f26340a52`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:ddcd04082be3abfdbe5452e0c278192955c5eb885305e7799abbbfc7e821ab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:317787c5f9c5665704c16b87ffc4224155d783ea0f992ef491850da9c4d399a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37404462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bdb5882e91fb1ae4a790c4740cb19dbb53a2a8684db77272751dcb2fe3acbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:38:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 12:38:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:38:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 12:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 12:38:53 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 12:38:54 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 12:38:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 12:38:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 12:38:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82aa82150b1c93abd6fff58189f411e9cd5669e99e6e09ff9108ae92dface6a`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae1beeecf00d85a0708dfe44241adde7e7976290e97975247baaf1cefc2372`  
		Last Modified: Tue, 13 Sep 2022 12:39:15 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2758bc163bbe99d76e7d182f22932bf6a88923ed82a2eb63a7dce2ed786a2a60`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 6.0 MB (5997085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cf59914bda870dedb72596f24260e5418ddd8459a75eb55127da360fcf204e`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6933f70f8f528137bf3e00ee05e38e58586e90df874f5de39560db7e4bfc406`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bd9a81a856577d66eaf6cfd405bf9c539ff906ce27ae11222a639153c4db8485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33948913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4defe2222797ff5ca89b8588bb9a49be81ce6737b0c9266bf9063a7d0853a57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 06:14:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 06:14:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 06:14:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 06:15:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 06:15:04 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 06:15:05 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 06:15:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 06:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 06:15:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca7ffdeda86ed9df2f347d061a9c5f1387060e845ea61d88b04808805e34147`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8357b564ff8103408646ce2c9c0d1466c58715889adcf374296474e9ea4be2f`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c51133d17bb4905ad2fd6b2a2af4609d3d860514ae110f62a62abb89fc23f8`  
		Last Modified: Tue, 23 Aug 2022 06:15:27 GMT  
		Size: 5.0 MB (5028416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95767529596e0e046a32e1f47de74f17a7e74c694a22f1416f733ae83fbc85c`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1ff78a52a381d96f4aa45a994ae5a3b48c7e69074a9fa747356b23d75af20`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cd7f30dfc79f53306bff898f026da0b3acb41e895bdca3e4e8d4a461af1d02ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31323838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cae80ccead5ae1f3fbc3ff3bb7f77c03d33379b82a83363acd4acf0e1c7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:01 GMT
ADD file:4cd1b4287674228db28402a76aa4f241740585448be48b5b15068d275ee9eb84 in / 
# Tue, 23 Aug 2022 01:43:01 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 04:13:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Aug 2022 04:13:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 04:13:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Aug 2022 04:13:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Aug 2022 04:13:27 GMT
VOLUME [/spiped]
# Wed, 24 Aug 2022 04:13:27 GMT
WORKDIR /spiped
# Wed, 24 Aug 2022 04:13:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Aug 2022 04:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 04:13:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:051ba72559abd0cf65b34b75605580f58636ec3cb994f97de317632a85d82761`  
		Last Modified: Tue, 23 Aug 2022 01:50:05 GMT  
		Size: 26.6 MB (26571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7211db57819091718a1379719cd9dd0680576ab726f68c110c512634db58a41`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f1ffa40647962acf28fffd0bc758f27af32ceab9ade1862834e78d36d3e162`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3a4aeb02b370203246c389d3f401c492facec3fe4b6d1469345cd7000d3d5`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 4.7 MB (4748854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5b9fef849a1f01df12a2523274fa3d03973e09af2f30f5b579c3ae7ba82f94`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328312dedd977c4d32c050796190108d42d2eef8c112310c0d979aa82c9ff017`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:6c24c93a45b59fb50ea46397bea78b6716f1522466bcb8e61b4c9b1ab64ff5ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35338883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9239ed5e15b573ebe5e6d415e128fe156381603fc7d8f787539f20eff91a3a11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:15:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 12:15:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 12:15:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 12:16:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 12:16:16 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 12:16:17 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 12:16:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 12:16:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 12:16:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1de4fdb0951d912e7bc1b85e380a01c3afed4fb95960b876e085ce399af5bb`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475209cde2c820c02a58b7ea087d3b81d27ec9b932049c876d8c33dff7b489b1`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0d1c2438066145aad09d04b34ee2cf519c4d82b080a4d953823ddb46b37b9`  
		Last Modified: Tue, 23 Aug 2022 12:16:52 GMT  
		Size: 5.3 MB (5272117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f54cf5e9c80a511efa854e53a810e694b06372f15bf0b5cd1990080cb7aa775`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aae186f3758daf6d7849bcb60912ba1c31d7189bf9894ab733240379af8d96b`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:080a3ea980d3a0cea9e71e608daac41551810d1d1e864065d09d82c3c71c12f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40275724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdec6799a11241ff8e045278507ad92d1c51719d5d5fab38a06aee9786c347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:38:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 13:38:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:38:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 13:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 13:38:32 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 13:38:33 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 13:38:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:38:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4432e37229888ed10498cbb73a3db7967d321668c0fe3a5ff19544ce4058b`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 1.6 KB (1609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebf7f2aa932c3b1343a7a5582ac1b2615872e7bb6de032c757ff8c82697b9cb`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd929440d2f3ee4d86d6505d860ea41e1afa4ec703c48d3a37bc788e6fa735ba`  
		Last Modified: Tue, 13 Sep 2022 13:39:08 GMT  
		Size: 7.9 MB (7888964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5899589487bc133bfdd2d1e78feb31137bbb2802f6d9c4b9ea3922107efe7ef`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febfe3cf381a26f3297bd9b2623ae878e93eca5772348ca35a0ebc631182724a`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:8d32205618e3d66af5367f472a5dc56e03ed3c925213d57d8038decebadccb85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30470de424b10ca7ffc0e87b80f277b41a9f576626b7fcd1daccd070f764b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 00:11:17 GMT
ADD file:37d58e8a76488fed0f1ebafd3ee993569a3c611b3a5d93400485783112b71386 in / 
# Tue, 23 Aug 2022 00:11:22 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 22:08:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 22:08:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:08:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 22:10:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 22:10:35 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 22:10:38 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 22:10:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:10:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e8d4fbcc8d2fc93de0170727f6e48b6fc7ec8931443fbda8a8cd154dc6f7d36`  
		Last Modified: Tue, 23 Aug 2022 00:19:35 GMT  
		Size: 29.6 MB (29639012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3039e6770ec9eb38b409a4455b2198633f3f42a688197dd0a584b82e0a0ab017`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996d8065e1459dc4aa31f7065ade324545d1e3a8e296790124b4e10bfbb63e9a`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58411fae19d2779901989446665c04634da716480f6181d9ad5cd1cc79890427`  
		Last Modified: Tue, 23 Aug 2022 22:11:10 GMT  
		Size: 5.7 MB (5706203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88986c318699becdad439b466d9025e1a7998cc49fd1d0197a138aa3f725a5f0`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163b344c0c7017792f8bf6d4951736d089c316d372eb92b607cfb3c691ec2771`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:4c582d46893c87c98ccafa957602578635aa15659c90cf8fe139274c6d8161dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41278927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e282a5da0630426f4ac6d354c2b8ce2221cc1567b8f463fbb486b79b829b5e60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:56 GMT
ADD file:8b05dcf5f16a2ae9169b27aa848b812e07cd30414e51e4d53df9a5f01cd4c1a4 in / 
# Tue, 13 Sep 2022 02:07:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:46:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 10:46:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:46:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 10:47:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 10:47:37 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 10:47:37 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 10:47:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 10:47:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9716ed411387b5ba1ec8278e9fb108a44d8a09ffbbbfd1639f06c63f20364b45`  
		Last Modified: Tue, 13 Sep 2022 02:13:40 GMT  
		Size: 35.3 MB (35277392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da9764568c091b695c70f5fb89d4dda9c7013c949db714af9c6dcaa96f4874d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84eaacb9d5368c4448078b023368b11b346b6aece474dd844c8316996dadfb7`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696d9f1c3f308ee0704a1a8ce4fcfbd75277b03bf6fe21c65fa2664f4890aca`  
		Last Modified: Tue, 13 Sep 2022 10:48:16 GMT  
		Size: 6.0 MB (5998275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12947163314fe6f97d5aea93e90e01c81ffbe5b9d5a5998a8d93cfb7f467678d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7523bbddd442a8fda5839b848b7290f044bc50451dffd9615e037a217de270a`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:decfc8601fe96dc6e51d43dd919f0771649cbbc869d79b5cfe6c16cac114707b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34824869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd77c43b80c05ef6493842813dee80b26f6adc3e763b5f69e2efd1e9eef7de8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:31:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 07:31:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:31:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 07:31:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 07:31:25 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 07:31:25 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 07:31:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 07:31:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:31:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04b9fd2ae538f5beed94d613350f72601dd2f3c78b56476ab431781bea81729`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6fe80519eef825419bf59adaa1d52c5e103f3609f3279a282ebf9b5c4fda3`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3280469a228dc957ea3fe90ff2ab7f4365596fc88da3ff3a3a98f69df5c8caa6`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 5.2 MB (5186529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6afc673d5d525b90cd3bb5060a5c41e5d44c9d583e3bbd158d25babee36ccc`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e89edd7ab987b085e5fc553e82d9d132f159e9a3fbb90d31050a3bc43a9fec0`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:07ff0a1ef1a50f0745ee97ebd2e91fd2c55a07e8877639d442a143bcb0c82b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:66b3d848f73df6532c49bb456c441a37691db14797c1288fa9cd5deb9cf9bdb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8fdfbde39b2b89abb4cdfac48560f245fff78fc822e3daac086fd5b29f78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:25:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:25:06 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:25:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:25:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:25:17 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:25:17 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:25:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:25:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:25:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210040c27162008830a83da8ed96f452757ffa50050398230f525b2f22a4541a`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05b54e70388210c7ffd8a9fbb864ca9f878f8ad3dc1613e4b96b107919baadc`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b8ff19a9777e30476c0a48eab4bc4817e9a96226faf7b42870225d69a37ba8`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f71a1b577cfb700f72058dad655d1ec9161da01b7fe6e8bb2b2461d1ddbbe`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c2f8d0b8416d1c553517142cd373249cbbdc3a03229d96604cd32b318a1195`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9bf39d60020a139fa461ebb060df6df01d5164425285c6bfc1b3113ef2242277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88197140375c26dcc5aa5dad079e8343608e24c8a03e91eb5d2fb13c9e09deec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:37:38 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 00:37:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 00:37:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 00:37:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 00:37:47 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 00:37:47 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 00:37:47 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 00:37:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 00:37:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f8a3e1b897eaae3127b4c0c6bf167dc3d7740bbf9596a97a994f1249716538`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa63959f901bfbea0a7da0112a6c04fe32edaaf453bc28bc784d942ef8a1c01`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb53413b98987994a206c07b7c3ba39980d1dd0149f4a1be509beab0c15b75da`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 205.9 KB (205888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12872e965332f5c42d1844aa3dfdbae46eda912838801110e130b89cc181ca`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a33b8651215087c0b9c9d0edc3a3fb9e0d18f0eaf36a0c0bfcddce94e338d57`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:50c8f30f14893fdc35670904e644b7a61a600294dbab4d18238198830510ec5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0a996edc8ef3c7120d02cd6c808d8adca8094539939b1c842bfdc578c3f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 03:46:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 03:46:09 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 03:46:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 03:46:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 03:46:17 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 03:46:17 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 03:46:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 03:46:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 03:46:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d2d1ea22931d8c79f9a9895368cefc8af2039f86e4795ad8e9d3d74ff4f7a6`  
		Last Modified: Thu, 11 Aug 2022 03:46:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b222ded0c4fe977a385f93c4edc434f1284118cb148a13442a3ae08b06718`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 7.7 KB (7731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a524ad23a1be21e15df07159b163bac902d8251f08372a02c998fcbe1f520`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 199.6 KB (199555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004c8029cac2bfb365d7b0a52fdccb5b64e8ae2a2c63bf1f5680b877e914189`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811d9f370333f86cfb5b0fdebf56e3d1d77472e98c127219d4d48584c23d8cb`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:31d9f2978a4900b825028e1c399cd7d0638f75f91f2400f6c6bc1d83d6274fb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031699f5a5efac86682c564a2c655c7eab52ce5aa91a856923d2032ea0517c52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:09:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 06:09:42 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 06:09:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 06:09:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 06:09:55 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 06:09:56 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 06:09:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 06:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:09:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9d3ec407b6270ec79bb3c0552c48d0afd7888773c72f1b25bfc396d4c3eb7`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1183a0c8143435d389abc100d22d7289e4a81f966ca3b9d8301cfb01947b2`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abc3813fe4a6ffebb8bdde4bd9005230c2935072094662e52a3a81cc9a9c3fa`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 214.3 KB (214262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3f496ad70b8f2f8ea93c54500ad75fb9fa4b72d7868ae964cce858765988a4`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46086b9ffd0c9eed5aadecf28229d0ab4532a26add5be2f474ced21cf4f25f7e`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ee4833bbef16308d250de2dac9ad7a6019a6f2e42880ed8eb3dfd4fcecc4ced4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c145e337e061db2f783bf06d6d6b2f1e63cf3e7dedb8ada91bc1744b707620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:02:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 00:02:18 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 00:02:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 00:02:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 00:02:31 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 00:02:32 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 00:02:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 00:02:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:02:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072149e09853327c1921fc351fbf7a93e1056edfefc5daa66cbdc6e48843cd13`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34965b4906426a2b44e36dc3fd455d5da36569c3a0c3de199beecfc03c85244c`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddeae6e8a846e3df57fb016e864191c85342272b8c766aea5b9cd0e001b0332`  
		Last Modified: Wed, 10 Aug 2022 00:03:05 GMT  
		Size: 231.3 KB (231325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463f4e96eadc8d28add083b4c188fcdde9cecb3831b8c5427343441c383e1136`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648573cf3f78bda63b9ea60198dd66926dda5cbd250025fbf6c5c0f08bbbcb4`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:d67f02f9e68884fbd145362c4f490cdfb403437bcf89d1135ad1a15c92052a5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd901b20c0f04f13ac388776797050b3e6a48903ceeccca414c16f53e1c29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:55:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:55:19 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:55:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:55:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:55:34 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:55:35 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:55:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:55:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:55:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8832ea95a37bc42923d861cfefd27ec973fed3564060fce137b8d54f75e02`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab0760cebdd26f5d818b164fe30701e72c6ec6c6c6b97b100ed16bc24fcf653`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cdb874eec093d50ac091467e93cb88955a1ee87db0d0dd84cc6344ad829323`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 220.3 KB (220255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a349e85c23948cd849a1a373c684ee566e0544af2297f9904d664dbb41dc8a6`  
		Last Modified: Wed, 10 Aug 2022 02:56:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd274005021e79dbc526fb1fd7ad0d420d2e5c10abf68e3c7ae46021ae45cbf`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:936312a4e0595fc377ed5e910f12d52cfc4fae63a6190fe388481f204758a480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa6705ab1cc71e7aa223e1b9c9ba81f85eacacdba00737aa34a7014d8d94163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 05:46:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 05:46:34 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 05:46:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 05:46:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 05:46:39 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 05:46:39 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 05:46:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 05:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 05:46:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997054cff6af24fce535516fc4358eabc7dace5f52f427e6a19340c04f6adfe`  
		Last Modified: Wed, 10 Aug 2022 05:47:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78da263b8c9f381935ae64289597db6f2e0d7e77fa388ce819ba7afecd17ef1`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 7.7 KB (7742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acce323c9898120275bb4b4763b7a8971f71720bf7cafb55201dc313247560c`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 208.4 KB (208429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b550d52792a92d7c50d7e5102763598d59d41f0c34d5bd928fbd55e16de8f8`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130443af95b4efa2ff2d4d039066967531a4e10357d515888d55082f26340a52`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:ddcd04082be3abfdbe5452e0c278192955c5eb885305e7799abbbfc7e821ab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6.2` - linux; amd64

```console
$ docker pull spiped@sha256:317787c5f9c5665704c16b87ffc4224155d783ea0f992ef491850da9c4d399a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37404462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bdb5882e91fb1ae4a790c4740cb19dbb53a2a8684db77272751dcb2fe3acbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:38:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 12:38:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:38:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 12:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 12:38:53 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 12:38:54 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 12:38:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 12:38:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 12:38:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82aa82150b1c93abd6fff58189f411e9cd5669e99e6e09ff9108ae92dface6a`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae1beeecf00d85a0708dfe44241adde7e7976290e97975247baaf1cefc2372`  
		Last Modified: Tue, 13 Sep 2022 12:39:15 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2758bc163bbe99d76e7d182f22932bf6a88923ed82a2eb63a7dce2ed786a2a60`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 6.0 MB (5997085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cf59914bda870dedb72596f24260e5418ddd8459a75eb55127da360fcf204e`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6933f70f8f528137bf3e00ee05e38e58586e90df874f5de39560db7e4bfc406`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bd9a81a856577d66eaf6cfd405bf9c539ff906ce27ae11222a639153c4db8485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33948913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4defe2222797ff5ca89b8588bb9a49be81ce6737b0c9266bf9063a7d0853a57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 06:14:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 06:14:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 06:14:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 06:15:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 06:15:04 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 06:15:05 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 06:15:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 06:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 06:15:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca7ffdeda86ed9df2f347d061a9c5f1387060e845ea61d88b04808805e34147`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8357b564ff8103408646ce2c9c0d1466c58715889adcf374296474e9ea4be2f`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c51133d17bb4905ad2fd6b2a2af4609d3d860514ae110f62a62abb89fc23f8`  
		Last Modified: Tue, 23 Aug 2022 06:15:27 GMT  
		Size: 5.0 MB (5028416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95767529596e0e046a32e1f47de74f17a7e74c694a22f1416f733ae83fbc85c`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1ff78a52a381d96f4aa45a994ae5a3b48c7e69074a9fa747356b23d75af20`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cd7f30dfc79f53306bff898f026da0b3acb41e895bdca3e4e8d4a461af1d02ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31323838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cae80ccead5ae1f3fbc3ff3bb7f77c03d33379b82a83363acd4acf0e1c7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:01 GMT
ADD file:4cd1b4287674228db28402a76aa4f241740585448be48b5b15068d275ee9eb84 in / 
# Tue, 23 Aug 2022 01:43:01 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 04:13:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Aug 2022 04:13:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 04:13:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Aug 2022 04:13:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Aug 2022 04:13:27 GMT
VOLUME [/spiped]
# Wed, 24 Aug 2022 04:13:27 GMT
WORKDIR /spiped
# Wed, 24 Aug 2022 04:13:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Aug 2022 04:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 04:13:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:051ba72559abd0cf65b34b75605580f58636ec3cb994f97de317632a85d82761`  
		Last Modified: Tue, 23 Aug 2022 01:50:05 GMT  
		Size: 26.6 MB (26571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7211db57819091718a1379719cd9dd0680576ab726f68c110c512634db58a41`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f1ffa40647962acf28fffd0bc758f27af32ceab9ade1862834e78d36d3e162`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3a4aeb02b370203246c389d3f401c492facec3fe4b6d1469345cd7000d3d5`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 4.7 MB (4748854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5b9fef849a1f01df12a2523274fa3d03973e09af2f30f5b579c3ae7ba82f94`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328312dedd977c4d32c050796190108d42d2eef8c112310c0d979aa82c9ff017`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:6c24c93a45b59fb50ea46397bea78b6716f1522466bcb8e61b4c9b1ab64ff5ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35338883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9239ed5e15b573ebe5e6d415e128fe156381603fc7d8f787539f20eff91a3a11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:15:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 12:15:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 12:15:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 12:16:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 12:16:16 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 12:16:17 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 12:16:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 12:16:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 12:16:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1de4fdb0951d912e7bc1b85e380a01c3afed4fb95960b876e085ce399af5bb`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475209cde2c820c02a58b7ea087d3b81d27ec9b932049c876d8c33dff7b489b1`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0d1c2438066145aad09d04b34ee2cf519c4d82b080a4d953823ddb46b37b9`  
		Last Modified: Tue, 23 Aug 2022 12:16:52 GMT  
		Size: 5.3 MB (5272117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f54cf5e9c80a511efa854e53a810e694b06372f15bf0b5cd1990080cb7aa775`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aae186f3758daf6d7849bcb60912ba1c31d7189bf9894ab733240379af8d96b`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:080a3ea980d3a0cea9e71e608daac41551810d1d1e864065d09d82c3c71c12f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40275724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdec6799a11241ff8e045278507ad92d1c51719d5d5fab38a06aee9786c347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:38:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 13:38:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:38:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 13:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 13:38:32 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 13:38:33 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 13:38:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:38:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4432e37229888ed10498cbb73a3db7967d321668c0fe3a5ff19544ce4058b`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 1.6 KB (1609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebf7f2aa932c3b1343a7a5582ac1b2615872e7bb6de032c757ff8c82697b9cb`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd929440d2f3ee4d86d6505d860ea41e1afa4ec703c48d3a37bc788e6fa735ba`  
		Last Modified: Tue, 13 Sep 2022 13:39:08 GMT  
		Size: 7.9 MB (7888964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5899589487bc133bfdd2d1e78feb31137bbb2802f6d9c4b9ea3922107efe7ef`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febfe3cf381a26f3297bd9b2623ae878e93eca5772348ca35a0ebc631182724a`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:8d32205618e3d66af5367f472a5dc56e03ed3c925213d57d8038decebadccb85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30470de424b10ca7ffc0e87b80f277b41a9f576626b7fcd1daccd070f764b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 00:11:17 GMT
ADD file:37d58e8a76488fed0f1ebafd3ee993569a3c611b3a5d93400485783112b71386 in / 
# Tue, 23 Aug 2022 00:11:22 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 22:08:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 22:08:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:08:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 22:10:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 22:10:35 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 22:10:38 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 22:10:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:10:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e8d4fbcc8d2fc93de0170727f6e48b6fc7ec8931443fbda8a8cd154dc6f7d36`  
		Last Modified: Tue, 23 Aug 2022 00:19:35 GMT  
		Size: 29.6 MB (29639012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3039e6770ec9eb38b409a4455b2198633f3f42a688197dd0a584b82e0a0ab017`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996d8065e1459dc4aa31f7065ade324545d1e3a8e296790124b4e10bfbb63e9a`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58411fae19d2779901989446665c04634da716480f6181d9ad5cd1cc79890427`  
		Last Modified: Tue, 23 Aug 2022 22:11:10 GMT  
		Size: 5.7 MB (5706203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88986c318699becdad439b466d9025e1a7998cc49fd1d0197a138aa3f725a5f0`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163b344c0c7017792f8bf6d4951736d089c316d372eb92b607cfb3c691ec2771`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:4c582d46893c87c98ccafa957602578635aa15659c90cf8fe139274c6d8161dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41278927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e282a5da0630426f4ac6d354c2b8ce2221cc1567b8f463fbb486b79b829b5e60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:56 GMT
ADD file:8b05dcf5f16a2ae9169b27aa848b812e07cd30414e51e4d53df9a5f01cd4c1a4 in / 
# Tue, 13 Sep 2022 02:07:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:46:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 10:46:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:46:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 10:47:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 10:47:37 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 10:47:37 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 10:47:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 10:47:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9716ed411387b5ba1ec8278e9fb108a44d8a09ffbbbfd1639f06c63f20364b45`  
		Last Modified: Tue, 13 Sep 2022 02:13:40 GMT  
		Size: 35.3 MB (35277392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da9764568c091b695c70f5fb89d4dda9c7013c949db714af9c6dcaa96f4874d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84eaacb9d5368c4448078b023368b11b346b6aece474dd844c8316996dadfb7`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696d9f1c3f308ee0704a1a8ce4fcfbd75277b03bf6fe21c65fa2664f4890aca`  
		Last Modified: Tue, 13 Sep 2022 10:48:16 GMT  
		Size: 6.0 MB (5998275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12947163314fe6f97d5aea93e90e01c81ffbe5b9d5a5998a8d93cfb7f467678d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7523bbddd442a8fda5839b848b7290f044bc50451dffd9615e037a217de270a`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:decfc8601fe96dc6e51d43dd919f0771649cbbc869d79b5cfe6c16cac114707b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34824869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd77c43b80c05ef6493842813dee80b26f6adc3e763b5f69e2efd1e9eef7de8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:31:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 07:31:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:31:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 07:31:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 07:31:25 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 07:31:25 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 07:31:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 07:31:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:31:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04b9fd2ae538f5beed94d613350f72601dd2f3c78b56476ab431781bea81729`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6fe80519eef825419bf59adaa1d52c5e103f3609f3279a282ebf9b5c4fda3`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3280469a228dc957ea3fe90ff2ab7f4365596fc88da3ff3a3a98f69df5c8caa6`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 5.2 MB (5186529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6afc673d5d525b90cd3bb5060a5c41e5d44c9d583e3bbd158d25babee36ccc`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e89edd7ab987b085e5fc553e82d9d132f159e9a3fbb90d31050a3bc43a9fec0`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:07ff0a1ef1a50f0745ee97ebd2e91fd2c55a07e8877639d442a143bcb0c82b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:66b3d848f73df6532c49bb456c441a37691db14797c1288fa9cd5deb9cf9bdb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8fdfbde39b2b89abb4cdfac48560f245fff78fc822e3daac086fd5b29f78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:25:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:25:06 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:25:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:25:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:25:17 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:25:17 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:25:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:25:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:25:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210040c27162008830a83da8ed96f452757ffa50050398230f525b2f22a4541a`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05b54e70388210c7ffd8a9fbb864ca9f878f8ad3dc1613e4b96b107919baadc`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b8ff19a9777e30476c0a48eab4bc4817e9a96226faf7b42870225d69a37ba8`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f71a1b577cfb700f72058dad655d1ec9161da01b7fe6e8bb2b2461d1ddbbe`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c2f8d0b8416d1c553517142cd373249cbbdc3a03229d96604cd32b318a1195`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9bf39d60020a139fa461ebb060df6df01d5164425285c6bfc1b3113ef2242277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88197140375c26dcc5aa5dad079e8343608e24c8a03e91eb5d2fb13c9e09deec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:37:38 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 00:37:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 00:37:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 00:37:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 00:37:47 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 00:37:47 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 00:37:47 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 00:37:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 00:37:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f8a3e1b897eaae3127b4c0c6bf167dc3d7740bbf9596a97a994f1249716538`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa63959f901bfbea0a7da0112a6c04fe32edaaf453bc28bc784d942ef8a1c01`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb53413b98987994a206c07b7c3ba39980d1dd0149f4a1be509beab0c15b75da`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 205.9 KB (205888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12872e965332f5c42d1844aa3dfdbae46eda912838801110e130b89cc181ca`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a33b8651215087c0b9c9d0edc3a3fb9e0d18f0eaf36a0c0bfcddce94e338d57`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:50c8f30f14893fdc35670904e644b7a61a600294dbab4d18238198830510ec5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0a996edc8ef3c7120d02cd6c808d8adca8094539939b1c842bfdc578c3f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 03:46:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 03:46:09 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 03:46:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 03:46:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 03:46:17 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 03:46:17 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 03:46:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 03:46:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 03:46:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d2d1ea22931d8c79f9a9895368cefc8af2039f86e4795ad8e9d3d74ff4f7a6`  
		Last Modified: Thu, 11 Aug 2022 03:46:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b222ded0c4fe977a385f93c4edc434f1284118cb148a13442a3ae08b06718`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 7.7 KB (7731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a524ad23a1be21e15df07159b163bac902d8251f08372a02c998fcbe1f520`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 199.6 KB (199555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004c8029cac2bfb365d7b0a52fdccb5b64e8ae2a2c63bf1f5680b877e914189`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811d9f370333f86cfb5b0fdebf56e3d1d77472e98c127219d4d48584c23d8cb`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:31d9f2978a4900b825028e1c399cd7d0638f75f91f2400f6c6bc1d83d6274fb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031699f5a5efac86682c564a2c655c7eab52ce5aa91a856923d2032ea0517c52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:09:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 06:09:42 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 06:09:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 06:09:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 06:09:55 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 06:09:56 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 06:09:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 06:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:09:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9d3ec407b6270ec79bb3c0552c48d0afd7888773c72f1b25bfc396d4c3eb7`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1183a0c8143435d389abc100d22d7289e4a81f966ca3b9d8301cfb01947b2`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abc3813fe4a6ffebb8bdde4bd9005230c2935072094662e52a3a81cc9a9c3fa`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 214.3 KB (214262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3f496ad70b8f2f8ea93c54500ad75fb9fa4b72d7868ae964cce858765988a4`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46086b9ffd0c9eed5aadecf28229d0ab4532a26add5be2f474ced21cf4f25f7e`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ee4833bbef16308d250de2dac9ad7a6019a6f2e42880ed8eb3dfd4fcecc4ced4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c145e337e061db2f783bf06d6d6b2f1e63cf3e7dedb8ada91bc1744b707620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:02:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 00:02:18 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 00:02:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 00:02:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 00:02:31 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 00:02:32 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 00:02:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 00:02:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:02:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072149e09853327c1921fc351fbf7a93e1056edfefc5daa66cbdc6e48843cd13`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34965b4906426a2b44e36dc3fd455d5da36569c3a0c3de199beecfc03c85244c`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddeae6e8a846e3df57fb016e864191c85342272b8c766aea5b9cd0e001b0332`  
		Last Modified: Wed, 10 Aug 2022 00:03:05 GMT  
		Size: 231.3 KB (231325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463f4e96eadc8d28add083b4c188fcdde9cecb3831b8c5427343441c383e1136`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648573cf3f78bda63b9ea60198dd66926dda5cbd250025fbf6c5c0f08bbbcb4`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:d67f02f9e68884fbd145362c4f490cdfb403437bcf89d1135ad1a15c92052a5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd901b20c0f04f13ac388776797050b3e6a48903ceeccca414c16f53e1c29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:55:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:55:19 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:55:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:55:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:55:34 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:55:35 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:55:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:55:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:55:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8832ea95a37bc42923d861cfefd27ec973fed3564060fce137b8d54f75e02`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab0760cebdd26f5d818b164fe30701e72c6ec6c6c6b97b100ed16bc24fcf653`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cdb874eec093d50ac091467e93cb88955a1ee87db0d0dd84cc6344ad829323`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 220.3 KB (220255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a349e85c23948cd849a1a373c684ee566e0544af2297f9904d664dbb41dc8a6`  
		Last Modified: Wed, 10 Aug 2022 02:56:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd274005021e79dbc526fb1fd7ad0d420d2e5c10abf68e3c7ae46021ae45cbf`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:936312a4e0595fc377ed5e910f12d52cfc4fae63a6190fe388481f204758a480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa6705ab1cc71e7aa223e1b9c9ba81f85eacacdba00737aa34a7014d8d94163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 05:46:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 05:46:34 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 05:46:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 05:46:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 05:46:39 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 05:46:39 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 05:46:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 05:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 05:46:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997054cff6af24fce535516fc4358eabc7dace5f52f427e6a19340c04f6adfe`  
		Last Modified: Wed, 10 Aug 2022 05:47:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78da263b8c9f381935ae64289597db6f2e0d7e77fa388ce819ba7afecd17ef1`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 7.7 KB (7742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acce323c9898120275bb4b4763b7a8971f71720bf7cafb55201dc313247560c`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 208.4 KB (208429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b550d52792a92d7c50d7e5102763598d59d41f0c34d5bd928fbd55e16de8f8`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130443af95b4efa2ff2d4d039066967531a4e10357d515888d55082f26340a52`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:07ff0a1ef1a50f0745ee97ebd2e91fd2c55a07e8877639d442a143bcb0c82b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:66b3d848f73df6532c49bb456c441a37691db14797c1288fa9cd5deb9cf9bdb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8fdfbde39b2b89abb4cdfac48560f245fff78fc822e3daac086fd5b29f78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:25:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:25:06 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:25:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:25:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:25:17 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:25:17 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:25:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:25:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:25:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210040c27162008830a83da8ed96f452757ffa50050398230f525b2f22a4541a`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05b54e70388210c7ffd8a9fbb864ca9f878f8ad3dc1613e4b96b107919baadc`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b8ff19a9777e30476c0a48eab4bc4817e9a96226faf7b42870225d69a37ba8`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f71a1b577cfb700f72058dad655d1ec9161da01b7fe6e8bb2b2461d1ddbbe`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c2f8d0b8416d1c553517142cd373249cbbdc3a03229d96604cd32b318a1195`  
		Last Modified: Wed, 10 Aug 2022 02:25:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9bf39d60020a139fa461ebb060df6df01d5164425285c6bfc1b3113ef2242277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88197140375c26dcc5aa5dad079e8343608e24c8a03e91eb5d2fb13c9e09deec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:37:38 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 00:37:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 00:37:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 00:37:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 00:37:47 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 00:37:47 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 00:37:47 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 00:37:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 00:37:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f8a3e1b897eaae3127b4c0c6bf167dc3d7740bbf9596a97a994f1249716538`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa63959f901bfbea0a7da0112a6c04fe32edaaf453bc28bc784d942ef8a1c01`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb53413b98987994a206c07b7c3ba39980d1dd0149f4a1be509beab0c15b75da`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 205.9 KB (205888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12872e965332f5c42d1844aa3dfdbae46eda912838801110e130b89cc181ca`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a33b8651215087c0b9c9d0edc3a3fb9e0d18f0eaf36a0c0bfcddce94e338d57`  
		Last Modified: Thu, 11 Aug 2022 00:38:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:50c8f30f14893fdc35670904e644b7a61a600294dbab4d18238198830510ec5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0a996edc8ef3c7120d02cd6c808d8adca8094539939b1c842bfdc578c3f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 03:46:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 11 Aug 2022 03:46:09 GMT
RUN apk add --no-cache libssl1.1
# Thu, 11 Aug 2022 03:46:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Aug 2022 03:46:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 11 Aug 2022 03:46:17 GMT
VOLUME [/spiped]
# Thu, 11 Aug 2022 03:46:17 GMT
WORKDIR /spiped
# Thu, 11 Aug 2022 03:46:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Aug 2022 03:46:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 03:46:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d2d1ea22931d8c79f9a9895368cefc8af2039f86e4795ad8e9d3d74ff4f7a6`  
		Last Modified: Thu, 11 Aug 2022 03:46:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b222ded0c4fe977a385f93c4edc434f1284118cb148a13442a3ae08b06718`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 7.7 KB (7731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a524ad23a1be21e15df07159b163bac902d8251f08372a02c998fcbe1f520`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 199.6 KB (199555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004c8029cac2bfb365d7b0a52fdccb5b64e8ae2a2c63bf1f5680b877e914189`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811d9f370333f86cfb5b0fdebf56e3d1d77472e98c127219d4d48584c23d8cb`  
		Last Modified: Thu, 11 Aug 2022 03:46:48 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:31d9f2978a4900b825028e1c399cd7d0638f75f91f2400f6c6bc1d83d6274fb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031699f5a5efac86682c564a2c655c7eab52ce5aa91a856923d2032ea0517c52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:09:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 06:09:42 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 06:09:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 06:09:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 06:09:55 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 06:09:56 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 06:09:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 06:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:09:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9d3ec407b6270ec79bb3c0552c48d0afd7888773c72f1b25bfc396d4c3eb7`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1183a0c8143435d389abc100d22d7289e4a81f966ca3b9d8301cfb01947b2`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abc3813fe4a6ffebb8bdde4bd9005230c2935072094662e52a3a81cc9a9c3fa`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 214.3 KB (214262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3f496ad70b8f2f8ea93c54500ad75fb9fa4b72d7868ae964cce858765988a4`  
		Last Modified: Wed, 10 Aug 2022 06:10:26 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46086b9ffd0c9eed5aadecf28229d0ab4532a26add5be2f474ced21cf4f25f7e`  
		Last Modified: Wed, 10 Aug 2022 06:10:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:ee4833bbef16308d250de2dac9ad7a6019a6f2e42880ed8eb3dfd4fcecc4ced4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c145e337e061db2f783bf06d6d6b2f1e63cf3e7dedb8ada91bc1744b707620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:02:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 00:02:18 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 00:02:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 00:02:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 00:02:31 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 00:02:32 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 00:02:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 00:02:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:02:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072149e09853327c1921fc351fbf7a93e1056edfefc5daa66cbdc6e48843cd13`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34965b4906426a2b44e36dc3fd455d5da36569c3a0c3de199beecfc03c85244c`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 7.7 KB (7710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddeae6e8a846e3df57fb016e864191c85342272b8c766aea5b9cd0e001b0332`  
		Last Modified: Wed, 10 Aug 2022 00:03:05 GMT  
		Size: 231.3 KB (231325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463f4e96eadc8d28add083b4c188fcdde9cecb3831b8c5427343441c383e1136`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648573cf3f78bda63b9ea60198dd66926dda5cbd250025fbf6c5c0f08bbbcb4`  
		Last Modified: Wed, 10 Aug 2022 00:03:04 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:d67f02f9e68884fbd145362c4f490cdfb403437bcf89d1135ad1a15c92052a5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd901b20c0f04f13ac388776797050b3e6a48903ceeccca414c16f53e1c29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:55:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 02:55:19 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 02:55:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 02:55:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 02:55:34 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 02:55:35 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 02:55:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:55:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:55:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8832ea95a37bc42923d861cfefd27ec973fed3564060fce137b8d54f75e02`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab0760cebdd26f5d818b164fe30701e72c6ec6c6c6b97b100ed16bc24fcf653`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cdb874eec093d50ac091467e93cb88955a1ee87db0d0dd84cc6344ad829323`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 220.3 KB (220255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a349e85c23948cd849a1a373c684ee566e0544af2297f9904d664dbb41dc8a6`  
		Last Modified: Wed, 10 Aug 2022 02:56:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd274005021e79dbc526fb1fd7ad0d420d2e5c10abf68e3c7ae46021ae45cbf`  
		Last Modified: Wed, 10 Aug 2022 02:56:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:936312a4e0595fc377ed5e910f12d52cfc4fae63a6190fe388481f204758a480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa6705ab1cc71e7aa223e1b9c9ba81f85eacacdba00737aa34a7014d8d94163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 05:46:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 10 Aug 2022 05:46:34 GMT
RUN apk add --no-cache libssl1.1
# Wed, 10 Aug 2022 05:46:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Aug 2022 05:46:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 10 Aug 2022 05:46:39 GMT
VOLUME [/spiped]
# Wed, 10 Aug 2022 05:46:39 GMT
WORKDIR /spiped
# Wed, 10 Aug 2022 05:46:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Aug 2022 05:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 05:46:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997054cff6af24fce535516fc4358eabc7dace5f52f427e6a19340c04f6adfe`  
		Last Modified: Wed, 10 Aug 2022 05:47:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78da263b8c9f381935ae64289597db6f2e0d7e77fa388ce819ba7afecd17ef1`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 7.7 KB (7742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acce323c9898120275bb4b4763b7a8971f71720bf7cafb55201dc313247560c`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 208.4 KB (208429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b550d52792a92d7c50d7e5102763598d59d41f0c34d5bd928fbd55e16de8f8`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130443af95b4efa2ff2d4d039066967531a4e10357d515888d55082f26340a52`  
		Last Modified: Wed, 10 Aug 2022 05:47:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:ddcd04082be3abfdbe5452e0c278192955c5eb885305e7799abbbfc7e821ab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:317787c5f9c5665704c16b87ffc4224155d783ea0f992ef491850da9c4d399a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37404462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bdb5882e91fb1ae4a790c4740cb19dbb53a2a8684db77272751dcb2fe3acbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:38:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 12:38:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:38:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 12:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 12:38:53 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 12:38:54 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 12:38:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 12:38:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 12:38:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82aa82150b1c93abd6fff58189f411e9cd5669e99e6e09ff9108ae92dface6a`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae1beeecf00d85a0708dfe44241adde7e7976290e97975247baaf1cefc2372`  
		Last Modified: Tue, 13 Sep 2022 12:39:15 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2758bc163bbe99d76e7d182f22932bf6a88923ed82a2eb63a7dce2ed786a2a60`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 6.0 MB (5997085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cf59914bda870dedb72596f24260e5418ddd8459a75eb55127da360fcf204e`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6933f70f8f528137bf3e00ee05e38e58586e90df874f5de39560db7e4bfc406`  
		Last Modified: Tue, 13 Sep 2022 12:39:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bd9a81a856577d66eaf6cfd405bf9c539ff906ce27ae11222a639153c4db8485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33948913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4defe2222797ff5ca89b8588bb9a49be81ce6737b0c9266bf9063a7d0853a57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 06:14:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 06:14:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 06:14:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 06:15:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 06:15:04 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 06:15:05 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 06:15:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 06:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 06:15:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca7ffdeda86ed9df2f347d061a9c5f1387060e845ea61d88b04808805e34147`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8357b564ff8103408646ce2c9c0d1466c58715889adcf374296474e9ea4be2f`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c51133d17bb4905ad2fd6b2a2af4609d3d860514ae110f62a62abb89fc23f8`  
		Last Modified: Tue, 23 Aug 2022 06:15:27 GMT  
		Size: 5.0 MB (5028416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95767529596e0e046a32e1f47de74f17a7e74c694a22f1416f733ae83fbc85c`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1ff78a52a381d96f4aa45a994ae5a3b48c7e69074a9fa747356b23d75af20`  
		Last Modified: Tue, 23 Aug 2022 06:15:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cd7f30dfc79f53306bff898f026da0b3acb41e895bdca3e4e8d4a461af1d02ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31323838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cae80ccead5ae1f3fbc3ff3bb7f77c03d33379b82a83363acd4acf0e1c7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:01 GMT
ADD file:4cd1b4287674228db28402a76aa4f241740585448be48b5b15068d275ee9eb84 in / 
# Tue, 23 Aug 2022 01:43:01 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 04:13:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Aug 2022 04:13:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 04:13:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Aug 2022 04:13:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Aug 2022 04:13:27 GMT
VOLUME [/spiped]
# Wed, 24 Aug 2022 04:13:27 GMT
WORKDIR /spiped
# Wed, 24 Aug 2022 04:13:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Aug 2022 04:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 04:13:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:051ba72559abd0cf65b34b75605580f58636ec3cb994f97de317632a85d82761`  
		Last Modified: Tue, 23 Aug 2022 01:50:05 GMT  
		Size: 26.6 MB (26571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7211db57819091718a1379719cd9dd0680576ab726f68c110c512634db58a41`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f1ffa40647962acf28fffd0bc758f27af32ceab9ade1862834e78d36d3e162`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3a4aeb02b370203246c389d3f401c492facec3fe4b6d1469345cd7000d3d5`  
		Last Modified: Wed, 24 Aug 2022 04:14:00 GMT  
		Size: 4.7 MB (4748854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5b9fef849a1f01df12a2523274fa3d03973e09af2f30f5b579c3ae7ba82f94`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328312dedd977c4d32c050796190108d42d2eef8c112310c0d979aa82c9ff017`  
		Last Modified: Wed, 24 Aug 2022 04:13:59 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:6c24c93a45b59fb50ea46397bea78b6716f1522466bcb8e61b4c9b1ab64ff5ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35338883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9239ed5e15b573ebe5e6d415e128fe156381603fc7d8f787539f20eff91a3a11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:15:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 12:15:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 12:15:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 12:16:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 12:16:16 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 12:16:17 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 12:16:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 12:16:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 12:16:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1de4fdb0951d912e7bc1b85e380a01c3afed4fb95960b876e085ce399af5bb`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475209cde2c820c02a58b7ea087d3b81d27ec9b932049c876d8c33dff7b489b1`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0d1c2438066145aad09d04b34ee2cf519c4d82b080a4d953823ddb46b37b9`  
		Last Modified: Tue, 23 Aug 2022 12:16:52 GMT  
		Size: 5.3 MB (5272117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f54cf5e9c80a511efa854e53a810e694b06372f15bf0b5cd1990080cb7aa775`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aae186f3758daf6d7849bcb60912ba1c31d7189bf9894ab733240379af8d96b`  
		Last Modified: Tue, 23 Aug 2022 12:16:51 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:080a3ea980d3a0cea9e71e608daac41551810d1d1e864065d09d82c3c71c12f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40275724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdec6799a11241ff8e045278507ad92d1c51719d5d5fab38a06aee9786c347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:38:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 13:38:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:38:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 13:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 13:38:32 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 13:38:33 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 13:38:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:38:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4432e37229888ed10498cbb73a3db7967d321668c0fe3a5ff19544ce4058b`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 1.6 KB (1609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebf7f2aa932c3b1343a7a5582ac1b2615872e7bb6de032c757ff8c82697b9cb`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd929440d2f3ee4d86d6505d860ea41e1afa4ec703c48d3a37bc788e6fa735ba`  
		Last Modified: Tue, 13 Sep 2022 13:39:08 GMT  
		Size: 7.9 MB (7888964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5899589487bc133bfdd2d1e78feb31137bbb2802f6d9c4b9ea3922107efe7ef`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febfe3cf381a26f3297bd9b2623ae878e93eca5772348ca35a0ebc631182724a`  
		Last Modified: Tue, 13 Sep 2022 13:39:07 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:8d32205618e3d66af5367f472a5dc56e03ed3c925213d57d8038decebadccb85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30470de424b10ca7ffc0e87b80f277b41a9f576626b7fcd1daccd070f764b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 23 Aug 2022 00:11:17 GMT
ADD file:37d58e8a76488fed0f1ebafd3ee993569a3c611b3a5d93400485783112b71386 in / 
# Tue, 23 Aug 2022 00:11:22 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 22:08:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 23 Aug 2022 22:08:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:08:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Aug 2022 22:10:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Aug 2022 22:10:35 GMT
VOLUME [/spiped]
# Tue, 23 Aug 2022 22:10:38 GMT
WORKDIR /spiped
# Tue, 23 Aug 2022 22:10:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:10:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e8d4fbcc8d2fc93de0170727f6e48b6fc7ec8931443fbda8a8cd154dc6f7d36`  
		Last Modified: Tue, 23 Aug 2022 00:19:35 GMT  
		Size: 29.6 MB (29639012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3039e6770ec9eb38b409a4455b2198633f3f42a688197dd0a584b82e0a0ab017`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996d8065e1459dc4aa31f7065ade324545d1e3a8e296790124b4e10bfbb63e9a`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58411fae19d2779901989446665c04634da716480f6181d9ad5cd1cc79890427`  
		Last Modified: Tue, 23 Aug 2022 22:11:10 GMT  
		Size: 5.7 MB (5706203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88986c318699becdad439b466d9025e1a7998cc49fd1d0197a138aa3f725a5f0`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163b344c0c7017792f8bf6d4951736d089c316d372eb92b607cfb3c691ec2771`  
		Last Modified: Tue, 23 Aug 2022 22:11:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:4c582d46893c87c98ccafa957602578635aa15659c90cf8fe139274c6d8161dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41278927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e282a5da0630426f4ac6d354c2b8ce2221cc1567b8f463fbb486b79b829b5e60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:56 GMT
ADD file:8b05dcf5f16a2ae9169b27aa848b812e07cd30414e51e4d53df9a5f01cd4c1a4 in / 
# Tue, 13 Sep 2022 02:07:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:46:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 10:46:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:46:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 10:47:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 10:47:37 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 10:47:37 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 10:47:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 10:47:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9716ed411387b5ba1ec8278e9fb108a44d8a09ffbbbfd1639f06c63f20364b45`  
		Last Modified: Tue, 13 Sep 2022 02:13:40 GMT  
		Size: 35.3 MB (35277392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da9764568c091b695c70f5fb89d4dda9c7013c949db714af9c6dcaa96f4874d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84eaacb9d5368c4448078b023368b11b346b6aece474dd844c8316996dadfb7`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696d9f1c3f308ee0704a1a8ce4fcfbd75277b03bf6fe21c65fa2664f4890aca`  
		Last Modified: Tue, 13 Sep 2022 10:48:16 GMT  
		Size: 6.0 MB (5998275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12947163314fe6f97d5aea93e90e01c81ffbe5b9d5a5998a8d93cfb7f467678d`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7523bbddd442a8fda5839b848b7290f044bc50451dffd9615e037a217de270a`  
		Last Modified: Tue, 13 Sep 2022 10:48:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:decfc8601fe96dc6e51d43dd919f0771649cbbc869d79b5cfe6c16cac114707b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34824869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd77c43b80c05ef6493842813dee80b26f6adc3e763b5f69e2efd1e9eef7de8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:31:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Sep 2022 07:31:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:31:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Sep 2022 07:31:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Sep 2022 07:31:25 GMT
VOLUME [/spiped]
# Tue, 13 Sep 2022 07:31:25 GMT
WORKDIR /spiped
# Tue, 13 Sep 2022 07:31:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Sep 2022 07:31:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:31:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04b9fd2ae538f5beed94d613350f72601dd2f3c78b56476ab431781bea81729`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6fe80519eef825419bf59adaa1d52c5e103f3609f3279a282ebf9b5c4fda3`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3280469a228dc957ea3fe90ff2ab7f4365596fc88da3ff3a3a98f69df5c8caa6`  
		Last Modified: Tue, 13 Sep 2022 07:31:59 GMT  
		Size: 5.2 MB (5186529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6afc673d5d525b90cd3bb5060a5c41e5d44c9d583e3bbd158d25babee36ccc`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e89edd7ab987b085e5fc553e82d9d132f159e9a3fbb90d31050a3bc43a9fec0`  
		Last Modified: Tue, 13 Sep 2022 07:31:58 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
