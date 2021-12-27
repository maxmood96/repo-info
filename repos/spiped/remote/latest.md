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
