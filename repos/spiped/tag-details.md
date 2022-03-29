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
$ docker pull spiped@sha256:460c7c717a55f8dd8e41ef1de3e7d16cd01f3f22aa7d53bc4a0634edb5769fa9
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
$ docker pull spiped@sha256:f236fca971a0526aa22ab4aa69709d302210d7e1f5bd42902bde2803ec0495bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37348627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab54c336e542bbe2bacf29196b05876f18889ca6f79cd1c223af52a9bcf3241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 12:05:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 12:05:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 12:05:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 12:06:07 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:07 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda024001dd8419f652d3fde717d37b32c648032cc3f92d00978db9268a65b97`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55c823e9d54047194e3c5cef477607293ed02e6d1b77f8f6f834f50fe2e9d05`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ae1339c87c4e759ff4a439ee8561a8481ea3131678ac5e2f58795506cb67fc`  
		Last Modified: Tue, 29 Mar 2022 12:06:38 GMT  
		Size: 6.0 MB (5966913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda9f112e9f42cfee9c6890693553b623bf2dd540c36f29ad14276acb22e044e`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ba00100ccbdece1902154d0d0d33ee3d70d4e184a6524a97b6ab7e2e53192`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:64df6483fac24c84ea4b5e9aec2d1c7dea0fb0f87a580f62c5ce01eff3a0adb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63789e395c9f230480e13fc49b3e9d594c93e077d747286874da11ec3961534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 00:17:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 19 Mar 2022 00:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 00:17:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 19 Mar 2022 00:17:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 00:18:00 GMT
VOLUME [/spiped]
# Sat, 19 Mar 2022 00:18:00 GMT
WORKDIR /spiped
# Sat, 19 Mar 2022 00:18:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 19 Mar 2022 00:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 00:18:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d94b024c830eb06047521525e6e80bed68148c75e03f53e9bc6fafa1075fbd`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d328e20862ea7e51f93bfb276fa99c6ecc53281333745ff3a811d84dc06af`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d11157c6c90d4f995b8e2b9478e1edea768653c860e008067edeb3a948299e`  
		Last Modified: Sat, 19 Mar 2022 00:19:37 GMT  
		Size: 4.7 MB (4747424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0020ef6e30c3643a1fda82b192c9979c157a532ea7f3062c052170a412e8543`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42887a9feb0c929ff8eb501d91b2d8ee08fc2fe05b96eb5a361902803b4cfa1`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:7bf4cc6d7160264b61ad5339a1b254c94c216125bf624adbb4a44b1a484a71b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40283723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e193db912bc32b089a793405a8541f1cb6d938b1dad5dc81b749bdb791619efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:43:59 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 10:44:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:44:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 10:44:25 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:26 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c323dcf632c3e6c78229ea96b201cd5c6a73598a208ba2fd88a55a2e53f6a`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 1.6 KB (1611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b0c52bcbc80dacdfd452f5135ca2e640ab57050b38fbf5890ca41339ce8cbf`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e273d1baff760d787e4bf5a3e20801cf5a8e2625eada853a4d7cdd86c1e25f`  
		Last Modified: Tue, 29 Mar 2022 10:45:20 GMT  
		Size: 7.9 MB (7891233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7f99497ff10c89ef5d937c4f127f94bcc0391017c3fa45d587bab079706dea`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bb3d200b36c323a0edaaa6ceb5990790f17562ef9d5e5c63d7fab6d1978d51`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:169edc440f22e80e02a4bea8bc4674fadb4add62123485ec46abaaf37f7e4cd0
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
$ docker pull spiped@sha256:d6e6dcfa6086494057f5f26469b25640bf3a9218b6cc4e845e510f611ffa60f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeba803d4f72b630a199361799d83475c4f2faaf4727b042f4dae3eab17cc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:06:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 12:06:13 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 12:06:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 12:06:23 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:23 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e2f649ba68890eb48b23f0629d3f0bebfad8591eededff7d1bebbea5d2c299`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9d24f2037910ca67089823983115eada5364357a69d3debbb44877fa797d9`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dbbc9dfedadaeb9831ec97ca27a4c042f24c707f35418fcb5e658ac718d4b2`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 214.9 KB (214880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca650d236223d767382cf22a1841bc16d8b4d27ac027dff84b481bd8b1f3ed09`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901204d6acb74fe11b3b5004cdfd8be4d3e9d9cbab4ceeeb099898ff581d0388`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:ae66fb10272b529530524084a214a11e65777dff6517d5a90d71357e60416246
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9a0570520cf722d24d3a84685d936a04a06d1b8e35de44be52daca29219ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:24:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 08:24:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 08:24:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 08:25:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 08:25:01 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 08:25:02 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 08:25:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:25:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc4ea1012b3262fa7706463586c4d41a0cf0a329238cbe52ea6d03bfbc07fae`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5659ae5d68adc8e4012f07c665ea352c4068ee821e83350f8bc165b6aea5583`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 7.8 KB (7774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf4925cebf49f63997a8c7389e423c3623dc4cd2e6c701e4282c664293e789b`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 199.2 KB (199158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac1b140b33266f585c96310939c5cdbac7bde1fcbc0bd4e8cde9f9f0dd5171`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b13e602bdbc874391ee6aee0f8abffe1e74ee57061d9e1faed46aa76ad44a0`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:189afc1c68703cff284e0c131d8d15c9c681d14a4542ddaf2c94693f232decc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ea0583224ba3af43c489fca633bcb591704ff4ee8d4cc17c4c606062389b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:14:52 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:14:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:14:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:15:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:15:13 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:15:14 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:15:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:15:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf5bdaf7a39a22f20503724a23944505c99126d9af994be53508ccc71c16eef`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40ed26b860753759abe491128ce51dbc0afdbc0cef72b3008dd2e524328df6`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99502b872eb38bf1f4dfc80216174c88c1d79d9cfb8c5abbc39917c0302aad`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 192.7 KB (192697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe098a5d357775ae0a8f18cb457fc9fd6b78d74aa6a76cee1416c0e170ccbacb`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5c27b0616f94be998b0bc78862d22586f0954d06bd7b91579d0d4b0358b624`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:5cf3bd78a417eef72a40bb5edc9f92fed7ee69c81ab9138a296beace753358e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdd5340762815a30efbd053fa60da4fe70e2b3c3db902bbce3eaf767667273e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 09:01:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 09:01:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 09:01:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 09:01:49 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 09:01:50 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 09:01:51 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 09:01:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 09:01:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 09:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463ad34ca3404a7db4e6dd575191b4296a912966781d5a403c539b4eaabfaaa2`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c512da9db190273a558923e74154dcce0aa8a0aef851adacdb31f943a15b61a`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f89501c409388621c3858647d0561c88144396b234207d41183ea9b2c6d28cc`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 207.2 KB (207229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ac9ba6c1d80bc4b7f2e1200df7698544bacf092b7d9e4c3e5eb89727f0d29`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249793a4f1201a6c5d84af7e93a06f803235fc07aa5a0adfb7cc7c91a236da28`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:768b79c1223f706478b3a0032c22112401fed0957e0cf316ba94683ee1ca7f36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a79e381a48f0dd00366b8a561ef5f702f1a5b4d8602eb791f1546c342911984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:32 GMT
ADD file:8d3b249cd4cd9b2fb1888f3efcc06d39c2f56b4c25257ecee645c1be0146f7fd in / 
# Tue, 29 Mar 2022 00:38:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:44:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 10:44:37 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 10:44:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 10:44:49 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:50 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:134f45dc6b904419acf27b9807970f271117691bc67b963b86de8965db932175`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 2.8 MB (2818926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b625a1ed487cfd98e806f31bc703a892a97d07f2a33c1657ad981d1072ba7f`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02845a45e1b2d5e8e499c956acc9795a048bca98576e02146f9eff14e6cecadf`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8cfab4e949c3e8dd9bcd7085b355b7ffd0167d5edfeffb931188144796b6b3`  
		Last Modified: Tue, 29 Mar 2022 10:45:38 GMT  
		Size: 225.4 KB (225419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7240d8e736fdc883bfc41a6ac79d6b16dbf424902f57637e76a57fc498daac`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5efcabfa8c561598869530135704b6302072794ecaaefe3cd2dff77e472af47`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3be6b11628019b8721551bcf42c3628c18c5ebdf340fb4078ece32b04e3127f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee6dcc472c36cf06945f815fb375fb17abbae162627a0bd9dae5cf9133ecf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:07:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:07:50 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:07:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:08:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:08:26 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:08:32 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:08:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:08:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81fc1468fcd0131d8000ddca3f44590fd14dfc35a9d912b6170011625bb5d8`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2287dd028ebee5d32aa4a025c7b7b3a9581671b877d8dac77525d5fcd74a648d`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 7.8 KB (7777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17c6d0a7d2e755d69202f2f313acd078d23cb1c5b140e708c86415dd093fa77`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 213.2 KB (213156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703007a36f936093de72f883ca3fa13de75df9286c761faef8935fe24910611f`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177f5f3c5ff6aa152c39236251b7ef5c8bf8bfcd9e24018c594d0837df55baf1`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:08c9db0fd409954398950249ab06e3475f408492d13e410c744ac05ef51ae71f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a610690959c677ecf4d87758d7555b8d94f304fe07e12639fd8b4baa0eb1056b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 22:05:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 23 Mar 2022 22:05:07 GMT
RUN apk add --no-cache libssl1.1
# Wed, 23 Mar 2022 22:05:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 23 Mar 2022 22:05:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 23 Mar 2022 22:05:12 GMT
VOLUME [/spiped]
# Wed, 23 Mar 2022 22:05:13 GMT
WORKDIR /spiped
# Wed, 23 Mar 2022 22:05:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 22:05:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de9b32a530d2ed90d0d2d66ec15e1aab12ba49f665ebed744593f9db9ade5f2`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7923d88ed9b87a2e84d74a28fa0f739b1c89a7c47eae042cadef2e340675ec`  
		Last Modified: Wed, 23 Mar 2022 22:05:38 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480a9c67a03f618e1ec73ac6b01f498501d9ccd5c45ec0b01a2b7b78e06653b1`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3697b4be3f3a9608a66911a63c16ce80dd128576b3f0ef447b71eaf43285047`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3607e6465da6c7df76ce5b46bc7dca3f9887226ee9d195bb0e25f5d2cb5ee`  
		Last Modified: Wed, 23 Mar 2022 22:05:40 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:460c7c717a55f8dd8e41ef1de3e7d16cd01f3f22aa7d53bc4a0634edb5769fa9
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
$ docker pull spiped@sha256:f236fca971a0526aa22ab4aa69709d302210d7e1f5bd42902bde2803ec0495bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37348627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab54c336e542bbe2bacf29196b05876f18889ca6f79cd1c223af52a9bcf3241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 12:05:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 12:05:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 12:05:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 12:06:07 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:07 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda024001dd8419f652d3fde717d37b32c648032cc3f92d00978db9268a65b97`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55c823e9d54047194e3c5cef477607293ed02e6d1b77f8f6f834f50fe2e9d05`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ae1339c87c4e759ff4a439ee8561a8481ea3131678ac5e2f58795506cb67fc`  
		Last Modified: Tue, 29 Mar 2022 12:06:38 GMT  
		Size: 6.0 MB (5966913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda9f112e9f42cfee9c6890693553b623bf2dd540c36f29ad14276acb22e044e`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ba00100ccbdece1902154d0d0d33ee3d70d4e184a6524a97b6ab7e2e53192`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:64df6483fac24c84ea4b5e9aec2d1c7dea0fb0f87a580f62c5ce01eff3a0adb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63789e395c9f230480e13fc49b3e9d594c93e077d747286874da11ec3961534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 00:17:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 19 Mar 2022 00:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 00:17:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 19 Mar 2022 00:17:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 00:18:00 GMT
VOLUME [/spiped]
# Sat, 19 Mar 2022 00:18:00 GMT
WORKDIR /spiped
# Sat, 19 Mar 2022 00:18:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 19 Mar 2022 00:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 00:18:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d94b024c830eb06047521525e6e80bed68148c75e03f53e9bc6fafa1075fbd`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d328e20862ea7e51f93bfb276fa99c6ecc53281333745ff3a811d84dc06af`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d11157c6c90d4f995b8e2b9478e1edea768653c860e008067edeb3a948299e`  
		Last Modified: Sat, 19 Mar 2022 00:19:37 GMT  
		Size: 4.7 MB (4747424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0020ef6e30c3643a1fda82b192c9979c157a532ea7f3062c052170a412e8543`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42887a9feb0c929ff8eb501d91b2d8ee08fc2fe05b96eb5a361902803b4cfa1`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:7bf4cc6d7160264b61ad5339a1b254c94c216125bf624adbb4a44b1a484a71b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40283723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e193db912bc32b089a793405a8541f1cb6d938b1dad5dc81b749bdb791619efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:43:59 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 10:44:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:44:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 10:44:25 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:26 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c323dcf632c3e6c78229ea96b201cd5c6a73598a208ba2fd88a55a2e53f6a`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 1.6 KB (1611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b0c52bcbc80dacdfd452f5135ca2e640ab57050b38fbf5890ca41339ce8cbf`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e273d1baff760d787e4bf5a3e20801cf5a8e2625eada853a4d7cdd86c1e25f`  
		Last Modified: Tue, 29 Mar 2022 10:45:20 GMT  
		Size: 7.9 MB (7891233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7f99497ff10c89ef5d937c4f127f94bcc0391017c3fa45d587bab079706dea`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bb3d200b36c323a0edaaa6ceb5990790f17562ef9d5e5c63d7fab6d1978d51`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:169edc440f22e80e02a4bea8bc4674fadb4add62123485ec46abaaf37f7e4cd0
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
$ docker pull spiped@sha256:d6e6dcfa6086494057f5f26469b25640bf3a9218b6cc4e845e510f611ffa60f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeba803d4f72b630a199361799d83475c4f2faaf4727b042f4dae3eab17cc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:06:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 12:06:13 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 12:06:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 12:06:23 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:23 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e2f649ba68890eb48b23f0629d3f0bebfad8591eededff7d1bebbea5d2c299`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9d24f2037910ca67089823983115eada5364357a69d3debbb44877fa797d9`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dbbc9dfedadaeb9831ec97ca27a4c042f24c707f35418fcb5e658ac718d4b2`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 214.9 KB (214880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca650d236223d767382cf22a1841bc16d8b4d27ac027dff84b481bd8b1f3ed09`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901204d6acb74fe11b3b5004cdfd8be4d3e9d9cbab4ceeeb099898ff581d0388`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:ae66fb10272b529530524084a214a11e65777dff6517d5a90d71357e60416246
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9a0570520cf722d24d3a84685d936a04a06d1b8e35de44be52daca29219ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:24:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 08:24:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 08:24:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 08:25:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 08:25:01 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 08:25:02 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 08:25:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:25:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc4ea1012b3262fa7706463586c4d41a0cf0a329238cbe52ea6d03bfbc07fae`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5659ae5d68adc8e4012f07c665ea352c4068ee821e83350f8bc165b6aea5583`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 7.8 KB (7774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf4925cebf49f63997a8c7389e423c3623dc4cd2e6c701e4282c664293e789b`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 199.2 KB (199158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac1b140b33266f585c96310939c5cdbac7bde1fcbc0bd4e8cde9f9f0dd5171`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b13e602bdbc874391ee6aee0f8abffe1e74ee57061d9e1faed46aa76ad44a0`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:189afc1c68703cff284e0c131d8d15c9c681d14a4542ddaf2c94693f232decc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ea0583224ba3af43c489fca633bcb591704ff4ee8d4cc17c4c606062389b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:14:52 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:14:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:14:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:15:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:15:13 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:15:14 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:15:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:15:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf5bdaf7a39a22f20503724a23944505c99126d9af994be53508ccc71c16eef`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40ed26b860753759abe491128ce51dbc0afdbc0cef72b3008dd2e524328df6`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99502b872eb38bf1f4dfc80216174c88c1d79d9cfb8c5abbc39917c0302aad`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 192.7 KB (192697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe098a5d357775ae0a8f18cb457fc9fd6b78d74aa6a76cee1416c0e170ccbacb`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5c27b0616f94be998b0bc78862d22586f0954d06bd7b91579d0d4b0358b624`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:5cf3bd78a417eef72a40bb5edc9f92fed7ee69c81ab9138a296beace753358e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdd5340762815a30efbd053fa60da4fe70e2b3c3db902bbce3eaf767667273e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 09:01:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 09:01:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 09:01:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 09:01:49 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 09:01:50 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 09:01:51 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 09:01:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 09:01:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 09:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463ad34ca3404a7db4e6dd575191b4296a912966781d5a403c539b4eaabfaaa2`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c512da9db190273a558923e74154dcce0aa8a0aef851adacdb31f943a15b61a`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f89501c409388621c3858647d0561c88144396b234207d41183ea9b2c6d28cc`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 207.2 KB (207229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ac9ba6c1d80bc4b7f2e1200df7698544bacf092b7d9e4c3e5eb89727f0d29`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249793a4f1201a6c5d84af7e93a06f803235fc07aa5a0adfb7cc7c91a236da28`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:768b79c1223f706478b3a0032c22112401fed0957e0cf316ba94683ee1ca7f36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a79e381a48f0dd00366b8a561ef5f702f1a5b4d8602eb791f1546c342911984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:32 GMT
ADD file:8d3b249cd4cd9b2fb1888f3efcc06d39c2f56b4c25257ecee645c1be0146f7fd in / 
# Tue, 29 Mar 2022 00:38:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:44:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 10:44:37 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 10:44:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 10:44:49 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:50 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:134f45dc6b904419acf27b9807970f271117691bc67b963b86de8965db932175`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 2.8 MB (2818926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b625a1ed487cfd98e806f31bc703a892a97d07f2a33c1657ad981d1072ba7f`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02845a45e1b2d5e8e499c956acc9795a048bca98576e02146f9eff14e6cecadf`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8cfab4e949c3e8dd9bcd7085b355b7ffd0167d5edfeffb931188144796b6b3`  
		Last Modified: Tue, 29 Mar 2022 10:45:38 GMT  
		Size: 225.4 KB (225419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7240d8e736fdc883bfc41a6ac79d6b16dbf424902f57637e76a57fc498daac`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5efcabfa8c561598869530135704b6302072794ecaaefe3cd2dff77e472af47`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3be6b11628019b8721551bcf42c3628c18c5ebdf340fb4078ece32b04e3127f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee6dcc472c36cf06945f815fb375fb17abbae162627a0bd9dae5cf9133ecf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:07:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:07:50 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:07:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:08:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:08:26 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:08:32 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:08:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:08:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81fc1468fcd0131d8000ddca3f44590fd14dfc35a9d912b6170011625bb5d8`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2287dd028ebee5d32aa4a025c7b7b3a9581671b877d8dac77525d5fcd74a648d`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 7.8 KB (7777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17c6d0a7d2e755d69202f2f313acd078d23cb1c5b140e708c86415dd093fa77`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 213.2 KB (213156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703007a36f936093de72f883ca3fa13de75df9286c761faef8935fe24910611f`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177f5f3c5ff6aa152c39236251b7ef5c8bf8bfcd9e24018c594d0837df55baf1`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:08c9db0fd409954398950249ab06e3475f408492d13e410c744ac05ef51ae71f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a610690959c677ecf4d87758d7555b8d94f304fe07e12639fd8b4baa0eb1056b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 22:05:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 23 Mar 2022 22:05:07 GMT
RUN apk add --no-cache libssl1.1
# Wed, 23 Mar 2022 22:05:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 23 Mar 2022 22:05:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 23 Mar 2022 22:05:12 GMT
VOLUME [/spiped]
# Wed, 23 Mar 2022 22:05:13 GMT
WORKDIR /spiped
# Wed, 23 Mar 2022 22:05:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 22:05:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de9b32a530d2ed90d0d2d66ec15e1aab12ba49f665ebed744593f9db9ade5f2`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7923d88ed9b87a2e84d74a28fa0f739b1c89a7c47eae042cadef2e340675ec`  
		Last Modified: Wed, 23 Mar 2022 22:05:38 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480a9c67a03f618e1ec73ac6b01f498501d9ccd5c45ec0b01a2b7b78e06653b1`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3697b4be3f3a9608a66911a63c16ce80dd128576b3f0ef447b71eaf43285047`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3607e6465da6c7df76ce5b46bc7dca3f9887226ee9d195bb0e25f5d2cb5ee`  
		Last Modified: Wed, 23 Mar 2022 22:05:40 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:460c7c717a55f8dd8e41ef1de3e7d16cd01f3f22aa7d53bc4a0634edb5769fa9
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
$ docker pull spiped@sha256:f236fca971a0526aa22ab4aa69709d302210d7e1f5bd42902bde2803ec0495bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37348627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab54c336e542bbe2bacf29196b05876f18889ca6f79cd1c223af52a9bcf3241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 12:05:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 12:05:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 12:05:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 12:06:07 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:07 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda024001dd8419f652d3fde717d37b32c648032cc3f92d00978db9268a65b97`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55c823e9d54047194e3c5cef477607293ed02e6d1b77f8f6f834f50fe2e9d05`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ae1339c87c4e759ff4a439ee8561a8481ea3131678ac5e2f58795506cb67fc`  
		Last Modified: Tue, 29 Mar 2022 12:06:38 GMT  
		Size: 6.0 MB (5966913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda9f112e9f42cfee9c6890693553b623bf2dd540c36f29ad14276acb22e044e`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ba00100ccbdece1902154d0d0d33ee3d70d4e184a6524a97b6ab7e2e53192`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:64df6483fac24c84ea4b5e9aec2d1c7dea0fb0f87a580f62c5ce01eff3a0adb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63789e395c9f230480e13fc49b3e9d594c93e077d747286874da11ec3961534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 00:17:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 19 Mar 2022 00:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 00:17:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 19 Mar 2022 00:17:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 00:18:00 GMT
VOLUME [/spiped]
# Sat, 19 Mar 2022 00:18:00 GMT
WORKDIR /spiped
# Sat, 19 Mar 2022 00:18:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 19 Mar 2022 00:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 00:18:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d94b024c830eb06047521525e6e80bed68148c75e03f53e9bc6fafa1075fbd`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d328e20862ea7e51f93bfb276fa99c6ecc53281333745ff3a811d84dc06af`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d11157c6c90d4f995b8e2b9478e1edea768653c860e008067edeb3a948299e`  
		Last Modified: Sat, 19 Mar 2022 00:19:37 GMT  
		Size: 4.7 MB (4747424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0020ef6e30c3643a1fda82b192c9979c157a532ea7f3062c052170a412e8543`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42887a9feb0c929ff8eb501d91b2d8ee08fc2fe05b96eb5a361902803b4cfa1`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:7bf4cc6d7160264b61ad5339a1b254c94c216125bf624adbb4a44b1a484a71b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40283723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e193db912bc32b089a793405a8541f1cb6d938b1dad5dc81b749bdb791619efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:43:59 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 10:44:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:44:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 10:44:25 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:26 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c323dcf632c3e6c78229ea96b201cd5c6a73598a208ba2fd88a55a2e53f6a`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 1.6 KB (1611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b0c52bcbc80dacdfd452f5135ca2e640ab57050b38fbf5890ca41339ce8cbf`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e273d1baff760d787e4bf5a3e20801cf5a8e2625eada853a4d7cdd86c1e25f`  
		Last Modified: Tue, 29 Mar 2022 10:45:20 GMT  
		Size: 7.9 MB (7891233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7f99497ff10c89ef5d937c4f127f94bcc0391017c3fa45d587bab079706dea`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bb3d200b36c323a0edaaa6ceb5990790f17562ef9d5e5c63d7fab6d1978d51`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:169edc440f22e80e02a4bea8bc4674fadb4add62123485ec46abaaf37f7e4cd0
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
$ docker pull spiped@sha256:d6e6dcfa6086494057f5f26469b25640bf3a9218b6cc4e845e510f611ffa60f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeba803d4f72b630a199361799d83475c4f2faaf4727b042f4dae3eab17cc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:06:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 12:06:13 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 12:06:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 12:06:23 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:23 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e2f649ba68890eb48b23f0629d3f0bebfad8591eededff7d1bebbea5d2c299`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9d24f2037910ca67089823983115eada5364357a69d3debbb44877fa797d9`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dbbc9dfedadaeb9831ec97ca27a4c042f24c707f35418fcb5e658ac718d4b2`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 214.9 KB (214880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca650d236223d767382cf22a1841bc16d8b4d27ac027dff84b481bd8b1f3ed09`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901204d6acb74fe11b3b5004cdfd8be4d3e9d9cbab4ceeeb099898ff581d0388`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:ae66fb10272b529530524084a214a11e65777dff6517d5a90d71357e60416246
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9a0570520cf722d24d3a84685d936a04a06d1b8e35de44be52daca29219ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:24:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 08:24:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 08:24:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 08:25:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 08:25:01 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 08:25:02 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 08:25:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:25:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc4ea1012b3262fa7706463586c4d41a0cf0a329238cbe52ea6d03bfbc07fae`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5659ae5d68adc8e4012f07c665ea352c4068ee821e83350f8bc165b6aea5583`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 7.8 KB (7774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf4925cebf49f63997a8c7389e423c3623dc4cd2e6c701e4282c664293e789b`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 199.2 KB (199158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac1b140b33266f585c96310939c5cdbac7bde1fcbc0bd4e8cde9f9f0dd5171`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b13e602bdbc874391ee6aee0f8abffe1e74ee57061d9e1faed46aa76ad44a0`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:189afc1c68703cff284e0c131d8d15c9c681d14a4542ddaf2c94693f232decc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ea0583224ba3af43c489fca633bcb591704ff4ee8d4cc17c4c606062389b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:14:52 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:14:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:14:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:15:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:15:13 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:15:14 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:15:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:15:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf5bdaf7a39a22f20503724a23944505c99126d9af994be53508ccc71c16eef`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40ed26b860753759abe491128ce51dbc0afdbc0cef72b3008dd2e524328df6`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99502b872eb38bf1f4dfc80216174c88c1d79d9cfb8c5abbc39917c0302aad`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 192.7 KB (192697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe098a5d357775ae0a8f18cb457fc9fd6b78d74aa6a76cee1416c0e170ccbacb`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5c27b0616f94be998b0bc78862d22586f0954d06bd7b91579d0d4b0358b624`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:5cf3bd78a417eef72a40bb5edc9f92fed7ee69c81ab9138a296beace753358e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdd5340762815a30efbd053fa60da4fe70e2b3c3db902bbce3eaf767667273e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 09:01:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 09:01:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 09:01:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 09:01:49 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 09:01:50 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 09:01:51 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 09:01:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 09:01:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 09:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463ad34ca3404a7db4e6dd575191b4296a912966781d5a403c539b4eaabfaaa2`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c512da9db190273a558923e74154dcce0aa8a0aef851adacdb31f943a15b61a`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f89501c409388621c3858647d0561c88144396b234207d41183ea9b2c6d28cc`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 207.2 KB (207229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ac9ba6c1d80bc4b7f2e1200df7698544bacf092b7d9e4c3e5eb89727f0d29`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249793a4f1201a6c5d84af7e93a06f803235fc07aa5a0adfb7cc7c91a236da28`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:768b79c1223f706478b3a0032c22112401fed0957e0cf316ba94683ee1ca7f36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a79e381a48f0dd00366b8a561ef5f702f1a5b4d8602eb791f1546c342911984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:32 GMT
ADD file:8d3b249cd4cd9b2fb1888f3efcc06d39c2f56b4c25257ecee645c1be0146f7fd in / 
# Tue, 29 Mar 2022 00:38:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:44:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 10:44:37 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 10:44:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 10:44:49 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:50 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:134f45dc6b904419acf27b9807970f271117691bc67b963b86de8965db932175`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 2.8 MB (2818926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b625a1ed487cfd98e806f31bc703a892a97d07f2a33c1657ad981d1072ba7f`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02845a45e1b2d5e8e499c956acc9795a048bca98576e02146f9eff14e6cecadf`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8cfab4e949c3e8dd9bcd7085b355b7ffd0167d5edfeffb931188144796b6b3`  
		Last Modified: Tue, 29 Mar 2022 10:45:38 GMT  
		Size: 225.4 KB (225419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7240d8e736fdc883bfc41a6ac79d6b16dbf424902f57637e76a57fc498daac`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5efcabfa8c561598869530135704b6302072794ecaaefe3cd2dff77e472af47`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3be6b11628019b8721551bcf42c3628c18c5ebdf340fb4078ece32b04e3127f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee6dcc472c36cf06945f815fb375fb17abbae162627a0bd9dae5cf9133ecf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:07:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:07:50 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:07:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:08:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:08:26 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:08:32 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:08:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:08:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81fc1468fcd0131d8000ddca3f44590fd14dfc35a9d912b6170011625bb5d8`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2287dd028ebee5d32aa4a025c7b7b3a9581671b877d8dac77525d5fcd74a648d`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 7.8 KB (7777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17c6d0a7d2e755d69202f2f313acd078d23cb1c5b140e708c86415dd093fa77`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 213.2 KB (213156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703007a36f936093de72f883ca3fa13de75df9286c761faef8935fe24910611f`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177f5f3c5ff6aa152c39236251b7ef5c8bf8bfcd9e24018c594d0837df55baf1`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:08c9db0fd409954398950249ab06e3475f408492d13e410c744ac05ef51ae71f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a610690959c677ecf4d87758d7555b8d94f304fe07e12639fd8b4baa0eb1056b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 22:05:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 23 Mar 2022 22:05:07 GMT
RUN apk add --no-cache libssl1.1
# Wed, 23 Mar 2022 22:05:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 23 Mar 2022 22:05:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 23 Mar 2022 22:05:12 GMT
VOLUME [/spiped]
# Wed, 23 Mar 2022 22:05:13 GMT
WORKDIR /spiped
# Wed, 23 Mar 2022 22:05:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 22:05:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de9b32a530d2ed90d0d2d66ec15e1aab12ba49f665ebed744593f9db9ade5f2`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7923d88ed9b87a2e84d74a28fa0f739b1c89a7c47eae042cadef2e340675ec`  
		Last Modified: Wed, 23 Mar 2022 22:05:38 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480a9c67a03f618e1ec73ac6b01f498501d9ccd5c45ec0b01a2b7b78e06653b1`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3697b4be3f3a9608a66911a63c16ce80dd128576b3f0ef447b71eaf43285047`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3607e6465da6c7df76ce5b46bc7dca3f9887226ee9d195bb0e25f5d2cb5ee`  
		Last Modified: Wed, 23 Mar 2022 22:05:40 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:169edc440f22e80e02a4bea8bc4674fadb4add62123485ec46abaaf37f7e4cd0
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
$ docker pull spiped@sha256:d6e6dcfa6086494057f5f26469b25640bf3a9218b6cc4e845e510f611ffa60f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeba803d4f72b630a199361799d83475c4f2faaf4727b042f4dae3eab17cc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:06:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 12:06:13 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 12:06:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 12:06:23 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:23 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e2f649ba68890eb48b23f0629d3f0bebfad8591eededff7d1bebbea5d2c299`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9d24f2037910ca67089823983115eada5364357a69d3debbb44877fa797d9`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dbbc9dfedadaeb9831ec97ca27a4c042f24c707f35418fcb5e658ac718d4b2`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 214.9 KB (214880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca650d236223d767382cf22a1841bc16d8b4d27ac027dff84b481bd8b1f3ed09`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901204d6acb74fe11b3b5004cdfd8be4d3e9d9cbab4ceeeb099898ff581d0388`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:ae66fb10272b529530524084a214a11e65777dff6517d5a90d71357e60416246
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9a0570520cf722d24d3a84685d936a04a06d1b8e35de44be52daca29219ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:24:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 08:24:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 08:24:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 08:25:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 08:25:01 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 08:25:02 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 08:25:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:25:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc4ea1012b3262fa7706463586c4d41a0cf0a329238cbe52ea6d03bfbc07fae`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5659ae5d68adc8e4012f07c665ea352c4068ee821e83350f8bc165b6aea5583`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 7.8 KB (7774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf4925cebf49f63997a8c7389e423c3623dc4cd2e6c701e4282c664293e789b`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 199.2 KB (199158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac1b140b33266f585c96310939c5cdbac7bde1fcbc0bd4e8cde9f9f0dd5171`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b13e602bdbc874391ee6aee0f8abffe1e74ee57061d9e1faed46aa76ad44a0`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:189afc1c68703cff284e0c131d8d15c9c681d14a4542ddaf2c94693f232decc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ea0583224ba3af43c489fca633bcb591704ff4ee8d4cc17c4c606062389b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:14:52 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:14:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:14:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:15:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:15:13 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:15:14 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:15:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:15:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf5bdaf7a39a22f20503724a23944505c99126d9af994be53508ccc71c16eef`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40ed26b860753759abe491128ce51dbc0afdbc0cef72b3008dd2e524328df6`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99502b872eb38bf1f4dfc80216174c88c1d79d9cfb8c5abbc39917c0302aad`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 192.7 KB (192697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe098a5d357775ae0a8f18cb457fc9fd6b78d74aa6a76cee1416c0e170ccbacb`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5c27b0616f94be998b0bc78862d22586f0954d06bd7b91579d0d4b0358b624`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:5cf3bd78a417eef72a40bb5edc9f92fed7ee69c81ab9138a296beace753358e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdd5340762815a30efbd053fa60da4fe70e2b3c3db902bbce3eaf767667273e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 09:01:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 09:01:39 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 09:01:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 09:01:49 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 09:01:50 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 09:01:51 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 09:01:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 09:01:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 09:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463ad34ca3404a7db4e6dd575191b4296a912966781d5a403c539b4eaabfaaa2`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c512da9db190273a558923e74154dcce0aa8a0aef851adacdb31f943a15b61a`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f89501c409388621c3858647d0561c88144396b234207d41183ea9b2c6d28cc`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 207.2 KB (207229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ac9ba6c1d80bc4b7f2e1200df7698544bacf092b7d9e4c3e5eb89727f0d29`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249793a4f1201a6c5d84af7e93a06f803235fc07aa5a0adfb7cc7c91a236da28`  
		Last Modified: Thu, 24 Mar 2022 09:02:20 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:768b79c1223f706478b3a0032c22112401fed0957e0cf316ba94683ee1ca7f36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a79e381a48f0dd00366b8a561ef5f702f1a5b4d8602eb791f1546c342911984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:32 GMT
ADD file:8d3b249cd4cd9b2fb1888f3efcc06d39c2f56b4c25257ecee645c1be0146f7fd in / 
# Tue, 29 Mar 2022 00:38:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:44:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 10:44:37 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 10:44:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 10:44:49 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:50 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:134f45dc6b904419acf27b9807970f271117691bc67b963b86de8965db932175`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 2.8 MB (2818926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b625a1ed487cfd98e806f31bc703a892a97d07f2a33c1657ad981d1072ba7f`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02845a45e1b2d5e8e499c956acc9795a048bca98576e02146f9eff14e6cecadf`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8cfab4e949c3e8dd9bcd7085b355b7ffd0167d5edfeffb931188144796b6b3`  
		Last Modified: Tue, 29 Mar 2022 10:45:38 GMT  
		Size: 225.4 KB (225419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7240d8e736fdc883bfc41a6ac79d6b16dbf424902f57637e76a57fc498daac`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5efcabfa8c561598869530135704b6302072794ecaaefe3cd2dff77e472af47`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3be6b11628019b8721551bcf42c3628c18c5ebdf340fb4078ece32b04e3127f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee6dcc472c36cf06945f815fb375fb17abbae162627a0bd9dae5cf9133ecf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:07:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:07:50 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:07:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:08:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:08:26 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:08:32 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:08:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:08:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:08:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81fc1468fcd0131d8000ddca3f44590fd14dfc35a9d912b6170011625bb5d8`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2287dd028ebee5d32aa4a025c7b7b3a9581671b877d8dac77525d5fcd74a648d`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 7.8 KB (7777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17c6d0a7d2e755d69202f2f313acd078d23cb1c5b140e708c86415dd093fa77`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 213.2 KB (213156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703007a36f936093de72f883ca3fa13de75df9286c761faef8935fe24910611f`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177f5f3c5ff6aa152c39236251b7ef5c8bf8bfcd9e24018c594d0837df55baf1`  
		Last Modified: Thu, 24 Mar 2022 03:09:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:08c9db0fd409954398950249ab06e3475f408492d13e410c744ac05ef51ae71f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a610690959c677ecf4d87758d7555b8d94f304fe07e12639fd8b4baa0eb1056b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 22:05:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 23 Mar 2022 22:05:07 GMT
RUN apk add --no-cache libssl1.1
# Wed, 23 Mar 2022 22:05:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 23 Mar 2022 22:05:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 23 Mar 2022 22:05:12 GMT
VOLUME [/spiped]
# Wed, 23 Mar 2022 22:05:13 GMT
WORKDIR /spiped
# Wed, 23 Mar 2022 22:05:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 22:05:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de9b32a530d2ed90d0d2d66ec15e1aab12ba49f665ebed744593f9db9ade5f2`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7923d88ed9b87a2e84d74a28fa0f739b1c89a7c47eae042cadef2e340675ec`  
		Last Modified: Wed, 23 Mar 2022 22:05:38 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480a9c67a03f618e1ec73ac6b01f498501d9ccd5c45ec0b01a2b7b78e06653b1`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3697b4be3f3a9608a66911a63c16ce80dd128576b3f0ef447b71eaf43285047`  
		Last Modified: Wed, 23 Mar 2022 22:05:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3607e6465da6c7df76ce5b46bc7dca3f9887226ee9d195bb0e25f5d2cb5ee`  
		Last Modified: Wed, 23 Mar 2022 22:05:40 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:460c7c717a55f8dd8e41ef1de3e7d16cd01f3f22aa7d53bc4a0634edb5769fa9
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
$ docker pull spiped@sha256:f236fca971a0526aa22ab4aa69709d302210d7e1f5bd42902bde2803ec0495bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37348627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab54c336e542bbe2bacf29196b05876f18889ca6f79cd1c223af52a9bcf3241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 12:05:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 12:05:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 12:05:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 12:06:07 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:07 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda024001dd8419f652d3fde717d37b32c648032cc3f92d00978db9268a65b97`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55c823e9d54047194e3c5cef477607293ed02e6d1b77f8f6f834f50fe2e9d05`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ae1339c87c4e759ff4a439ee8561a8481ea3131678ac5e2f58795506cb67fc`  
		Last Modified: Tue, 29 Mar 2022 12:06:38 GMT  
		Size: 6.0 MB (5966913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda9f112e9f42cfee9c6890693553b623bf2dd540c36f29ad14276acb22e044e`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ba00100ccbdece1902154d0d0d33ee3d70d4e184a6524a97b6ab7e2e53192`  
		Last Modified: Tue, 29 Mar 2022 12:06:37 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:64df6483fac24c84ea4b5e9aec2d1c7dea0fb0f87a580f62c5ce01eff3a0adb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63789e395c9f230480e13fc49b3e9d594c93e077d747286874da11ec3961534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 00:17:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 19 Mar 2022 00:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 00:17:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 19 Mar 2022 00:17:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 00:18:00 GMT
VOLUME [/spiped]
# Sat, 19 Mar 2022 00:18:00 GMT
WORKDIR /spiped
# Sat, 19 Mar 2022 00:18:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 19 Mar 2022 00:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 00:18:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d94b024c830eb06047521525e6e80bed68148c75e03f53e9bc6fafa1075fbd`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d328e20862ea7e51f93bfb276fa99c6ecc53281333745ff3a811d84dc06af`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d11157c6c90d4f995b8e2b9478e1edea768653c860e008067edeb3a948299e`  
		Last Modified: Sat, 19 Mar 2022 00:19:37 GMT  
		Size: 4.7 MB (4747424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0020ef6e30c3643a1fda82b192c9979c157a532ea7f3062c052170a412e8543`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42887a9feb0c929ff8eb501d91b2d8ee08fc2fe05b96eb5a361902803b4cfa1`  
		Last Modified: Sat, 19 Mar 2022 00:19:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:7bf4cc6d7160264b61ad5339a1b254c94c216125bf624adbb4a44b1a484a71b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40283723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e193db912bc32b089a793405a8541f1cb6d938b1dad5dc81b749bdb791619efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:43:59 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 29 Mar 2022 10:44:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:44:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 10:44:25 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:26 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c323dcf632c3e6c78229ea96b201cd5c6a73598a208ba2fd88a55a2e53f6a`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 1.6 KB (1611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b0c52bcbc80dacdfd452f5135ca2e640ab57050b38fbf5890ca41339ce8cbf`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e273d1baff760d787e4bf5a3e20801cf5a8e2625eada853a4d7cdd86c1e25f`  
		Last Modified: Tue, 29 Mar 2022 10:45:20 GMT  
		Size: 7.9 MB (7891233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7f99497ff10c89ef5d937c4f127f94bcc0391017c3fa45d587bab079706dea`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bb3d200b36c323a0edaaa6ceb5990790f17562ef9d5e5c63d7fab6d1978d51`  
		Last Modified: Tue, 29 Mar 2022 10:45:19 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
