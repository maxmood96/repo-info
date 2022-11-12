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
$ docker pull spiped@sha256:01bb4fad315331c78828762173a0366e94a4d893aa658ddb9cf53cb889800ebd
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bec294b09c78593825a2b2745d8beaefe664bf7525a74768aa893a1fbfd0d4ca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a966e54f796f9e67f911192f24d84a2a8799089982ffbd7662c4f120b1d310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:17:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 13:17:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:17:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 13:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 13:17:45 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 13:17:45 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 13:17:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 13:17:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803b55095434aaa3d11e9b5e9284ef3504c108fc7c9b2896bffc704ceb414f9`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c907032efd5fd6f56e7e9b61ef7e6cc91900a4252d79ab649d6b7c1bdec07`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a2a8e948369bcf9864e3c29a9db1202bc2466eb99a1e8b26e3721af615964f`  
		Last Modified: Tue, 25 Oct 2022 13:18:11 GMT  
		Size: 5.0 MB (5029357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf3d8f8c02978f0bdd2c44b497430f98e6d372d50d17f59862b5b82b11bf47e`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8519585714a1c7006b29cdff549a37b56461039ac36987eda783d2952830b7`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bfff3efcf03753ba51d784c4deaee4cb8e634cede50272f622be6701a39e2c2e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31331482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d92b57a070235e7c98b6ba242d1cbd18b6492b75f763388eff3d53dc4d2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:08:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 04:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 04:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 04:09:01 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 04:09:01 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 04:09:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 04:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 04:09:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf378b5b9701669a758188b83d55e929eb48bd4c543f9b8f8a431570a6711d`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c6587474e215654a49ffdca22b9d48921c15b50cf53a07d57670bb4caaf2cd`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b726e98a4dbc4add399728b2912edba24f9efb947fd81fd7e885e02c4ba50a`  
		Last Modified: Wed, 26 Oct 2022 04:09:54 GMT  
		Size: 4.7 MB (4749002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f830752e5f1c0df89505c43f8ee698e7b59e1a17aa5a93d366d0d83dc1d2d5d6`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce0b6a93edcda9a62223fb9e4977ef54baffc64715df9cfbbce9b2d943e9950`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:897e91a4d21d0fae67bcbed5a4447e5b4eb8a149a789ff6d87f8c2ce8cc29402
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35339663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61a90308fbcfc22f1f4a881d8d9bf0faec4a1483fa12cecb76ef4cc1259ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:11:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 23:11:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 23:11:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 23:11:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 23:11:52 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 23:11:52 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 23:11:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 23:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 23:11:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69482e7b58c5931d995e34db7a7cbba3f4431db68de75f560fc508617719a6f`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891268266b651aee698b2c749f24de54c6fe4557aea4bfc38cfc5c8386c0a9`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c08e6ba5fa29b4d689527bcfb715ff1e4aac410b285cb6221722abd528798e0`  
		Last Modified: Tue, 25 Oct 2022 23:12:23 GMT  
		Size: 5.3 MB (5272497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b038bf62637279e7a01ac52ef0faf07e3dfc01d8026cea6bbaf1bf5ccd1b1c`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ae65a5081b5b08460f8abe03254f50e69b1f73f9cf7582bff83e250e84c5a7`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:6b101ec27a5ae8f320604e0cf0e9546c392ad8d8065545353a1fba58298c7ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dd3c8b180ee6f7e59a56438dfed96642932fd382c54a203437c206d8caff1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 11:34:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 11:34:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 11:35:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 11:35:16 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 11:35:17 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 11:35:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 11:35:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 11:35:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed83e739e0a2df94abb07b64af6442cadc8604341a6c92d12553b1d016f22a`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e27fa8cbddf583608745d18bb43feaabff04c2588b9e1c1f94bb325a4c7ec4b`  
		Last Modified: Tue, 25 Oct 2022 11:35:51 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf74edda461ba871a76c19f77e0ef97044be562ccb1c8d61a75b94e13d1ae6`  
		Last Modified: Tue, 25 Oct 2022 11:35:52 GMT  
		Size: 7.9 MB (7890559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acddd776b18a97632e23e0bf36ae521a40f00274c77cbf7c76b00f91e5f6f553`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3c0fbbbfa9f279ecb2c1951b886b9105fce2f77f710b00db682fa3f411cead`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:00fc981d65507228c242aa4bdb4e1fc6139afcebba2683c34743dc496e8077dc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35350067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155db8255c6ac9a079e7228c64edb0119d3255a4b23a67a8f19dba64c69677e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:25 GMT
ADD file:222c5611b805658925ba615b0e69d40aa3dfa37223bc06f150909f7e944e426b in / 
# Tue, 25 Oct 2022 04:39:29 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 05:57:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 05:57:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 05:57:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 05:58:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 05:58:56 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 05:58:59 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 05:59:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 05:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 05:59:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f344f7fa0587aa4dbdc8d09d838d444853a1789047586a0927fa09fa89bb8f`  
		Last Modified: Tue, 25 Oct 2022 04:47:25 GMT  
		Size: 29.6 MB (29640590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690b2de19d8b758195a521ea98837b08f3b18bdeaf8e13fc48ad6981b3cb258c`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81aa4e5e1cfa28f7d8b4b77fadcb3b868b50c1dfb9509742f11a31583e80ae8b`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4cab88bca13a73ee16be74d5b6954fd7cc493932eae28211d1d38c59ff45bb`  
		Last Modified: Wed, 26 Oct 2022 05:59:23 GMT  
		Size: 5.7 MB (5706496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7037feb4132dd15404ae3b7a88c848f4902ea7eeea1adac94169bcc3beaf513e`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a68cac1944e8fd353746991422bc9603c5623d12f599ec437cb5d1d4d2524aa`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:9fb1b03f0a8a685b4498c68cd5015cf4a09bb8ab67f00b497978bdc360ea54bb
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0efc6c3831eb2faf7335225ec92ce9fb02a206c4365a071f17e1b74788758614
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868463e78de77da4bef4772aa7cc6a7d28464ef542579c0261c09e2c8c781f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:27 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Thu, 10 Nov 2022 20:49:27 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:57:34 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 11:57:35 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 11:57:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 11:57:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 11:57:44 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 11:57:44 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 11:57:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 11:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 11:57:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc27c5af139465b6aa05baab3c0d20030b5e8a48f4d493905c4a04c47f2cceb`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9cf0a5a0c3c72f63de85ff87dbfbcd89f59cd361ccef40daf03a79b48f956e`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289f75d111fa4b0724c680dd28515c34016f39b3a3e985eef7a39b7fb09035b8`  
		Last Modified: Fri, 11 Nov 2022 11:58:06 GMT  
		Size: 1.8 MB (1833585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d265756106316b71be7bb36cc32aad20cd231c0ad2f1c3a3a4cf12025d427294`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a6706272ed824e7db29975247f2a56a7e5a468b56a15e8f2f93b203d036b2`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:da26d167b81e6942d2bf840b15ff59a945c83bcb6c34968a2cb76d61b48368d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335ebf8c2444c91778b85ac23284d5a8bb8a0564755cb6ea06160705fc72ebfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:09:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:10:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:10:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:10:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:10:09 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:10:09 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:10:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:10:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adeca438422069f0b2d529c93aa015b2d66ff14e7f811a2db7155b3780f3f17`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a307f22f7b61faf288c16b2e278af2069d3f0f1d7ccb5de2669081f800b82595`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 7.8 KB (7766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ada82ce81437697e7bbaef8a8df96fe30079d2b62708af97071da84c0be91f`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 199.6 KB (199550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650ecac6d83dd8ac1473ff90545abe2e47ad63985de2031e7fb65a25c99847b2`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304511b2e0cd4c9408aace74412dcce1dcbb72f7cc52fa88e57892bfe2beae31`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd655cf784128209a6ce84327a6d97766bea83bac20745aeb465d4053cd4f105
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d0ae659c9b8298694e19a19e61e1096d1ea1af24b229862d9c37f6deb1b68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 05:24:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 05:24:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 05:24:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 05:24:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 05:24:55 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 05:24:55 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 05:24:55 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 05:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 05:24:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc0fd009f6ccc62d80c4b480c66a29b1585894ea074dbe47eb333980bf9bd6`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236aea0d806ec2bb4e08480c6db584b2e726baae7d26439a2bc394b4c5fc88a`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28c32b7753ad7c53a2bf64f16493bc5a3032cd1a4043d9bf7bd38c3b1d1640`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 2.0 MB (1971114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6352383f529cef4add4006f77dbfaf604b1e246e11a14b8d50a03e50998a361e`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ba1f3cf56eca1bd4f9b02d4fd58f55791f2463be1bc0d0f049c817423dc30d`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:843ee0a06fce410e9185f279bedec495552d30a9b235351c9e52bd669095b6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9c942ec6bc7f10412698170c354b1c1e3784c5293bb45763683f9fae4ff45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:29:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 07:29:08 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 07:29:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 07:29:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 07:29:21 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 07:29:22 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 07:29:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:29:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:29:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809fb6be6b6c5126ea93c77f723eabd38a79da96195f2112d4ba37475d11cec`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4111161b7b7d291c73883105977d83b95161ff3092cb8c51baa969a0f4f40`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefd93dcc118fc9b6c2575a0e2e6442cf1941ad36cd7c23a11ff37f954d72696`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 231.4 KB (231353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12465fe04c57bef25da7dd19448585a8f389a2be5002904390928db02803c463`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f19ff97a8609ea6c7b399819d80dd69016ccd3db9c032fb36c9caaec3462cde`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:01bb4fad315331c78828762173a0366e94a4d893aa658ddb9cf53cb889800ebd
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bec294b09c78593825a2b2745d8beaefe664bf7525a74768aa893a1fbfd0d4ca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a966e54f796f9e67f911192f24d84a2a8799089982ffbd7662c4f120b1d310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:17:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 13:17:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:17:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 13:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 13:17:45 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 13:17:45 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 13:17:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 13:17:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803b55095434aaa3d11e9b5e9284ef3504c108fc7c9b2896bffc704ceb414f9`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c907032efd5fd6f56e7e9b61ef7e6cc91900a4252d79ab649d6b7c1bdec07`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a2a8e948369bcf9864e3c29a9db1202bc2466eb99a1e8b26e3721af615964f`  
		Last Modified: Tue, 25 Oct 2022 13:18:11 GMT  
		Size: 5.0 MB (5029357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf3d8f8c02978f0bdd2c44b497430f98e6d372d50d17f59862b5b82b11bf47e`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8519585714a1c7006b29cdff549a37b56461039ac36987eda783d2952830b7`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bfff3efcf03753ba51d784c4deaee4cb8e634cede50272f622be6701a39e2c2e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31331482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d92b57a070235e7c98b6ba242d1cbd18b6492b75f763388eff3d53dc4d2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:08:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 04:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 04:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 04:09:01 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 04:09:01 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 04:09:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 04:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 04:09:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf378b5b9701669a758188b83d55e929eb48bd4c543f9b8f8a431570a6711d`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c6587474e215654a49ffdca22b9d48921c15b50cf53a07d57670bb4caaf2cd`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b726e98a4dbc4add399728b2912edba24f9efb947fd81fd7e885e02c4ba50a`  
		Last Modified: Wed, 26 Oct 2022 04:09:54 GMT  
		Size: 4.7 MB (4749002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f830752e5f1c0df89505c43f8ee698e7b59e1a17aa5a93d366d0d83dc1d2d5d6`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce0b6a93edcda9a62223fb9e4977ef54baffc64715df9cfbbce9b2d943e9950`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:897e91a4d21d0fae67bcbed5a4447e5b4eb8a149a789ff6d87f8c2ce8cc29402
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35339663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61a90308fbcfc22f1f4a881d8d9bf0faec4a1483fa12cecb76ef4cc1259ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:11:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 23:11:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 23:11:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 23:11:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 23:11:52 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 23:11:52 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 23:11:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 23:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 23:11:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69482e7b58c5931d995e34db7a7cbba3f4431db68de75f560fc508617719a6f`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891268266b651aee698b2c749f24de54c6fe4557aea4bfc38cfc5c8386c0a9`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c08e6ba5fa29b4d689527bcfb715ff1e4aac410b285cb6221722abd528798e0`  
		Last Modified: Tue, 25 Oct 2022 23:12:23 GMT  
		Size: 5.3 MB (5272497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b038bf62637279e7a01ac52ef0faf07e3dfc01d8026cea6bbaf1bf5ccd1b1c`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ae65a5081b5b08460f8abe03254f50e69b1f73f9cf7582bff83e250e84c5a7`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:6b101ec27a5ae8f320604e0cf0e9546c392ad8d8065545353a1fba58298c7ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dd3c8b180ee6f7e59a56438dfed96642932fd382c54a203437c206d8caff1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 11:34:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 11:34:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 11:35:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 11:35:16 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 11:35:17 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 11:35:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 11:35:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 11:35:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed83e739e0a2df94abb07b64af6442cadc8604341a6c92d12553b1d016f22a`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e27fa8cbddf583608745d18bb43feaabff04c2588b9e1c1f94bb325a4c7ec4b`  
		Last Modified: Tue, 25 Oct 2022 11:35:51 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf74edda461ba871a76c19f77e0ef97044be562ccb1c8d61a75b94e13d1ae6`  
		Last Modified: Tue, 25 Oct 2022 11:35:52 GMT  
		Size: 7.9 MB (7890559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acddd776b18a97632e23e0bf36ae521a40f00274c77cbf7c76b00f91e5f6f553`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3c0fbbbfa9f279ecb2c1951b886b9105fce2f77f710b00db682fa3f411cead`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:00fc981d65507228c242aa4bdb4e1fc6139afcebba2683c34743dc496e8077dc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35350067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155db8255c6ac9a079e7228c64edb0119d3255a4b23a67a8f19dba64c69677e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:25 GMT
ADD file:222c5611b805658925ba615b0e69d40aa3dfa37223bc06f150909f7e944e426b in / 
# Tue, 25 Oct 2022 04:39:29 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 05:57:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 05:57:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 05:57:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 05:58:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 05:58:56 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 05:58:59 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 05:59:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 05:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 05:59:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f344f7fa0587aa4dbdc8d09d838d444853a1789047586a0927fa09fa89bb8f`  
		Last Modified: Tue, 25 Oct 2022 04:47:25 GMT  
		Size: 29.6 MB (29640590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690b2de19d8b758195a521ea98837b08f3b18bdeaf8e13fc48ad6981b3cb258c`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81aa4e5e1cfa28f7d8b4b77fadcb3b868b50c1dfb9509742f11a31583e80ae8b`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4cab88bca13a73ee16be74d5b6954fd7cc493932eae28211d1d38c59ff45bb`  
		Last Modified: Wed, 26 Oct 2022 05:59:23 GMT  
		Size: 5.7 MB (5706496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7037feb4132dd15404ae3b7a88c848f4902ea7eeea1adac94169bcc3beaf513e`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a68cac1944e8fd353746991422bc9603c5623d12f599ec437cb5d1d4d2524aa`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:9fb1b03f0a8a685b4498c68cd5015cf4a09bb8ab67f00b497978bdc360ea54bb
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0efc6c3831eb2faf7335225ec92ce9fb02a206c4365a071f17e1b74788758614
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868463e78de77da4bef4772aa7cc6a7d28464ef542579c0261c09e2c8c781f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:27 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Thu, 10 Nov 2022 20:49:27 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:57:34 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 11:57:35 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 11:57:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 11:57:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 11:57:44 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 11:57:44 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 11:57:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 11:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 11:57:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc27c5af139465b6aa05baab3c0d20030b5e8a48f4d493905c4a04c47f2cceb`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9cf0a5a0c3c72f63de85ff87dbfbcd89f59cd361ccef40daf03a79b48f956e`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289f75d111fa4b0724c680dd28515c34016f39b3a3e985eef7a39b7fb09035b8`  
		Last Modified: Fri, 11 Nov 2022 11:58:06 GMT  
		Size: 1.8 MB (1833585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d265756106316b71be7bb36cc32aad20cd231c0ad2f1c3a3a4cf12025d427294`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a6706272ed824e7db29975247f2a56a7e5a468b56a15e8f2f93b203d036b2`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:da26d167b81e6942d2bf840b15ff59a945c83bcb6c34968a2cb76d61b48368d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335ebf8c2444c91778b85ac23284d5a8bb8a0564755cb6ea06160705fc72ebfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:09:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:10:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:10:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:10:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:10:09 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:10:09 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:10:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:10:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adeca438422069f0b2d529c93aa015b2d66ff14e7f811a2db7155b3780f3f17`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a307f22f7b61faf288c16b2e278af2069d3f0f1d7ccb5de2669081f800b82595`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 7.8 KB (7766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ada82ce81437697e7bbaef8a8df96fe30079d2b62708af97071da84c0be91f`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 199.6 KB (199550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650ecac6d83dd8ac1473ff90545abe2e47ad63985de2031e7fb65a25c99847b2`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304511b2e0cd4c9408aace74412dcce1dcbb72f7cc52fa88e57892bfe2beae31`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd655cf784128209a6ce84327a6d97766bea83bac20745aeb465d4053cd4f105
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d0ae659c9b8298694e19a19e61e1096d1ea1af24b229862d9c37f6deb1b68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 05:24:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 05:24:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 05:24:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 05:24:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 05:24:55 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 05:24:55 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 05:24:55 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 05:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 05:24:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc0fd009f6ccc62d80c4b480c66a29b1585894ea074dbe47eb333980bf9bd6`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236aea0d806ec2bb4e08480c6db584b2e726baae7d26439a2bc394b4c5fc88a`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28c32b7753ad7c53a2bf64f16493bc5a3032cd1a4043d9bf7bd38c3b1d1640`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 2.0 MB (1971114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6352383f529cef4add4006f77dbfaf604b1e246e11a14b8d50a03e50998a361e`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ba1f3cf56eca1bd4f9b02d4fd58f55791f2463be1bc0d0f049c817423dc30d`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:843ee0a06fce410e9185f279bedec495552d30a9b235351c9e52bd669095b6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9c942ec6bc7f10412698170c354b1c1e3784c5293bb45763683f9fae4ff45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:29:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 07:29:08 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 07:29:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 07:29:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 07:29:21 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 07:29:22 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 07:29:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:29:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:29:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809fb6be6b6c5126ea93c77f723eabd38a79da96195f2112d4ba37475d11cec`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4111161b7b7d291c73883105977d83b95161ff3092cb8c51baa969a0f4f40`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefd93dcc118fc9b6c2575a0e2e6442cf1941ad36cd7c23a11ff37f954d72696`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 231.4 KB (231353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12465fe04c57bef25da7dd19448585a8f389a2be5002904390928db02803c463`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f19ff97a8609ea6c7b399819d80dd69016ccd3db9c032fb36c9caaec3462cde`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:01bb4fad315331c78828762173a0366e94a4d893aa658ddb9cf53cb889800ebd
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bec294b09c78593825a2b2745d8beaefe664bf7525a74768aa893a1fbfd0d4ca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a966e54f796f9e67f911192f24d84a2a8799089982ffbd7662c4f120b1d310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:17:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 13:17:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:17:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 13:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 13:17:45 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 13:17:45 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 13:17:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 13:17:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803b55095434aaa3d11e9b5e9284ef3504c108fc7c9b2896bffc704ceb414f9`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c907032efd5fd6f56e7e9b61ef7e6cc91900a4252d79ab649d6b7c1bdec07`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a2a8e948369bcf9864e3c29a9db1202bc2466eb99a1e8b26e3721af615964f`  
		Last Modified: Tue, 25 Oct 2022 13:18:11 GMT  
		Size: 5.0 MB (5029357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf3d8f8c02978f0bdd2c44b497430f98e6d372d50d17f59862b5b82b11bf47e`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8519585714a1c7006b29cdff549a37b56461039ac36987eda783d2952830b7`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bfff3efcf03753ba51d784c4deaee4cb8e634cede50272f622be6701a39e2c2e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31331482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d92b57a070235e7c98b6ba242d1cbd18b6492b75f763388eff3d53dc4d2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:08:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 04:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 04:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 04:09:01 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 04:09:01 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 04:09:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 04:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 04:09:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf378b5b9701669a758188b83d55e929eb48bd4c543f9b8f8a431570a6711d`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c6587474e215654a49ffdca22b9d48921c15b50cf53a07d57670bb4caaf2cd`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b726e98a4dbc4add399728b2912edba24f9efb947fd81fd7e885e02c4ba50a`  
		Last Modified: Wed, 26 Oct 2022 04:09:54 GMT  
		Size: 4.7 MB (4749002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f830752e5f1c0df89505c43f8ee698e7b59e1a17aa5a93d366d0d83dc1d2d5d6`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce0b6a93edcda9a62223fb9e4977ef54baffc64715df9cfbbce9b2d943e9950`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:897e91a4d21d0fae67bcbed5a4447e5b4eb8a149a789ff6d87f8c2ce8cc29402
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35339663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61a90308fbcfc22f1f4a881d8d9bf0faec4a1483fa12cecb76ef4cc1259ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:11:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 23:11:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 23:11:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 23:11:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 23:11:52 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 23:11:52 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 23:11:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 23:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 23:11:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69482e7b58c5931d995e34db7a7cbba3f4431db68de75f560fc508617719a6f`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891268266b651aee698b2c749f24de54c6fe4557aea4bfc38cfc5c8386c0a9`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c08e6ba5fa29b4d689527bcfb715ff1e4aac410b285cb6221722abd528798e0`  
		Last Modified: Tue, 25 Oct 2022 23:12:23 GMT  
		Size: 5.3 MB (5272497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b038bf62637279e7a01ac52ef0faf07e3dfc01d8026cea6bbaf1bf5ccd1b1c`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ae65a5081b5b08460f8abe03254f50e69b1f73f9cf7582bff83e250e84c5a7`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:6b101ec27a5ae8f320604e0cf0e9546c392ad8d8065545353a1fba58298c7ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dd3c8b180ee6f7e59a56438dfed96642932fd382c54a203437c206d8caff1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 11:34:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 11:34:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 11:35:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 11:35:16 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 11:35:17 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 11:35:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 11:35:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 11:35:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed83e739e0a2df94abb07b64af6442cadc8604341a6c92d12553b1d016f22a`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e27fa8cbddf583608745d18bb43feaabff04c2588b9e1c1f94bb325a4c7ec4b`  
		Last Modified: Tue, 25 Oct 2022 11:35:51 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf74edda461ba871a76c19f77e0ef97044be562ccb1c8d61a75b94e13d1ae6`  
		Last Modified: Tue, 25 Oct 2022 11:35:52 GMT  
		Size: 7.9 MB (7890559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acddd776b18a97632e23e0bf36ae521a40f00274c77cbf7c76b00f91e5f6f553`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3c0fbbbfa9f279ecb2c1951b886b9105fce2f77f710b00db682fa3f411cead`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:00fc981d65507228c242aa4bdb4e1fc6139afcebba2683c34743dc496e8077dc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35350067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155db8255c6ac9a079e7228c64edb0119d3255a4b23a67a8f19dba64c69677e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:25 GMT
ADD file:222c5611b805658925ba615b0e69d40aa3dfa37223bc06f150909f7e944e426b in / 
# Tue, 25 Oct 2022 04:39:29 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 05:57:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 05:57:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 05:57:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 05:58:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 05:58:56 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 05:58:59 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 05:59:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 05:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 05:59:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f344f7fa0587aa4dbdc8d09d838d444853a1789047586a0927fa09fa89bb8f`  
		Last Modified: Tue, 25 Oct 2022 04:47:25 GMT  
		Size: 29.6 MB (29640590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690b2de19d8b758195a521ea98837b08f3b18bdeaf8e13fc48ad6981b3cb258c`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81aa4e5e1cfa28f7d8b4b77fadcb3b868b50c1dfb9509742f11a31583e80ae8b`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4cab88bca13a73ee16be74d5b6954fd7cc493932eae28211d1d38c59ff45bb`  
		Last Modified: Wed, 26 Oct 2022 05:59:23 GMT  
		Size: 5.7 MB (5706496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7037feb4132dd15404ae3b7a88c848f4902ea7eeea1adac94169bcc3beaf513e`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a68cac1944e8fd353746991422bc9603c5623d12f599ec437cb5d1d4d2524aa`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:9fb1b03f0a8a685b4498c68cd5015cf4a09bb8ab67f00b497978bdc360ea54bb
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0efc6c3831eb2faf7335225ec92ce9fb02a206c4365a071f17e1b74788758614
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868463e78de77da4bef4772aa7cc6a7d28464ef542579c0261c09e2c8c781f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:27 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Thu, 10 Nov 2022 20:49:27 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:57:34 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 11:57:35 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 11:57:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 11:57:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 11:57:44 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 11:57:44 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 11:57:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 11:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 11:57:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc27c5af139465b6aa05baab3c0d20030b5e8a48f4d493905c4a04c47f2cceb`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9cf0a5a0c3c72f63de85ff87dbfbcd89f59cd361ccef40daf03a79b48f956e`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289f75d111fa4b0724c680dd28515c34016f39b3a3e985eef7a39b7fb09035b8`  
		Last Modified: Fri, 11 Nov 2022 11:58:06 GMT  
		Size: 1.8 MB (1833585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d265756106316b71be7bb36cc32aad20cd231c0ad2f1c3a3a4cf12025d427294`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a6706272ed824e7db29975247f2a56a7e5a468b56a15e8f2f93b203d036b2`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:da26d167b81e6942d2bf840b15ff59a945c83bcb6c34968a2cb76d61b48368d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335ebf8c2444c91778b85ac23284d5a8bb8a0564755cb6ea06160705fc72ebfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:09:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:10:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:10:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:10:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:10:09 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:10:09 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:10:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:10:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adeca438422069f0b2d529c93aa015b2d66ff14e7f811a2db7155b3780f3f17`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a307f22f7b61faf288c16b2e278af2069d3f0f1d7ccb5de2669081f800b82595`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 7.8 KB (7766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ada82ce81437697e7bbaef8a8df96fe30079d2b62708af97071da84c0be91f`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 199.6 KB (199550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650ecac6d83dd8ac1473ff90545abe2e47ad63985de2031e7fb65a25c99847b2`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304511b2e0cd4c9408aace74412dcce1dcbb72f7cc52fa88e57892bfe2beae31`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd655cf784128209a6ce84327a6d97766bea83bac20745aeb465d4053cd4f105
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d0ae659c9b8298694e19a19e61e1096d1ea1af24b229862d9c37f6deb1b68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 05:24:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 05:24:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 05:24:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 05:24:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 05:24:55 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 05:24:55 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 05:24:55 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 05:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 05:24:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc0fd009f6ccc62d80c4b480c66a29b1585894ea074dbe47eb333980bf9bd6`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236aea0d806ec2bb4e08480c6db584b2e726baae7d26439a2bc394b4c5fc88a`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28c32b7753ad7c53a2bf64f16493bc5a3032cd1a4043d9bf7bd38c3b1d1640`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 2.0 MB (1971114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6352383f529cef4add4006f77dbfaf604b1e246e11a14b8d50a03e50998a361e`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ba1f3cf56eca1bd4f9b02d4fd58f55791f2463be1bc0d0f049c817423dc30d`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:843ee0a06fce410e9185f279bedec495552d30a9b235351c9e52bd669095b6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9c942ec6bc7f10412698170c354b1c1e3784c5293bb45763683f9fae4ff45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:29:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 07:29:08 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 07:29:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 07:29:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 07:29:21 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 07:29:22 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 07:29:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:29:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:29:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809fb6be6b6c5126ea93c77f723eabd38a79da96195f2112d4ba37475d11cec`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4111161b7b7d291c73883105977d83b95161ff3092cb8c51baa969a0f4f40`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefd93dcc118fc9b6c2575a0e2e6442cf1941ad36cd7c23a11ff37f954d72696`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 231.4 KB (231353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12465fe04c57bef25da7dd19448585a8f389a2be5002904390928db02803c463`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f19ff97a8609ea6c7b399819d80dd69016ccd3db9c032fb36c9caaec3462cde`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:9fb1b03f0a8a685b4498c68cd5015cf4a09bb8ab67f00b497978bdc360ea54bb
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0efc6c3831eb2faf7335225ec92ce9fb02a206c4365a071f17e1b74788758614
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868463e78de77da4bef4772aa7cc6a7d28464ef542579c0261c09e2c8c781f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:27 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Thu, 10 Nov 2022 20:49:27 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:57:34 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 11:57:35 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 11:57:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 11:57:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 11:57:44 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 11:57:44 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 11:57:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 11:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 11:57:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc27c5af139465b6aa05baab3c0d20030b5e8a48f4d493905c4a04c47f2cceb`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9cf0a5a0c3c72f63de85ff87dbfbcd89f59cd361ccef40daf03a79b48f956e`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289f75d111fa4b0724c680dd28515c34016f39b3a3e985eef7a39b7fb09035b8`  
		Last Modified: Fri, 11 Nov 2022 11:58:06 GMT  
		Size: 1.8 MB (1833585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d265756106316b71be7bb36cc32aad20cd231c0ad2f1c3a3a4cf12025d427294`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a6706272ed824e7db29975247f2a56a7e5a468b56a15e8f2f93b203d036b2`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:da26d167b81e6942d2bf840b15ff59a945c83bcb6c34968a2cb76d61b48368d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335ebf8c2444c91778b85ac23284d5a8bb8a0564755cb6ea06160705fc72ebfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:09:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:10:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:10:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:10:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:10:09 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:10:09 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:10:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:10:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adeca438422069f0b2d529c93aa015b2d66ff14e7f811a2db7155b3780f3f17`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a307f22f7b61faf288c16b2e278af2069d3f0f1d7ccb5de2669081f800b82595`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 7.8 KB (7766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ada82ce81437697e7bbaef8a8df96fe30079d2b62708af97071da84c0be91f`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 199.6 KB (199550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650ecac6d83dd8ac1473ff90545abe2e47ad63985de2031e7fb65a25c99847b2`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304511b2e0cd4c9408aace74412dcce1dcbb72f7cc52fa88e57892bfe2beae31`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd655cf784128209a6ce84327a6d97766bea83bac20745aeb465d4053cd4f105
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d0ae659c9b8298694e19a19e61e1096d1ea1af24b229862d9c37f6deb1b68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 05:24:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 05:24:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 05:24:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 05:24:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 05:24:55 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 05:24:55 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 05:24:55 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 05:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 05:24:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc0fd009f6ccc62d80c4b480c66a29b1585894ea074dbe47eb333980bf9bd6`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236aea0d806ec2bb4e08480c6db584b2e726baae7d26439a2bc394b4c5fc88a`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28c32b7753ad7c53a2bf64f16493bc5a3032cd1a4043d9bf7bd38c3b1d1640`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 2.0 MB (1971114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6352383f529cef4add4006f77dbfaf604b1e246e11a14b8d50a03e50998a361e`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ba1f3cf56eca1bd4f9b02d4fd58f55791f2463be1bc0d0f049c817423dc30d`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:843ee0a06fce410e9185f279bedec495552d30a9b235351c9e52bd669095b6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9c942ec6bc7f10412698170c354b1c1e3784c5293bb45763683f9fae4ff45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:29:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 07:29:08 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 07:29:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 07:29:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 07:29:21 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 07:29:22 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 07:29:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:29:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:29:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809fb6be6b6c5126ea93c77f723eabd38a79da96195f2112d4ba37475d11cec`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4111161b7b7d291c73883105977d83b95161ff3092cb8c51baa969a0f4f40`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefd93dcc118fc9b6c2575a0e2e6442cf1941ad36cd7c23a11ff37f954d72696`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 231.4 KB (231353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12465fe04c57bef25da7dd19448585a8f389a2be5002904390928db02803c463`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f19ff97a8609ea6c7b399819d80dd69016ccd3db9c032fb36c9caaec3462cde`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:01bb4fad315331c78828762173a0366e94a4d893aa658ddb9cf53cb889800ebd
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:bec294b09c78593825a2b2745d8beaefe664bf7525a74768aa893a1fbfd0d4ca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a966e54f796f9e67f911192f24d84a2a8799089982ffbd7662c4f120b1d310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:17:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 13:17:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:17:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 13:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 13:17:45 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 13:17:45 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 13:17:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 13:17:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803b55095434aaa3d11e9b5e9284ef3504c108fc7c9b2896bffc704ceb414f9`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c907032efd5fd6f56e7e9b61ef7e6cc91900a4252d79ab649d6b7c1bdec07`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a2a8e948369bcf9864e3c29a9db1202bc2466eb99a1e8b26e3721af615964f`  
		Last Modified: Tue, 25 Oct 2022 13:18:11 GMT  
		Size: 5.0 MB (5029357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf3d8f8c02978f0bdd2c44b497430f98e6d372d50d17f59862b5b82b11bf47e`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8519585714a1c7006b29cdff549a37b56461039ac36987eda783d2952830b7`  
		Last Modified: Tue, 25 Oct 2022 13:18:10 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bfff3efcf03753ba51d784c4deaee4cb8e634cede50272f622be6701a39e2c2e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31331482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d92b57a070235e7c98b6ba242d1cbd18b6492b75f763388eff3d53dc4d2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:08:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 04:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 04:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 04:09:01 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 04:09:01 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 04:09:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 04:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 04:09:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf378b5b9701669a758188b83d55e929eb48bd4c543f9b8f8a431570a6711d`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c6587474e215654a49ffdca22b9d48921c15b50cf53a07d57670bb4caaf2cd`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b726e98a4dbc4add399728b2912edba24f9efb947fd81fd7e885e02c4ba50a`  
		Last Modified: Wed, 26 Oct 2022 04:09:54 GMT  
		Size: 4.7 MB (4749002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f830752e5f1c0df89505c43f8ee698e7b59e1a17aa5a93d366d0d83dc1d2d5d6`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce0b6a93edcda9a62223fb9e4977ef54baffc64715df9cfbbce9b2d943e9950`  
		Last Modified: Wed, 26 Oct 2022 04:09:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:897e91a4d21d0fae67bcbed5a4447e5b4eb8a149a789ff6d87f8c2ce8cc29402
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35339663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61a90308fbcfc22f1f4a881d8d9bf0faec4a1483fa12cecb76ef4cc1259ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:11:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 23:11:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 23:11:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 23:11:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 23:11:52 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 23:11:52 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 23:11:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 23:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 23:11:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69482e7b58c5931d995e34db7a7cbba3f4431db68de75f560fc508617719a6f`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891268266b651aee698b2c749f24de54c6fe4557aea4bfc38cfc5c8386c0a9`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c08e6ba5fa29b4d689527bcfb715ff1e4aac410b285cb6221722abd528798e0`  
		Last Modified: Tue, 25 Oct 2022 23:12:23 GMT  
		Size: 5.3 MB (5272497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b038bf62637279e7a01ac52ef0faf07e3dfc01d8026cea6bbaf1bf5ccd1b1c`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ae65a5081b5b08460f8abe03254f50e69b1f73f9cf7582bff83e250e84c5a7`  
		Last Modified: Tue, 25 Oct 2022 23:12:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:6b101ec27a5ae8f320604e0cf0e9546c392ad8d8065545353a1fba58298c7ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dd3c8b180ee6f7e59a56438dfed96642932fd382c54a203437c206d8caff1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 11:34:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 11:34:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 11:35:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 11:35:16 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 11:35:17 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 11:35:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 11:35:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 11:35:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed83e739e0a2df94abb07b64af6442cadc8604341a6c92d12553b1d016f22a`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e27fa8cbddf583608745d18bb43feaabff04c2588b9e1c1f94bb325a4c7ec4b`  
		Last Modified: Tue, 25 Oct 2022 11:35:51 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf74edda461ba871a76c19f77e0ef97044be562ccb1c8d61a75b94e13d1ae6`  
		Last Modified: Tue, 25 Oct 2022 11:35:52 GMT  
		Size: 7.9 MB (7890559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acddd776b18a97632e23e0bf36ae521a40f00274c77cbf7c76b00f91e5f6f553`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3c0fbbbfa9f279ecb2c1951b886b9105fce2f77f710b00db682fa3f411cead`  
		Last Modified: Tue, 25 Oct 2022 11:35:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:00fc981d65507228c242aa4bdb4e1fc6139afcebba2683c34743dc496e8077dc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35350067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155db8255c6ac9a079e7228c64edb0119d3255a4b23a67a8f19dba64c69677e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:25 GMT
ADD file:222c5611b805658925ba615b0e69d40aa3dfa37223bc06f150909f7e944e426b in / 
# Tue, 25 Oct 2022 04:39:29 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 05:57:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 26 Oct 2022 05:57:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 05:57:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 26 Oct 2022 05:58:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Oct 2022 05:58:56 GMT
VOLUME [/spiped]
# Wed, 26 Oct 2022 05:58:59 GMT
WORKDIR /spiped
# Wed, 26 Oct 2022 05:59:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 26 Oct 2022 05:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 05:59:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f344f7fa0587aa4dbdc8d09d838d444853a1789047586a0927fa09fa89bb8f`  
		Last Modified: Tue, 25 Oct 2022 04:47:25 GMT  
		Size: 29.6 MB (29640590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690b2de19d8b758195a521ea98837b08f3b18bdeaf8e13fc48ad6981b3cb258c`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81aa4e5e1cfa28f7d8b4b77fadcb3b868b50c1dfb9509742f11a31583e80ae8b`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4cab88bca13a73ee16be74d5b6954fd7cc493932eae28211d1d38c59ff45bb`  
		Last Modified: Wed, 26 Oct 2022 05:59:23 GMT  
		Size: 5.7 MB (5706496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7037feb4132dd15404ae3b7a88c848f4902ea7eeea1adac94169bcc3beaf513e`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a68cac1944e8fd353746991422bc9603c5623d12f599ec437cb5d1d4d2524aa`  
		Last Modified: Wed, 26 Oct 2022 05:59:18 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
