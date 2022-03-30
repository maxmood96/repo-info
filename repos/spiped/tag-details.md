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
$ docker pull spiped@sha256:2e14bed1f0f5c488b645227d87390860b8f165d5bf1b71886cf4f2aab66c06b8
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
$ docker pull spiped@sha256:94736a8efc0da3dd2c4c38b0a356b70873aee616c541dbccdfa95068dc6c0cb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb46d52c65a3d3391adc84884f180419a0f9437774a897d2ba90ecff46cb1cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:37 GMT
ADD file:6b9a30e6ef50a46e87cf9d7f5a491c7951fdb6dd6fab3c9d4a9c3c40f92b8db4 in / 
# Tue, 29 Mar 2022 00:50:38 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:08:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:09:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:09:32 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:09:32 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:09:33 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:09:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a41aba0a099ec129c20f41f6370b97daa4c3d4d3edc76ea1863bc5f76f9e5e5`  
		Last Modified: Tue, 29 Mar 2022 01:05:21 GMT  
		Size: 28.9 MB (28920513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd77f21f54e947717641dc9eb4a3c32a321dd3df6f615e082da0d916f9c6ca`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6a8e69828bdad8405be855d17ef3331b8093c3773b6a6ed726e8788cc3fe1`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e672a3f91acf51a5b4252fc7a5e23c4bd9539029d819fafe90af13149b18a97`  
		Last Modified: Wed, 30 Mar 2022 01:10:12 GMT  
		Size: 5.0 MB (5027710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11475c4da412af9a0208f5a0962e32a7bd674a732fc2cb1bd58a16deb9aac2e4`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adba7e3a404697c9d1e15fe08cfbb357d8dd16b877a299ca347781afd782675`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
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
$ docker pull spiped@sha256:489251bdbc8f5a1d43cb461dba8917af4fb58142240f15e7d2c7c31f7d859b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bead5c7928697f7d3aded01a859186f595bedcb48737aebb29d40d92c78230e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:01:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:01:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:01:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:01:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:01:58 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:01:59 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1c5ff6bd12cad4539ef42aba72b9e2a79fd5e03cf703d178e9179cf3ca28d3`  
		Last Modified: Wed, 30 Mar 2022 01:03:05 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32807b7cfbcaf6c5dda896ed26a7d5b103161f8237a6f762874f9d2e713509`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc810f776215aefbbbcac36475250c8768eea0d0fdb5cdeceb3a2ed84c8dbb8`  
		Last Modified: Wed, 30 Mar 2022 01:03:06 GMT  
		Size: 5.3 MB (5270525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1419d96420314f5d538869ef6bf4d3e349c952c254f754fba1e39a0ba1a36c`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533163ce32b9d79dc658ade7a26d7f71cece5b9bf114cc7b7dc3596ba66609ba`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:bc909d5eeee60c7823173755c87467307f944145474e127199afc7d15643b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34845094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0bcec57634c726f934b24b28bf162da99aacbf72dd089108346ddd627e4284`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:17:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 02:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:17:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:17:29 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:29 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9488a45de61a7c26b2a863c250a52839737d409c8bac0426e2161131489985d3`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abedbd8409757c2b32910d965e11e1ba2d29a16105361932d6d8bd82b611d64d`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eb1d8925fb8e4d0edc85c85b1f0d782db61bdf479a93bc6a0ccd97410d5a81`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 5.2 MB (5186412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987418a0dc4bd8525c7ad87f10f5f7ca2fdd8060ac0807f66714351df3d27cc`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3647b49ea4318215c86c777031179b0cacb01790a04d0208a9d80a7962bb5768`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:a18aa63bc7e9407d82c82d106ac1bfe2eb7704c4a0273c76ad74c4dc64d125fd
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
$ docker pull spiped@sha256:c0d28956af21c9ad7d0e3d4cf972b301ea28efa0c8755d1ee62841b09754b0ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11675ed63f0f0f4c5e2d5175c06bade440268d204f7a4b104eba50db3f998da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 01:02:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 01:02:15 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 01:02:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:02:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 01:02:35 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:02:36 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef7ee2c7f3dc7bcaf9752a844248d8127145ffd675ae5de72b4be177fc37cd5`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c53830f06d1a108ac255dbff68c71fabc58723d0a42943fec7681cbebe653a`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1f94f19caf7b781c37e261530b5861447ecd5ab33d55ad4d2f12a932db1cf8`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 207.2 KB (207237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b259955a7b787ff533a05f42050e5172ba829db902cac41506236e30a45be04e`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29db0547b8fb18568f5c6616a8622211952741a2a93da0e86cb506b1ee4c941c`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
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
$ docker pull spiped@sha256:c25c47af1a6bc11637de15ec17dad117ad78343cf7347c265f1e56f0e4b3a414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2811657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97239b742fae078cff3e290263aa752534ee95461d5f5a32fd585ee92dcdf5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:32 GMT
ADD file:75e6f1cb0cdf63de14d99f8419ce47d61e295300299c18b08bd484dff0da4e93 in / 
# Tue, 29 Mar 2022 00:41:32 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 02:17:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 02:17:37 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 02:17:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 02:17:43 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:43 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c33ece150b7a4954636e49b807bdf240c422de7a78f45728d2fcdb7c96d14a3`  
		Last Modified: Tue, 29 Mar 2022 00:44:03 GMT  
		Size: 2.6 MB (2600441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e144ceffef75cc7c2c1c03a85a5beb968414bdf4a4c7bf32a7e80bb4867085`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8228374fcc60d9ce3f830403b582c951b61d5f290da2cdc5d46470960e122`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7189dcfd4895b30653e04d921ea51db9d3cf616a80caef0b9eb4b2a478a0a0`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 201.7 KB (201697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24add8a228de11738a6e3ffc4d1659680ba2a1ea46ecd69f23ae7d8cfb62cc17`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925172ba0226c4330bc068f3815476dbdb5a96c19ef9cdf4f7a51be59fd06c63`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:2e14bed1f0f5c488b645227d87390860b8f165d5bf1b71886cf4f2aab66c06b8
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
$ docker pull spiped@sha256:94736a8efc0da3dd2c4c38b0a356b70873aee616c541dbccdfa95068dc6c0cb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb46d52c65a3d3391adc84884f180419a0f9437774a897d2ba90ecff46cb1cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:37 GMT
ADD file:6b9a30e6ef50a46e87cf9d7f5a491c7951fdb6dd6fab3c9d4a9c3c40f92b8db4 in / 
# Tue, 29 Mar 2022 00:50:38 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:08:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:09:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:09:32 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:09:32 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:09:33 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:09:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a41aba0a099ec129c20f41f6370b97daa4c3d4d3edc76ea1863bc5f76f9e5e5`  
		Last Modified: Tue, 29 Mar 2022 01:05:21 GMT  
		Size: 28.9 MB (28920513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd77f21f54e947717641dc9eb4a3c32a321dd3df6f615e082da0d916f9c6ca`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6a8e69828bdad8405be855d17ef3331b8093c3773b6a6ed726e8788cc3fe1`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e672a3f91acf51a5b4252fc7a5e23c4bd9539029d819fafe90af13149b18a97`  
		Last Modified: Wed, 30 Mar 2022 01:10:12 GMT  
		Size: 5.0 MB (5027710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11475c4da412af9a0208f5a0962e32a7bd674a732fc2cb1bd58a16deb9aac2e4`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adba7e3a404697c9d1e15fe08cfbb357d8dd16b877a299ca347781afd782675`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
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
$ docker pull spiped@sha256:489251bdbc8f5a1d43cb461dba8917af4fb58142240f15e7d2c7c31f7d859b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bead5c7928697f7d3aded01a859186f595bedcb48737aebb29d40d92c78230e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:01:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:01:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:01:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:01:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:01:58 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:01:59 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1c5ff6bd12cad4539ef42aba72b9e2a79fd5e03cf703d178e9179cf3ca28d3`  
		Last Modified: Wed, 30 Mar 2022 01:03:05 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32807b7cfbcaf6c5dda896ed26a7d5b103161f8237a6f762874f9d2e713509`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc810f776215aefbbbcac36475250c8768eea0d0fdb5cdeceb3a2ed84c8dbb8`  
		Last Modified: Wed, 30 Mar 2022 01:03:06 GMT  
		Size: 5.3 MB (5270525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1419d96420314f5d538869ef6bf4d3e349c952c254f754fba1e39a0ba1a36c`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533163ce32b9d79dc658ade7a26d7f71cece5b9bf114cc7b7dc3596ba66609ba`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:bc909d5eeee60c7823173755c87467307f944145474e127199afc7d15643b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34845094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0bcec57634c726f934b24b28bf162da99aacbf72dd089108346ddd627e4284`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:17:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 02:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:17:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:17:29 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:29 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9488a45de61a7c26b2a863c250a52839737d409c8bac0426e2161131489985d3`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abedbd8409757c2b32910d965e11e1ba2d29a16105361932d6d8bd82b611d64d`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eb1d8925fb8e4d0edc85c85b1f0d782db61bdf479a93bc6a0ccd97410d5a81`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 5.2 MB (5186412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987418a0dc4bd8525c7ad87f10f5f7ca2fdd8060ac0807f66714351df3d27cc`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3647b49ea4318215c86c777031179b0cacb01790a04d0208a9d80a7962bb5768`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:a18aa63bc7e9407d82c82d106ac1bfe2eb7704c4a0273c76ad74c4dc64d125fd
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
$ docker pull spiped@sha256:c0d28956af21c9ad7d0e3d4cf972b301ea28efa0c8755d1ee62841b09754b0ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11675ed63f0f0f4c5e2d5175c06bade440268d204f7a4b104eba50db3f998da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 01:02:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 01:02:15 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 01:02:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:02:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 01:02:35 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:02:36 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef7ee2c7f3dc7bcaf9752a844248d8127145ffd675ae5de72b4be177fc37cd5`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c53830f06d1a108ac255dbff68c71fabc58723d0a42943fec7681cbebe653a`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1f94f19caf7b781c37e261530b5861447ecd5ab33d55ad4d2f12a932db1cf8`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 207.2 KB (207237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b259955a7b787ff533a05f42050e5172ba829db902cac41506236e30a45be04e`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29db0547b8fb18568f5c6616a8622211952741a2a93da0e86cb506b1ee4c941c`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
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
$ docker pull spiped@sha256:c25c47af1a6bc11637de15ec17dad117ad78343cf7347c265f1e56f0e4b3a414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2811657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97239b742fae078cff3e290263aa752534ee95461d5f5a32fd585ee92dcdf5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:32 GMT
ADD file:75e6f1cb0cdf63de14d99f8419ce47d61e295300299c18b08bd484dff0da4e93 in / 
# Tue, 29 Mar 2022 00:41:32 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 02:17:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 02:17:37 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 02:17:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 02:17:43 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:43 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c33ece150b7a4954636e49b807bdf240c422de7a78f45728d2fcdb7c96d14a3`  
		Last Modified: Tue, 29 Mar 2022 00:44:03 GMT  
		Size: 2.6 MB (2600441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e144ceffef75cc7c2c1c03a85a5beb968414bdf4a4c7bf32a7e80bb4867085`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8228374fcc60d9ce3f830403b582c951b61d5f290da2cdc5d46470960e122`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7189dcfd4895b30653e04d921ea51db9d3cf616a80caef0b9eb4b2a478a0a0`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 201.7 KB (201697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24add8a228de11738a6e3ffc4d1659680ba2a1ea46ecd69f23ae7d8cfb62cc17`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925172ba0226c4330bc068f3815476dbdb5a96c19ef9cdf4f7a51be59fd06c63`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:2e14bed1f0f5c488b645227d87390860b8f165d5bf1b71886cf4f2aab66c06b8
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
$ docker pull spiped@sha256:94736a8efc0da3dd2c4c38b0a356b70873aee616c541dbccdfa95068dc6c0cb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb46d52c65a3d3391adc84884f180419a0f9437774a897d2ba90ecff46cb1cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:37 GMT
ADD file:6b9a30e6ef50a46e87cf9d7f5a491c7951fdb6dd6fab3c9d4a9c3c40f92b8db4 in / 
# Tue, 29 Mar 2022 00:50:38 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:08:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:09:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:09:32 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:09:32 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:09:33 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:09:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a41aba0a099ec129c20f41f6370b97daa4c3d4d3edc76ea1863bc5f76f9e5e5`  
		Last Modified: Tue, 29 Mar 2022 01:05:21 GMT  
		Size: 28.9 MB (28920513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd77f21f54e947717641dc9eb4a3c32a321dd3df6f615e082da0d916f9c6ca`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6a8e69828bdad8405be855d17ef3331b8093c3773b6a6ed726e8788cc3fe1`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e672a3f91acf51a5b4252fc7a5e23c4bd9539029d819fafe90af13149b18a97`  
		Last Modified: Wed, 30 Mar 2022 01:10:12 GMT  
		Size: 5.0 MB (5027710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11475c4da412af9a0208f5a0962e32a7bd674a732fc2cb1bd58a16deb9aac2e4`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adba7e3a404697c9d1e15fe08cfbb357d8dd16b877a299ca347781afd782675`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
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
$ docker pull spiped@sha256:489251bdbc8f5a1d43cb461dba8917af4fb58142240f15e7d2c7c31f7d859b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bead5c7928697f7d3aded01a859186f595bedcb48737aebb29d40d92c78230e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:01:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:01:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:01:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:01:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:01:58 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:01:59 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1c5ff6bd12cad4539ef42aba72b9e2a79fd5e03cf703d178e9179cf3ca28d3`  
		Last Modified: Wed, 30 Mar 2022 01:03:05 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32807b7cfbcaf6c5dda896ed26a7d5b103161f8237a6f762874f9d2e713509`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc810f776215aefbbbcac36475250c8768eea0d0fdb5cdeceb3a2ed84c8dbb8`  
		Last Modified: Wed, 30 Mar 2022 01:03:06 GMT  
		Size: 5.3 MB (5270525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1419d96420314f5d538869ef6bf4d3e349c952c254f754fba1e39a0ba1a36c`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533163ce32b9d79dc658ade7a26d7f71cece5b9bf114cc7b7dc3596ba66609ba`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:bc909d5eeee60c7823173755c87467307f944145474e127199afc7d15643b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34845094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0bcec57634c726f934b24b28bf162da99aacbf72dd089108346ddd627e4284`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:17:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 02:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:17:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:17:29 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:29 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9488a45de61a7c26b2a863c250a52839737d409c8bac0426e2161131489985d3`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abedbd8409757c2b32910d965e11e1ba2d29a16105361932d6d8bd82b611d64d`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eb1d8925fb8e4d0edc85c85b1f0d782db61bdf479a93bc6a0ccd97410d5a81`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 5.2 MB (5186412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987418a0dc4bd8525c7ad87f10f5f7ca2fdd8060ac0807f66714351df3d27cc`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3647b49ea4318215c86c777031179b0cacb01790a04d0208a9d80a7962bb5768`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:a18aa63bc7e9407d82c82d106ac1bfe2eb7704c4a0273c76ad74c4dc64d125fd
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
$ docker pull spiped@sha256:c0d28956af21c9ad7d0e3d4cf972b301ea28efa0c8755d1ee62841b09754b0ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11675ed63f0f0f4c5e2d5175c06bade440268d204f7a4b104eba50db3f998da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 01:02:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 01:02:15 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 01:02:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:02:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 01:02:35 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:02:36 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef7ee2c7f3dc7bcaf9752a844248d8127145ffd675ae5de72b4be177fc37cd5`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c53830f06d1a108ac255dbff68c71fabc58723d0a42943fec7681cbebe653a`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1f94f19caf7b781c37e261530b5861447ecd5ab33d55ad4d2f12a932db1cf8`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 207.2 KB (207237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b259955a7b787ff533a05f42050e5172ba829db902cac41506236e30a45be04e`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29db0547b8fb18568f5c6616a8622211952741a2a93da0e86cb506b1ee4c941c`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
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
$ docker pull spiped@sha256:c25c47af1a6bc11637de15ec17dad117ad78343cf7347c265f1e56f0e4b3a414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2811657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97239b742fae078cff3e290263aa752534ee95461d5f5a32fd585ee92dcdf5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:32 GMT
ADD file:75e6f1cb0cdf63de14d99f8419ce47d61e295300299c18b08bd484dff0da4e93 in / 
# Tue, 29 Mar 2022 00:41:32 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 02:17:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 02:17:37 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 02:17:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 02:17:43 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:43 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c33ece150b7a4954636e49b807bdf240c422de7a78f45728d2fcdb7c96d14a3`  
		Last Modified: Tue, 29 Mar 2022 00:44:03 GMT  
		Size: 2.6 MB (2600441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e144ceffef75cc7c2c1c03a85a5beb968414bdf4a4c7bf32a7e80bb4867085`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8228374fcc60d9ce3f830403b582c951b61d5f290da2cdc5d46470960e122`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7189dcfd4895b30653e04d921ea51db9d3cf616a80caef0b9eb4b2a478a0a0`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 201.7 KB (201697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24add8a228de11738a6e3ffc4d1659680ba2a1ea46ecd69f23ae7d8cfb62cc17`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925172ba0226c4330bc068f3815476dbdb5a96c19ef9cdf4f7a51be59fd06c63`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:a18aa63bc7e9407d82c82d106ac1bfe2eb7704c4a0273c76ad74c4dc64d125fd
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
$ docker pull spiped@sha256:c0d28956af21c9ad7d0e3d4cf972b301ea28efa0c8755d1ee62841b09754b0ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11675ed63f0f0f4c5e2d5175c06bade440268d204f7a4b104eba50db3f998da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 01:02:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 01:02:15 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 01:02:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:02:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 01:02:35 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:02:36 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef7ee2c7f3dc7bcaf9752a844248d8127145ffd675ae5de72b4be177fc37cd5`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c53830f06d1a108ac255dbff68c71fabc58723d0a42943fec7681cbebe653a`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1f94f19caf7b781c37e261530b5861447ecd5ab33d55ad4d2f12a932db1cf8`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 207.2 KB (207237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b259955a7b787ff533a05f42050e5172ba829db902cac41506236e30a45be04e`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29db0547b8fb18568f5c6616a8622211952741a2a93da0e86cb506b1ee4c941c`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
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
$ docker pull spiped@sha256:c25c47af1a6bc11637de15ec17dad117ad78343cf7347c265f1e56f0e4b3a414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2811657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97239b742fae078cff3e290263aa752534ee95461d5f5a32fd585ee92dcdf5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:32 GMT
ADD file:75e6f1cb0cdf63de14d99f8419ce47d61e295300299c18b08bd484dff0da4e93 in / 
# Tue, 29 Mar 2022 00:41:32 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 02:17:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 02:17:37 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 02:17:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 02:17:43 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:43 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c33ece150b7a4954636e49b807bdf240c422de7a78f45728d2fcdb7c96d14a3`  
		Last Modified: Tue, 29 Mar 2022 00:44:03 GMT  
		Size: 2.6 MB (2600441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e144ceffef75cc7c2c1c03a85a5beb968414bdf4a4c7bf32a7e80bb4867085`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8228374fcc60d9ce3f830403b582c951b61d5f290da2cdc5d46470960e122`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7189dcfd4895b30653e04d921ea51db9d3cf616a80caef0b9eb4b2a478a0a0`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 201.7 KB (201697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24add8a228de11738a6e3ffc4d1659680ba2a1ea46ecd69f23ae7d8cfb62cc17`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925172ba0226c4330bc068f3815476dbdb5a96c19ef9cdf4f7a51be59fd06c63`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:2e14bed1f0f5c488b645227d87390860b8f165d5bf1b71886cf4f2aab66c06b8
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
$ docker pull spiped@sha256:94736a8efc0da3dd2c4c38b0a356b70873aee616c541dbccdfa95068dc6c0cb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33951476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb46d52c65a3d3391adc84884f180419a0f9437774a897d2ba90ecff46cb1cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:37 GMT
ADD file:6b9a30e6ef50a46e87cf9d7f5a491c7951fdb6dd6fab3c9d4a9c3c40f92b8db4 in / 
# Tue, 29 Mar 2022 00:50:38 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:08:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:08:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:08:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:09:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:09:32 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:09:32 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:09:33 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:09:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a41aba0a099ec129c20f41f6370b97daa4c3d4d3edc76ea1863bc5f76f9e5e5`  
		Last Modified: Tue, 29 Mar 2022 01:05:21 GMT  
		Size: 28.9 MB (28920513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd77f21f54e947717641dc9eb4a3c32a321dd3df6f615e082da0d916f9c6ca`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6a8e69828bdad8405be855d17ef3331b8093c3773b6a6ed726e8788cc3fe1`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e672a3f91acf51a5b4252fc7a5e23c4bd9539029d819fafe90af13149b18a97`  
		Last Modified: Wed, 30 Mar 2022 01:10:12 GMT  
		Size: 5.0 MB (5027710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11475c4da412af9a0208f5a0962e32a7bd674a732fc2cb1bd58a16deb9aac2e4`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adba7e3a404697c9d1e15fe08cfbb357d8dd16b877a299ca347781afd782675`  
		Last Modified: Wed, 30 Mar 2022 01:10:09 GMT  
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
$ docker pull spiped@sha256:489251bdbc8f5a1d43cb461dba8917af4fb58142240f15e7d2c7c31f7d859b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bead5c7928697f7d3aded01a859186f595bedcb48737aebb29d40d92c78230e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:01:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 01:01:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:01:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:01:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 01:01:58 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:01:59 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1c5ff6bd12cad4539ef42aba72b9e2a79fd5e03cf703d178e9179cf3ca28d3`  
		Last Modified: Wed, 30 Mar 2022 01:03:05 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32807b7cfbcaf6c5dda896ed26a7d5b103161f8237a6f762874f9d2e713509`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc810f776215aefbbbcac36475250c8768eea0d0fdb5cdeceb3a2ed84c8dbb8`  
		Last Modified: Wed, 30 Mar 2022 01:03:06 GMT  
		Size: 5.3 MB (5270525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1419d96420314f5d538869ef6bf4d3e349c952c254f754fba1e39a0ba1a36c`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533163ce32b9d79dc658ade7a26d7f71cece5b9bf114cc7b7dc3596ba66609ba`  
		Last Modified: Wed, 30 Mar 2022 01:03:04 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:bc909d5eeee60c7823173755c87467307f944145474e127199afc7d15643b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34845094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0bcec57634c726f934b24b28bf162da99aacbf72dd089108346ddd627e4284`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:17:13 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 30 Mar 2022 02:17:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:17:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:17:29 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:29 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9488a45de61a7c26b2a863c250a52839737d409c8bac0426e2161131489985d3`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abedbd8409757c2b32910d965e11e1ba2d29a16105361932d6d8bd82b611d64d`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eb1d8925fb8e4d0edc85c85b1f0d782db61bdf479a93bc6a0ccd97410d5a81`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 5.2 MB (5186412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987418a0dc4bd8525c7ad87f10f5f7ca2fdd8060ac0807f66714351df3d27cc`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3647b49ea4318215c86c777031179b0cacb01790a04d0208a9d80a7962bb5768`  
		Last Modified: Wed, 30 Mar 2022 02:18:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
