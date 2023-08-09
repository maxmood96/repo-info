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
$ docker pull spiped@sha256:56b14b78a9337d99d4ae782cf7eb963ffb624a3bfd1f190d3648e95f819ff63a
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
$ docker pull spiped@sha256:024914f355d7df64887dde657bbcff7a61d2d4ccff5d43f4d3c3567092c3febd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38182082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7aa4b5d7b93c36ffc255e368fb924352cc5cdfd7eb91236c16fcf4f4309725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:36:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 14:36:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:36:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 14:37:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 14:37:18 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 14:37:18 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 14:37:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 14:37:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:37:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412f31823c3607ee7cf0f7ea2f70c0dc3f6eb610159a5582d2709f811e1168e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc70ab580442c24348a92d6781d1838c5d4811b03f958c534e18f34badb2d13`  
		Last Modified: Fri, 28 Jul 2023 14:37:32 GMT  
		Size: 2.6 MB (2586440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcc43564849e7d5dd99f86722dd00f61728bce2693f6bb0c1617942f0ec3f5a`  
		Last Modified: Fri, 28 Jul 2023 14:37:33 GMT  
		Size: 6.5 MB (6469507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea13792cc71ce8c887d6fe133b488092fafe74a36d98c02f75772fed5c47afee`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac29c4f562adf69c6ed89ee22148edd123f7eb4ab4e23444a343ed4c3c8836e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5bcd09c77588a67caae49433d4c86c6f91c69bae205ad672619afc5d749b5aba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34305753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756c18f247bb62bc63d31e0a50b9c68a64cd1a3347826060fc7e1eb4ed5b5785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:29 GMT
ADD file:53cf36eb7b72a7e970f4b18af1589402b2900f12e30820cdeccc8bb0c166df80 in / 
# Thu, 27 Jul 2023 23:48:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:18:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 06:18:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:18:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 06:18:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 06:18:32 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 06:18:32 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 06:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 06:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 06:18:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bd6dfc5281e13a0ca9fb8d9238ac9f14a0de04489913030c8e33b9398b4a4af`  
		Last Modified: Thu, 27 Jul 2023 23:51:28 GMT  
		Size: 27.0 MB (26983508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7867b868ea0c086b3cc19dffa7c4079dcd6909627f2495585866ef6686512`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eab6f4031dd2cbeb97b96eef0ca6ddeba7937c5a9fcb18252ba28e5f4c781b`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 2.2 MB (2184071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a21b08acfc2c6384677556aa01a3474ac7b9a055627d511785767566f9b7199`  
		Last Modified: Fri, 28 Jul 2023 06:18:48 GMT  
		Size: 5.1 MB (5136574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc10c0d99355974881d1e65b5a900d628c5d5beac6aeaa79ed789dd684a4e9`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b0514ba063b176ab332ff323fe4db1c5853e0bef483a0f7c0a0201fb4a6b2`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ed1463617a6ec4787fcfc89a0a312ac4af942cb5eb9ae05242f2bc91528b934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31728068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d79e97fafa93125c458792ea4e4ff699e48b2ea7c1a9e11ee8c4a15035e9e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:46 GMT
ADD file:b23161e9856801127e0136a920bcf075410ac23de605c82ca91d285b9f35941c in / 
# Thu, 27 Jul 2023 23:57:47 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 19:06:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 19:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 19:06:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 19:06:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 19:06:31 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 19:06:31 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 19:06:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 19:06:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 19:06:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb5b735234291ca6f672f489206ea5b6354d358f7d75a05036bdf84a6858d9f9`  
		Last Modified: Fri, 28 Jul 2023 00:03:11 GMT  
		Size: 24.8 MB (24805329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d222898f46d95805a7326b6800d1edeee028a45347a57164c34b37ae06c916ba`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782d770de44ba4a001c52e1933a14c4686dc69da2466959e091cb22b267309e`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 2.0 MB (2043254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6845efb4f08681fcd1ede0dcd46a25e88a6d18ffbfb220b7d87e608ccaa8283e`  
		Last Modified: Fri, 28 Jul 2023 19:06:48 GMT  
		Size: 4.9 MB (4877885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b4fe27ccb17150a9da129395b58336fa81ccea0fd84be8939f430df02eed7c`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7714096bd95fe9880e2181c0f6ea219e61883238224df612c68f2e5c9c0eec`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d88ac9d16fa209562e1a5179a8f008564588f851a68aee3ec5a597bb542d7df2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37067376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa29c1d765fbe597c57928bb35b8f9aa041e162896456d044076dae18b92d5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:19:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 01:19:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:19:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 01:20:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:20:03 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 01:20:03 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 01:20:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:20:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060019e05b5b6d10ebdcdfff5a1a17f7ea00e0c44edfa1a5d072061224979a8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c02a5e6dc6cb81fd967dcdd4813036b6e464930632ce048376eead8ee42a31d`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 2.4 MB (2429832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c0fde9cbba82047d390c8e027e769c909fd6ab0fda3c2275ed45f504faeb79`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 5.5 MB (5478716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a1efc6ee647d9b6aabdca7ed186fadc36667099750b3e749529f10bd02dd7c`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344e88b061ad36bcf2280ada625717ab2f97a1a36c5221c4987a23ca75fdec8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:1216033a6e3898df4dd046c41f47edd73e1ff860ad33686522b764b2fa8adea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1ff9f0b632345760ef1d669ec428f4f625912ebde09ad811a3ef25abee9f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 08:51:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 08:51:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 08:51:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 08:52:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 08:52:11 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 08:52:11 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 08:52:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 08:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 08:52:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5564c2bb87752c3c5b8455b4bd96d46493f6581cc3196a8cc8b8ea6bfeb3256d`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1900018d5bd91e250d0d6c226754b197866471c946aee6f8b71d49d58e937e2`  
		Last Modified: Fri, 28 Jul 2023 08:52:24 GMT  
		Size: 2.6 MB (2583603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb81d86a6894ea4e17723fa3b13fa8eea27aa34705b04b5f96a042615a07910`  
		Last Modified: Fri, 28 Jul 2023 08:52:25 GMT  
		Size: 5.9 MB (5940136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a12139c2df309d503138107a1dbe05ba8ce8182765eeb1da8c3d31775b6eb4f`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5b2d4b8b2a52e1a7eee9ece86c2c20678b566c98bc6d7cd965304487f8fa3`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:49a899236dbde8ea8d2213bd436cf4c527455e3f1e3c26e40c4f159e25c2a79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36756450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e63cf365261cf8e3b4451fe65ba8ae3798771cb198caca7960f5dc7920ca11a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:23 GMT
ADD file:90cbcf9a2aaf48a433b00118dd0821eeb291092da7b7f67ce6a525ce2cba1e3f in / 
# Thu, 27 Jul 2023 23:11:27 GMT
CMD ["bash"]
# Sat, 29 Jul 2023 02:27:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 29 Jul 2023 02:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 02:28:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 29 Jul 2023 02:30:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 29 Jul 2023 02:30:06 GMT
VOLUME [/spiped]
# Sat, 29 Jul 2023 02:30:09 GMT
WORKDIR /spiped
# Sat, 29 Jul 2023 02:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 29 Jul 2023 02:30:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jul 2023 02:30:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3252778e08fa8eb67ab052ad63281284b5ef1afdc40a36021228133487ab5d52`  
		Last Modified: Thu, 27 Jul 2023 23:22:26 GMT  
		Size: 29.1 MB (29121405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f33521a849a8bfb41d141a0ac9948095b8234c24ee434bdb5417b0e517eb7`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72f40d8259783265cafe9e800687826fc9f2dcb9ba5f5aaf1b5dd369a780f53`  
		Last Modified: Sat, 29 Jul 2023 02:30:44 GMT  
		Size: 1.8 MB (1831677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679711062d9a9f57e3af4f49a9bee04b0d0d8fa97e87b904115c9b612df7e7d`  
		Last Modified: Sat, 29 Jul 2023 02:30:47 GMT  
		Size: 5.8 MB (5801849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cae99e313273de740a8d561c3a00eadb3b3f6196b5c2114f9932159d4af207`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e972a6889d3ea08969c5cd356feade5bf9a9cd8453869165c924ad6cf766047a`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:cda509b294751f959f7764d1e1af011f4ce61c61e34eefbd25203a9ca0b28aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42306118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc441e69e8db9c2db390a467a61c87ec2e35d7a2a63c359e0e788615281064e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:01 GMT
ADD file:774a99e5c40757d27c981eb5ad6e03eb72970bb0c54f799eab1442624238ea3e in / 
# Thu, 27 Jul 2023 23:23:03 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 15:42:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 15:43:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:43:02 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 15:44:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 15:44:05 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 15:44:05 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 15:44:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 15:44:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 15:44:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad974e0ada84177d519dec70d0d7d9ff6a4f468bc7306425feb8429bc276bd8a`  
		Last Modified: Thu, 27 Jul 2023 23:29:24 GMT  
		Size: 33.1 MB (33119211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0834a39a8f321e61913bcebc5b10f2f4388ad008aed3aa0b7108c1c98aa672b8`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8637b8770fbcc45d233bc8c0685a004f863248524d9589bb8133462ad2ef98`  
		Last Modified: Fri, 28 Jul 2023 15:44:25 GMT  
		Size: 2.8 MB (2764991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e47b32eeb162a453e0f56b17945b85e59188dea37e5050beeb9fe549df43b6`  
		Last Modified: Fri, 28 Jul 2023 15:44:26 GMT  
		Size: 6.4 MB (6420314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ad0fc910585043bd75c1f9f637776962532c3318497e750adf297becfa27a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513cc6e981f0bcc9b41c0abcbebb0c975a964bdfc186524bcefd2f32b1496a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:9801f1b6d304727b25886ba0032e711317558ed43cc79dc97ef18474a21be5f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35132404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39476c9ecacb96484f9f9c5e593e97a9b1cba7f0ff99edcceac18924d9147c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:11 GMT
ADD file:0a5e1e86b375d60637d0829f77a12085777cf2ca07495b0f6249d8efea84e958 in / 
# Thu, 27 Jul 2023 23:47:13 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 12:21:25 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 12:21:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 12:21:29 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 12:21:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 12:21:42 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 12:21:42 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 12:21:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 12:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 12:21:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4301d25bb1bea85fcc5b364aec84ff58274f714cea191ab22d9b1b1e4f78527`  
		Last Modified: Thu, 27 Jul 2023 23:52:17 GMT  
		Size: 27.5 MB (27489697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef348951d7c2528189aaf990c50c94d47926bae33acaefdec1fc4dc9bdb677`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51341c3a783b2da9ec9d887eef33aebd6fecf5ec697f91fc4a64e0d7984678ba`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 2.3 MB (2257974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108045faf0e5fe4811d2bf60828dc7765761f5e5efc5bab62d8657cf552f885`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 5.4 MB (5383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209582ae96311472b03295510ead4f5bbad00cedca11bcab880a2e5f3684bd7`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901f1b400960248f49695ddd7e61dfc22b5aede3913f7604ce5e9cca49a75182`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:38016b388e6e908798c978ddd9fc91eb325925932ae89973fd9cceecbeaeeee3
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
$ docker pull spiped@sha256:d50ba6a73229914485b07e034308874110b29ff4248bbcd662f55717c0fa55ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ec3311c4035c9336c868279b0d420cc09b44cb5b9d93a813ed0c85d27304f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:20:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:20:54 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:21:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:21:05 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:21:05 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:21:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:21:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68caf666f4bb5f440531a0253294f702094d48f8694afeb159c3bee3a955928f`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56cc31d2500b156ae258f8cc835c039611b28a7fc664f9b5bec635f26a165f1`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.4 MB (1433005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0f60cfc992e735eab6827e81ef8ab9410faa8bb5a3aa95bcccd8324b6982b9`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 2.7 MB (2675293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfca5f8c6c25a4d506776dd84d3a716ba26161c5b53d23200c2131ad7abf8c5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5512defaf613253867bb293bce40f0f1572c7b5909bc313ff20891f7fdf3e5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:92c72514aab4032a46bd337535d95862b853d6c7e90cb1e86e689409cc93616f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4589191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b3dd418f5fe3e7be9bbb2632a3fd0fbbedad7f67e01d907d0d41c06bb6ce98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:36:09 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:36:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:36:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:36:17 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:36:17 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:36:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ffd38f9a9109fd6f2d98e59fac671a21acbcbd826d953a190916b8e28c4d7c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe31ddd32f93d6462563149d47e652289246cae76c3d69e2ae22c7f2dc157`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.2 MB (1236777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711c8b1ac9af3a0357e5e2ae10175a62c27bdea58e2e79fb7d413e2fa3a10138`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2f76630a196bedcec1d4f1f0542336e3189757e62aa7c83bd7f7e8f58680c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f674889b446c00cdd7da82689ee81ea78c84e02c462ad671bf3f9afd926afb1`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6b4ce7a3a962f7016da46f810228189be1cd6de1de0409f784505adca9fee42d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4264646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8b18499e87820bcff1593b1ccee12dbf54a9a32e6f7412af5d5c00268ce73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:51:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 21:51:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 21:51:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 21:51:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 21:51:52 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 21:51:52 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 21:51:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:51:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:51:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd254e37c3835d8a90d159f62497146fa2c0a51539455baafa4b5f3ad94073a`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b87a0e27917b2f49aabe18b41a38f10f52561eaed9cd75ecbf9bb54dd5ad657`  
		Last Modified: Tue, 08 Aug 2023 21:52:10 GMT  
		Size: 1.2 MB (1163899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a3f71f875284eede5e8bb82a4d0706d42594a0fec380b98dd516f0f75ed88`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 199.5 KB (199532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0eec6ac7d1270176b9ec72709b3186f9c9af79d5c747bdd03ac4818437e4b9`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da618866e96da51da8e7f96815a2d1e87198583082d2e819eaea328e7698149`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e44e0d5e538f2c9b96c690fff1ddb28d4803c23999f1d454965db93bbd687b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7264425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91392764bb6d58165d856113b83126cace6414f5457df110974537188a7da7be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:03:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:03:38 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:03:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:03:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:03:46 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:03:46 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:03:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:03:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29059dc293c00f54da752a558300b577b0437eae0d9b5f256f9a658105ca21ee`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351829a8bd360584cadfe089bec88f0a556d95f7cd39439affae43ea13c8a4b8`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.4 MB (1362700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f438d5a167cd51de9296e034ad6a94ce4848c706dfb163b6d19c35c1c3432`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 2.6 MB (2570731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3702fb444a3ca3cc36e82826eec5dbdc01917e9ff3532bcf06e5f3f4f00e9745`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e20649f92b6732530e48c20749ec1bfc6c47e65b61a2c24d7acde959d9a463`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:3b9156620133e8bd472e78fcdc63367c0bd8ce4728e9b37100cecab16f9ba20b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ba2e93561dabc36ed836ecddc93cde747f6c0533764e243a1059c63a1ea4f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:25:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 22:25:18 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 22:25:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 22:25:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 22:25:30 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 22:25:30 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 22:25:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:25:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:25:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000c31dcd775c39ea60679a161fbb3ec0114ed4a665986290232a4978c9b6a4e`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724475632ebc1a22d1c3ca248315c7f4e6f7c5296f4eae98f587b0b3d246cb8`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.4 MB (1353881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a4abf10ff23af34214cad41a3ae8c5d722d0e578c719b02dcc3b303fa33ba`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 231.6 KB (231630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efbd75e8157b70348066566d4008a9c0bada288c04ada82ba412b78dc02e0c`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06b78bd941b6d435a0daeb98222178fc6fdbd36c9b3cf1c59533e4bb87eb77b`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:b970c43232a9d83311742cddc2169c379db8304ab7409d9da95ff993ac82fbcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45510f2b3a9a17d1bb74f84ca2abab8ed1061dff0e55839a3e8754e2c3290639`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:49:46 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:50:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:50:03 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:50:04 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:50:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:50:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc475aa02ec0250350b4a331524b0a1e029de0aa51afc8d13cde5114f9a38f3`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64752c695a009aa97f4b6b21ee3618c0e6a15c1ccff9682ad7b50a01c411c09a`  
		Last Modified: Tue, 08 Aug 2023 23:50:27 GMT  
		Size: 1.4 MB (1361737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d6958824bc296d0ee662dc09b65827f4c19cf6d08b0bc88c29c0aac7daef4b`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe94a7a7ea3e66fec66bafea8a8825cb0e1e4d4e13a6dd126caa55abc4368d`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d36cfcde9b1ab7cc6cd3e055bd3be46da17fbb42fd44094957dc575cb2aef`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0c67d19c417d964e0fa15c5d365329a73cd5788e7c19e5f53a5b55fc870bc075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d15792a85e1bb890a83d0944741e7eb83b2c5986e752741cfb30fbefc01c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:42:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:42:59 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:42:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:43:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:43:08 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:43:08 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:43:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:43:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:43:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc2b61c233457afa4e875ea1072a41c83d8960d39d9aca2b510f19196183762`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91626c38ef7493a3034539c6f4b3cb05312bc7d9cd68767337fcb080f406f1`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.2 MB (1221498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4c8e4aad25c008e64ac4daeaa49158ce6be40d29a2b375e44b58e884de05b`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 2.4 MB (2431542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a65a1664c27d1527d4df8a094a4579394f4a254569198914d63f38e9cdfb98`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066b14d5da75b2e61d93352a2d245ef33cea8f6f7a4ef6015667d941a14debd`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:56b14b78a9337d99d4ae782cf7eb963ffb624a3bfd1f190d3648e95f819ff63a
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
$ docker pull spiped@sha256:024914f355d7df64887dde657bbcff7a61d2d4ccff5d43f4d3c3567092c3febd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38182082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7aa4b5d7b93c36ffc255e368fb924352cc5cdfd7eb91236c16fcf4f4309725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:36:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 14:36:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:36:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 14:37:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 14:37:18 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 14:37:18 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 14:37:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 14:37:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:37:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412f31823c3607ee7cf0f7ea2f70c0dc3f6eb610159a5582d2709f811e1168e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc70ab580442c24348a92d6781d1838c5d4811b03f958c534e18f34badb2d13`  
		Last Modified: Fri, 28 Jul 2023 14:37:32 GMT  
		Size: 2.6 MB (2586440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcc43564849e7d5dd99f86722dd00f61728bce2693f6bb0c1617942f0ec3f5a`  
		Last Modified: Fri, 28 Jul 2023 14:37:33 GMT  
		Size: 6.5 MB (6469507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea13792cc71ce8c887d6fe133b488092fafe74a36d98c02f75772fed5c47afee`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac29c4f562adf69c6ed89ee22148edd123f7eb4ab4e23444a343ed4c3c8836e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5bcd09c77588a67caae49433d4c86c6f91c69bae205ad672619afc5d749b5aba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34305753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756c18f247bb62bc63d31e0a50b9c68a64cd1a3347826060fc7e1eb4ed5b5785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:29 GMT
ADD file:53cf36eb7b72a7e970f4b18af1589402b2900f12e30820cdeccc8bb0c166df80 in / 
# Thu, 27 Jul 2023 23:48:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:18:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 06:18:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:18:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 06:18:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 06:18:32 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 06:18:32 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 06:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 06:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 06:18:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bd6dfc5281e13a0ca9fb8d9238ac9f14a0de04489913030c8e33b9398b4a4af`  
		Last Modified: Thu, 27 Jul 2023 23:51:28 GMT  
		Size: 27.0 MB (26983508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7867b868ea0c086b3cc19dffa7c4079dcd6909627f2495585866ef6686512`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eab6f4031dd2cbeb97b96eef0ca6ddeba7937c5a9fcb18252ba28e5f4c781b`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 2.2 MB (2184071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a21b08acfc2c6384677556aa01a3474ac7b9a055627d511785767566f9b7199`  
		Last Modified: Fri, 28 Jul 2023 06:18:48 GMT  
		Size: 5.1 MB (5136574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc10c0d99355974881d1e65b5a900d628c5d5beac6aeaa79ed789dd684a4e9`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b0514ba063b176ab332ff323fe4db1c5853e0bef483a0f7c0a0201fb4a6b2`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ed1463617a6ec4787fcfc89a0a312ac4af942cb5eb9ae05242f2bc91528b934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31728068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d79e97fafa93125c458792ea4e4ff699e48b2ea7c1a9e11ee8c4a15035e9e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:46 GMT
ADD file:b23161e9856801127e0136a920bcf075410ac23de605c82ca91d285b9f35941c in / 
# Thu, 27 Jul 2023 23:57:47 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 19:06:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 19:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 19:06:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 19:06:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 19:06:31 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 19:06:31 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 19:06:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 19:06:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 19:06:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb5b735234291ca6f672f489206ea5b6354d358f7d75a05036bdf84a6858d9f9`  
		Last Modified: Fri, 28 Jul 2023 00:03:11 GMT  
		Size: 24.8 MB (24805329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d222898f46d95805a7326b6800d1edeee028a45347a57164c34b37ae06c916ba`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782d770de44ba4a001c52e1933a14c4686dc69da2466959e091cb22b267309e`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 2.0 MB (2043254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6845efb4f08681fcd1ede0dcd46a25e88a6d18ffbfb220b7d87e608ccaa8283e`  
		Last Modified: Fri, 28 Jul 2023 19:06:48 GMT  
		Size: 4.9 MB (4877885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b4fe27ccb17150a9da129395b58336fa81ccea0fd84be8939f430df02eed7c`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7714096bd95fe9880e2181c0f6ea219e61883238224df612c68f2e5c9c0eec`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d88ac9d16fa209562e1a5179a8f008564588f851a68aee3ec5a597bb542d7df2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37067376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa29c1d765fbe597c57928bb35b8f9aa041e162896456d044076dae18b92d5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:19:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 01:19:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:19:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 01:20:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:20:03 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 01:20:03 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 01:20:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:20:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060019e05b5b6d10ebdcdfff5a1a17f7ea00e0c44edfa1a5d072061224979a8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c02a5e6dc6cb81fd967dcdd4813036b6e464930632ce048376eead8ee42a31d`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 2.4 MB (2429832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c0fde9cbba82047d390c8e027e769c909fd6ab0fda3c2275ed45f504faeb79`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 5.5 MB (5478716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a1efc6ee647d9b6aabdca7ed186fadc36667099750b3e749529f10bd02dd7c`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344e88b061ad36bcf2280ada625717ab2f97a1a36c5221c4987a23ca75fdec8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:1216033a6e3898df4dd046c41f47edd73e1ff860ad33686522b764b2fa8adea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1ff9f0b632345760ef1d669ec428f4f625912ebde09ad811a3ef25abee9f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 08:51:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 08:51:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 08:51:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 08:52:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 08:52:11 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 08:52:11 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 08:52:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 08:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 08:52:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5564c2bb87752c3c5b8455b4bd96d46493f6581cc3196a8cc8b8ea6bfeb3256d`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1900018d5bd91e250d0d6c226754b197866471c946aee6f8b71d49d58e937e2`  
		Last Modified: Fri, 28 Jul 2023 08:52:24 GMT  
		Size: 2.6 MB (2583603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb81d86a6894ea4e17723fa3b13fa8eea27aa34705b04b5f96a042615a07910`  
		Last Modified: Fri, 28 Jul 2023 08:52:25 GMT  
		Size: 5.9 MB (5940136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a12139c2df309d503138107a1dbe05ba8ce8182765eeb1da8c3d31775b6eb4f`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5b2d4b8b2a52e1a7eee9ece86c2c20678b566c98bc6d7cd965304487f8fa3`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:49a899236dbde8ea8d2213bd436cf4c527455e3f1e3c26e40c4f159e25c2a79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36756450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e63cf365261cf8e3b4451fe65ba8ae3798771cb198caca7960f5dc7920ca11a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:23 GMT
ADD file:90cbcf9a2aaf48a433b00118dd0821eeb291092da7b7f67ce6a525ce2cba1e3f in / 
# Thu, 27 Jul 2023 23:11:27 GMT
CMD ["bash"]
# Sat, 29 Jul 2023 02:27:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 29 Jul 2023 02:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 02:28:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 29 Jul 2023 02:30:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 29 Jul 2023 02:30:06 GMT
VOLUME [/spiped]
# Sat, 29 Jul 2023 02:30:09 GMT
WORKDIR /spiped
# Sat, 29 Jul 2023 02:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 29 Jul 2023 02:30:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jul 2023 02:30:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3252778e08fa8eb67ab052ad63281284b5ef1afdc40a36021228133487ab5d52`  
		Last Modified: Thu, 27 Jul 2023 23:22:26 GMT  
		Size: 29.1 MB (29121405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f33521a849a8bfb41d141a0ac9948095b8234c24ee434bdb5417b0e517eb7`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72f40d8259783265cafe9e800687826fc9f2dcb9ba5f5aaf1b5dd369a780f53`  
		Last Modified: Sat, 29 Jul 2023 02:30:44 GMT  
		Size: 1.8 MB (1831677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679711062d9a9f57e3af4f49a9bee04b0d0d8fa97e87b904115c9b612df7e7d`  
		Last Modified: Sat, 29 Jul 2023 02:30:47 GMT  
		Size: 5.8 MB (5801849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cae99e313273de740a8d561c3a00eadb3b3f6196b5c2114f9932159d4af207`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e972a6889d3ea08969c5cd356feade5bf9a9cd8453869165c924ad6cf766047a`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:cda509b294751f959f7764d1e1af011f4ce61c61e34eefbd25203a9ca0b28aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42306118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc441e69e8db9c2db390a467a61c87ec2e35d7a2a63c359e0e788615281064e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:01 GMT
ADD file:774a99e5c40757d27c981eb5ad6e03eb72970bb0c54f799eab1442624238ea3e in / 
# Thu, 27 Jul 2023 23:23:03 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 15:42:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 15:43:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:43:02 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 15:44:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 15:44:05 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 15:44:05 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 15:44:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 15:44:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 15:44:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad974e0ada84177d519dec70d0d7d9ff6a4f468bc7306425feb8429bc276bd8a`  
		Last Modified: Thu, 27 Jul 2023 23:29:24 GMT  
		Size: 33.1 MB (33119211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0834a39a8f321e61913bcebc5b10f2f4388ad008aed3aa0b7108c1c98aa672b8`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8637b8770fbcc45d233bc8c0685a004f863248524d9589bb8133462ad2ef98`  
		Last Modified: Fri, 28 Jul 2023 15:44:25 GMT  
		Size: 2.8 MB (2764991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e47b32eeb162a453e0f56b17945b85e59188dea37e5050beeb9fe549df43b6`  
		Last Modified: Fri, 28 Jul 2023 15:44:26 GMT  
		Size: 6.4 MB (6420314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ad0fc910585043bd75c1f9f637776962532c3318497e750adf297becfa27a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513cc6e981f0bcc9b41c0abcbebb0c975a964bdfc186524bcefd2f32b1496a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:9801f1b6d304727b25886ba0032e711317558ed43cc79dc97ef18474a21be5f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35132404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39476c9ecacb96484f9f9c5e593e97a9b1cba7f0ff99edcceac18924d9147c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:11 GMT
ADD file:0a5e1e86b375d60637d0829f77a12085777cf2ca07495b0f6249d8efea84e958 in / 
# Thu, 27 Jul 2023 23:47:13 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 12:21:25 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 12:21:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 12:21:29 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 12:21:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 12:21:42 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 12:21:42 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 12:21:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 12:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 12:21:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4301d25bb1bea85fcc5b364aec84ff58274f714cea191ab22d9b1b1e4f78527`  
		Last Modified: Thu, 27 Jul 2023 23:52:17 GMT  
		Size: 27.5 MB (27489697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef348951d7c2528189aaf990c50c94d47926bae33acaefdec1fc4dc9bdb677`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51341c3a783b2da9ec9d887eef33aebd6fecf5ec697f91fc4a64e0d7984678ba`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 2.3 MB (2257974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108045faf0e5fe4811d2bf60828dc7765761f5e5efc5bab62d8657cf552f885`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 5.4 MB (5383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209582ae96311472b03295510ead4f5bbad00cedca11bcab880a2e5f3684bd7`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901f1b400960248f49695ddd7e61dfc22b5aede3913f7604ce5e9cca49a75182`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:38016b388e6e908798c978ddd9fc91eb325925932ae89973fd9cceecbeaeeee3
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
$ docker pull spiped@sha256:d50ba6a73229914485b07e034308874110b29ff4248bbcd662f55717c0fa55ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ec3311c4035c9336c868279b0d420cc09b44cb5b9d93a813ed0c85d27304f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:20:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:20:54 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:21:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:21:05 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:21:05 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:21:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:21:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68caf666f4bb5f440531a0253294f702094d48f8694afeb159c3bee3a955928f`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56cc31d2500b156ae258f8cc835c039611b28a7fc664f9b5bec635f26a165f1`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.4 MB (1433005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0f60cfc992e735eab6827e81ef8ab9410faa8bb5a3aa95bcccd8324b6982b9`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 2.7 MB (2675293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfca5f8c6c25a4d506776dd84d3a716ba26161c5b53d23200c2131ad7abf8c5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5512defaf613253867bb293bce40f0f1572c7b5909bc313ff20891f7fdf3e5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:92c72514aab4032a46bd337535d95862b853d6c7e90cb1e86e689409cc93616f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4589191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b3dd418f5fe3e7be9bbb2632a3fd0fbbedad7f67e01d907d0d41c06bb6ce98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:36:09 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:36:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:36:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:36:17 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:36:17 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:36:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ffd38f9a9109fd6f2d98e59fac671a21acbcbd826d953a190916b8e28c4d7c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe31ddd32f93d6462563149d47e652289246cae76c3d69e2ae22c7f2dc157`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.2 MB (1236777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711c8b1ac9af3a0357e5e2ae10175a62c27bdea58e2e79fb7d413e2fa3a10138`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2f76630a196bedcec1d4f1f0542336e3189757e62aa7c83bd7f7e8f58680c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f674889b446c00cdd7da82689ee81ea78c84e02c462ad671bf3f9afd926afb1`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6b4ce7a3a962f7016da46f810228189be1cd6de1de0409f784505adca9fee42d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4264646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8b18499e87820bcff1593b1ccee12dbf54a9a32e6f7412af5d5c00268ce73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:51:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 21:51:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 21:51:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 21:51:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 21:51:52 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 21:51:52 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 21:51:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:51:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:51:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd254e37c3835d8a90d159f62497146fa2c0a51539455baafa4b5f3ad94073a`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b87a0e27917b2f49aabe18b41a38f10f52561eaed9cd75ecbf9bb54dd5ad657`  
		Last Modified: Tue, 08 Aug 2023 21:52:10 GMT  
		Size: 1.2 MB (1163899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a3f71f875284eede5e8bb82a4d0706d42594a0fec380b98dd516f0f75ed88`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 199.5 KB (199532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0eec6ac7d1270176b9ec72709b3186f9c9af79d5c747bdd03ac4818437e4b9`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da618866e96da51da8e7f96815a2d1e87198583082d2e819eaea328e7698149`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e44e0d5e538f2c9b96c690fff1ddb28d4803c23999f1d454965db93bbd687b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7264425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91392764bb6d58165d856113b83126cace6414f5457df110974537188a7da7be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:03:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:03:38 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:03:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:03:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:03:46 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:03:46 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:03:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:03:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29059dc293c00f54da752a558300b577b0437eae0d9b5f256f9a658105ca21ee`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351829a8bd360584cadfe089bec88f0a556d95f7cd39439affae43ea13c8a4b8`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.4 MB (1362700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f438d5a167cd51de9296e034ad6a94ce4848c706dfb163b6d19c35c1c3432`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 2.6 MB (2570731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3702fb444a3ca3cc36e82826eec5dbdc01917e9ff3532bcf06e5f3f4f00e9745`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e20649f92b6732530e48c20749ec1bfc6c47e65b61a2c24d7acde959d9a463`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:3b9156620133e8bd472e78fcdc63367c0bd8ce4728e9b37100cecab16f9ba20b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ba2e93561dabc36ed836ecddc93cde747f6c0533764e243a1059c63a1ea4f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:25:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 22:25:18 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 22:25:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 22:25:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 22:25:30 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 22:25:30 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 22:25:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:25:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:25:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000c31dcd775c39ea60679a161fbb3ec0114ed4a665986290232a4978c9b6a4e`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724475632ebc1a22d1c3ca248315c7f4e6f7c5296f4eae98f587b0b3d246cb8`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.4 MB (1353881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a4abf10ff23af34214cad41a3ae8c5d722d0e578c719b02dcc3b303fa33ba`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 231.6 KB (231630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efbd75e8157b70348066566d4008a9c0bada288c04ada82ba412b78dc02e0c`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06b78bd941b6d435a0daeb98222178fc6fdbd36c9b3cf1c59533e4bb87eb77b`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:b970c43232a9d83311742cddc2169c379db8304ab7409d9da95ff993ac82fbcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45510f2b3a9a17d1bb74f84ca2abab8ed1061dff0e55839a3e8754e2c3290639`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:49:46 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:50:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:50:03 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:50:04 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:50:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:50:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc475aa02ec0250350b4a331524b0a1e029de0aa51afc8d13cde5114f9a38f3`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64752c695a009aa97f4b6b21ee3618c0e6a15c1ccff9682ad7b50a01c411c09a`  
		Last Modified: Tue, 08 Aug 2023 23:50:27 GMT  
		Size: 1.4 MB (1361737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d6958824bc296d0ee662dc09b65827f4c19cf6d08b0bc88c29c0aac7daef4b`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe94a7a7ea3e66fec66bafea8a8825cb0e1e4d4e13a6dd126caa55abc4368d`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d36cfcde9b1ab7cc6cd3e055bd3be46da17fbb42fd44094957dc575cb2aef`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0c67d19c417d964e0fa15c5d365329a73cd5788e7c19e5f53a5b55fc870bc075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d15792a85e1bb890a83d0944741e7eb83b2c5986e752741cfb30fbefc01c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:42:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:42:59 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:42:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:43:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:43:08 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:43:08 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:43:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:43:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:43:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc2b61c233457afa4e875ea1072a41c83d8960d39d9aca2b510f19196183762`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91626c38ef7493a3034539c6f4b3cb05312bc7d9cd68767337fcb080f406f1`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.2 MB (1221498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4c8e4aad25c008e64ac4daeaa49158ce6be40d29a2b375e44b58e884de05b`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 2.4 MB (2431542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a65a1664c27d1527d4df8a094a4579394f4a254569198914d63f38e9cdfb98`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066b14d5da75b2e61d93352a2d245ef33cea8f6f7a4ef6015667d941a14debd`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:56b14b78a9337d99d4ae782cf7eb963ffb624a3bfd1f190d3648e95f819ff63a
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
$ docker pull spiped@sha256:024914f355d7df64887dde657bbcff7a61d2d4ccff5d43f4d3c3567092c3febd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38182082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7aa4b5d7b93c36ffc255e368fb924352cc5cdfd7eb91236c16fcf4f4309725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:36:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 14:36:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:36:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 14:37:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 14:37:18 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 14:37:18 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 14:37:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 14:37:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:37:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412f31823c3607ee7cf0f7ea2f70c0dc3f6eb610159a5582d2709f811e1168e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc70ab580442c24348a92d6781d1838c5d4811b03f958c534e18f34badb2d13`  
		Last Modified: Fri, 28 Jul 2023 14:37:32 GMT  
		Size: 2.6 MB (2586440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcc43564849e7d5dd99f86722dd00f61728bce2693f6bb0c1617942f0ec3f5a`  
		Last Modified: Fri, 28 Jul 2023 14:37:33 GMT  
		Size: 6.5 MB (6469507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea13792cc71ce8c887d6fe133b488092fafe74a36d98c02f75772fed5c47afee`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac29c4f562adf69c6ed89ee22148edd123f7eb4ab4e23444a343ed4c3c8836e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5bcd09c77588a67caae49433d4c86c6f91c69bae205ad672619afc5d749b5aba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34305753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756c18f247bb62bc63d31e0a50b9c68a64cd1a3347826060fc7e1eb4ed5b5785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:29 GMT
ADD file:53cf36eb7b72a7e970f4b18af1589402b2900f12e30820cdeccc8bb0c166df80 in / 
# Thu, 27 Jul 2023 23:48:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:18:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 06:18:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:18:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 06:18:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 06:18:32 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 06:18:32 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 06:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 06:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 06:18:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bd6dfc5281e13a0ca9fb8d9238ac9f14a0de04489913030c8e33b9398b4a4af`  
		Last Modified: Thu, 27 Jul 2023 23:51:28 GMT  
		Size: 27.0 MB (26983508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7867b868ea0c086b3cc19dffa7c4079dcd6909627f2495585866ef6686512`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eab6f4031dd2cbeb97b96eef0ca6ddeba7937c5a9fcb18252ba28e5f4c781b`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 2.2 MB (2184071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a21b08acfc2c6384677556aa01a3474ac7b9a055627d511785767566f9b7199`  
		Last Modified: Fri, 28 Jul 2023 06:18:48 GMT  
		Size: 5.1 MB (5136574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc10c0d99355974881d1e65b5a900d628c5d5beac6aeaa79ed789dd684a4e9`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b0514ba063b176ab332ff323fe4db1c5853e0bef483a0f7c0a0201fb4a6b2`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ed1463617a6ec4787fcfc89a0a312ac4af942cb5eb9ae05242f2bc91528b934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31728068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d79e97fafa93125c458792ea4e4ff699e48b2ea7c1a9e11ee8c4a15035e9e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:46 GMT
ADD file:b23161e9856801127e0136a920bcf075410ac23de605c82ca91d285b9f35941c in / 
# Thu, 27 Jul 2023 23:57:47 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 19:06:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 19:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 19:06:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 19:06:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 19:06:31 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 19:06:31 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 19:06:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 19:06:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 19:06:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb5b735234291ca6f672f489206ea5b6354d358f7d75a05036bdf84a6858d9f9`  
		Last Modified: Fri, 28 Jul 2023 00:03:11 GMT  
		Size: 24.8 MB (24805329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d222898f46d95805a7326b6800d1edeee028a45347a57164c34b37ae06c916ba`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782d770de44ba4a001c52e1933a14c4686dc69da2466959e091cb22b267309e`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 2.0 MB (2043254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6845efb4f08681fcd1ede0dcd46a25e88a6d18ffbfb220b7d87e608ccaa8283e`  
		Last Modified: Fri, 28 Jul 2023 19:06:48 GMT  
		Size: 4.9 MB (4877885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b4fe27ccb17150a9da129395b58336fa81ccea0fd84be8939f430df02eed7c`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7714096bd95fe9880e2181c0f6ea219e61883238224df612c68f2e5c9c0eec`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d88ac9d16fa209562e1a5179a8f008564588f851a68aee3ec5a597bb542d7df2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37067376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa29c1d765fbe597c57928bb35b8f9aa041e162896456d044076dae18b92d5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:19:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 01:19:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:19:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 01:20:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:20:03 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 01:20:03 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 01:20:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:20:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060019e05b5b6d10ebdcdfff5a1a17f7ea00e0c44edfa1a5d072061224979a8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c02a5e6dc6cb81fd967dcdd4813036b6e464930632ce048376eead8ee42a31d`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 2.4 MB (2429832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c0fde9cbba82047d390c8e027e769c909fd6ab0fda3c2275ed45f504faeb79`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 5.5 MB (5478716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a1efc6ee647d9b6aabdca7ed186fadc36667099750b3e749529f10bd02dd7c`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344e88b061ad36bcf2280ada625717ab2f97a1a36c5221c4987a23ca75fdec8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:1216033a6e3898df4dd046c41f47edd73e1ff860ad33686522b764b2fa8adea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1ff9f0b632345760ef1d669ec428f4f625912ebde09ad811a3ef25abee9f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 08:51:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 08:51:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 08:51:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 08:52:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 08:52:11 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 08:52:11 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 08:52:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 08:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 08:52:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5564c2bb87752c3c5b8455b4bd96d46493f6581cc3196a8cc8b8ea6bfeb3256d`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1900018d5bd91e250d0d6c226754b197866471c946aee6f8b71d49d58e937e2`  
		Last Modified: Fri, 28 Jul 2023 08:52:24 GMT  
		Size: 2.6 MB (2583603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb81d86a6894ea4e17723fa3b13fa8eea27aa34705b04b5f96a042615a07910`  
		Last Modified: Fri, 28 Jul 2023 08:52:25 GMT  
		Size: 5.9 MB (5940136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a12139c2df309d503138107a1dbe05ba8ce8182765eeb1da8c3d31775b6eb4f`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5b2d4b8b2a52e1a7eee9ece86c2c20678b566c98bc6d7cd965304487f8fa3`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:49a899236dbde8ea8d2213bd436cf4c527455e3f1e3c26e40c4f159e25c2a79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36756450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e63cf365261cf8e3b4451fe65ba8ae3798771cb198caca7960f5dc7920ca11a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:23 GMT
ADD file:90cbcf9a2aaf48a433b00118dd0821eeb291092da7b7f67ce6a525ce2cba1e3f in / 
# Thu, 27 Jul 2023 23:11:27 GMT
CMD ["bash"]
# Sat, 29 Jul 2023 02:27:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 29 Jul 2023 02:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 02:28:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 29 Jul 2023 02:30:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 29 Jul 2023 02:30:06 GMT
VOLUME [/spiped]
# Sat, 29 Jul 2023 02:30:09 GMT
WORKDIR /spiped
# Sat, 29 Jul 2023 02:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 29 Jul 2023 02:30:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jul 2023 02:30:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3252778e08fa8eb67ab052ad63281284b5ef1afdc40a36021228133487ab5d52`  
		Last Modified: Thu, 27 Jul 2023 23:22:26 GMT  
		Size: 29.1 MB (29121405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f33521a849a8bfb41d141a0ac9948095b8234c24ee434bdb5417b0e517eb7`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72f40d8259783265cafe9e800687826fc9f2dcb9ba5f5aaf1b5dd369a780f53`  
		Last Modified: Sat, 29 Jul 2023 02:30:44 GMT  
		Size: 1.8 MB (1831677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679711062d9a9f57e3af4f49a9bee04b0d0d8fa97e87b904115c9b612df7e7d`  
		Last Modified: Sat, 29 Jul 2023 02:30:47 GMT  
		Size: 5.8 MB (5801849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cae99e313273de740a8d561c3a00eadb3b3f6196b5c2114f9932159d4af207`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e972a6889d3ea08969c5cd356feade5bf9a9cd8453869165c924ad6cf766047a`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:cda509b294751f959f7764d1e1af011f4ce61c61e34eefbd25203a9ca0b28aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42306118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc441e69e8db9c2db390a467a61c87ec2e35d7a2a63c359e0e788615281064e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:01 GMT
ADD file:774a99e5c40757d27c981eb5ad6e03eb72970bb0c54f799eab1442624238ea3e in / 
# Thu, 27 Jul 2023 23:23:03 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 15:42:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 15:43:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:43:02 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 15:44:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 15:44:05 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 15:44:05 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 15:44:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 15:44:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 15:44:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad974e0ada84177d519dec70d0d7d9ff6a4f468bc7306425feb8429bc276bd8a`  
		Last Modified: Thu, 27 Jul 2023 23:29:24 GMT  
		Size: 33.1 MB (33119211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0834a39a8f321e61913bcebc5b10f2f4388ad008aed3aa0b7108c1c98aa672b8`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8637b8770fbcc45d233bc8c0685a004f863248524d9589bb8133462ad2ef98`  
		Last Modified: Fri, 28 Jul 2023 15:44:25 GMT  
		Size: 2.8 MB (2764991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e47b32eeb162a453e0f56b17945b85e59188dea37e5050beeb9fe549df43b6`  
		Last Modified: Fri, 28 Jul 2023 15:44:26 GMT  
		Size: 6.4 MB (6420314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ad0fc910585043bd75c1f9f637776962532c3318497e750adf297becfa27a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513cc6e981f0bcc9b41c0abcbebb0c975a964bdfc186524bcefd2f32b1496a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:9801f1b6d304727b25886ba0032e711317558ed43cc79dc97ef18474a21be5f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35132404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39476c9ecacb96484f9f9c5e593e97a9b1cba7f0ff99edcceac18924d9147c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:11 GMT
ADD file:0a5e1e86b375d60637d0829f77a12085777cf2ca07495b0f6249d8efea84e958 in / 
# Thu, 27 Jul 2023 23:47:13 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 12:21:25 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 12:21:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 12:21:29 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 12:21:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 12:21:42 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 12:21:42 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 12:21:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 12:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 12:21:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4301d25bb1bea85fcc5b364aec84ff58274f714cea191ab22d9b1b1e4f78527`  
		Last Modified: Thu, 27 Jul 2023 23:52:17 GMT  
		Size: 27.5 MB (27489697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef348951d7c2528189aaf990c50c94d47926bae33acaefdec1fc4dc9bdb677`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51341c3a783b2da9ec9d887eef33aebd6fecf5ec697f91fc4a64e0d7984678ba`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 2.3 MB (2257974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108045faf0e5fe4811d2bf60828dc7765761f5e5efc5bab62d8657cf552f885`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 5.4 MB (5383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209582ae96311472b03295510ead4f5bbad00cedca11bcab880a2e5f3684bd7`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901f1b400960248f49695ddd7e61dfc22b5aede3913f7604ce5e9cca49a75182`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:38016b388e6e908798c978ddd9fc91eb325925932ae89973fd9cceecbeaeeee3
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
$ docker pull spiped@sha256:d50ba6a73229914485b07e034308874110b29ff4248bbcd662f55717c0fa55ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ec3311c4035c9336c868279b0d420cc09b44cb5b9d93a813ed0c85d27304f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:20:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:20:54 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:21:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:21:05 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:21:05 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:21:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:21:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68caf666f4bb5f440531a0253294f702094d48f8694afeb159c3bee3a955928f`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56cc31d2500b156ae258f8cc835c039611b28a7fc664f9b5bec635f26a165f1`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.4 MB (1433005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0f60cfc992e735eab6827e81ef8ab9410faa8bb5a3aa95bcccd8324b6982b9`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 2.7 MB (2675293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfca5f8c6c25a4d506776dd84d3a716ba26161c5b53d23200c2131ad7abf8c5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5512defaf613253867bb293bce40f0f1572c7b5909bc313ff20891f7fdf3e5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:92c72514aab4032a46bd337535d95862b853d6c7e90cb1e86e689409cc93616f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4589191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b3dd418f5fe3e7be9bbb2632a3fd0fbbedad7f67e01d907d0d41c06bb6ce98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:36:09 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:36:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:36:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:36:17 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:36:17 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:36:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ffd38f9a9109fd6f2d98e59fac671a21acbcbd826d953a190916b8e28c4d7c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe31ddd32f93d6462563149d47e652289246cae76c3d69e2ae22c7f2dc157`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.2 MB (1236777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711c8b1ac9af3a0357e5e2ae10175a62c27bdea58e2e79fb7d413e2fa3a10138`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2f76630a196bedcec1d4f1f0542336e3189757e62aa7c83bd7f7e8f58680c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f674889b446c00cdd7da82689ee81ea78c84e02c462ad671bf3f9afd926afb1`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6b4ce7a3a962f7016da46f810228189be1cd6de1de0409f784505adca9fee42d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4264646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8b18499e87820bcff1593b1ccee12dbf54a9a32e6f7412af5d5c00268ce73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:51:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 21:51:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 21:51:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 21:51:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 21:51:52 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 21:51:52 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 21:51:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:51:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:51:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd254e37c3835d8a90d159f62497146fa2c0a51539455baafa4b5f3ad94073a`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b87a0e27917b2f49aabe18b41a38f10f52561eaed9cd75ecbf9bb54dd5ad657`  
		Last Modified: Tue, 08 Aug 2023 21:52:10 GMT  
		Size: 1.2 MB (1163899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a3f71f875284eede5e8bb82a4d0706d42594a0fec380b98dd516f0f75ed88`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 199.5 KB (199532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0eec6ac7d1270176b9ec72709b3186f9c9af79d5c747bdd03ac4818437e4b9`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da618866e96da51da8e7f96815a2d1e87198583082d2e819eaea328e7698149`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e44e0d5e538f2c9b96c690fff1ddb28d4803c23999f1d454965db93bbd687b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7264425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91392764bb6d58165d856113b83126cace6414f5457df110974537188a7da7be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:03:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:03:38 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:03:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:03:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:03:46 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:03:46 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:03:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:03:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29059dc293c00f54da752a558300b577b0437eae0d9b5f256f9a658105ca21ee`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351829a8bd360584cadfe089bec88f0a556d95f7cd39439affae43ea13c8a4b8`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.4 MB (1362700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f438d5a167cd51de9296e034ad6a94ce4848c706dfb163b6d19c35c1c3432`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 2.6 MB (2570731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3702fb444a3ca3cc36e82826eec5dbdc01917e9ff3532bcf06e5f3f4f00e9745`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e20649f92b6732530e48c20749ec1bfc6c47e65b61a2c24d7acde959d9a463`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:3b9156620133e8bd472e78fcdc63367c0bd8ce4728e9b37100cecab16f9ba20b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ba2e93561dabc36ed836ecddc93cde747f6c0533764e243a1059c63a1ea4f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:25:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 22:25:18 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 22:25:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 22:25:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 22:25:30 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 22:25:30 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 22:25:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:25:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:25:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000c31dcd775c39ea60679a161fbb3ec0114ed4a665986290232a4978c9b6a4e`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724475632ebc1a22d1c3ca248315c7f4e6f7c5296f4eae98f587b0b3d246cb8`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.4 MB (1353881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a4abf10ff23af34214cad41a3ae8c5d722d0e578c719b02dcc3b303fa33ba`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 231.6 KB (231630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efbd75e8157b70348066566d4008a9c0bada288c04ada82ba412b78dc02e0c`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06b78bd941b6d435a0daeb98222178fc6fdbd36c9b3cf1c59533e4bb87eb77b`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:b970c43232a9d83311742cddc2169c379db8304ab7409d9da95ff993ac82fbcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45510f2b3a9a17d1bb74f84ca2abab8ed1061dff0e55839a3e8754e2c3290639`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:49:46 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:50:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:50:03 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:50:04 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:50:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:50:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc475aa02ec0250350b4a331524b0a1e029de0aa51afc8d13cde5114f9a38f3`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64752c695a009aa97f4b6b21ee3618c0e6a15c1ccff9682ad7b50a01c411c09a`  
		Last Modified: Tue, 08 Aug 2023 23:50:27 GMT  
		Size: 1.4 MB (1361737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d6958824bc296d0ee662dc09b65827f4c19cf6d08b0bc88c29c0aac7daef4b`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe94a7a7ea3e66fec66bafea8a8825cb0e1e4d4e13a6dd126caa55abc4368d`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d36cfcde9b1ab7cc6cd3e055bd3be46da17fbb42fd44094957dc575cb2aef`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0c67d19c417d964e0fa15c5d365329a73cd5788e7c19e5f53a5b55fc870bc075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d15792a85e1bb890a83d0944741e7eb83b2c5986e752741cfb30fbefc01c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:42:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:42:59 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:42:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:43:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:43:08 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:43:08 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:43:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:43:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:43:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc2b61c233457afa4e875ea1072a41c83d8960d39d9aca2b510f19196183762`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91626c38ef7493a3034539c6f4b3cb05312bc7d9cd68767337fcb080f406f1`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.2 MB (1221498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4c8e4aad25c008e64ac4daeaa49158ce6be40d29a2b375e44b58e884de05b`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 2.4 MB (2431542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a65a1664c27d1527d4df8a094a4579394f4a254569198914d63f38e9cdfb98`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066b14d5da75b2e61d93352a2d245ef33cea8f6f7a4ef6015667d941a14debd`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:38016b388e6e908798c978ddd9fc91eb325925932ae89973fd9cceecbeaeeee3
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
$ docker pull spiped@sha256:d50ba6a73229914485b07e034308874110b29ff4248bbcd662f55717c0fa55ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ec3311c4035c9336c868279b0d420cc09b44cb5b9d93a813ed0c85d27304f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:20:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:20:54 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:21:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:21:05 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:21:05 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:21:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:21:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68caf666f4bb5f440531a0253294f702094d48f8694afeb159c3bee3a955928f`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56cc31d2500b156ae258f8cc835c039611b28a7fc664f9b5bec635f26a165f1`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.4 MB (1433005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0f60cfc992e735eab6827e81ef8ab9410faa8bb5a3aa95bcccd8324b6982b9`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 2.7 MB (2675293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfca5f8c6c25a4d506776dd84d3a716ba26161c5b53d23200c2131ad7abf8c5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5512defaf613253867bb293bce40f0f1572c7b5909bc313ff20891f7fdf3e5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:92c72514aab4032a46bd337535d95862b853d6c7e90cb1e86e689409cc93616f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4589191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b3dd418f5fe3e7be9bbb2632a3fd0fbbedad7f67e01d907d0d41c06bb6ce98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:36:09 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:36:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:36:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:36:17 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:36:17 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:36:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ffd38f9a9109fd6f2d98e59fac671a21acbcbd826d953a190916b8e28c4d7c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe31ddd32f93d6462563149d47e652289246cae76c3d69e2ae22c7f2dc157`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 1.2 MB (1236777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711c8b1ac9af3a0357e5e2ae10175a62c27bdea58e2e79fb7d413e2fa3a10138`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2f76630a196bedcec1d4f1f0542336e3189757e62aa7c83bd7f7e8f58680c`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f674889b446c00cdd7da82689ee81ea78c84e02c462ad671bf3f9afd926afb1`  
		Last Modified: Tue, 08 Aug 2023 23:36:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6b4ce7a3a962f7016da46f810228189be1cd6de1de0409f784505adca9fee42d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4264646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8b18499e87820bcff1593b1ccee12dbf54a9a32e6f7412af5d5c00268ce73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:51:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 21:51:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 21:51:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 21:51:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 21:51:52 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 21:51:52 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 21:51:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:51:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:51:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd254e37c3835d8a90d159f62497146fa2c0a51539455baafa4b5f3ad94073a`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b87a0e27917b2f49aabe18b41a38f10f52561eaed9cd75ecbf9bb54dd5ad657`  
		Last Modified: Tue, 08 Aug 2023 21:52:10 GMT  
		Size: 1.2 MB (1163899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a3f71f875284eede5e8bb82a4d0706d42594a0fec380b98dd516f0f75ed88`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 199.5 KB (199532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0eec6ac7d1270176b9ec72709b3186f9c9af79d5c747bdd03ac4818437e4b9`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da618866e96da51da8e7f96815a2d1e87198583082d2e819eaea328e7698149`  
		Last Modified: Tue, 08 Aug 2023 21:52:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e44e0d5e538f2c9b96c690fff1ddb28d4803c23999f1d454965db93bbd687b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7264425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91392764bb6d58165d856113b83126cace6414f5457df110974537188a7da7be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:03:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:03:38 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:03:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:03:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:03:46 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:03:46 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:03:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:03:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29059dc293c00f54da752a558300b577b0437eae0d9b5f256f9a658105ca21ee`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351829a8bd360584cadfe089bec88f0a556d95f7cd39439affae43ea13c8a4b8`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.4 MB (1362700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f438d5a167cd51de9296e034ad6a94ce4848c706dfb163b6d19c35c1c3432`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 2.6 MB (2570731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3702fb444a3ca3cc36e82826eec5dbdc01917e9ff3532bcf06e5f3f4f00e9745`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e20649f92b6732530e48c20749ec1bfc6c47e65b61a2c24d7acde959d9a463`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:3b9156620133e8bd472e78fcdc63367c0bd8ce4728e9b37100cecab16f9ba20b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ba2e93561dabc36ed836ecddc93cde747f6c0533764e243a1059c63a1ea4f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:25:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 22:25:18 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 22:25:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 22:25:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 22:25:30 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 22:25:30 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 22:25:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:25:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:25:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000c31dcd775c39ea60679a161fbb3ec0114ed4a665986290232a4978c9b6a4e`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724475632ebc1a22d1c3ca248315c7f4e6f7c5296f4eae98f587b0b3d246cb8`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 1.4 MB (1353881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a4abf10ff23af34214cad41a3ae8c5d722d0e578c719b02dcc3b303fa33ba`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 231.6 KB (231630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efbd75e8157b70348066566d4008a9c0bada288c04ada82ba412b78dc02e0c`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06b78bd941b6d435a0daeb98222178fc6fdbd36c9b3cf1c59533e4bb87eb77b`  
		Last Modified: Tue, 08 Aug 2023 22:25:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:b970c43232a9d83311742cddc2169c379db8304ab7409d9da95ff993ac82fbcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45510f2b3a9a17d1bb74f84ca2abab8ed1061dff0e55839a3e8754e2c3290639`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:49:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 08 Aug 2023 23:49:46 GMT
RUN apk add --no-cache libssl1.1
# Tue, 08 Aug 2023 23:49:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 08 Aug 2023 23:50:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 08 Aug 2023 23:50:03 GMT
VOLUME [/spiped]
# Tue, 08 Aug 2023 23:50:04 GMT
WORKDIR /spiped
# Tue, 08 Aug 2023 23:50:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:50:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc475aa02ec0250350b4a331524b0a1e029de0aa51afc8d13cde5114f9a38f3`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64752c695a009aa97f4b6b21ee3618c0e6a15c1ccff9682ad7b50a01c411c09a`  
		Last Modified: Tue, 08 Aug 2023 23:50:27 GMT  
		Size: 1.4 MB (1361737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d6958824bc296d0ee662dc09b65827f4c19cf6d08b0bc88c29c0aac7daef4b`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe94a7a7ea3e66fec66bafea8a8825cb0e1e4d4e13a6dd126caa55abc4368d`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d36cfcde9b1ab7cc6cd3e055bd3be46da17fbb42fd44094957dc575cb2aef`  
		Last Modified: Tue, 08 Aug 2023 23:50:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0c67d19c417d964e0fa15c5d365329a73cd5788e7c19e5f53a5b55fc870bc075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d15792a85e1bb890a83d0944741e7eb83b2c5986e752741cfb30fbefc01c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:42:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:42:59 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:42:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:43:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:43:08 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:43:08 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:43:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:43:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:43:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc2b61c233457afa4e875ea1072a41c83d8960d39d9aca2b510f19196183762`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91626c38ef7493a3034539c6f4b3cb05312bc7d9cd68767337fcb080f406f1`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.2 MB (1221498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4c8e4aad25c008e64ac4daeaa49158ce6be40d29a2b375e44b58e884de05b`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 2.4 MB (2431542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a65a1664c27d1527d4df8a094a4579394f4a254569198914d63f38e9cdfb98`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066b14d5da75b2e61d93352a2d245ef33cea8f6f7a4ef6015667d941a14debd`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:56b14b78a9337d99d4ae782cf7eb963ffb624a3bfd1f190d3648e95f819ff63a
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
$ docker pull spiped@sha256:024914f355d7df64887dde657bbcff7a61d2d4ccff5d43f4d3c3567092c3febd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38182082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7aa4b5d7b93c36ffc255e368fb924352cc5cdfd7eb91236c16fcf4f4309725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:36:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 14:36:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:36:57 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 14:37:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 14:37:18 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 14:37:18 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 14:37:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 14:37:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:37:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412f31823c3607ee7cf0f7ea2f70c0dc3f6eb610159a5582d2709f811e1168e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc70ab580442c24348a92d6781d1838c5d4811b03f958c534e18f34badb2d13`  
		Last Modified: Fri, 28 Jul 2023 14:37:32 GMT  
		Size: 2.6 MB (2586440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcc43564849e7d5dd99f86722dd00f61728bce2693f6bb0c1617942f0ec3f5a`  
		Last Modified: Fri, 28 Jul 2023 14:37:33 GMT  
		Size: 6.5 MB (6469507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea13792cc71ce8c887d6fe133b488092fafe74a36d98c02f75772fed5c47afee`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac29c4f562adf69c6ed89ee22148edd123f7eb4ab4e23444a343ed4c3c8836e`  
		Last Modified: Fri, 28 Jul 2023 14:37:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5bcd09c77588a67caae49433d4c86c6f91c69bae205ad672619afc5d749b5aba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34305753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756c18f247bb62bc63d31e0a50b9c68a64cd1a3347826060fc7e1eb4ed5b5785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:29 GMT
ADD file:53cf36eb7b72a7e970f4b18af1589402b2900f12e30820cdeccc8bb0c166df80 in / 
# Thu, 27 Jul 2023 23:48:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:18:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 06:18:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:18:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 06:18:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 06:18:32 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 06:18:32 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 06:18:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 06:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 06:18:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bd6dfc5281e13a0ca9fb8d9238ac9f14a0de04489913030c8e33b9398b4a4af`  
		Last Modified: Thu, 27 Jul 2023 23:51:28 GMT  
		Size: 27.0 MB (26983508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7867b868ea0c086b3cc19dffa7c4079dcd6909627f2495585866ef6686512`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eab6f4031dd2cbeb97b96eef0ca6ddeba7937c5a9fcb18252ba28e5f4c781b`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 2.2 MB (2184071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a21b08acfc2c6384677556aa01a3474ac7b9a055627d511785767566f9b7199`  
		Last Modified: Fri, 28 Jul 2023 06:18:48 GMT  
		Size: 5.1 MB (5136574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc10c0d99355974881d1e65b5a900d628c5d5beac6aeaa79ed789dd684a4e9`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b0514ba063b176ab332ff323fe4db1c5853e0bef483a0f7c0a0201fb4a6b2`  
		Last Modified: Fri, 28 Jul 2023 06:18:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ed1463617a6ec4787fcfc89a0a312ac4af942cb5eb9ae05242f2bc91528b934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31728068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d79e97fafa93125c458792ea4e4ff699e48b2ea7c1a9e11ee8c4a15035e9e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:46 GMT
ADD file:b23161e9856801127e0136a920bcf075410ac23de605c82ca91d285b9f35941c in / 
# Thu, 27 Jul 2023 23:57:47 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 19:06:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 19:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 19:06:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 19:06:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 19:06:31 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 19:06:31 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 19:06:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 19:06:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 19:06:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb5b735234291ca6f672f489206ea5b6354d358f7d75a05036bdf84a6858d9f9`  
		Last Modified: Fri, 28 Jul 2023 00:03:11 GMT  
		Size: 24.8 MB (24805329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d222898f46d95805a7326b6800d1edeee028a45347a57164c34b37ae06c916ba`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782d770de44ba4a001c52e1933a14c4686dc69da2466959e091cb22b267309e`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 2.0 MB (2043254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6845efb4f08681fcd1ede0dcd46a25e88a6d18ffbfb220b7d87e608ccaa8283e`  
		Last Modified: Fri, 28 Jul 2023 19:06:48 GMT  
		Size: 4.9 MB (4877885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b4fe27ccb17150a9da129395b58336fa81ccea0fd84be8939f430df02eed7c`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7714096bd95fe9880e2181c0f6ea219e61883238224df612c68f2e5c9c0eec`  
		Last Modified: Fri, 28 Jul 2023 19:06:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d88ac9d16fa209562e1a5179a8f008564588f851a68aee3ec5a597bb542d7df2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37067376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa29c1d765fbe597c57928bb35b8f9aa041e162896456d044076dae18b92d5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:19:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 01:19:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:19:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 01:20:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:20:03 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 01:20:03 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 01:20:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:20:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060019e05b5b6d10ebdcdfff5a1a17f7ea00e0c44edfa1a5d072061224979a8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c02a5e6dc6cb81fd967dcdd4813036b6e464930632ce048376eead8ee42a31d`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 2.4 MB (2429832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c0fde9cbba82047d390c8e027e769c909fd6ab0fda3c2275ed45f504faeb79`  
		Last Modified: Fri, 28 Jul 2023 01:20:16 GMT  
		Size: 5.5 MB (5478716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a1efc6ee647d9b6aabdca7ed186fadc36667099750b3e749529f10bd02dd7c`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344e88b061ad36bcf2280ada625717ab2f97a1a36c5221c4987a23ca75fdec8`  
		Last Modified: Fri, 28 Jul 2023 01:20:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:1216033a6e3898df4dd046c41f47edd73e1ff860ad33686522b764b2fa8adea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1ff9f0b632345760ef1d669ec428f4f625912ebde09ad811a3ef25abee9f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 08:51:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 08:51:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 08:51:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 08:52:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 08:52:11 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 08:52:11 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 08:52:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 08:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 08:52:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5564c2bb87752c3c5b8455b4bd96d46493f6581cc3196a8cc8b8ea6bfeb3256d`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1900018d5bd91e250d0d6c226754b197866471c946aee6f8b71d49d58e937e2`  
		Last Modified: Fri, 28 Jul 2023 08:52:24 GMT  
		Size: 2.6 MB (2583603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb81d86a6894ea4e17723fa3b13fa8eea27aa34705b04b5f96a042615a07910`  
		Last Modified: Fri, 28 Jul 2023 08:52:25 GMT  
		Size: 5.9 MB (5940136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a12139c2df309d503138107a1dbe05ba8ce8182765eeb1da8c3d31775b6eb4f`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5b2d4b8b2a52e1a7eee9ece86c2c20678b566c98bc6d7cd965304487f8fa3`  
		Last Modified: Fri, 28 Jul 2023 08:52:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:49a899236dbde8ea8d2213bd436cf4c527455e3f1e3c26e40c4f159e25c2a79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36756450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e63cf365261cf8e3b4451fe65ba8ae3798771cb198caca7960f5dc7920ca11a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:23 GMT
ADD file:90cbcf9a2aaf48a433b00118dd0821eeb291092da7b7f67ce6a525ce2cba1e3f in / 
# Thu, 27 Jul 2023 23:11:27 GMT
CMD ["bash"]
# Sat, 29 Jul 2023 02:27:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 29 Jul 2023 02:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 02:28:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 29 Jul 2023 02:30:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 29 Jul 2023 02:30:06 GMT
VOLUME [/spiped]
# Sat, 29 Jul 2023 02:30:09 GMT
WORKDIR /spiped
# Sat, 29 Jul 2023 02:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 29 Jul 2023 02:30:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jul 2023 02:30:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3252778e08fa8eb67ab052ad63281284b5ef1afdc40a36021228133487ab5d52`  
		Last Modified: Thu, 27 Jul 2023 23:22:26 GMT  
		Size: 29.1 MB (29121405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f33521a849a8bfb41d141a0ac9948095b8234c24ee434bdb5417b0e517eb7`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72f40d8259783265cafe9e800687826fc9f2dcb9ba5f5aaf1b5dd369a780f53`  
		Last Modified: Sat, 29 Jul 2023 02:30:44 GMT  
		Size: 1.8 MB (1831677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679711062d9a9f57e3af4f49a9bee04b0d0d8fa97e87b904115c9b612df7e7d`  
		Last Modified: Sat, 29 Jul 2023 02:30:47 GMT  
		Size: 5.8 MB (5801849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cae99e313273de740a8d561c3a00eadb3b3f6196b5c2114f9932159d4af207`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e972a6889d3ea08969c5cd356feade5bf9a9cd8453869165c924ad6cf766047a`  
		Last Modified: Sat, 29 Jul 2023 02:30:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:cda509b294751f959f7764d1e1af011f4ce61c61e34eefbd25203a9ca0b28aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42306118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc441e69e8db9c2db390a467a61c87ec2e35d7a2a63c359e0e788615281064e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:01 GMT
ADD file:774a99e5c40757d27c981eb5ad6e03eb72970bb0c54f799eab1442624238ea3e in / 
# Thu, 27 Jul 2023 23:23:03 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 15:42:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 15:43:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:43:02 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 15:44:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 15:44:05 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 15:44:05 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 15:44:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 15:44:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 15:44:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad974e0ada84177d519dec70d0d7d9ff6a4f468bc7306425feb8429bc276bd8a`  
		Last Modified: Thu, 27 Jul 2023 23:29:24 GMT  
		Size: 33.1 MB (33119211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0834a39a8f321e61913bcebc5b10f2f4388ad008aed3aa0b7108c1c98aa672b8`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8637b8770fbcc45d233bc8c0685a004f863248524d9589bb8133462ad2ef98`  
		Last Modified: Fri, 28 Jul 2023 15:44:25 GMT  
		Size: 2.8 MB (2764991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e47b32eeb162a453e0f56b17945b85e59188dea37e5050beeb9fe549df43b6`  
		Last Modified: Fri, 28 Jul 2023 15:44:26 GMT  
		Size: 6.4 MB (6420314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ad0fc910585043bd75c1f9f637776962532c3318497e750adf297becfa27a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513cc6e981f0bcc9b41c0abcbebb0c975a964bdfc186524bcefd2f32b1496a`  
		Last Modified: Fri, 28 Jul 2023 15:44:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:9801f1b6d304727b25886ba0032e711317558ed43cc79dc97ef18474a21be5f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35132404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39476c9ecacb96484f9f9c5e593e97a9b1cba7f0ff99edcceac18924d9147c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:11 GMT
ADD file:0a5e1e86b375d60637d0829f77a12085777cf2ca07495b0f6249d8efea84e958 in / 
# Thu, 27 Jul 2023 23:47:13 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 12:21:25 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 28 Jul 2023 12:21:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 12:21:29 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 28 Jul 2023 12:21:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 12:21:42 GMT
VOLUME [/spiped]
# Fri, 28 Jul 2023 12:21:42 GMT
WORKDIR /spiped
# Fri, 28 Jul 2023 12:21:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 28 Jul 2023 12:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 12:21:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4301d25bb1bea85fcc5b364aec84ff58274f714cea191ab22d9b1b1e4f78527`  
		Last Modified: Thu, 27 Jul 2023 23:52:17 GMT  
		Size: 27.5 MB (27489697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef348951d7c2528189aaf990c50c94d47926bae33acaefdec1fc4dc9bdb677`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51341c3a783b2da9ec9d887eef33aebd6fecf5ec697f91fc4a64e0d7984678ba`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 2.3 MB (2257974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108045faf0e5fe4811d2bf60828dc7765761f5e5efc5bab62d8657cf552f885`  
		Last Modified: Fri, 28 Jul 2023 12:22:05 GMT  
		Size: 5.4 MB (5383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209582ae96311472b03295510ead4f5bbad00cedca11bcab880a2e5f3684bd7`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901f1b400960248f49695ddd7e61dfc22b5aede3913f7604ce5e9cca49a75182`  
		Last Modified: Fri, 28 Jul 2023 12:22:04 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
