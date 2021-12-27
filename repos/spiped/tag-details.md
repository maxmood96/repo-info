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
$ docker pull spiped@sha256:4827c3db0ce1c675a500d8272f10dffa716f6d1915ba8527a0115e4af08f5677
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
$ docker pull spiped@sha256:2bd2286a40c61a56f280444f68f9c3d0ae7a310858860aba77b0403b8890c9f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37321326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4914da9141203212b68712b5f3a3711294f5e0e02a612eec74bd1b2e1241b9b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 12:54:46 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 12:54:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 12:54:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 12:55:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 12:55:16 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 12:55:16 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 12:55:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 12:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 12:55:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5942a3089c9d199ffd7567fc18e1491777fdade26ec8bdf4d160bf3c8d83f324`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f2d189091c21b4eee0a6fe6553c7c7ad5a1fba49319eac9c272a96ac7fbdd`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f16287ae7ba5070d7edb0070fe71b973932136de80e4a4dd1013707e336b0c7`  
		Last Modified: Tue, 21 Dec 2021 12:55:41 GMT  
		Size: 6.0 MB (5960446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e68e4478591fe99bf722077de675519de67d719f9677d67f1ddc4d8f2cec294`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587fde5003f001f256acac00acf4ea7b0205ea8770d68ee6a9a2d3c87c369d95`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2bb8d6f9786620cb6d809309fe172b33c989c54afa2e70963dc028539cc711de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33930835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb20a687f8f10c7552075675e860628f3cabd9d85426df4168e2085074497125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:48:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:48:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:48:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:49:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:49:39 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:49:40 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:49:40 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:49:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a6f781a7abbf2236545af22e3b305148755b938eb4b3f80acfddda83fb330`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901947b41fdff91f97c93d69ea6510e742f77e91ebe42dfb3151adcdaf03441a`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f468550fb64a624779d011e733e2288492ceeefbf1195d64f8bd54e57f57e4f`  
		Last Modified: Mon, 27 Dec 2021 17:50:18 GMT  
		Size: 5.0 MB (5027325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa37e6545912e2b7148568d33bbf517e5deadd118df40ce2ebe5f74710c2d66`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0df784f0906422ce5e4c8eb5ee379506682e1ad31e783eeca4525c79ba55c`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5ff37adf5b2ffdb562129ff2c4c257c774150b80d954a9a0de388a5cd9c14ab4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31311461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa1788ed3cfcc665390b07c5ea81b3818793dc7e8cd3cff01c89fc109cb0be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:59:48 GMT
ADD file:6a5555c3e40db91fae5bb112464a4c405a976de17ff64c98f25d3033a6a608d8 in / 
# Tue, 21 Dec 2021 01:59:48 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:58:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:58:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:58:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:59:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:59:47 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:59:47 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:59:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:59:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d0061d6703dc4975804c3419e00c85efbe3f1b79c86d87e048fa14a683e88e31`  
		Last Modified: Tue, 21 Dec 2021 02:15:26 GMT  
		Size: 26.6 MB (26560815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d1aaaf5cba2bb5aa182cc038a59938629d1ad6ec388340be3e8f34e5e65b0`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6950d1ddd5e954a00fd9b56a607f737d4394ec2519f9c9d47ce2820e12bcfb`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6424dc46a62a8c5530fa74a2aaddc612ea6e099df67cfbe39b49dad4b2416fa4`  
		Last Modified: Mon, 27 Dec 2021 18:01:21 GMT  
		Size: 4.7 MB (4747390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b16a5e406437b655a5c55e8e9027607ad607deb3047cf60539ca94a8a6dd8be`  
		Last Modified: Mon, 27 Dec 2021 18:01:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c526844e52b7ac486211e17526f3bd96806de407bdad85bbace1e9268e01d2c`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:076eed23d69622023465551277b292c4b20c7e53ff970f4ec2c0c88c721002a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558381a048e4dd5c28f2a72bdfb28f021302afc0b9044d17373f8513e2c57b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 13:37:31 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 13:37:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 13:37:35 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 13:37:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 13:37:57 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 13:37:58 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 13:38:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 13:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 13:38:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11307cfb62981d1477c624d0946d440cae59b97d5241be5622b4a1a2170b7087`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b4f4a9f9d7183fa8a6390427dd6151121434bd32d1539e46a81b5b7195e9e`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498cf759f2f5ad49bf12c6c9162ea1c630f9fba1005c0a5cd96d9d40f3c3bc9c`  
		Last Modified: Tue, 21 Dec 2021 13:38:30 GMT  
		Size: 5.3 MB (5263680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7310cca9b3933670873fa963c55ba0370617e570124050a904a3eabfd50f0b8a`  
		Last Modified: Tue, 21 Dec 2021 13:38:29 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ebb7feec0bee35aea3ecb3f98485656fa38f1ef9c1c9faccf4d07b68e3ebbe`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:5b3875cce8fad4903a3c884cef05e5abad051bc9951e8e5410114e95e0dac53e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40258475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302f102ca38e8fbd96146e30bc1ab35ebeaf9330138e5b0b7d258e8c9cb0b61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 21:50:17 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 21:50:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 21:50:24 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 21:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 21:51:10 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 21:51:11 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 21:51:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 21:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 21:51:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489da5566cb0c924c029e46f8dad5bcafab6d42a56da88a93f2801d29558ff51`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db213f8397acea926fb592d3befbbdb2c002c268a3d54cb1d5c2d98de07b6f00`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a4ea8b87e71f3244324d2ead099212bccde6f64ef51cbe9d8ec4d43b36028`  
		Last Modified: Tue, 21 Dec 2021 21:52:08 GMT  
		Size: 7.9 MB (7884366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5619dad69ca0adbec11d01730713268fe39795d31498b6b4fe5494a59579236`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3945ddda45549df85f0eed7cab7fef6325fd37f1b4ef32546894d2af03acfd`  
		Last Modified: Tue, 21 Dec 2021 21:52:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:130c01d2a02859608af1ff69b512e606c6b0afab129f4f55f3b214e4439a961e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35327767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8059d8a507f312d8d77dc186576b8b33cbc65306a9ff8fd918ca17b2b9163198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:07:30 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:08:36 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:08:37 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:08:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:08:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc41050c10fb28c363303084d216e4a84358c365e0c0c3ea780e76094ac5b62`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccfed374e34e3e33bb1dac88ddd7d7bd1e7f5274368492e37c693a71768d15b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7546f5c1590f88787a1fc6a1c2e0d48c67af85dd4b7e8249ff573bee2daad`  
		Last Modified: Mon, 27 Dec 2021 18:08:55 GMT  
		Size: 5.7 MB (5705389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85af9afd2d869bd928b4990f6fd908f635c5421d1dc8083fc5fd377b8bbd90`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870f16daf77f715fb9dc96eccb5b8d4af6d8b166fa70454d7fab605bd39d022b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:60a73d5603e4031736039ecc463577365c1f717538d9abebaffc2f8772464669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41260220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b349656fc3b5caf98e066d0fdb6c40beca910e76b65314e5f1f5cfea9fc2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:16:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:17:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:18:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:18:28 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:18:31 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:18:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:18:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45821758d9ac9ef7ddf59278b25a098454da513ab2a4469079d31efd2872e496`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621a4339ab8321307888b642f6c34ede9ba4af6ac0ed96e946ac50ec1227849`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb85ea75c9e8b313cfbfc6e4cfef155d0183d2f926c786afe58fc17f96afdae`  
		Last Modified: Mon, 27 Dec 2021 18:20:03 GMT  
		Size: 6.0 MB (5997966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8831f840f6baaf8d56f6cae0b098c6a56d239108b4ae79ca3788881609e16`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e7af5ea63b6fcb7ce923b4e73eaf873a1247710e432fc8214fd19aad04405`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:6ca814db8831771b57c2fc6fec100a2a7172d558595020784313b259c022266e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34829005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f2f35891cf31904936c0d30cebe83dde721ab69f4d0b103091bc34e002fe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:27 GMT
ADD file:c8a482d41bf09dfb6484bf2a6e38535bf0594d26dd6eedd5abde4e3cc811fa6c in / 
# Tue, 21 Dec 2021 01:42:29 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 11:22:51 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 11:22:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 11:22:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 11:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 11:23:21 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 11:23:22 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 11:23:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 11:23:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 11:23:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:12562551722a758d23ceea9abcdc2bee737e38c8f62a0f3d3afb2cc2626c28b1`  
		Last Modified: Tue, 21 Dec 2021 01:48:15 GMT  
		Size: 29.6 MB (29641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ef12e9110fade1b5f49cd9bd409a215546e6a659caf0b7c782b63e68b435d`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc8f56cc872687f2f42c48ebccd7820d167ec5866466852bb6646f18e519803`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5ad9022f51f5dafe11dbde04206e78d75fffe06678398a3ed65c9cdf16e303`  
		Last Modified: Tue, 21 Dec 2021 11:24:01 GMT  
		Size: 5.2 MB (5184106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f5e0810a75c82e2c625f9723799e72c4c00697d471245d2df256a5490e7049`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfe444b90c33b185e97434acae972e7f8cdcb010a7fa9709cef3db394bc323`  
		Last Modified: Tue, 21 Dec 2021 11:24:01 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:7598f09fe725e5aa7eeece082ec6893c4cb4de06d4c32c1c04d8af9b32fcd6d1
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
$ docker pull spiped@sha256:5759c6e68d7e93789c7fc574722f42f3d3bafcaab2c4a8aeeeac5bb4772012a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3e3a8422cee08ac18b30d97939a3a6bd28e94a61d0caaaa96ff86dd8f425c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:30:36 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 13 Nov 2021 07:30:37 GMT
RUN apk add --no-cache libssl1.1
# Sat, 13 Nov 2021 07:30:37 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Nov 2021 07:31:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 13 Nov 2021 07:31:02 GMT
VOLUME [/spiped]
# Sat, 13 Nov 2021 07:31:03 GMT
WORKDIR /spiped
# Sat, 13 Nov 2021 07:31:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:31:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 07:31:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d272f2608cb29aaf56aaa58c4e8245793833d52257971c0a4a90c1445945548`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588bebf547583661fb31be182d777849262971941c241f7b072c041f54e3c4ff`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 7.8 KB (7767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f41a1ab4447065d651caf78075639eb1027290f0756c4d489a10c43a745af`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 213.1 KB (213113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d7a22ad75e07e938780270586c7d97ddd070bf6b70ee31e6fbe14b6c79cda6`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b484100590c35b883633e127830518528f9cc47bce7f4b864394b4bd85acb54`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b6482b55d0b7700b0393783f0ea8e49e6a4329c07187fdf826b6902d0ccfa3e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df9593d1c7a93c5f606ef97c05cc8d86e1a5bce25cd9895c104e2e1a7edbe19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 17:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 17:49:46 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 17:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:50:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 17:50:07 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:50:07 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:50:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:50:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f27a458746dfc1d07b0b03b9b8f205b08ebef9d6060ef92027b709fee313e`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fffa3b0ec9bb32d2efab9fa903af078baf37201f4ec2026c0afce9c14156229`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2344d51f830abe738f710343c04e056b2ec80e33a48522878caa568c9f553c`  
		Last Modified: Mon, 27 Dec 2021 17:50:42 GMT  
		Size: 1.4 MB (1439576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3eeeb2545dce6884a99d866ca20bd742d7e133aacf869b4cddbe974bfde627`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681e39729f29c202bc97138be5a28bb84d92220ffe45df47fb643301eef46aa`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ed9db1b4a0c65f0ca88573ca4e82bafaedde5032f465971dba93432ddcf67f67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04afce967f7cf45ad1faa0b6e1d955f2bad9d1aff37c3659db5e809170762140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:40:39 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 20:40:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 20:40:41 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 20:41:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 20:41:14 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 20:41:14 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 20:41:15 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:41:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 20:41:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abea20678ed9ffc78867f8fc9674162184169da3d7c198cd24ec6b7439e0c88`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f04cc4ba71752a6b9075421e6b0b7f08625406fb105f85e23547c4eb23b25f3`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 7.8 KB (7770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae957cbfbd7f9f36494cb3954e91d1ead35e68d61bbddf48904c4b6133c4c878`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 223.9 KB (223875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911b8888c5d7d41e887ed34d5f9c93d1d3241ad814e69f4d7def6b5debc96ae8`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d46a3df042754e1b8e655e102bf789f899a1f3758442759be66fe90573dbd2`  
		Last Modified: Fri, 12 Nov 2021 20:41:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:bdb5c0f748fb29dd4c96f71d1eec1c471f348b68e39063a5674e88c6655400ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4447359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ab0ba82f0f9badd5246249195a67d4e12bc4f6cfb1822b3454aca1c3dae586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:18:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:19:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:19:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:19:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:19:25 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:19:28 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:19:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:19:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef2b17ec4445a63d712289fc62b0e3e30ab15992e0a0d38ab25e290abcb38e`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210460e69fcfc508eae94f5666c4fc57c0cdf6163c3a6e39710f5da7a2e5ceb6`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 7.7 KB (7737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0860c3c69dcd2673558f15fc9c46c8447274ce23c207e936804fe5a268e5e7f`  
		Last Modified: Mon, 27 Dec 2021 18:20:22 GMT  
		Size: 1.6 MB (1623097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cd96844150db5d01e32349b5f650aafd01dd1789c2a11fee82b6f55bd43560`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b1de785dfc0bc3d07ee3d3f619d0681bc34b7eeee205db16da01946663a91`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:118a8c071df238ccc4affa6c1ad90ecaa58fd6f20861ee190449b34b1f5734bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a068554fae2e46941a18261fe2601c6c40df867a7b227b9bf154694451ba5390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:55:55 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 19:55:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 19:55:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 19:56:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 19:56:06 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 19:56:06 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 19:56:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 19:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 19:56:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc797db23a37010d6b83bb8a9eaa1336ed352043857e5a44d68a4b8efad9e0b5`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e810eed7330856c73daba855bc8adf50fdde87ccab6697c3416ee314886ca`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95a425358f95dbc88c89aac4c0c745bacaceb3d4598a051af18b0df4a28d76e`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 205.8 KB (205773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c7009eddad4f11d690d41e57f47828edf66b3f5113d35cf2a68eee8beed75`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5522513383757fa4cc180054c6b6b641c302050e0dce5ddfdd2a8881e7efcfa2`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:4827c3db0ce1c675a500d8272f10dffa716f6d1915ba8527a0115e4af08f5677
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
$ docker pull spiped@sha256:2bd2286a40c61a56f280444f68f9c3d0ae7a310858860aba77b0403b8890c9f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37321326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4914da9141203212b68712b5f3a3711294f5e0e02a612eec74bd1b2e1241b9b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 12:54:46 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 12:54:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 12:54:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 12:55:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 12:55:16 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 12:55:16 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 12:55:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 12:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 12:55:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5942a3089c9d199ffd7567fc18e1491777fdade26ec8bdf4d160bf3c8d83f324`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f2d189091c21b4eee0a6fe6553c7c7ad5a1fba49319eac9c272a96ac7fbdd`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f16287ae7ba5070d7edb0070fe71b973932136de80e4a4dd1013707e336b0c7`  
		Last Modified: Tue, 21 Dec 2021 12:55:41 GMT  
		Size: 6.0 MB (5960446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e68e4478591fe99bf722077de675519de67d719f9677d67f1ddc4d8f2cec294`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587fde5003f001f256acac00acf4ea7b0205ea8770d68ee6a9a2d3c87c369d95`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2bb8d6f9786620cb6d809309fe172b33c989c54afa2e70963dc028539cc711de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33930835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb20a687f8f10c7552075675e860628f3cabd9d85426df4168e2085074497125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:48:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:48:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:48:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:49:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:49:39 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:49:40 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:49:40 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:49:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a6f781a7abbf2236545af22e3b305148755b938eb4b3f80acfddda83fb330`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901947b41fdff91f97c93d69ea6510e742f77e91ebe42dfb3151adcdaf03441a`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f468550fb64a624779d011e733e2288492ceeefbf1195d64f8bd54e57f57e4f`  
		Last Modified: Mon, 27 Dec 2021 17:50:18 GMT  
		Size: 5.0 MB (5027325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa37e6545912e2b7148568d33bbf517e5deadd118df40ce2ebe5f74710c2d66`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0df784f0906422ce5e4c8eb5ee379506682e1ad31e783eeca4525c79ba55c`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5ff37adf5b2ffdb562129ff2c4c257c774150b80d954a9a0de388a5cd9c14ab4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31311461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa1788ed3cfcc665390b07c5ea81b3818793dc7e8cd3cff01c89fc109cb0be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:59:48 GMT
ADD file:6a5555c3e40db91fae5bb112464a4c405a976de17ff64c98f25d3033a6a608d8 in / 
# Tue, 21 Dec 2021 01:59:48 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:58:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:58:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:58:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:59:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:59:47 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:59:47 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:59:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:59:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d0061d6703dc4975804c3419e00c85efbe3f1b79c86d87e048fa14a683e88e31`  
		Last Modified: Tue, 21 Dec 2021 02:15:26 GMT  
		Size: 26.6 MB (26560815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d1aaaf5cba2bb5aa182cc038a59938629d1ad6ec388340be3e8f34e5e65b0`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6950d1ddd5e954a00fd9b56a607f737d4394ec2519f9c9d47ce2820e12bcfb`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6424dc46a62a8c5530fa74a2aaddc612ea6e099df67cfbe39b49dad4b2416fa4`  
		Last Modified: Mon, 27 Dec 2021 18:01:21 GMT  
		Size: 4.7 MB (4747390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b16a5e406437b655a5c55e8e9027607ad607deb3047cf60539ca94a8a6dd8be`  
		Last Modified: Mon, 27 Dec 2021 18:01:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c526844e52b7ac486211e17526f3bd96806de407bdad85bbace1e9268e01d2c`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:076eed23d69622023465551277b292c4b20c7e53ff970f4ec2c0c88c721002a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558381a048e4dd5c28f2a72bdfb28f021302afc0b9044d17373f8513e2c57b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 13:37:31 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 13:37:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 13:37:35 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 13:37:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 13:37:57 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 13:37:58 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 13:38:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 13:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 13:38:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11307cfb62981d1477c624d0946d440cae59b97d5241be5622b4a1a2170b7087`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b4f4a9f9d7183fa8a6390427dd6151121434bd32d1539e46a81b5b7195e9e`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498cf759f2f5ad49bf12c6c9162ea1c630f9fba1005c0a5cd96d9d40f3c3bc9c`  
		Last Modified: Tue, 21 Dec 2021 13:38:30 GMT  
		Size: 5.3 MB (5263680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7310cca9b3933670873fa963c55ba0370617e570124050a904a3eabfd50f0b8a`  
		Last Modified: Tue, 21 Dec 2021 13:38:29 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ebb7feec0bee35aea3ecb3f98485656fa38f1ef9c1c9faccf4d07b68e3ebbe`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:5b3875cce8fad4903a3c884cef05e5abad051bc9951e8e5410114e95e0dac53e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40258475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302f102ca38e8fbd96146e30bc1ab35ebeaf9330138e5b0b7d258e8c9cb0b61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 21:50:17 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 21:50:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 21:50:24 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 21:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 21:51:10 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 21:51:11 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 21:51:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 21:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 21:51:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489da5566cb0c924c029e46f8dad5bcafab6d42a56da88a93f2801d29558ff51`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db213f8397acea926fb592d3befbbdb2c002c268a3d54cb1d5c2d98de07b6f00`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a4ea8b87e71f3244324d2ead099212bccde6f64ef51cbe9d8ec4d43b36028`  
		Last Modified: Tue, 21 Dec 2021 21:52:08 GMT  
		Size: 7.9 MB (7884366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5619dad69ca0adbec11d01730713268fe39795d31498b6b4fe5494a59579236`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3945ddda45549df85f0eed7cab7fef6325fd37f1b4ef32546894d2af03acfd`  
		Last Modified: Tue, 21 Dec 2021 21:52:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:130c01d2a02859608af1ff69b512e606c6b0afab129f4f55f3b214e4439a961e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35327767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8059d8a507f312d8d77dc186576b8b33cbc65306a9ff8fd918ca17b2b9163198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:07:30 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:08:36 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:08:37 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:08:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:08:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc41050c10fb28c363303084d216e4a84358c365e0c0c3ea780e76094ac5b62`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccfed374e34e3e33bb1dac88ddd7d7bd1e7f5274368492e37c693a71768d15b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7546f5c1590f88787a1fc6a1c2e0d48c67af85dd4b7e8249ff573bee2daad`  
		Last Modified: Mon, 27 Dec 2021 18:08:55 GMT  
		Size: 5.7 MB (5705389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85af9afd2d869bd928b4990f6fd908f635c5421d1dc8083fc5fd377b8bbd90`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870f16daf77f715fb9dc96eccb5b8d4af6d8b166fa70454d7fab605bd39d022b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:60a73d5603e4031736039ecc463577365c1f717538d9abebaffc2f8772464669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41260220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b349656fc3b5caf98e066d0fdb6c40beca910e76b65314e5f1f5cfea9fc2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:16:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:17:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:18:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:18:28 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:18:31 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:18:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:18:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45821758d9ac9ef7ddf59278b25a098454da513ab2a4469079d31efd2872e496`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621a4339ab8321307888b642f6c34ede9ba4af6ac0ed96e946ac50ec1227849`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb85ea75c9e8b313cfbfc6e4cfef155d0183d2f926c786afe58fc17f96afdae`  
		Last Modified: Mon, 27 Dec 2021 18:20:03 GMT  
		Size: 6.0 MB (5997966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8831f840f6baaf8d56f6cae0b098c6a56d239108b4ae79ca3788881609e16`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e7af5ea63b6fcb7ce923b4e73eaf873a1247710e432fc8214fd19aad04405`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:6ca814db8831771b57c2fc6fec100a2a7172d558595020784313b259c022266e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34829005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f2f35891cf31904936c0d30cebe83dde721ab69f4d0b103091bc34e002fe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:27 GMT
ADD file:c8a482d41bf09dfb6484bf2a6e38535bf0594d26dd6eedd5abde4e3cc811fa6c in / 
# Tue, 21 Dec 2021 01:42:29 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 11:22:51 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 11:22:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 11:22:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 11:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 11:23:21 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 11:23:22 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 11:23:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 11:23:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 11:23:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:12562551722a758d23ceea9abcdc2bee737e38c8f62a0f3d3afb2cc2626c28b1`  
		Last Modified: Tue, 21 Dec 2021 01:48:15 GMT  
		Size: 29.6 MB (29641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ef12e9110fade1b5f49cd9bd409a215546e6a659caf0b7c782b63e68b435d`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc8f56cc872687f2f42c48ebccd7820d167ec5866466852bb6646f18e519803`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5ad9022f51f5dafe11dbde04206e78d75fffe06678398a3ed65c9cdf16e303`  
		Last Modified: Tue, 21 Dec 2021 11:24:01 GMT  
		Size: 5.2 MB (5184106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f5e0810a75c82e2c625f9723799e72c4c00697d471245d2df256a5490e7049`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfe444b90c33b185e97434acae972e7f8cdcb010a7fa9709cef3db394bc323`  
		Last Modified: Tue, 21 Dec 2021 11:24:01 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:7598f09fe725e5aa7eeece082ec6893c4cb4de06d4c32c1c04d8af9b32fcd6d1
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
$ docker pull spiped@sha256:5759c6e68d7e93789c7fc574722f42f3d3bafcaab2c4a8aeeeac5bb4772012a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3e3a8422cee08ac18b30d97939a3a6bd28e94a61d0caaaa96ff86dd8f425c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:30:36 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 13 Nov 2021 07:30:37 GMT
RUN apk add --no-cache libssl1.1
# Sat, 13 Nov 2021 07:30:37 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Nov 2021 07:31:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 13 Nov 2021 07:31:02 GMT
VOLUME [/spiped]
# Sat, 13 Nov 2021 07:31:03 GMT
WORKDIR /spiped
# Sat, 13 Nov 2021 07:31:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:31:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 07:31:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d272f2608cb29aaf56aaa58c4e8245793833d52257971c0a4a90c1445945548`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588bebf547583661fb31be182d777849262971941c241f7b072c041f54e3c4ff`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 7.8 KB (7767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f41a1ab4447065d651caf78075639eb1027290f0756c4d489a10c43a745af`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 213.1 KB (213113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d7a22ad75e07e938780270586c7d97ddd070bf6b70ee31e6fbe14b6c79cda6`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b484100590c35b883633e127830518528f9cc47bce7f4b864394b4bd85acb54`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b6482b55d0b7700b0393783f0ea8e49e6a4329c07187fdf826b6902d0ccfa3e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df9593d1c7a93c5f606ef97c05cc8d86e1a5bce25cd9895c104e2e1a7edbe19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 17:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 17:49:46 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 17:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:50:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 17:50:07 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:50:07 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:50:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:50:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f27a458746dfc1d07b0b03b9b8f205b08ebef9d6060ef92027b709fee313e`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fffa3b0ec9bb32d2efab9fa903af078baf37201f4ec2026c0afce9c14156229`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2344d51f830abe738f710343c04e056b2ec80e33a48522878caa568c9f553c`  
		Last Modified: Mon, 27 Dec 2021 17:50:42 GMT  
		Size: 1.4 MB (1439576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3eeeb2545dce6884a99d866ca20bd742d7e133aacf869b4cddbe974bfde627`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681e39729f29c202bc97138be5a28bb84d92220ffe45df47fb643301eef46aa`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ed9db1b4a0c65f0ca88573ca4e82bafaedde5032f465971dba93432ddcf67f67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04afce967f7cf45ad1faa0b6e1d955f2bad9d1aff37c3659db5e809170762140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:40:39 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 20:40:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 20:40:41 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 20:41:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 20:41:14 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 20:41:14 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 20:41:15 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:41:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 20:41:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abea20678ed9ffc78867f8fc9674162184169da3d7c198cd24ec6b7439e0c88`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f04cc4ba71752a6b9075421e6b0b7f08625406fb105f85e23547c4eb23b25f3`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 7.8 KB (7770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae957cbfbd7f9f36494cb3954e91d1ead35e68d61bbddf48904c4b6133c4c878`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 223.9 KB (223875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911b8888c5d7d41e887ed34d5f9c93d1d3241ad814e69f4d7def6b5debc96ae8`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d46a3df042754e1b8e655e102bf789f899a1f3758442759be66fe90573dbd2`  
		Last Modified: Fri, 12 Nov 2021 20:41:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:bdb5c0f748fb29dd4c96f71d1eec1c471f348b68e39063a5674e88c6655400ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4447359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ab0ba82f0f9badd5246249195a67d4e12bc4f6cfb1822b3454aca1c3dae586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:18:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:19:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:19:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:19:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:19:25 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:19:28 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:19:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:19:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef2b17ec4445a63d712289fc62b0e3e30ab15992e0a0d38ab25e290abcb38e`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210460e69fcfc508eae94f5666c4fc57c0cdf6163c3a6e39710f5da7a2e5ceb6`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 7.7 KB (7737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0860c3c69dcd2673558f15fc9c46c8447274ce23c207e936804fe5a268e5e7f`  
		Last Modified: Mon, 27 Dec 2021 18:20:22 GMT  
		Size: 1.6 MB (1623097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cd96844150db5d01e32349b5f650aafd01dd1789c2a11fee82b6f55bd43560`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b1de785dfc0bc3d07ee3d3f619d0681bc34b7eeee205db16da01946663a91`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:118a8c071df238ccc4affa6c1ad90ecaa58fd6f20861ee190449b34b1f5734bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a068554fae2e46941a18261fe2601c6c40df867a7b227b9bf154694451ba5390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:55:55 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 19:55:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 19:55:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 19:56:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 19:56:06 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 19:56:06 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 19:56:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 19:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 19:56:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc797db23a37010d6b83bb8a9eaa1336ed352043857e5a44d68a4b8efad9e0b5`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e810eed7330856c73daba855bc8adf50fdde87ccab6697c3416ee314886ca`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95a425358f95dbc88c89aac4c0c745bacaceb3d4598a051af18b0df4a28d76e`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 205.8 KB (205773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c7009eddad4f11d690d41e57f47828edf66b3f5113d35cf2a68eee8beed75`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5522513383757fa4cc180054c6b6b641c302050e0dce5ddfdd2a8881e7efcfa2`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:5a301df96744ed06a9f152151e423ea8634efae63f88968acc5642b149dbd186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; mips64le
	-	linux; ppc64le

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2bb8d6f9786620cb6d809309fe172b33c989c54afa2e70963dc028539cc711de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33930835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb20a687f8f10c7552075675e860628f3cabd9d85426df4168e2085074497125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:48:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:48:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:48:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:49:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:49:39 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:49:40 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:49:40 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:49:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a6f781a7abbf2236545af22e3b305148755b938eb4b3f80acfddda83fb330`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901947b41fdff91f97c93d69ea6510e742f77e91ebe42dfb3151adcdaf03441a`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f468550fb64a624779d011e733e2288492ceeefbf1195d64f8bd54e57f57e4f`  
		Last Modified: Mon, 27 Dec 2021 17:50:18 GMT  
		Size: 5.0 MB (5027325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa37e6545912e2b7148568d33bbf517e5deadd118df40ce2ebe5f74710c2d66`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0df784f0906422ce5e4c8eb5ee379506682e1ad31e783eeca4525c79ba55c`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5ff37adf5b2ffdb562129ff2c4c257c774150b80d954a9a0de388a5cd9c14ab4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31311461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa1788ed3cfcc665390b07c5ea81b3818793dc7e8cd3cff01c89fc109cb0be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:59:48 GMT
ADD file:6a5555c3e40db91fae5bb112464a4c405a976de17ff64c98f25d3033a6a608d8 in / 
# Tue, 21 Dec 2021 01:59:48 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:58:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:58:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:58:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:59:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:59:47 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:59:47 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:59:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:59:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d0061d6703dc4975804c3419e00c85efbe3f1b79c86d87e048fa14a683e88e31`  
		Last Modified: Tue, 21 Dec 2021 02:15:26 GMT  
		Size: 26.6 MB (26560815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d1aaaf5cba2bb5aa182cc038a59938629d1ad6ec388340be3e8f34e5e65b0`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6950d1ddd5e954a00fd9b56a607f737d4394ec2519f9c9d47ce2820e12bcfb`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6424dc46a62a8c5530fa74a2aaddc612ea6e099df67cfbe39b49dad4b2416fa4`  
		Last Modified: Mon, 27 Dec 2021 18:01:21 GMT  
		Size: 4.7 MB (4747390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b16a5e406437b655a5c55e8e9027607ad607deb3047cf60539ca94a8a6dd8be`  
		Last Modified: Mon, 27 Dec 2021 18:01:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c526844e52b7ac486211e17526f3bd96806de407bdad85bbace1e9268e01d2c`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:130c01d2a02859608af1ff69b512e606c6b0afab129f4f55f3b214e4439a961e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35327767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8059d8a507f312d8d77dc186576b8b33cbc65306a9ff8fd918ca17b2b9163198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:07:30 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:08:36 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:08:37 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:08:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:08:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc41050c10fb28c363303084d216e4a84358c365e0c0c3ea780e76094ac5b62`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccfed374e34e3e33bb1dac88ddd7d7bd1e7f5274368492e37c693a71768d15b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7546f5c1590f88787a1fc6a1c2e0d48c67af85dd4b7e8249ff573bee2daad`  
		Last Modified: Mon, 27 Dec 2021 18:08:55 GMT  
		Size: 5.7 MB (5705389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85af9afd2d869bd928b4990f6fd908f635c5421d1dc8083fc5fd377b8bbd90`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870f16daf77f715fb9dc96eccb5b8d4af6d8b166fa70454d7fab605bd39d022b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:60a73d5603e4031736039ecc463577365c1f717538d9abebaffc2f8772464669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41260220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b349656fc3b5caf98e066d0fdb6c40beca910e76b65314e5f1f5cfea9fc2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:16:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:17:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:18:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:18:28 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:18:31 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:18:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:18:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45821758d9ac9ef7ddf59278b25a098454da513ab2a4469079d31efd2872e496`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621a4339ab8321307888b642f6c34ede9ba4af6ac0ed96e946ac50ec1227849`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb85ea75c9e8b313cfbfc6e4cfef155d0183d2f926c786afe58fc17f96afdae`  
		Last Modified: Mon, 27 Dec 2021 18:20:03 GMT  
		Size: 6.0 MB (5997966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8831f840f6baaf8d56f6cae0b098c6a56d239108b4ae79ca3788881609e16`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e7af5ea63b6fcb7ce923b4e73eaf873a1247710e432fc8214fd19aad04405`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:2037df8259df258e0ba3059928d171506540783b15b51d880aae1c1c85ebe995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; ppc64le

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b6482b55d0b7700b0393783f0ea8e49e6a4329c07187fdf826b6902d0ccfa3e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df9593d1c7a93c5f606ef97c05cc8d86e1a5bce25cd9895c104e2e1a7edbe19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 17:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 17:49:46 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 17:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:50:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 17:50:07 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:50:07 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:50:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:50:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f27a458746dfc1d07b0b03b9b8f205b08ebef9d6060ef92027b709fee313e`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fffa3b0ec9bb32d2efab9fa903af078baf37201f4ec2026c0afce9c14156229`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2344d51f830abe738f710343c04e056b2ec80e33a48522878caa568c9f553c`  
		Last Modified: Mon, 27 Dec 2021 17:50:42 GMT  
		Size: 1.4 MB (1439576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3eeeb2545dce6884a99d866ca20bd742d7e133aacf869b4cddbe974bfde627`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681e39729f29c202bc97138be5a28bb84d92220ffe45df47fb643301eef46aa`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:bdb5c0f748fb29dd4c96f71d1eec1c471f348b68e39063a5674e88c6655400ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4447359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ab0ba82f0f9badd5246249195a67d4e12bc4f6cfb1822b3454aca1c3dae586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:18:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:19:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:19:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:19:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:19:25 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:19:28 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:19:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:19:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef2b17ec4445a63d712289fc62b0e3e30ab15992e0a0d38ab25e290abcb38e`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210460e69fcfc508eae94f5666c4fc57c0cdf6163c3a6e39710f5da7a2e5ceb6`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 7.7 KB (7737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0860c3c69dcd2673558f15fc9c46c8447274ce23c207e936804fe5a268e5e7f`  
		Last Modified: Mon, 27 Dec 2021 18:20:22 GMT  
		Size: 1.6 MB (1623097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cd96844150db5d01e32349b5f650aafd01dd1789c2a11fee82b6f55bd43560`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b1de785dfc0bc3d07ee3d3f619d0681bc34b7eeee205db16da01946663a91`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:7598f09fe725e5aa7eeece082ec6893c4cb4de06d4c32c1c04d8af9b32fcd6d1
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
$ docker pull spiped@sha256:5759c6e68d7e93789c7fc574722f42f3d3bafcaab2c4a8aeeeac5bb4772012a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3e3a8422cee08ac18b30d97939a3a6bd28e94a61d0caaaa96ff86dd8f425c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:30:36 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 13 Nov 2021 07:30:37 GMT
RUN apk add --no-cache libssl1.1
# Sat, 13 Nov 2021 07:30:37 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Nov 2021 07:31:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 13 Nov 2021 07:31:02 GMT
VOLUME [/spiped]
# Sat, 13 Nov 2021 07:31:03 GMT
WORKDIR /spiped
# Sat, 13 Nov 2021 07:31:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:31:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 07:31:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d272f2608cb29aaf56aaa58c4e8245793833d52257971c0a4a90c1445945548`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588bebf547583661fb31be182d777849262971941c241f7b072c041f54e3c4ff`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 7.8 KB (7767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f41a1ab4447065d651caf78075639eb1027290f0756c4d489a10c43a745af`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 213.1 KB (213113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d7a22ad75e07e938780270586c7d97ddd070bf6b70ee31e6fbe14b6c79cda6`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b484100590c35b883633e127830518528f9cc47bce7f4b864394b4bd85acb54`  
		Last Modified: Sat, 13 Nov 2021 07:31:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b6482b55d0b7700b0393783f0ea8e49e6a4329c07187fdf826b6902d0ccfa3e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df9593d1c7a93c5f606ef97c05cc8d86e1a5bce25cd9895c104e2e1a7edbe19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 17:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 17:49:46 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 17:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:50:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 17:50:07 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:50:07 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:50:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:50:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f27a458746dfc1d07b0b03b9b8f205b08ebef9d6060ef92027b709fee313e`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fffa3b0ec9bb32d2efab9fa903af078baf37201f4ec2026c0afce9c14156229`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2344d51f830abe738f710343c04e056b2ec80e33a48522878caa568c9f553c`  
		Last Modified: Mon, 27 Dec 2021 17:50:42 GMT  
		Size: 1.4 MB (1439576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3eeeb2545dce6884a99d866ca20bd742d7e133aacf869b4cddbe974bfde627`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681e39729f29c202bc97138be5a28bb84d92220ffe45df47fb643301eef46aa`  
		Last Modified: Mon, 27 Dec 2021 17:50:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:ed9db1b4a0c65f0ca88573ca4e82bafaedde5032f465971dba93432ddcf67f67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04afce967f7cf45ad1faa0b6e1d955f2bad9d1aff37c3659db5e809170762140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:40:39 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 20:40:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 20:40:41 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 20:41:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 20:41:14 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 20:41:14 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 20:41:15 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:41:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 20:41:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abea20678ed9ffc78867f8fc9674162184169da3d7c198cd24ec6b7439e0c88`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f04cc4ba71752a6b9075421e6b0b7f08625406fb105f85e23547c4eb23b25f3`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 7.8 KB (7770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae957cbfbd7f9f36494cb3954e91d1ead35e68d61bbddf48904c4b6133c4c878`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 223.9 KB (223875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911b8888c5d7d41e887ed34d5f9c93d1d3241ad814e69f4d7def6b5debc96ae8`  
		Last Modified: Fri, 12 Nov 2021 20:41:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d46a3df042754e1b8e655e102bf789f899a1f3758442759be66fe90573dbd2`  
		Last Modified: Fri, 12 Nov 2021 20:41:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:bdb5c0f748fb29dd4c96f71d1eec1c471f348b68e39063a5674e88c6655400ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4447359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ab0ba82f0f9badd5246249195a67d4e12bc4f6cfb1822b3454aca1c3dae586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:18:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:19:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:19:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:19:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:19:25 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:19:28 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:19:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:19:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef2b17ec4445a63d712289fc62b0e3e30ab15992e0a0d38ab25e290abcb38e`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210460e69fcfc508eae94f5666c4fc57c0cdf6163c3a6e39710f5da7a2e5ceb6`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 7.7 KB (7737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0860c3c69dcd2673558f15fc9c46c8447274ce23c207e936804fe5a268e5e7f`  
		Last Modified: Mon, 27 Dec 2021 18:20:22 GMT  
		Size: 1.6 MB (1623097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cd96844150db5d01e32349b5f650aafd01dd1789c2a11fee82b6f55bd43560`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b1de785dfc0bc3d07ee3d3f619d0681bc34b7eeee205db16da01946663a91`  
		Last Modified: Mon, 27 Dec 2021 18:20:21 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:118a8c071df238ccc4affa6c1ad90ecaa58fd6f20861ee190449b34b1f5734bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a068554fae2e46941a18261fe2601c6c40df867a7b227b9bf154694451ba5390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:55:55 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 19:55:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 19:55:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 19:56:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 19:56:06 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 19:56:06 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 19:56:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 19:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 19:56:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc797db23a37010d6b83bb8a9eaa1336ed352043857e5a44d68a4b8efad9e0b5`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e810eed7330856c73daba855bc8adf50fdde87ccab6697c3416ee314886ca`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95a425358f95dbc88c89aac4c0c745bacaceb3d4598a051af18b0df4a28d76e`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 205.8 KB (205773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c7009eddad4f11d690d41e57f47828edf66b3f5113d35cf2a68eee8beed75`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5522513383757fa4cc180054c6b6b641c302050e0dce5ddfdd2a8881e7efcfa2`  
		Last Modified: Fri, 12 Nov 2021 19:56:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:4827c3db0ce1c675a500d8272f10dffa716f6d1915ba8527a0115e4af08f5677
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
$ docker pull spiped@sha256:2bd2286a40c61a56f280444f68f9c3d0ae7a310858860aba77b0403b8890c9f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37321326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4914da9141203212b68712b5f3a3711294f5e0e02a612eec74bd1b2e1241b9b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 12:54:46 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 12:54:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 12:54:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 12:55:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 12:55:16 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 12:55:16 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 12:55:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 12:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 12:55:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5942a3089c9d199ffd7567fc18e1491777fdade26ec8bdf4d160bf3c8d83f324`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f2d189091c21b4eee0a6fe6553c7c7ad5a1fba49319eac9c272a96ac7fbdd`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f16287ae7ba5070d7edb0070fe71b973932136de80e4a4dd1013707e336b0c7`  
		Last Modified: Tue, 21 Dec 2021 12:55:41 GMT  
		Size: 6.0 MB (5960446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e68e4478591fe99bf722077de675519de67d719f9677d67f1ddc4d8f2cec294`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587fde5003f001f256acac00acf4ea7b0205ea8770d68ee6a9a2d3c87c369d95`  
		Last Modified: Tue, 21 Dec 2021 12:55:39 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2bb8d6f9786620cb6d809309fe172b33c989c54afa2e70963dc028539cc711de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33930835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb20a687f8f10c7552075675e860628f3cabd9d85426df4168e2085074497125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:48:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:48:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:48:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:49:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:49:39 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:49:40 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:49:40 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:49:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a6f781a7abbf2236545af22e3b305148755b938eb4b3f80acfddda83fb330`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901947b41fdff91f97c93d69ea6510e742f77e91ebe42dfb3151adcdaf03441a`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f468550fb64a624779d011e733e2288492ceeefbf1195d64f8bd54e57f57e4f`  
		Last Modified: Mon, 27 Dec 2021 17:50:18 GMT  
		Size: 5.0 MB (5027325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa37e6545912e2b7148568d33bbf517e5deadd118df40ce2ebe5f74710c2d66`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0df784f0906422ce5e4c8eb5ee379506682e1ad31e783eeca4525c79ba55c`  
		Last Modified: Mon, 27 Dec 2021 17:50:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5ff37adf5b2ffdb562129ff2c4c257c774150b80d954a9a0de388a5cd9c14ab4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31311461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa1788ed3cfcc665390b07c5ea81b3818793dc7e8cd3cff01c89fc109cb0be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:59:48 GMT
ADD file:6a5555c3e40db91fae5bb112464a4c405a976de17ff64c98f25d3033a6a608d8 in / 
# Tue, 21 Dec 2021 01:59:48 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 17:58:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 17:58:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 17:58:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 17:59:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 17:59:47 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 17:59:47 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 17:59:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 17:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 17:59:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d0061d6703dc4975804c3419e00c85efbe3f1b79c86d87e048fa14a683e88e31`  
		Last Modified: Tue, 21 Dec 2021 02:15:26 GMT  
		Size: 26.6 MB (26560815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d1aaaf5cba2bb5aa182cc038a59938629d1ad6ec388340be3e8f34e5e65b0`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6950d1ddd5e954a00fd9b56a607f737d4394ec2519f9c9d47ce2820e12bcfb`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6424dc46a62a8c5530fa74a2aaddc612ea6e099df67cfbe39b49dad4b2416fa4`  
		Last Modified: Mon, 27 Dec 2021 18:01:21 GMT  
		Size: 4.7 MB (4747390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b16a5e406437b655a5c55e8e9027607ad607deb3047cf60539ca94a8a6dd8be`  
		Last Modified: Mon, 27 Dec 2021 18:01:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c526844e52b7ac486211e17526f3bd96806de407bdad85bbace1e9268e01d2c`  
		Last Modified: Mon, 27 Dec 2021 18:01:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:076eed23d69622023465551277b292c4b20c7e53ff970f4ec2c0c88c721002a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558381a048e4dd5c28f2a72bdfb28f021302afc0b9044d17373f8513e2c57b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 13:37:31 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 13:37:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 13:37:35 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 13:37:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 13:37:57 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 13:37:58 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 13:38:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 13:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 13:38:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11307cfb62981d1477c624d0946d440cae59b97d5241be5622b4a1a2170b7087`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b4f4a9f9d7183fa8a6390427dd6151121434bd32d1539e46a81b5b7195e9e`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498cf759f2f5ad49bf12c6c9162ea1c630f9fba1005c0a5cd96d9d40f3c3bc9c`  
		Last Modified: Tue, 21 Dec 2021 13:38:30 GMT  
		Size: 5.3 MB (5263680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7310cca9b3933670873fa963c55ba0370617e570124050a904a3eabfd50f0b8a`  
		Last Modified: Tue, 21 Dec 2021 13:38:29 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ebb7feec0bee35aea3ecb3f98485656fa38f1ef9c1c9faccf4d07b68e3ebbe`  
		Last Modified: Tue, 21 Dec 2021 13:38:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:5b3875cce8fad4903a3c884cef05e5abad051bc9951e8e5410114e95e0dac53e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40258475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302f102ca38e8fbd96146e30bc1ab35ebeaf9330138e5b0b7d258e8c9cb0b61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 21:50:17 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 21:50:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 21:50:24 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 21:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 21:51:10 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 21:51:11 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 21:51:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 21:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 21:51:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489da5566cb0c924c029e46f8dad5bcafab6d42a56da88a93f2801d29558ff51`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db213f8397acea926fb592d3befbbdb2c002c268a3d54cb1d5c2d98de07b6f00`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a4ea8b87e71f3244324d2ead099212bccde6f64ef51cbe9d8ec4d43b36028`  
		Last Modified: Tue, 21 Dec 2021 21:52:08 GMT  
		Size: 7.9 MB (7884366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5619dad69ca0adbec11d01730713268fe39795d31498b6b4fe5494a59579236`  
		Last Modified: Tue, 21 Dec 2021 21:52:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3945ddda45549df85f0eed7cab7fef6325fd37f1b4ef32546894d2af03acfd`  
		Last Modified: Tue, 21 Dec 2021 21:52:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:130c01d2a02859608af1ff69b512e606c6b0afab129f4f55f3b214e4439a961e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35327767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8059d8a507f312d8d77dc186576b8b33cbc65306a9ff8fd918ca17b2b9163198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:07:30 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:08:36 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:08:37 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:08:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:08:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc41050c10fb28c363303084d216e4a84358c365e0c0c3ea780e76094ac5b62`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccfed374e34e3e33bb1dac88ddd7d7bd1e7f5274368492e37c693a71768d15b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7546f5c1590f88787a1fc6a1c2e0d48c67af85dd4b7e8249ff573bee2daad`  
		Last Modified: Mon, 27 Dec 2021 18:08:55 GMT  
		Size: 5.7 MB (5705389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85af9afd2d869bd928b4990f6fd908f635c5421d1dc8083fc5fd377b8bbd90`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870f16daf77f715fb9dc96eccb5b8d4af6d8b166fa70454d7fab605bd39d022b`  
		Last Modified: Mon, 27 Dec 2021 18:08:50 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:60a73d5603e4031736039ecc463577365c1f717538d9abebaffc2f8772464669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41260220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b349656fc3b5caf98e066d0fdb6c40beca910e76b65314e5f1f5cfea9fc2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Mon, 27 Dec 2021 18:16:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Mon, 27 Dec 2021 18:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Mon, 27 Dec 2021 18:17:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:18:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Mon, 27 Dec 2021 18:18:28 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:18:31 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:18:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:18:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45821758d9ac9ef7ddf59278b25a098454da513ab2a4469079d31efd2872e496`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621a4339ab8321307888b642f6c34ede9ba4af6ac0ed96e946ac50ec1227849`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb85ea75c9e8b313cfbfc6e4cfef155d0183d2f926c786afe58fc17f96afdae`  
		Last Modified: Mon, 27 Dec 2021 18:20:03 GMT  
		Size: 6.0 MB (5997966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8831f840f6baaf8d56f6cae0b098c6a56d239108b4ae79ca3788881609e16`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e7af5ea63b6fcb7ce923b4e73eaf873a1247710e432fc8214fd19aad04405`  
		Last Modified: Mon, 27 Dec 2021 18:20:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:6ca814db8831771b57c2fc6fec100a2a7172d558595020784313b259c022266e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34829005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f2f35891cf31904936c0d30cebe83dde721ab69f4d0b103091bc34e002fe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:27 GMT
ADD file:c8a482d41bf09dfb6484bf2a6e38535bf0594d26dd6eedd5abde4e3cc811fa6c in / 
# Tue, 21 Dec 2021 01:42:29 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 11:22:51 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 21 Dec 2021 11:22:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 11:22:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 21 Dec 2021 11:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 11:23:21 GMT
VOLUME [/spiped]
# Tue, 21 Dec 2021 11:23:22 GMT
WORKDIR /spiped
# Tue, 21 Dec 2021 11:23:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 21 Dec 2021 11:23:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 11:23:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:12562551722a758d23ceea9abcdc2bee737e38c8f62a0f3d3afb2cc2626c28b1`  
		Last Modified: Tue, 21 Dec 2021 01:48:15 GMT  
		Size: 29.6 MB (29641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ef12e9110fade1b5f49cd9bd409a215546e6a659caf0b7c782b63e68b435d`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc8f56cc872687f2f42c48ebccd7820d167ec5866466852bb6646f18e519803`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5ad9022f51f5dafe11dbde04206e78d75fffe06678398a3ed65c9cdf16e303`  
		Last Modified: Tue, 21 Dec 2021 11:24:01 GMT  
		Size: 5.2 MB (5184106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f5e0810a75c82e2c625f9723799e72c4c00697d471245d2df256a5490e7049`  
		Last Modified: Tue, 21 Dec 2021 11:24:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfe444b90c33b185e97434acae972e7f8cdcb010a7fa9709cef3db394bc323`  
		Last Modified: Tue, 21 Dec 2021 11:24:01 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
