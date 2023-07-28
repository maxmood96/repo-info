## `spiped:latest`

```console
$ docker pull spiped@sha256:bc45ffb892a0d602a75b7a30c198a29e82001b7039a55317054a5d0142ecbf26
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
$ docker pull spiped@sha256:fa8d158ea62aae373b010ecee32e5ecea6fb4b437a2eb49aca790fae1736d647
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31723078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1b970d4425fc1f51cea7f5490f388e981e5d34fb3d9ce808c13f03413e26b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Jul 2023 00:57:54 GMT
ADD file:d168d1710cbca4edb322c26348dafaf2b3a64980f52b8b790f334cdbd6a7047e in / 
# Tue, 04 Jul 2023 00:57:55 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 15:38:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 04 Jul 2023 15:38:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:38:29 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 04 Jul 2023 15:38:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 15:39:00 GMT
VOLUME [/spiped]
# Tue, 04 Jul 2023 15:39:00 GMT
WORKDIR /spiped
# Tue, 04 Jul 2023 15:39:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 04 Jul 2023 15:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 15:39:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:340ace0baa422f18db718d7634c1c88a9650f4871dda2630ef15577120aa6816`  
		Last Modified: Tue, 04 Jul 2023 01:02:50 GMT  
		Size: 24.8 MB (24801264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3403c8419ded94d78b4756589f9377598959311520c9817d426929dd63659d`  
		Last Modified: Tue, 04 Jul 2023 15:39:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e44f54d21c1788863d34d076c0eb22f62f3a2ae411d37e866f85c47e68b9e38`  
		Last Modified: Tue, 04 Jul 2023 15:39:19 GMT  
		Size: 2.0 MB (2043275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fb7cd0361eb4be25908a03aad1082a7bf6098ee6b8d10b3d2a5903eb5ed391`  
		Last Modified: Tue, 04 Jul 2023 15:39:20 GMT  
		Size: 4.9 MB (4876936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9151574768b755fac6c25ce6badff07f10c8c3faef3210d692cba091ef8bc2a9`  
		Last Modified: Tue, 04 Jul 2023 15:39:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d35983368786e50998af1a99a87e7b6667403aeecdcb0b06bf199bb5ac02d7d`  
		Last Modified: Tue, 04 Jul 2023 15:39:18 GMT  
		Size: 343.0 B  
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
$ docker pull spiped@sha256:7828d1ba4ad693f840919aad0cb1e0e41abf15d45e4e18003cace27821904f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36751895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8be90d1d0cd2a6310b0bb4f84e20519e4cef602052b662880c8b18e9ffdfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Jul 2023 01:09:28 GMT
ADD file:cf4b72a35644a7b9f5f1ca39a54e484822f408f6821f0800f1167ae48ad6e38e in / 
# Tue, 04 Jul 2023 01:09:32 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:26:54 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 04 Jul 2023 19:27:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:27:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 04 Jul 2023 19:28:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 19:28:59 GMT
VOLUME [/spiped]
# Tue, 04 Jul 2023 19:29:02 GMT
WORKDIR /spiped
# Tue, 04 Jul 2023 19:29:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 04 Jul 2023 19:29:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 19:29:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:502a81d5004983c2a770a910286271410d8e2b20d0cb61ef7397e664e1e72654`  
		Last Modified: Tue, 04 Jul 2023 01:19:57 GMT  
		Size: 29.1 MB (29118201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd72a1da8eadcc7f546db387b7d5db2cb3f5c275470134400731b157019549`  
		Last Modified: Tue, 04 Jul 2023 19:29:23 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94883ccc7bee39640c9c5e1367539c5c1f804f0b93b617f05df643875af480ed`  
		Last Modified: Tue, 04 Jul 2023 19:29:24 GMT  
		Size: 1.8 MB (1831639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91bd9d103397dcbe82f481782e4dd0f11d6d09507e1dc10260613fd2cad06e7`  
		Last Modified: Tue, 04 Jul 2023 19:29:28 GMT  
		Size: 5.8 MB (5800537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2070ac4c1d28067212b8eb40f2ad23b8418704e0fa5964286420c72d250f061f`  
		Last Modified: Tue, 04 Jul 2023 19:29:23 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7ab12d58ce7a0d93d2b5e99bef7c2303828489033eb8a77edc5912eb28b4ba`  
		Last Modified: Tue, 04 Jul 2023 19:29:23 GMT  
		Size: 342.0 B  
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
