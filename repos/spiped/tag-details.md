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
$ docker pull spiped@sha256:b38dace8681c0548ca3efbeca7e98bfa787889fde945cbbd25e8a6a35a2df731
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
$ docker pull spiped@sha256:d6174dce3fecf3b6752dcd38c821b61e7fc94edc40c28d4bb5bb7e11fb81a466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38193851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d058ee727fdd6ebd8b86ce4f02abd119215fb3dc80d173ada87510328f94c6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:15:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 13:15:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:15:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 13:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 13:16:02 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 13:16:02 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 13:16:02 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 13:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 13:16:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9c3db1430bb3bd4dc4849a1330c4d869d2b731302a886a7fbc1880de64dad`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3350265def55a8f71539dca78f809bfea1615012072d72c6cbce2b2827fe39ce`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 2.6 MB (2590333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5943e7091aad57897fe68399111e43dfef451b76640b770f06c387826ddabb69`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 6.5 MB (6470559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f951925ea27afd7ff5cc0c832081ac7592f3feb9623d189260d4f1d69a3d8c49`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42f29d205de5866142124bac2d35bad9be7dec698d16af553d9c4d011126fd`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:29cfa4a321a429c9b20ea1db9e7635fb6ed60985c4569e2bf7d5a0c4c9ad8134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e746249f4c8fb405f348f12442c524fa9a15ffe766beabd7c54a48189f1de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 07:02:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 07:03:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:03:24 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 07:03:24 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 07:03:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 07:03:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d70989a804772fa099915cf1f907752715416e4e6a60985123f3b4cf2c4fa`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98132b986a9f117de02bb9bea9ea5b11909c0cbdc926be2406ebf804de0cd7bb`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 2.2 MB (2186959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae3ad664f72c6675d6854f5c92ae71d7a632b50437ebf3c33dd9e41c4875bcb`  
		Last Modified: Wed, 24 Apr 2024 07:03:34 GMT  
		Size: 5.1 MB (5142340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a52c4d6d159cda9baefbba9ab66b3ff953393b649690faaf8f1b65d7483f863`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a5f1c9349256949e4c2629a695bee764fa25d5270b91f1e6c040ce8e3677d9`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:97c17ddda18815a90a68b089abd261afcddb82b0e728c3ec43779fabeae427e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31648679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc71fc11101036e82749c58bbd5bfa789a0576b376f5d00130aff46330648c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 16:04:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 16:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 16:04:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 16:04:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 16:04:35 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 16:04:35 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 16:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 16:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 16:04:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0990cbdedce81ba65542d2fc3d123e27a6a11627ae6f9259952cb540b29377f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6705082be3386703306885feca37b8974ddab469a1b0092df43d30e13774ed34`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 2.0 MB (2044476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c216c018f20ec8b64085fd63e1b1e741ff081806d11153904f7fa41b12c468f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 4.9 MB (4879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b410b3980597e402a3375364b2677d566d90b41714b118a9b9e9535aba6ce05`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63510e11e1f66013642941772002d9bf23f53b7b27465131fe530221a9a51639`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9b18f6421993df7b7940976a131d689d7ed05c759206243fdb06cb451580c61a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408126d9550c2e9f53104587861d2efa41ed4b7b0c9a1fb3d93a44d36186722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 04:50:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 04:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:50:56 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 04:50:56 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 04:50:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:50:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:50:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53970c46362bb01a0345775eaba46c322728503b9354aeade73726799298bb94`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8e180690fdca3427f856d945ba08d9c5abc495893c1cf095df0433f4058e33`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 2.4 MB (2435026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca6da188e741a20decdbcf35788a2207d4c3c34a45733009a10dcb89b2c6cfb`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 5.5 MB (5485188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f8447f7d27a20d4083434a2cc8b6d0949813046638d88601c1119727f690b3`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16872a3d652b7e2c9c6f6b40c9373252674245690d2518a4bf357d65435b243`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:bdba44e97110e57fcb8a8c3f406f208f2a689a9e13fd6ff0cfc22eedf589313a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38676627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2fe7597cb270c6f19680ec990775086ff4780f81c1ec421de469b9ef39a2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:11 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 10 Apr 2024 00:57:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:26:03 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 07:26:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:26:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 07:26:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:26:38 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 07:26:38 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 07:26:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 07:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:26:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075041208cdfef42198fe1bb70c1f10feb1541009652b87faf1bcd0a7ee9caeb`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0771f9109ecabee7626450fd61b2e0d4b3a574867f0789dd72a9f29446e03`  
		Last Modified: Wed, 10 Apr 2024 07:26:53 GMT  
		Size: 2.6 MB (2586949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7765b812712ad2e7626ff5367b0b44a8569131ba953b52a5b6cdef58a98f854`  
		Last Modified: Wed, 10 Apr 2024 07:26:54 GMT  
		Size: 5.9 MB (5941565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d043586f23f69ddcc864bbcbb00cb559e5438ce10dc2b6e034203ef8be924`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f41e6a7707a86706698981f8a7040cbb1d71f3588621e5152008ac1e3f06d1`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:8d2fb7b1a07834381a69712d17b76fc2bb9c341300782b7c3a6991deeb7c629c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36786488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0694e1277f4a2bba651d06570e194e3aa011cdce846e39cfff689c147f9d6970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:40:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:41:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:41:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:42:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:42:48 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:42:51 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:42:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:42:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9998a31469d47d778d8a6759e7d9bb9d7c9ff375249f7e10e2e88bf561fdb7`  
		Last Modified: Wed, 24 Apr 2024 10:43:14 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da15c24913f3f9219b06da69b2ff323608ba103b55e5001df9236a2371ac77f`  
		Last Modified: Wed, 24 Apr 2024 10:43:16 GMT  
		Size: 1.8 MB (1834540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b285d8064a24cdb8bafe1712226e54bcc4a06e34e8ab06660ce7d2b62d0da40`  
		Last Modified: Wed, 24 Apr 2024 10:43:19 GMT  
		Size: 5.8 MB (5806259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac76759b6581e81ab55a788f759a01a0357a57ba638a10cf6a7c560ed32bb6`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43f983e5168a2c5b6c7a2c720ab374be550c7d878fa87e19ab747d67dc45a`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:68a0177c7364d26a8ee8e112cb1826bb7438f3ed29a63572bc90549d2f3f8e63
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44b181c4c73d1dceabd1c334a2d4eff7e26145b1fc12f9074caed8ec282b56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:27:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 09:27:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:27:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 09:28:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 09:28:51 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 09:28:52 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 09:28:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c9ebe0bb7de83f9151e1fa7f228595bc68566f9b23284903a01d2c800ca2eb`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa4fb75b2521ba7763a2137a188ac23b74e2965251e8dce818b88db6962bd6`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 2.8 MB (2770794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a014e889c4d9fd5a6b0b7a051da79384a745238b1b7f21ada67ef03bd8c5aef`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 6.4 MB (6425079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0424dc308576165962e23be07d49ab5c6ed1335514b572b59bde2183d5c997`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383f9e0c42daa653f374d309ace5ad3592429df00f5cc2b54aa3af69fb383f09`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:856d257cf760fc4c60b561cf644e5cbfb74ac4282b49b88395dcbcf55d115763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35166159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0ec465f0aa002e7a0ecca9f6be2ecaf6c17494425b225eeadf2371feb00ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:30:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:31:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:31:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:31:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:31:53 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:31:54 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:31:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:31:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b44c3362a19a50805e038d9890ba476b988d1992b3751b5357cb198e524b27`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a6f0da68d7ad89ef8d2651158acc8337bb3d587155e4ba5e246d8eb4a1a69e`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 2.3 MB (2262737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20083ad877538927d5d4be2218bd1b596a47f11244ca451c7ef8441cec52c04`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 5.4 MB (5389464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cdc8b500171048ec3d191873fa7b2fc052e91eb62932e020d46c2193fc285`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121c88ab8e74a88539e50f98eb34ec0ecc99b553ab37fdaf48e7d2282e860e9e`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac9655daf19c8c0147be28fd461895ef3a1c79db08b596ed2d588b6a3c816504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ddadfdc5396a002ff71f7430163abb731e6890e7a49c16d77c5649e58dba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:07:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:08:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:08:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:08:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:08:13 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:08:13 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:08:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508806baeb68406329423224090a40940d296f944edc857b31946a1e0b2eb94`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d8676a55b9005ca166d422eafb181f4e0dd038fe4912102eb35278224336b`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.4 MB (1353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a80dfc8677984adef1a26dd3a1761ea6cb42ae6b57a49cdf27458771baa848`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2b104abfcd98f8e2aaab8be718007a2219883fc986e109873f9e777847b30`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae79c3a2a70ad960e3ab773fce80eea1b3cda5966da88a81b40895af47cda41`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:b38dace8681c0548ca3efbeca7e98bfa787889fde945cbbd25e8a6a35a2df731
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
$ docker pull spiped@sha256:d6174dce3fecf3b6752dcd38c821b61e7fc94edc40c28d4bb5bb7e11fb81a466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38193851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d058ee727fdd6ebd8b86ce4f02abd119215fb3dc80d173ada87510328f94c6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:15:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 13:15:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:15:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 13:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 13:16:02 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 13:16:02 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 13:16:02 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 13:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 13:16:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9c3db1430bb3bd4dc4849a1330c4d869d2b731302a886a7fbc1880de64dad`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3350265def55a8f71539dca78f809bfea1615012072d72c6cbce2b2827fe39ce`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 2.6 MB (2590333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5943e7091aad57897fe68399111e43dfef451b76640b770f06c387826ddabb69`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 6.5 MB (6470559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f951925ea27afd7ff5cc0c832081ac7592f3feb9623d189260d4f1d69a3d8c49`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42f29d205de5866142124bac2d35bad9be7dec698d16af553d9c4d011126fd`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:29cfa4a321a429c9b20ea1db9e7635fb6ed60985c4569e2bf7d5a0c4c9ad8134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e746249f4c8fb405f348f12442c524fa9a15ffe766beabd7c54a48189f1de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 07:02:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 07:03:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:03:24 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 07:03:24 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 07:03:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 07:03:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d70989a804772fa099915cf1f907752715416e4e6a60985123f3b4cf2c4fa`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98132b986a9f117de02bb9bea9ea5b11909c0cbdc926be2406ebf804de0cd7bb`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 2.2 MB (2186959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae3ad664f72c6675d6854f5c92ae71d7a632b50437ebf3c33dd9e41c4875bcb`  
		Last Modified: Wed, 24 Apr 2024 07:03:34 GMT  
		Size: 5.1 MB (5142340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a52c4d6d159cda9baefbba9ab66b3ff953393b649690faaf8f1b65d7483f863`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a5f1c9349256949e4c2629a695bee764fa25d5270b91f1e6c040ce8e3677d9`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:97c17ddda18815a90a68b089abd261afcddb82b0e728c3ec43779fabeae427e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31648679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc71fc11101036e82749c58bbd5bfa789a0576b376f5d00130aff46330648c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 16:04:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 16:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 16:04:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 16:04:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 16:04:35 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 16:04:35 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 16:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 16:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 16:04:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0990cbdedce81ba65542d2fc3d123e27a6a11627ae6f9259952cb540b29377f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6705082be3386703306885feca37b8974ddab469a1b0092df43d30e13774ed34`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 2.0 MB (2044476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c216c018f20ec8b64085fd63e1b1e741ff081806d11153904f7fa41b12c468f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 4.9 MB (4879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b410b3980597e402a3375364b2677d566d90b41714b118a9b9e9535aba6ce05`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63510e11e1f66013642941772002d9bf23f53b7b27465131fe530221a9a51639`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9b18f6421993df7b7940976a131d689d7ed05c759206243fdb06cb451580c61a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408126d9550c2e9f53104587861d2efa41ed4b7b0c9a1fb3d93a44d36186722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 04:50:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 04:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:50:56 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 04:50:56 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 04:50:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:50:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:50:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53970c46362bb01a0345775eaba46c322728503b9354aeade73726799298bb94`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8e180690fdca3427f856d945ba08d9c5abc495893c1cf095df0433f4058e33`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 2.4 MB (2435026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca6da188e741a20decdbcf35788a2207d4c3c34a45733009a10dcb89b2c6cfb`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 5.5 MB (5485188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f8447f7d27a20d4083434a2cc8b6d0949813046638d88601c1119727f690b3`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16872a3d652b7e2c9c6f6b40c9373252674245690d2518a4bf357d65435b243`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:bdba44e97110e57fcb8a8c3f406f208f2a689a9e13fd6ff0cfc22eedf589313a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38676627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2fe7597cb270c6f19680ec990775086ff4780f81c1ec421de469b9ef39a2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:11 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 10 Apr 2024 00:57:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:26:03 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 07:26:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:26:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 07:26:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:26:38 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 07:26:38 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 07:26:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 07:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:26:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075041208cdfef42198fe1bb70c1f10feb1541009652b87faf1bcd0a7ee9caeb`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0771f9109ecabee7626450fd61b2e0d4b3a574867f0789dd72a9f29446e03`  
		Last Modified: Wed, 10 Apr 2024 07:26:53 GMT  
		Size: 2.6 MB (2586949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7765b812712ad2e7626ff5367b0b44a8569131ba953b52a5b6cdef58a98f854`  
		Last Modified: Wed, 10 Apr 2024 07:26:54 GMT  
		Size: 5.9 MB (5941565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d043586f23f69ddcc864bbcbb00cb559e5438ce10dc2b6e034203ef8be924`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f41e6a7707a86706698981f8a7040cbb1d71f3588621e5152008ac1e3f06d1`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:8d2fb7b1a07834381a69712d17b76fc2bb9c341300782b7c3a6991deeb7c629c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36786488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0694e1277f4a2bba651d06570e194e3aa011cdce846e39cfff689c147f9d6970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:40:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:41:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:41:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:42:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:42:48 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:42:51 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:42:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:42:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9998a31469d47d778d8a6759e7d9bb9d7c9ff375249f7e10e2e88bf561fdb7`  
		Last Modified: Wed, 24 Apr 2024 10:43:14 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da15c24913f3f9219b06da69b2ff323608ba103b55e5001df9236a2371ac77f`  
		Last Modified: Wed, 24 Apr 2024 10:43:16 GMT  
		Size: 1.8 MB (1834540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b285d8064a24cdb8bafe1712226e54bcc4a06e34e8ab06660ce7d2b62d0da40`  
		Last Modified: Wed, 24 Apr 2024 10:43:19 GMT  
		Size: 5.8 MB (5806259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac76759b6581e81ab55a788f759a01a0357a57ba638a10cf6a7c560ed32bb6`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43f983e5168a2c5b6c7a2c720ab374be550c7d878fa87e19ab747d67dc45a`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:68a0177c7364d26a8ee8e112cb1826bb7438f3ed29a63572bc90549d2f3f8e63
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44b181c4c73d1dceabd1c334a2d4eff7e26145b1fc12f9074caed8ec282b56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:27:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 09:27:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:27:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 09:28:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 09:28:51 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 09:28:52 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 09:28:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c9ebe0bb7de83f9151e1fa7f228595bc68566f9b23284903a01d2c800ca2eb`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa4fb75b2521ba7763a2137a188ac23b74e2965251e8dce818b88db6962bd6`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 2.8 MB (2770794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a014e889c4d9fd5a6b0b7a051da79384a745238b1b7f21ada67ef03bd8c5aef`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 6.4 MB (6425079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0424dc308576165962e23be07d49ab5c6ed1335514b572b59bde2183d5c997`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383f9e0c42daa653f374d309ace5ad3592429df00f5cc2b54aa3af69fb383f09`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:856d257cf760fc4c60b561cf644e5cbfb74ac4282b49b88395dcbcf55d115763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35166159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0ec465f0aa002e7a0ecca9f6be2ecaf6c17494425b225eeadf2371feb00ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:30:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:31:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:31:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:31:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:31:53 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:31:54 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:31:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:31:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b44c3362a19a50805e038d9890ba476b988d1992b3751b5357cb198e524b27`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a6f0da68d7ad89ef8d2651158acc8337bb3d587155e4ba5e246d8eb4a1a69e`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 2.3 MB (2262737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20083ad877538927d5d4be2218bd1b596a47f11244ca451c7ef8441cec52c04`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 5.4 MB (5389464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cdc8b500171048ec3d191873fa7b2fc052e91eb62932e020d46c2193fc285`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121c88ab8e74a88539e50f98eb34ec0ecc99b553ab37fdaf48e7d2282e860e9e`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac9655daf19c8c0147be28fd461895ef3a1c79db08b596ed2d588b6a3c816504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ddadfdc5396a002ff71f7430163abb731e6890e7a49c16d77c5649e58dba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:07:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:08:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:08:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:08:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:08:13 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:08:13 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:08:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508806baeb68406329423224090a40940d296f944edc857b31946a1e0b2eb94`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d8676a55b9005ca166d422eafb181f4e0dd038fe4912102eb35278224336b`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.4 MB (1353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a80dfc8677984adef1a26dd3a1761ea6cb42ae6b57a49cdf27458771baa848`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2b104abfcd98f8e2aaab8be718007a2219883fc986e109873f9e777847b30`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae79c3a2a70ad960e3ab773fce80eea1b3cda5966da88a81b40895af47cda41`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:b38dace8681c0548ca3efbeca7e98bfa787889fde945cbbd25e8a6a35a2df731
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
$ docker pull spiped@sha256:d6174dce3fecf3b6752dcd38c821b61e7fc94edc40c28d4bb5bb7e11fb81a466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38193851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d058ee727fdd6ebd8b86ce4f02abd119215fb3dc80d173ada87510328f94c6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:15:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 13:15:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:15:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 13:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 13:16:02 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 13:16:02 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 13:16:02 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 13:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 13:16:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9c3db1430bb3bd4dc4849a1330c4d869d2b731302a886a7fbc1880de64dad`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3350265def55a8f71539dca78f809bfea1615012072d72c6cbce2b2827fe39ce`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 2.6 MB (2590333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5943e7091aad57897fe68399111e43dfef451b76640b770f06c387826ddabb69`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 6.5 MB (6470559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f951925ea27afd7ff5cc0c832081ac7592f3feb9623d189260d4f1d69a3d8c49`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42f29d205de5866142124bac2d35bad9be7dec698d16af553d9c4d011126fd`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:29cfa4a321a429c9b20ea1db9e7635fb6ed60985c4569e2bf7d5a0c4c9ad8134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e746249f4c8fb405f348f12442c524fa9a15ffe766beabd7c54a48189f1de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 07:02:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 07:03:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:03:24 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 07:03:24 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 07:03:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 07:03:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d70989a804772fa099915cf1f907752715416e4e6a60985123f3b4cf2c4fa`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98132b986a9f117de02bb9bea9ea5b11909c0cbdc926be2406ebf804de0cd7bb`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 2.2 MB (2186959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae3ad664f72c6675d6854f5c92ae71d7a632b50437ebf3c33dd9e41c4875bcb`  
		Last Modified: Wed, 24 Apr 2024 07:03:34 GMT  
		Size: 5.1 MB (5142340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a52c4d6d159cda9baefbba9ab66b3ff953393b649690faaf8f1b65d7483f863`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a5f1c9349256949e4c2629a695bee764fa25d5270b91f1e6c040ce8e3677d9`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:97c17ddda18815a90a68b089abd261afcddb82b0e728c3ec43779fabeae427e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31648679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc71fc11101036e82749c58bbd5bfa789a0576b376f5d00130aff46330648c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 16:04:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 16:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 16:04:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 16:04:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 16:04:35 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 16:04:35 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 16:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 16:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 16:04:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0990cbdedce81ba65542d2fc3d123e27a6a11627ae6f9259952cb540b29377f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6705082be3386703306885feca37b8974ddab469a1b0092df43d30e13774ed34`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 2.0 MB (2044476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c216c018f20ec8b64085fd63e1b1e741ff081806d11153904f7fa41b12c468f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 4.9 MB (4879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b410b3980597e402a3375364b2677d566d90b41714b118a9b9e9535aba6ce05`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63510e11e1f66013642941772002d9bf23f53b7b27465131fe530221a9a51639`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9b18f6421993df7b7940976a131d689d7ed05c759206243fdb06cb451580c61a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408126d9550c2e9f53104587861d2efa41ed4b7b0c9a1fb3d93a44d36186722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 04:50:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 04:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:50:56 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 04:50:56 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 04:50:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:50:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:50:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53970c46362bb01a0345775eaba46c322728503b9354aeade73726799298bb94`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8e180690fdca3427f856d945ba08d9c5abc495893c1cf095df0433f4058e33`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 2.4 MB (2435026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca6da188e741a20decdbcf35788a2207d4c3c34a45733009a10dcb89b2c6cfb`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 5.5 MB (5485188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f8447f7d27a20d4083434a2cc8b6d0949813046638d88601c1119727f690b3`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16872a3d652b7e2c9c6f6b40c9373252674245690d2518a4bf357d65435b243`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:bdba44e97110e57fcb8a8c3f406f208f2a689a9e13fd6ff0cfc22eedf589313a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38676627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2fe7597cb270c6f19680ec990775086ff4780f81c1ec421de469b9ef39a2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:11 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 10 Apr 2024 00:57:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:26:03 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 07:26:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:26:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 07:26:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:26:38 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 07:26:38 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 07:26:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 07:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:26:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075041208cdfef42198fe1bb70c1f10feb1541009652b87faf1bcd0a7ee9caeb`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0771f9109ecabee7626450fd61b2e0d4b3a574867f0789dd72a9f29446e03`  
		Last Modified: Wed, 10 Apr 2024 07:26:53 GMT  
		Size: 2.6 MB (2586949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7765b812712ad2e7626ff5367b0b44a8569131ba953b52a5b6cdef58a98f854`  
		Last Modified: Wed, 10 Apr 2024 07:26:54 GMT  
		Size: 5.9 MB (5941565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d043586f23f69ddcc864bbcbb00cb559e5438ce10dc2b6e034203ef8be924`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f41e6a7707a86706698981f8a7040cbb1d71f3588621e5152008ac1e3f06d1`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:8d2fb7b1a07834381a69712d17b76fc2bb9c341300782b7c3a6991deeb7c629c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36786488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0694e1277f4a2bba651d06570e194e3aa011cdce846e39cfff689c147f9d6970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:40:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:41:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:41:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:42:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:42:48 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:42:51 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:42:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:42:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9998a31469d47d778d8a6759e7d9bb9d7c9ff375249f7e10e2e88bf561fdb7`  
		Last Modified: Wed, 24 Apr 2024 10:43:14 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da15c24913f3f9219b06da69b2ff323608ba103b55e5001df9236a2371ac77f`  
		Last Modified: Wed, 24 Apr 2024 10:43:16 GMT  
		Size: 1.8 MB (1834540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b285d8064a24cdb8bafe1712226e54bcc4a06e34e8ab06660ce7d2b62d0da40`  
		Last Modified: Wed, 24 Apr 2024 10:43:19 GMT  
		Size: 5.8 MB (5806259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac76759b6581e81ab55a788f759a01a0357a57ba638a10cf6a7c560ed32bb6`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43f983e5168a2c5b6c7a2c720ab374be550c7d878fa87e19ab747d67dc45a`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:68a0177c7364d26a8ee8e112cb1826bb7438f3ed29a63572bc90549d2f3f8e63
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44b181c4c73d1dceabd1c334a2d4eff7e26145b1fc12f9074caed8ec282b56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:27:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 09:27:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:27:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 09:28:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 09:28:51 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 09:28:52 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 09:28:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c9ebe0bb7de83f9151e1fa7f228595bc68566f9b23284903a01d2c800ca2eb`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa4fb75b2521ba7763a2137a188ac23b74e2965251e8dce818b88db6962bd6`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 2.8 MB (2770794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a014e889c4d9fd5a6b0b7a051da79384a745238b1b7f21ada67ef03bd8c5aef`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 6.4 MB (6425079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0424dc308576165962e23be07d49ab5c6ed1335514b572b59bde2183d5c997`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383f9e0c42daa653f374d309ace5ad3592429df00f5cc2b54aa3af69fb383f09`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:856d257cf760fc4c60b561cf644e5cbfb74ac4282b49b88395dcbcf55d115763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35166159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0ec465f0aa002e7a0ecca9f6be2ecaf6c17494425b225eeadf2371feb00ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:30:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:31:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:31:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:31:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:31:53 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:31:54 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:31:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:31:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b44c3362a19a50805e038d9890ba476b988d1992b3751b5357cb198e524b27`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a6f0da68d7ad89ef8d2651158acc8337bb3d587155e4ba5e246d8eb4a1a69e`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 2.3 MB (2262737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20083ad877538927d5d4be2218bd1b596a47f11244ca451c7ef8441cec52c04`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 5.4 MB (5389464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cdc8b500171048ec3d191873fa7b2fc052e91eb62932e020d46c2193fc285`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121c88ab8e74a88539e50f98eb34ec0ecc99b553ab37fdaf48e7d2282e860e9e`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac9655daf19c8c0147be28fd461895ef3a1c79db08b596ed2d588b6a3c816504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ddadfdc5396a002ff71f7430163abb731e6890e7a49c16d77c5649e58dba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:07:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:08:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:08:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:08:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:08:13 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:08:13 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:08:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508806baeb68406329423224090a40940d296f944edc857b31946a1e0b2eb94`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d8676a55b9005ca166d422eafb181f4e0dd038fe4912102eb35278224336b`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.4 MB (1353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a80dfc8677984adef1a26dd3a1761ea6cb42ae6b57a49cdf27458771baa848`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2b104abfcd98f8e2aaab8be718007a2219883fc986e109873f9e777847b30`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae79c3a2a70ad960e3ab773fce80eea1b3cda5966da88a81b40895af47cda41`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac9655daf19c8c0147be28fd461895ef3a1c79db08b596ed2d588b6a3c816504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ddadfdc5396a002ff71f7430163abb731e6890e7a49c16d77c5649e58dba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:07:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:08:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:08:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:08:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:08:13 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:08:13 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:08:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508806baeb68406329423224090a40940d296f944edc857b31946a1e0b2eb94`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d8676a55b9005ca166d422eafb181f4e0dd038fe4912102eb35278224336b`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.4 MB (1353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a80dfc8677984adef1a26dd3a1761ea6cb42ae6b57a49cdf27458771baa848`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2b104abfcd98f8e2aaab8be718007a2219883fc986e109873f9e777847b30`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae79c3a2a70ad960e3ab773fce80eea1b3cda5966da88a81b40895af47cda41`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:b38dace8681c0548ca3efbeca7e98bfa787889fde945cbbd25e8a6a35a2df731
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
$ docker pull spiped@sha256:d6174dce3fecf3b6752dcd38c821b61e7fc94edc40c28d4bb5bb7e11fb81a466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38193851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d058ee727fdd6ebd8b86ce4f02abd119215fb3dc80d173ada87510328f94c6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:15:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 13:15:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:15:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 13:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 13:16:02 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 13:16:02 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 13:16:02 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 13:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 13:16:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9c3db1430bb3bd4dc4849a1330c4d869d2b731302a886a7fbc1880de64dad`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3350265def55a8f71539dca78f809bfea1615012072d72c6cbce2b2827fe39ce`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 2.6 MB (2590333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5943e7091aad57897fe68399111e43dfef451b76640b770f06c387826ddabb69`  
		Last Modified: Wed, 10 Apr 2024 13:16:19 GMT  
		Size: 6.5 MB (6470559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f951925ea27afd7ff5cc0c832081ac7592f3feb9623d189260d4f1d69a3d8c49`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42f29d205de5866142124bac2d35bad9be7dec698d16af553d9c4d011126fd`  
		Last Modified: Wed, 10 Apr 2024 13:16:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:29cfa4a321a429c9b20ea1db9e7635fb6ed60985c4569e2bf7d5a0c4c9ad8134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e746249f4c8fb405f348f12442c524fa9a15ffe766beabd7c54a48189f1de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 07:02:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 07:03:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:03:24 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 07:03:24 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 07:03:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 07:03:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d70989a804772fa099915cf1f907752715416e4e6a60985123f3b4cf2c4fa`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98132b986a9f117de02bb9bea9ea5b11909c0cbdc926be2406ebf804de0cd7bb`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 2.2 MB (2186959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae3ad664f72c6675d6854f5c92ae71d7a632b50437ebf3c33dd9e41c4875bcb`  
		Last Modified: Wed, 24 Apr 2024 07:03:34 GMT  
		Size: 5.1 MB (5142340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a52c4d6d159cda9baefbba9ab66b3ff953393b649690faaf8f1b65d7483f863`  
		Last Modified: Wed, 24 Apr 2024 07:03:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a5f1c9349256949e4c2629a695bee764fa25d5270b91f1e6c040ce8e3677d9`  
		Last Modified: Wed, 24 Apr 2024 07:03:32 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:97c17ddda18815a90a68b089abd261afcddb82b0e728c3ec43779fabeae427e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31648679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc71fc11101036e82749c58bbd5bfa789a0576b376f5d00130aff46330648c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 16:04:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 16:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 16:04:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 16:04:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 16:04:35 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 16:04:35 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 16:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 16:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 16:04:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0990cbdedce81ba65542d2fc3d123e27a6a11627ae6f9259952cb540b29377f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6705082be3386703306885feca37b8974ddab469a1b0092df43d30e13774ed34`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 2.0 MB (2044476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c216c018f20ec8b64085fd63e1b1e741ff081806d11153904f7fa41b12c468f`  
		Last Modified: Wed, 10 Apr 2024 16:04:50 GMT  
		Size: 4.9 MB (4879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b410b3980597e402a3375364b2677d566d90b41714b118a9b9e9535aba6ce05`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63510e11e1f66013642941772002d9bf23f53b7b27465131fe530221a9a51639`  
		Last Modified: Wed, 10 Apr 2024 16:04:49 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9b18f6421993df7b7940976a131d689d7ed05c759206243fdb06cb451580c61a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408126d9550c2e9f53104587861d2efa41ed4b7b0c9a1fb3d93a44d36186722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 04:50:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 04:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:50:56 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 04:50:56 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 04:50:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:50:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:50:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53970c46362bb01a0345775eaba46c322728503b9354aeade73726799298bb94`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8e180690fdca3427f856d945ba08d9c5abc495893c1cf095df0433f4058e33`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 2.4 MB (2435026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca6da188e741a20decdbcf35788a2207d4c3c34a45733009a10dcb89b2c6cfb`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 5.5 MB (5485188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f8447f7d27a20d4083434a2cc8b6d0949813046638d88601c1119727f690b3`  
		Last Modified: Wed, 24 Apr 2024 04:51:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16872a3d652b7e2c9c6f6b40c9373252674245690d2518a4bf357d65435b243`  
		Last Modified: Wed, 24 Apr 2024 04:51:10 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:bdba44e97110e57fcb8a8c3f406f208f2a689a9e13fd6ff0cfc22eedf589313a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38676627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2fe7597cb270c6f19680ec990775086ff4780f81c1ec421de469b9ef39a2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:11 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 10 Apr 2024 00:57:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:26:03 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 10 Apr 2024 07:26:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:26:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 10 Apr 2024 07:26:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:26:38 GMT
VOLUME [/spiped]
# Wed, 10 Apr 2024 07:26:38 GMT
WORKDIR /spiped
# Wed, 10 Apr 2024 07:26:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 10 Apr 2024 07:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:26:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075041208cdfef42198fe1bb70c1f10feb1541009652b87faf1bcd0a7ee9caeb`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0771f9109ecabee7626450fd61b2e0d4b3a574867f0789dd72a9f29446e03`  
		Last Modified: Wed, 10 Apr 2024 07:26:53 GMT  
		Size: 2.6 MB (2586949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7765b812712ad2e7626ff5367b0b44a8569131ba953b52a5b6cdef58a98f854`  
		Last Modified: Wed, 10 Apr 2024 07:26:54 GMT  
		Size: 5.9 MB (5941565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d043586f23f69ddcc864bbcbb00cb559e5438ce10dc2b6e034203ef8be924`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f41e6a7707a86706698981f8a7040cbb1d71f3588621e5152008ac1e3f06d1`  
		Last Modified: Wed, 10 Apr 2024 07:26:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:8d2fb7b1a07834381a69712d17b76fc2bb9c341300782b7c3a6991deeb7c629c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36786488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0694e1277f4a2bba651d06570e194e3aa011cdce846e39cfff689c147f9d6970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:40:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:41:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:41:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:42:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:42:48 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:42:51 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:42:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:42:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9998a31469d47d778d8a6759e7d9bb9d7c9ff375249f7e10e2e88bf561fdb7`  
		Last Modified: Wed, 24 Apr 2024 10:43:14 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da15c24913f3f9219b06da69b2ff323608ba103b55e5001df9236a2371ac77f`  
		Last Modified: Wed, 24 Apr 2024 10:43:16 GMT  
		Size: 1.8 MB (1834540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b285d8064a24cdb8bafe1712226e54bcc4a06e34e8ab06660ce7d2b62d0da40`  
		Last Modified: Wed, 24 Apr 2024 10:43:19 GMT  
		Size: 5.8 MB (5806259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac76759b6581e81ab55a788f759a01a0357a57ba638a10cf6a7c560ed32bb6`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43f983e5168a2c5b6c7a2c720ab374be550c7d878fa87e19ab747d67dc45a`  
		Last Modified: Wed, 24 Apr 2024 10:43:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:68a0177c7364d26a8ee8e112cb1826bb7438f3ed29a63572bc90549d2f3f8e63
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44b181c4c73d1dceabd1c334a2d4eff7e26145b1fc12f9074caed8ec282b56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:27:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 09:27:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:27:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 09:28:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 09:28:51 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 09:28:52 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 09:28:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c9ebe0bb7de83f9151e1fa7f228595bc68566f9b23284903a01d2c800ca2eb`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa4fb75b2521ba7763a2137a188ac23b74e2965251e8dce818b88db6962bd6`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 2.8 MB (2770794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a014e889c4d9fd5a6b0b7a051da79384a745238b1b7f21ada67ef03bd8c5aef`  
		Last Modified: Wed, 24 Apr 2024 09:29:09 GMT  
		Size: 6.4 MB (6425079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0424dc308576165962e23be07d49ab5c6ed1335514b572b59bde2183d5c997`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383f9e0c42daa653f374d309ace5ad3592429df00f5cc2b54aa3af69fb383f09`  
		Last Modified: Wed, 24 Apr 2024 09:29:08 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:856d257cf760fc4c60b561cf644e5cbfb74ac4282b49b88395dcbcf55d115763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35166159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0ec465f0aa002e7a0ecca9f6be2ecaf6c17494425b225eeadf2371feb00ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:30:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 10:31:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:31:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 10:31:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:31:53 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 10:31:54 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 10:31:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 10:31:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b44c3362a19a50805e038d9890ba476b988d1992b3751b5357cb198e524b27`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a6f0da68d7ad89ef8d2651158acc8337bb3d587155e4ba5e246d8eb4a1a69e`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 2.3 MB (2262737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20083ad877538927d5d4be2218bd1b596a47f11244ca451c7ef8441cec52c04`  
		Last Modified: Wed, 24 Apr 2024 10:32:26 GMT  
		Size: 5.4 MB (5389464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cdc8b500171048ec3d191873fa7b2fc052e91eb62932e020d46c2193fc285`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121c88ab8e74a88539e50f98eb34ec0ecc99b553ab37fdaf48e7d2282e860e9e`  
		Last Modified: Wed, 24 Apr 2024 10:32:25 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
