## `spiped:latest`

```console
$ docker pull spiped@sha256:94359a8e1990ff36ab853ab8369adb12ca79d37c1a885535f33682a38c741c2a
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
$ docker pull spiped@sha256:90bfd10416afa78342540458b60380813136513dbd699664c8f99c4d68adf69b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38219444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d3cfcbb0a10c837a116b2f94b7fec72111a304d6b8ab2c9056f7356694ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:18:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 13:19:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:19:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 13:19:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 13:19:22 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 13:19:23 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 13:19:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 13:19:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 13:19:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512847f08e361b83bbac733bdf6c42ca80ea324f279a928ba756398ad20b9f43`  
		Last Modified: Wed, 24 Apr 2024 13:19:39 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1d3c4014b5a6534a414fac33f12d900f201ca54d549ea29f88a1d566657df5`  
		Last Modified: Wed, 24 Apr 2024 13:19:40 GMT  
		Size: 2.6 MB (2592141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d46a0930b6b160d223e6a8da2ee59fe89fa19b8fa5e2890ccace5eba7453d4c`  
		Last Modified: Wed, 24 Apr 2024 13:19:41 GMT  
		Size: 6.5 MB (6475222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c196fc438d9bab1552429bb643aebadc43f5ec4509e0a00cb19771a0381d74`  
		Last Modified: Wed, 24 Apr 2024 13:19:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8a8342a6b58fb102725d313661598a0fd9d51db1fdb7fd0bf041fa9ab9267c`  
		Last Modified: Wed, 24 Apr 2024 13:19:39 GMT  
		Size: 344.0 B  
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
$ docker pull spiped@sha256:21457cf1ed38aa248779952748b4014975ca971705a87e05d1cdc061e4757ddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31672395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6e9ada855a2a0f20f5bd7b3e3b3e496db0e1154344e946fd4766a128132a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:01:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 13:01:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:01:44 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 13:02:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 13:02:08 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 13:02:08 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 13:02:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 13:02:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 13:02:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d60d7d9ffcab89deddf2709b5314b8a901e6d68caf58f078b7b7a4d79e947d1`  
		Last Modified: Wed, 24 Apr 2024 13:02:25 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db2b34705f4cb651ef79bd01ebd29e2e955ebc29862ab78652092f8ec95c52`  
		Last Modified: Wed, 24 Apr 2024 13:02:25 GMT  
		Size: 2.0 MB (2046415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12102e48a882e96af443cb7230770deac4785f7e1c026c5003520d4c222d334a`  
		Last Modified: Wed, 24 Apr 2024 13:02:26 GMT  
		Size: 4.9 MB (4883934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425bee311e09ca9c8bfecd563c12753e9af5a69a2a0faa92c8026295f19ada7c`  
		Last Modified: Wed, 24 Apr 2024 13:02:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e41d786c9d0a238c0f9b3fd160e244113a870dbf5ca0fa93aa7fcb5823d223`  
		Last Modified: Wed, 24 Apr 2024 13:02:25 GMT  
		Size: 343.0 B  
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
$ docker pull spiped@sha256:d809bed5cf52243dbec9f0a0e3de72e8e1d34c37c3d3f9ccc7d916a39c69811f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38698227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf144c8375300b4ec8b408091590e0deec233d576a7bd0ab16ff92f7afbe800b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 16:54:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 24 Apr 2024 16:54:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 16:54:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 24 Apr 2024 16:54:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 16:54:43 GMT
VOLUME [/spiped]
# Wed, 24 Apr 2024 16:54:43 GMT
WORKDIR /spiped
# Wed, 24 Apr 2024 16:54:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 24 Apr 2024 16:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 16:54:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbf383dddbefc6d5de6faf8ed3e709485edec43cf5e24f57b63ec6129ff68f6`  
		Last Modified: Wed, 24 Apr 2024 16:54:54 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6bd4db8c563bb823a564937f4c3b9882106d71b4761d85669fe8ca81c0d74`  
		Last Modified: Wed, 24 Apr 2024 16:54:55 GMT  
		Size: 2.6 MB (2588288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b008a29ce9573edfc0a450f42aef408fcfb2af2866910922228f53971b9953`  
		Last Modified: Wed, 24 Apr 2024 16:54:56 GMT  
		Size: 5.9 MB (5945152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bdf4f63537c73f3e98df61d0bd77dfccfba35c29d4ab4a40473e83d8110bba`  
		Last Modified: Wed, 24 Apr 2024 16:54:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca6127ee95492810ceb1041a1aa3a3c0f8cbb788e1fa2be5e4352b3ad064363`  
		Last Modified: Wed, 24 Apr 2024 16:54:54 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:153c24f0dd09a5353e5dd1ed1dd054e5d45510ac12a5afd5f0d3b58f7d5e4cbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36785923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef848aabf72196d3c11ed91fe034ac69ed5617749f87d6c0ab03126ee1c5cc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:54:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 01:54:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:54:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 01:56:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 01:56:34 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 01:56:37 GMT
WORKDIR /spiped
# Tue, 14 May 2024 01:56:40 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 01:56:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 01:56:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdef46e105edb86c2552ac869a95fdd2c4824367627de638e257917180b08e`  
		Last Modified: Tue, 14 May 2024 01:57:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57680acccba3efceb1cf1b81f865c782625a6603485adc2ecea4bc1b32adc13a`  
		Last Modified: Tue, 14 May 2024 01:57:01 GMT  
		Size: 1.8 MB (1834563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85de9ca2f18714209ebd2ebc5e4dd213f29e68ffbcc1089c43225e915c1505a`  
		Last Modified: Tue, 14 May 2024 01:57:05 GMT  
		Size: 5.8 MB (5806157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ba8af9bbb4dab3a866eff279447121a64b6512af4b0a8e0bdaf191c833d22f`  
		Last Modified: Tue, 14 May 2024 01:57:00 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f87615d4306c239185378d1cb528e347e472092a12103536524bee2bb3fc75`  
		Last Modified: Tue, 14 May 2024 01:57:00 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:6ba8ee9fa6ed511e98b95b32a45ad011fde8d90aeeea92f49623fd202fc52df9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff4881054aa04b3aad0cd4f0f1757d4a0b258c40be84d8dc7c80736de5b331f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:47:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 06:47:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:47:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 06:48:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 06:48:21 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 06:48:21 GMT
WORKDIR /spiped
# Tue, 14 May 2024 06:48:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 06:48:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 06:48:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87e7ca095f6f11a12a340c19fd86321fc30b650e1e355c1a1b43b6cbb5781cc`  
		Last Modified: Tue, 14 May 2024 06:48:39 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48603cf0fb1dffd29e54fe2c2d7040537d3668125b90d35291ed7f9bb227b107`  
		Last Modified: Tue, 14 May 2024 06:48:40 GMT  
		Size: 2.8 MB (2770765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5dc61ca9c9ab4a5f0ae665363e8cfa2e872daa9daf57b5553d2280353bdb4`  
		Last Modified: Tue, 14 May 2024 06:48:41 GMT  
		Size: 6.4 MB (6424884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18eeea73825afd2eb18d24926f745919b93945c906bddb0522f76cefb059d17c`  
		Last Modified: Tue, 14 May 2024 06:48:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c0320b97124baa632f512164fc9d2da4ff936c97ec40bb09430177055d89b2`  
		Last Modified: Tue, 14 May 2024 06:48:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:2db77c5e870d6a0bfc488aee998b73b040369578d0d5d33932c2de0ed72e1bb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35165927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e75fe4cfb078b5e1c46b9354e383febfaf3ac8183dfe0c17276055f395fb14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:48:20 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 06:48:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:48:23 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 06:48:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 06:48:37 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 06:48:37 GMT
WORKDIR /spiped
# Tue, 14 May 2024 06:48:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 06:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 06:48:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0d2ce59bd3f63a7a42b12a54baec96507c187187178f61cd61d8ae8b792cf0`  
		Last Modified: Tue, 14 May 2024 06:48:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2dfd7e1fd2144c3454dbb88cbf55fb0fe7d0d06f014c5e5bc52f579a5cced`  
		Last Modified: Tue, 14 May 2024 06:48:59 GMT  
		Size: 2.3 MB (2262636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd4e5c8132655f27c1d4a02f3d0acebf642421c74a0e109f7050164b56351f1`  
		Last Modified: Tue, 14 May 2024 06:48:59 GMT  
		Size: 5.4 MB (5389293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e088cd40c8854632b76cbbf6ade3222b21d52ca79989edbba9c46f0dd9d80e4`  
		Last Modified: Tue, 14 May 2024 06:48:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7183cdf2e54b1f4e16d47b08f138bb3c940a6d698a04cbabfb3a699cb293c6`  
		Last Modified: Tue, 14 May 2024 06:48:58 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
