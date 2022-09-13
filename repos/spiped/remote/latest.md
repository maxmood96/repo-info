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
