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
$ docker pull spiped@sha256:23f75f451120264e35f6fba4a2255e0d7c34c3fc14d8a1073eb3d9e76a48fbad
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
$ docker pull spiped@sha256:b9d410b612429c56c7bfc201428e054e133b3687a23c6ab56cdf78a8c9ad5c7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38188305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3c9d102eb55c2c6c87ed605fae08cffd0c4e04332b24fa0f37d59b2669e92c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:22:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:22:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:22:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:22:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:22:36 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:22:37 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:22:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:22:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e237e28b6c8479420ca602f6d9000c52b84b038600906da0b91c42da69a5a0`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4e443d4cd640e99746f86e1e59871a4ada3b96633f72d79fc6e6067891001`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 2.6 MB (2590190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3e1422a236883c466850e64011b55a1b56e0c81a9545cfcd117adabeaab6b`  
		Last Modified: Thu, 11 Jan 2024 15:22:54 GMT  
		Size: 6.5 MB (6470596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e9783f12fe977d3c3fb97f2140d152d4a266d13d7d695ee4bae14ef8aff1`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babb199a86c149623a233c7dfb363392a7e6cb2ab371278c984af637a5d902c6`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:48e3aec207f11f554d11f7cca3617dd0a20c63a99979dd52383f616781065e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34210288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6552c4cc72e079d96ac29b7b30f77891c4a148dd26b9214d8ad2127af31c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:56 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 11 Jan 2024 01:48:57 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:15:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:15:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:15:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:16:15 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:16:16 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:16:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:16:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:16:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efaf7aa15745e00ee1310cdd0c0a0fa04c9babc4b14f47a0511774e612c17cd`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef6770767dc97b364a92dd7e63c992849f75a389374a2b4a8e3d0b49171d840`  
		Last Modified: Thu, 11 Jan 2024 08:16:31 GMT  
		Size: 2.2 MB (2185812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9428fb70e931ef7456f037c3775b80a743f8c4408b0ba9e82f5b87746e30f8`  
		Last Modified: Thu, 11 Jan 2024 08:16:32 GMT  
		Size: 5.1 MB (5137399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8614ffef08a25ece6a906817bc2c8db1a70f645556aa00be2a766712227daa27`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7de8146f9a20caf7ce4138446d67ec581dda9f7a7c3b21a158483369b19f4`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:649e6cc2ba661d32ef4256888cb13271ddbd95f30b237e8cd364585d269f95db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31643371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7652136d8cffbe4332d3b1d5eaa62b715afbddf4f65d40febad02fd1ded6ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:48:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:48:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:48:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:49:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:49:26 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:49:26 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:49:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:49:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc0d0a8576d9a44d6b4db5cc4f97e623d6bacb291afeb35f258395422a17c9`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1370755c9f61f9d8e5787bcf44b8c87a1f8ef8d4a4fb06ed5b875241ab8bab`  
		Last Modified: Thu, 11 Jan 2024 19:49:43 GMT  
		Size: 2.0 MB (2044341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f48cde4d3929bef49e5aa54ffc6d3b24ff2928a8064474cd99d88cb6ae755ac`  
		Last Modified: Thu, 11 Jan 2024 19:49:44 GMT  
		Size: 4.9 MB (4879298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9101dc3ba57dc33cf3f5784dd33320028deb6a8acea5608535f35068eebe01`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818ec00e89763b0bbe261764ee08b7fc2e910fcaf1e1c6b97d9e014aeff02444`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8d46f6f1c78ff1ed0b3ad00a406bb7dfc11c6e39c7cc975822c2b6d102bd321c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37072116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76215eda00699b15fb0556eac76cf0a4af5d809749b14252b3334749d355379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:29:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:29:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:29:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:30:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:30:12 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:30:12 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:30:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:30:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a186769736ab6aafdd22af7f10d8e13a171d6f765babc242afde5b22f8e021`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89d5b689695e58a4b728e643310efd87f5b30b89d212f9f9805317e6d3d44e9`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 2.4 MB (2433129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20aa23ac8908dff126d96ec7cbe95309d0065002cc0f8ee4d20fe5be7294c11`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 5.5 MB (5480057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6694d2fbcae3e5b0c2c7144d4d8dd14321da5319438a3f43600f4a36b12f2977`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5fbb626e824adb903fbe948e55bd6c1a28321f09b5cf69f0a200ed25471de`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:fd98c9c853fa5a97230af82572ebcf43f560102c6df845a39886ad9916e747bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38673622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec415dd64331e77243cc53d1694750e9d873861a85647c362da7e4772d1852cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:14:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:14:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:14:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:14:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:14:35 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:14:35 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:14:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:14:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219d5afd5c80285ae297ac65047d682e4464a2bd13c5a0c40a0f9676f277503`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458658e0a88c324acd7e3779b7b9f2ef21f36e42bb8792755618eb54b652ad`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 2.6 MB (2586819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba0e8f8301c454ae49e2a06c26833a39423500fdea848c6a651431e4a7ffce`  
		Last Modified: Thu, 11 Jan 2024 15:14:52 GMT  
		Size: 5.9 MB (5941327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029a95a90cc76ed338c96fdbde9b3f8d8ae82fed8ed0638510a92e3cf2d53ee`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d585163d11cdefbc4f1aeed2629cd1f7d42248657db82a57065d9e9fd199f5`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:8df4224500ebe6450955a361308a1477c405408c15fb18d78898367e96485845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36760029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608deccb69dd65cd1c30cfd92453f4110bfc407cb5eb90dea9359191bb51cd23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:46 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 11 Jan 2024 02:11:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:27:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:28:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:28:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:29:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:29:54 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:29:56 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:29:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:30:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd46628fd7683deb3e871331ca13e13a6a6b9f52e2b95664db3553ace5976072`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c440be7820b7f425d0f7805d8d998ba570bfe049ee58308256c53d7a4634cd`  
		Last Modified: Thu, 11 Jan 2024 19:30:22 GMT  
		Size: 1.8 MB (1834348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c992cb9fa388c0602093f4e7132009ce8dfa69d8b130db629e8c6827c1a6c5fc`  
		Last Modified: Thu, 11 Jan 2024 19:30:25 GMT  
		Size: 5.8 MB (5802770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ab8ad9c391168c89ebd0d8a1b2a01525859846b1f624563d7f17567f5a14a`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42164cb6fcc44321ff95e388bc7616373edf4d0c24d377f2285040857a541b4`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:764b7df81dd7d86333ce5b7ca92010d23c2f3fc9c2d7dd13246be720993c2793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42313200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f14ae01ad7b8f3c003b12fbe2d899c5f4d8826a3abb0316ab4d31a9529a54fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:33:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:33:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 07:34:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 07:34:23 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 07:34:23 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 07:34:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:34:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ade73c36eccaaf1b719e4716d382e7a04b8d35d90350d3123d7a93d1137b54`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ccd0557a9cfbb9b7fd784f33b8cce1b87b02442b0536344db386a6c050e49`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 2.8 MB (2769149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4da6798029b0cbbf11779f41a9dc4093b5d0e4955383a8792705ad5f712e14`  
		Last Modified: Thu, 11 Jan 2024 07:34:39 GMT  
		Size: 6.4 MB (6421918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f5df5b7e161aec8d718577a51f297f7f7c55d711cfbf0e6d04f3a9a21c1944`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2770c2c06e8d52033f213a8302837f4f3fe92c7b17e4ee50393ffb59f18daa`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:8460c43f50154dd2d81bcda32d49c1b2630492b81af7f6ef4234aa08d8ca6da1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35138721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96298ac6187d2c17e9ec5cd018bbbd064f59ad841cd21041e96356b347daaeda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:31:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:31:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:31:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:31:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:31:43 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:31:43 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:31:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:31:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:31:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc7df99d6feb97fc1b8c09e7cc15ed28a5c2044d90959ca6282d2e594155ba`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507bb72a5f4749be5f3b6839f7a19c8ad385c1010d7976be3eff7eb3d2b64d`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 2.3 MB (2260721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f29ec00eafde08f306e88d5c35bd960026ebbda97f7bd077a98d77b533efd`  
		Last Modified: Thu, 11 Jan 2024 08:32:08 GMT  
		Size: 5.4 MB (5384555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aebe89a49f2a8cfc48fac744b77c973d1991772b665f667bd7b22c50a2c5a3`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fed5b84874c5eb13bdb5054962a3292a66b05ff968423c916a0ea686dc5195`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:73c463bbbd5f620dbb1aa0ab91b6f7973c8579ba6d720f3642f9b1550c8cca95
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
$ docker pull spiped@sha256:bbcb559f4d5d2f95adfeef51c918f2c078dcf991b30279a34be08e7614eda451
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e068a31dc93f7fbe323b521ca3e2dce275263b1eb366f065ef43b018191ac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:00:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 06:00:04 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 06:00:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 06:00:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 06:00:14 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 06:00:14 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 06:00:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 06:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc456d15d6c4f02d60102c7538cc196adfd3073fa382d3a6c9410c2acfa02238`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac40e9085148fd6ad0718c4bb551770cb399db60f6d9e0e6ae11e2af695afc`  
		Last Modified: Fri, 01 Dec 2023 06:00:26 GMT  
		Size: 1.4 MB (1433002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b55d95977f08a50d321f83fd17bb10e943234260c0d005d9596170d5ef3941b`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fa71cb099a874587efb2d18cba67b14c33ca2472939d01c1695f39e969163c`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1429def50f578086adeafeb1154a9f6683ab8f11715a60a8a1b321413c7c7f38`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:56621f2fd5b22773d7a82548848c99caa44d7526774fccbff6db3e6cf6e2ed7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc63c886e4bd1a4b9a2c5f65cb983191d831e4c5e90b709a27b7ad0468306b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 11:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 11:13:49 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 11:13:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 11:13:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 11:13:57 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 11:13:57 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 11:13:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 11:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c3d326b144045f9766875844acf4350469a75b0a68c61aab0f7ff911f87c40`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39220be7b9073c1b18c05a3956edc927bf596eaf0d654d7b0056fd406cb2a9d9`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.2 MB (1236778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2272caa48ca2695c3ee259c5049bda74ac674fc0349ffce0eb63c15cbcfb373b`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103f3bdb7f64e2684703c5f2a8310fa523b4b883c094984d24a0953897db969`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af16d05b1bfd95db714b4710e950d578ad3ded205b96654b373384e99c72a64`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e20e033984b23e87d819762aa3be4ac888c7573b1fe380a37edc231668cabab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75811072665665f41fe5fd77242815ccd7ba1ada919ff4d133df4c010228f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:09:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:09:14 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:09:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:09:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:09:21 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:09:21 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:09:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:09:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776ef4d306aa7de299bd8db61e455d766a093b7f593b4cb003b7c7436d79d6b`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80582de4f02357b676b2af9cdb5e56aa702680fd50254af56c20b451949c4efb`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.2 MB (1163890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4fd5daf33693bf1e78930cd893f86c3b358b42b11140bad181d50be0636580`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 199.5 KB (199547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a963f13cfdeafcdd2c65f6a266762a0e9f1679aeba08b0ebe2f515f4188753`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfc83b30d29a5ba12424db7d486ed08e84ab517be2c9518f1cde49bb01a6853`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b7bbfd15a130193c126e6305dde27ab1f812b1bde9bcdce939a472c991928997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a827ded63ac80140d8297b83d5b15fbe600917d04d811f7a104d5a81a45446f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:28:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:28:42 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:28:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:28:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:28:50 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:28:50 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:28:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:28:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a00b6b0251227c993c68fbac4ca61cbf6db9b390d4c9dfe2a005132c2c753`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c1951c258ad0eb59a0d4d33d432578b0760a47bef312a1e5bf8cccf477f47`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.4 MB (1362693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733da67e58e7549c947540df4ff581a3d9297a816340ca183083f623809e34bc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 215.7 KB (215687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f459526992eea15e16c15645ca376ef0435b204fc518f1fc404a1a1e2ebec6fc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a81f75355f25a9bd668c3d651a02f8124af05c3fa0dfb1e2265074389ca80`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:f975a9f3d41c92bff597add76b603827306ff8055d25df0b20f1186aa29b952c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c779ff3e48cf1e88a23dff62390543e9e2ab6c1b75a812f8d5dfa915323f58d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:03:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:03:26 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:03:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:03:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:03:39 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:03:39 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:03:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:03:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:03:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1d22c178557ad5427b2e2e39899f1ac5e8a7d3cbdbccccd75d44ef6c2ac2a`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f618f916fa34a39758083d0aea4bb87b1a9ac184745b09c642b66a0771671`  
		Last Modified: Fri, 01 Dec 2023 09:03:53 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88db827583d93974059d468003fccdeccfdcd9a21fc15a9286c04d5162b60f00`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 231.6 KB (231631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75849bdf81842f9eff8ef36f098d4df3977533d63126bd042ce3dbf0feb91482`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b858156e16033fc7497c09956fac005c37a0f152b38074431dd9e5bf0d25ce`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:81cf97596c96bf2c8a7f16eec43b20e866143ae03a0cf8161f1f48263918269c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86b6487c29a72435af58323fd6eb163641668280416e87e7ee28eb55ea2b72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:20:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:20:58 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:21:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:21:15 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:21:19 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:21:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:21:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:21:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9351f6531fdc8fd4540a86dac5a66a5860f3985ed2e1e145f0eefecf312a4fc0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041f2592c836041c592a462e184775818c484807025efe56ec1473d2b13465d0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.4 MB (1361751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f71b1afe6f19e25c6412567f2ad476a7153baa201b4d75943e2cf9a041475`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 220.0 KB (220038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b30773a6064abc0c64614a42aca7bb8a0357867cd6ff0810d45240ab0de638`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edff0700419d6610c5b04cf162c75c7bccadfc322ab5c27f670963d1e7b1165`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:f8bed32d8fdba1fdb13b94080f008c65343ad2b3f05ae4cfffa6668cbe5eb52d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c98b6934770e5e69df9564d2c52b9f16c900aa31148984cc7a432c75a5f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:48:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 08:48:25 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 08:48:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 08:48:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 08:48:31 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 08:48:31 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 08:48:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 08:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:48:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b69c2be0d2e048804506af3efc37e709bf98661c409d99087d1184f0304631`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae960024d613c1bc136f3ae0b33c9fa92f11bdf496d5a2a40fe6c46f1132e06f`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.2 MB (1221481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1ec3a08579d63b87f03caf7152bed9ee8fda71ebaa41c5f0565b423dd6ec1`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 208.6 KB (208647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613853307ecba30c7c7f935ec69ed6aab0e74d6f261598b8e3504b156232c4ef`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c380a4795962e93d6ce5552fe1957ccbb666076846f911fe97fc8aa3b9513ec`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:23f75f451120264e35f6fba4a2255e0d7c34c3fc14d8a1073eb3d9e76a48fbad
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
$ docker pull spiped@sha256:b9d410b612429c56c7bfc201428e054e133b3687a23c6ab56cdf78a8c9ad5c7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38188305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3c9d102eb55c2c6c87ed605fae08cffd0c4e04332b24fa0f37d59b2669e92c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:22:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:22:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:22:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:22:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:22:36 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:22:37 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:22:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:22:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e237e28b6c8479420ca602f6d9000c52b84b038600906da0b91c42da69a5a0`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4e443d4cd640e99746f86e1e59871a4ada3b96633f72d79fc6e6067891001`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 2.6 MB (2590190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3e1422a236883c466850e64011b55a1b56e0c81a9545cfcd117adabeaab6b`  
		Last Modified: Thu, 11 Jan 2024 15:22:54 GMT  
		Size: 6.5 MB (6470596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e9783f12fe977d3c3fb97f2140d152d4a266d13d7d695ee4bae14ef8aff1`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babb199a86c149623a233c7dfb363392a7e6cb2ab371278c984af637a5d902c6`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:48e3aec207f11f554d11f7cca3617dd0a20c63a99979dd52383f616781065e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34210288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6552c4cc72e079d96ac29b7b30f77891c4a148dd26b9214d8ad2127af31c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:56 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 11 Jan 2024 01:48:57 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:15:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:15:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:15:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:16:15 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:16:16 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:16:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:16:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:16:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efaf7aa15745e00ee1310cdd0c0a0fa04c9babc4b14f47a0511774e612c17cd`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef6770767dc97b364a92dd7e63c992849f75a389374a2b4a8e3d0b49171d840`  
		Last Modified: Thu, 11 Jan 2024 08:16:31 GMT  
		Size: 2.2 MB (2185812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9428fb70e931ef7456f037c3775b80a743f8c4408b0ba9e82f5b87746e30f8`  
		Last Modified: Thu, 11 Jan 2024 08:16:32 GMT  
		Size: 5.1 MB (5137399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8614ffef08a25ece6a906817bc2c8db1a70f645556aa00be2a766712227daa27`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7de8146f9a20caf7ce4138446d67ec581dda9f7a7c3b21a158483369b19f4`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:649e6cc2ba661d32ef4256888cb13271ddbd95f30b237e8cd364585d269f95db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31643371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7652136d8cffbe4332d3b1d5eaa62b715afbddf4f65d40febad02fd1ded6ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:48:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:48:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:48:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:49:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:49:26 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:49:26 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:49:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:49:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc0d0a8576d9a44d6b4db5cc4f97e623d6bacb291afeb35f258395422a17c9`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1370755c9f61f9d8e5787bcf44b8c87a1f8ef8d4a4fb06ed5b875241ab8bab`  
		Last Modified: Thu, 11 Jan 2024 19:49:43 GMT  
		Size: 2.0 MB (2044341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f48cde4d3929bef49e5aa54ffc6d3b24ff2928a8064474cd99d88cb6ae755ac`  
		Last Modified: Thu, 11 Jan 2024 19:49:44 GMT  
		Size: 4.9 MB (4879298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9101dc3ba57dc33cf3f5784dd33320028deb6a8acea5608535f35068eebe01`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818ec00e89763b0bbe261764ee08b7fc2e910fcaf1e1c6b97d9e014aeff02444`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8d46f6f1c78ff1ed0b3ad00a406bb7dfc11c6e39c7cc975822c2b6d102bd321c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37072116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76215eda00699b15fb0556eac76cf0a4af5d809749b14252b3334749d355379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:29:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:29:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:29:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:30:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:30:12 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:30:12 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:30:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:30:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a186769736ab6aafdd22af7f10d8e13a171d6f765babc242afde5b22f8e021`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89d5b689695e58a4b728e643310efd87f5b30b89d212f9f9805317e6d3d44e9`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 2.4 MB (2433129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20aa23ac8908dff126d96ec7cbe95309d0065002cc0f8ee4d20fe5be7294c11`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 5.5 MB (5480057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6694d2fbcae3e5b0c2c7144d4d8dd14321da5319438a3f43600f4a36b12f2977`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5fbb626e824adb903fbe948e55bd6c1a28321f09b5cf69f0a200ed25471de`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:fd98c9c853fa5a97230af82572ebcf43f560102c6df845a39886ad9916e747bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38673622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec415dd64331e77243cc53d1694750e9d873861a85647c362da7e4772d1852cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:14:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:14:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:14:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:14:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:14:35 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:14:35 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:14:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:14:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219d5afd5c80285ae297ac65047d682e4464a2bd13c5a0c40a0f9676f277503`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458658e0a88c324acd7e3779b7b9f2ef21f36e42bb8792755618eb54b652ad`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 2.6 MB (2586819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba0e8f8301c454ae49e2a06c26833a39423500fdea848c6a651431e4a7ffce`  
		Last Modified: Thu, 11 Jan 2024 15:14:52 GMT  
		Size: 5.9 MB (5941327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029a95a90cc76ed338c96fdbde9b3f8d8ae82fed8ed0638510a92e3cf2d53ee`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d585163d11cdefbc4f1aeed2629cd1f7d42248657db82a57065d9e9fd199f5`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:8df4224500ebe6450955a361308a1477c405408c15fb18d78898367e96485845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36760029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608deccb69dd65cd1c30cfd92453f4110bfc407cb5eb90dea9359191bb51cd23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:46 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 11 Jan 2024 02:11:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:27:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:28:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:28:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:29:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:29:54 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:29:56 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:29:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:30:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd46628fd7683deb3e871331ca13e13a6a6b9f52e2b95664db3553ace5976072`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c440be7820b7f425d0f7805d8d998ba570bfe049ee58308256c53d7a4634cd`  
		Last Modified: Thu, 11 Jan 2024 19:30:22 GMT  
		Size: 1.8 MB (1834348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c992cb9fa388c0602093f4e7132009ce8dfa69d8b130db629e8c6827c1a6c5fc`  
		Last Modified: Thu, 11 Jan 2024 19:30:25 GMT  
		Size: 5.8 MB (5802770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ab8ad9c391168c89ebd0d8a1b2a01525859846b1f624563d7f17567f5a14a`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42164cb6fcc44321ff95e388bc7616373edf4d0c24d377f2285040857a541b4`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:764b7df81dd7d86333ce5b7ca92010d23c2f3fc9c2d7dd13246be720993c2793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42313200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f14ae01ad7b8f3c003b12fbe2d899c5f4d8826a3abb0316ab4d31a9529a54fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:33:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:33:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 07:34:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 07:34:23 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 07:34:23 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 07:34:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:34:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ade73c36eccaaf1b719e4716d382e7a04b8d35d90350d3123d7a93d1137b54`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ccd0557a9cfbb9b7fd784f33b8cce1b87b02442b0536344db386a6c050e49`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 2.8 MB (2769149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4da6798029b0cbbf11779f41a9dc4093b5d0e4955383a8792705ad5f712e14`  
		Last Modified: Thu, 11 Jan 2024 07:34:39 GMT  
		Size: 6.4 MB (6421918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f5df5b7e161aec8d718577a51f297f7f7c55d711cfbf0e6d04f3a9a21c1944`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2770c2c06e8d52033f213a8302837f4f3fe92c7b17e4ee50393ffb59f18daa`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:8460c43f50154dd2d81bcda32d49c1b2630492b81af7f6ef4234aa08d8ca6da1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35138721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96298ac6187d2c17e9ec5cd018bbbd064f59ad841cd21041e96356b347daaeda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:31:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:31:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:31:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:31:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:31:43 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:31:43 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:31:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:31:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:31:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc7df99d6feb97fc1b8c09e7cc15ed28a5c2044d90959ca6282d2e594155ba`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507bb72a5f4749be5f3b6839f7a19c8ad385c1010d7976be3eff7eb3d2b64d`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 2.3 MB (2260721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f29ec00eafde08f306e88d5c35bd960026ebbda97f7bd077a98d77b533efd`  
		Last Modified: Thu, 11 Jan 2024 08:32:08 GMT  
		Size: 5.4 MB (5384555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aebe89a49f2a8cfc48fac744b77c973d1991772b665f667bd7b22c50a2c5a3`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fed5b84874c5eb13bdb5054962a3292a66b05ff968423c916a0ea686dc5195`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:73c463bbbd5f620dbb1aa0ab91b6f7973c8579ba6d720f3642f9b1550c8cca95
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
$ docker pull spiped@sha256:bbcb559f4d5d2f95adfeef51c918f2c078dcf991b30279a34be08e7614eda451
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e068a31dc93f7fbe323b521ca3e2dce275263b1eb366f065ef43b018191ac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:00:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 06:00:04 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 06:00:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 06:00:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 06:00:14 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 06:00:14 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 06:00:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 06:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc456d15d6c4f02d60102c7538cc196adfd3073fa382d3a6c9410c2acfa02238`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac40e9085148fd6ad0718c4bb551770cb399db60f6d9e0e6ae11e2af695afc`  
		Last Modified: Fri, 01 Dec 2023 06:00:26 GMT  
		Size: 1.4 MB (1433002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b55d95977f08a50d321f83fd17bb10e943234260c0d005d9596170d5ef3941b`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fa71cb099a874587efb2d18cba67b14c33ca2472939d01c1695f39e969163c`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1429def50f578086adeafeb1154a9f6683ab8f11715a60a8a1b321413c7c7f38`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:56621f2fd5b22773d7a82548848c99caa44d7526774fccbff6db3e6cf6e2ed7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc63c886e4bd1a4b9a2c5f65cb983191d831e4c5e90b709a27b7ad0468306b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 11:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 11:13:49 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 11:13:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 11:13:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 11:13:57 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 11:13:57 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 11:13:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 11:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c3d326b144045f9766875844acf4350469a75b0a68c61aab0f7ff911f87c40`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39220be7b9073c1b18c05a3956edc927bf596eaf0d654d7b0056fd406cb2a9d9`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.2 MB (1236778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2272caa48ca2695c3ee259c5049bda74ac674fc0349ffce0eb63c15cbcfb373b`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103f3bdb7f64e2684703c5f2a8310fa523b4b883c094984d24a0953897db969`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af16d05b1bfd95db714b4710e950d578ad3ded205b96654b373384e99c72a64`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e20e033984b23e87d819762aa3be4ac888c7573b1fe380a37edc231668cabab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75811072665665f41fe5fd77242815ccd7ba1ada919ff4d133df4c010228f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:09:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:09:14 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:09:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:09:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:09:21 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:09:21 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:09:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:09:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776ef4d306aa7de299bd8db61e455d766a093b7f593b4cb003b7c7436d79d6b`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80582de4f02357b676b2af9cdb5e56aa702680fd50254af56c20b451949c4efb`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.2 MB (1163890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4fd5daf33693bf1e78930cd893f86c3b358b42b11140bad181d50be0636580`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 199.5 KB (199547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a963f13cfdeafcdd2c65f6a266762a0e9f1679aeba08b0ebe2f515f4188753`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfc83b30d29a5ba12424db7d486ed08e84ab517be2c9518f1cde49bb01a6853`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b7bbfd15a130193c126e6305dde27ab1f812b1bde9bcdce939a472c991928997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a827ded63ac80140d8297b83d5b15fbe600917d04d811f7a104d5a81a45446f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:28:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:28:42 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:28:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:28:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:28:50 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:28:50 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:28:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:28:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a00b6b0251227c993c68fbac4ca61cbf6db9b390d4c9dfe2a005132c2c753`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c1951c258ad0eb59a0d4d33d432578b0760a47bef312a1e5bf8cccf477f47`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.4 MB (1362693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733da67e58e7549c947540df4ff581a3d9297a816340ca183083f623809e34bc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 215.7 KB (215687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f459526992eea15e16c15645ca376ef0435b204fc518f1fc404a1a1e2ebec6fc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a81f75355f25a9bd668c3d651a02f8124af05c3fa0dfb1e2265074389ca80`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:f975a9f3d41c92bff597add76b603827306ff8055d25df0b20f1186aa29b952c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c779ff3e48cf1e88a23dff62390543e9e2ab6c1b75a812f8d5dfa915323f58d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:03:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:03:26 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:03:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:03:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:03:39 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:03:39 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:03:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:03:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:03:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1d22c178557ad5427b2e2e39899f1ac5e8a7d3cbdbccccd75d44ef6c2ac2a`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f618f916fa34a39758083d0aea4bb87b1a9ac184745b09c642b66a0771671`  
		Last Modified: Fri, 01 Dec 2023 09:03:53 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88db827583d93974059d468003fccdeccfdcd9a21fc15a9286c04d5162b60f00`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 231.6 KB (231631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75849bdf81842f9eff8ef36f098d4df3977533d63126bd042ce3dbf0feb91482`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b858156e16033fc7497c09956fac005c37a0f152b38074431dd9e5bf0d25ce`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:81cf97596c96bf2c8a7f16eec43b20e866143ae03a0cf8161f1f48263918269c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86b6487c29a72435af58323fd6eb163641668280416e87e7ee28eb55ea2b72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:20:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:20:58 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:21:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:21:15 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:21:19 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:21:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:21:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:21:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9351f6531fdc8fd4540a86dac5a66a5860f3985ed2e1e145f0eefecf312a4fc0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041f2592c836041c592a462e184775818c484807025efe56ec1473d2b13465d0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.4 MB (1361751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f71b1afe6f19e25c6412567f2ad476a7153baa201b4d75943e2cf9a041475`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 220.0 KB (220038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b30773a6064abc0c64614a42aca7bb8a0357867cd6ff0810d45240ab0de638`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edff0700419d6610c5b04cf162c75c7bccadfc322ab5c27f670963d1e7b1165`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:f8bed32d8fdba1fdb13b94080f008c65343ad2b3f05ae4cfffa6668cbe5eb52d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c98b6934770e5e69df9564d2c52b9f16c900aa31148984cc7a432c75a5f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:48:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 08:48:25 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 08:48:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 08:48:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 08:48:31 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 08:48:31 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 08:48:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 08:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:48:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b69c2be0d2e048804506af3efc37e709bf98661c409d99087d1184f0304631`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae960024d613c1bc136f3ae0b33c9fa92f11bdf496d5a2a40fe6c46f1132e06f`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.2 MB (1221481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1ec3a08579d63b87f03caf7152bed9ee8fda71ebaa41c5f0565b423dd6ec1`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 208.6 KB (208647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613853307ecba30c7c7f935ec69ed6aab0e74d6f261598b8e3504b156232c4ef`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c380a4795962e93d6ce5552fe1957ccbb666076846f911fe97fc8aa3b9513ec`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:23f75f451120264e35f6fba4a2255e0d7c34c3fc14d8a1073eb3d9e76a48fbad
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
$ docker pull spiped@sha256:b9d410b612429c56c7bfc201428e054e133b3687a23c6ab56cdf78a8c9ad5c7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38188305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3c9d102eb55c2c6c87ed605fae08cffd0c4e04332b24fa0f37d59b2669e92c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:22:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:22:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:22:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:22:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:22:36 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:22:37 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:22:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:22:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e237e28b6c8479420ca602f6d9000c52b84b038600906da0b91c42da69a5a0`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4e443d4cd640e99746f86e1e59871a4ada3b96633f72d79fc6e6067891001`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 2.6 MB (2590190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3e1422a236883c466850e64011b55a1b56e0c81a9545cfcd117adabeaab6b`  
		Last Modified: Thu, 11 Jan 2024 15:22:54 GMT  
		Size: 6.5 MB (6470596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e9783f12fe977d3c3fb97f2140d152d4a266d13d7d695ee4bae14ef8aff1`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babb199a86c149623a233c7dfb363392a7e6cb2ab371278c984af637a5d902c6`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:48e3aec207f11f554d11f7cca3617dd0a20c63a99979dd52383f616781065e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34210288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6552c4cc72e079d96ac29b7b30f77891c4a148dd26b9214d8ad2127af31c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:56 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 11 Jan 2024 01:48:57 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:15:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:15:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:15:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:16:15 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:16:16 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:16:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:16:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:16:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efaf7aa15745e00ee1310cdd0c0a0fa04c9babc4b14f47a0511774e612c17cd`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef6770767dc97b364a92dd7e63c992849f75a389374a2b4a8e3d0b49171d840`  
		Last Modified: Thu, 11 Jan 2024 08:16:31 GMT  
		Size: 2.2 MB (2185812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9428fb70e931ef7456f037c3775b80a743f8c4408b0ba9e82f5b87746e30f8`  
		Last Modified: Thu, 11 Jan 2024 08:16:32 GMT  
		Size: 5.1 MB (5137399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8614ffef08a25ece6a906817bc2c8db1a70f645556aa00be2a766712227daa27`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7de8146f9a20caf7ce4138446d67ec581dda9f7a7c3b21a158483369b19f4`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:649e6cc2ba661d32ef4256888cb13271ddbd95f30b237e8cd364585d269f95db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31643371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7652136d8cffbe4332d3b1d5eaa62b715afbddf4f65d40febad02fd1ded6ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:48:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:48:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:48:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:49:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:49:26 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:49:26 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:49:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:49:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc0d0a8576d9a44d6b4db5cc4f97e623d6bacb291afeb35f258395422a17c9`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1370755c9f61f9d8e5787bcf44b8c87a1f8ef8d4a4fb06ed5b875241ab8bab`  
		Last Modified: Thu, 11 Jan 2024 19:49:43 GMT  
		Size: 2.0 MB (2044341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f48cde4d3929bef49e5aa54ffc6d3b24ff2928a8064474cd99d88cb6ae755ac`  
		Last Modified: Thu, 11 Jan 2024 19:49:44 GMT  
		Size: 4.9 MB (4879298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9101dc3ba57dc33cf3f5784dd33320028deb6a8acea5608535f35068eebe01`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818ec00e89763b0bbe261764ee08b7fc2e910fcaf1e1c6b97d9e014aeff02444`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8d46f6f1c78ff1ed0b3ad00a406bb7dfc11c6e39c7cc975822c2b6d102bd321c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37072116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76215eda00699b15fb0556eac76cf0a4af5d809749b14252b3334749d355379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:29:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:29:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:29:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:30:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:30:12 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:30:12 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:30:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:30:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a186769736ab6aafdd22af7f10d8e13a171d6f765babc242afde5b22f8e021`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89d5b689695e58a4b728e643310efd87f5b30b89d212f9f9805317e6d3d44e9`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 2.4 MB (2433129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20aa23ac8908dff126d96ec7cbe95309d0065002cc0f8ee4d20fe5be7294c11`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 5.5 MB (5480057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6694d2fbcae3e5b0c2c7144d4d8dd14321da5319438a3f43600f4a36b12f2977`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5fbb626e824adb903fbe948e55bd6c1a28321f09b5cf69f0a200ed25471de`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:fd98c9c853fa5a97230af82572ebcf43f560102c6df845a39886ad9916e747bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38673622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec415dd64331e77243cc53d1694750e9d873861a85647c362da7e4772d1852cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:14:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:14:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:14:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:14:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:14:35 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:14:35 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:14:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:14:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219d5afd5c80285ae297ac65047d682e4464a2bd13c5a0c40a0f9676f277503`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458658e0a88c324acd7e3779b7b9f2ef21f36e42bb8792755618eb54b652ad`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 2.6 MB (2586819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba0e8f8301c454ae49e2a06c26833a39423500fdea848c6a651431e4a7ffce`  
		Last Modified: Thu, 11 Jan 2024 15:14:52 GMT  
		Size: 5.9 MB (5941327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029a95a90cc76ed338c96fdbde9b3f8d8ae82fed8ed0638510a92e3cf2d53ee`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d585163d11cdefbc4f1aeed2629cd1f7d42248657db82a57065d9e9fd199f5`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:8df4224500ebe6450955a361308a1477c405408c15fb18d78898367e96485845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36760029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608deccb69dd65cd1c30cfd92453f4110bfc407cb5eb90dea9359191bb51cd23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:46 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 11 Jan 2024 02:11:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:27:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:28:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:28:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:29:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:29:54 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:29:56 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:29:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:30:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd46628fd7683deb3e871331ca13e13a6a6b9f52e2b95664db3553ace5976072`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c440be7820b7f425d0f7805d8d998ba570bfe049ee58308256c53d7a4634cd`  
		Last Modified: Thu, 11 Jan 2024 19:30:22 GMT  
		Size: 1.8 MB (1834348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c992cb9fa388c0602093f4e7132009ce8dfa69d8b130db629e8c6827c1a6c5fc`  
		Last Modified: Thu, 11 Jan 2024 19:30:25 GMT  
		Size: 5.8 MB (5802770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ab8ad9c391168c89ebd0d8a1b2a01525859846b1f624563d7f17567f5a14a`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42164cb6fcc44321ff95e388bc7616373edf4d0c24d377f2285040857a541b4`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:764b7df81dd7d86333ce5b7ca92010d23c2f3fc9c2d7dd13246be720993c2793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42313200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f14ae01ad7b8f3c003b12fbe2d899c5f4d8826a3abb0316ab4d31a9529a54fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:33:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:33:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 07:34:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 07:34:23 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 07:34:23 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 07:34:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:34:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ade73c36eccaaf1b719e4716d382e7a04b8d35d90350d3123d7a93d1137b54`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ccd0557a9cfbb9b7fd784f33b8cce1b87b02442b0536344db386a6c050e49`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 2.8 MB (2769149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4da6798029b0cbbf11779f41a9dc4093b5d0e4955383a8792705ad5f712e14`  
		Last Modified: Thu, 11 Jan 2024 07:34:39 GMT  
		Size: 6.4 MB (6421918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f5df5b7e161aec8d718577a51f297f7f7c55d711cfbf0e6d04f3a9a21c1944`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2770c2c06e8d52033f213a8302837f4f3fe92c7b17e4ee50393ffb59f18daa`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:8460c43f50154dd2d81bcda32d49c1b2630492b81af7f6ef4234aa08d8ca6da1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35138721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96298ac6187d2c17e9ec5cd018bbbd064f59ad841cd21041e96356b347daaeda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:31:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:31:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:31:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:31:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:31:43 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:31:43 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:31:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:31:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:31:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc7df99d6feb97fc1b8c09e7cc15ed28a5c2044d90959ca6282d2e594155ba`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507bb72a5f4749be5f3b6839f7a19c8ad385c1010d7976be3eff7eb3d2b64d`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 2.3 MB (2260721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f29ec00eafde08f306e88d5c35bd960026ebbda97f7bd077a98d77b533efd`  
		Last Modified: Thu, 11 Jan 2024 08:32:08 GMT  
		Size: 5.4 MB (5384555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aebe89a49f2a8cfc48fac744b77c973d1991772b665f667bd7b22c50a2c5a3`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fed5b84874c5eb13bdb5054962a3292a66b05ff968423c916a0ea686dc5195`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:73c463bbbd5f620dbb1aa0ab91b6f7973c8579ba6d720f3642f9b1550c8cca95
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
$ docker pull spiped@sha256:bbcb559f4d5d2f95adfeef51c918f2c078dcf991b30279a34be08e7614eda451
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e068a31dc93f7fbe323b521ca3e2dce275263b1eb366f065ef43b018191ac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:00:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 06:00:04 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 06:00:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 06:00:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 06:00:14 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 06:00:14 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 06:00:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 06:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc456d15d6c4f02d60102c7538cc196adfd3073fa382d3a6c9410c2acfa02238`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac40e9085148fd6ad0718c4bb551770cb399db60f6d9e0e6ae11e2af695afc`  
		Last Modified: Fri, 01 Dec 2023 06:00:26 GMT  
		Size: 1.4 MB (1433002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b55d95977f08a50d321f83fd17bb10e943234260c0d005d9596170d5ef3941b`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fa71cb099a874587efb2d18cba67b14c33ca2472939d01c1695f39e969163c`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1429def50f578086adeafeb1154a9f6683ab8f11715a60a8a1b321413c7c7f38`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:56621f2fd5b22773d7a82548848c99caa44d7526774fccbff6db3e6cf6e2ed7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc63c886e4bd1a4b9a2c5f65cb983191d831e4c5e90b709a27b7ad0468306b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 11:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 11:13:49 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 11:13:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 11:13:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 11:13:57 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 11:13:57 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 11:13:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 11:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c3d326b144045f9766875844acf4350469a75b0a68c61aab0f7ff911f87c40`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39220be7b9073c1b18c05a3956edc927bf596eaf0d654d7b0056fd406cb2a9d9`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.2 MB (1236778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2272caa48ca2695c3ee259c5049bda74ac674fc0349ffce0eb63c15cbcfb373b`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103f3bdb7f64e2684703c5f2a8310fa523b4b883c094984d24a0953897db969`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af16d05b1bfd95db714b4710e950d578ad3ded205b96654b373384e99c72a64`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e20e033984b23e87d819762aa3be4ac888c7573b1fe380a37edc231668cabab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75811072665665f41fe5fd77242815ccd7ba1ada919ff4d133df4c010228f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:09:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:09:14 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:09:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:09:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:09:21 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:09:21 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:09:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:09:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776ef4d306aa7de299bd8db61e455d766a093b7f593b4cb003b7c7436d79d6b`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80582de4f02357b676b2af9cdb5e56aa702680fd50254af56c20b451949c4efb`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.2 MB (1163890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4fd5daf33693bf1e78930cd893f86c3b358b42b11140bad181d50be0636580`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 199.5 KB (199547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a963f13cfdeafcdd2c65f6a266762a0e9f1679aeba08b0ebe2f515f4188753`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfc83b30d29a5ba12424db7d486ed08e84ab517be2c9518f1cde49bb01a6853`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b7bbfd15a130193c126e6305dde27ab1f812b1bde9bcdce939a472c991928997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a827ded63ac80140d8297b83d5b15fbe600917d04d811f7a104d5a81a45446f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:28:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:28:42 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:28:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:28:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:28:50 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:28:50 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:28:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:28:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a00b6b0251227c993c68fbac4ca61cbf6db9b390d4c9dfe2a005132c2c753`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c1951c258ad0eb59a0d4d33d432578b0760a47bef312a1e5bf8cccf477f47`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.4 MB (1362693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733da67e58e7549c947540df4ff581a3d9297a816340ca183083f623809e34bc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 215.7 KB (215687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f459526992eea15e16c15645ca376ef0435b204fc518f1fc404a1a1e2ebec6fc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a81f75355f25a9bd668c3d651a02f8124af05c3fa0dfb1e2265074389ca80`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:f975a9f3d41c92bff597add76b603827306ff8055d25df0b20f1186aa29b952c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c779ff3e48cf1e88a23dff62390543e9e2ab6c1b75a812f8d5dfa915323f58d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:03:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:03:26 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:03:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:03:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:03:39 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:03:39 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:03:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:03:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:03:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1d22c178557ad5427b2e2e39899f1ac5e8a7d3cbdbccccd75d44ef6c2ac2a`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f618f916fa34a39758083d0aea4bb87b1a9ac184745b09c642b66a0771671`  
		Last Modified: Fri, 01 Dec 2023 09:03:53 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88db827583d93974059d468003fccdeccfdcd9a21fc15a9286c04d5162b60f00`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 231.6 KB (231631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75849bdf81842f9eff8ef36f098d4df3977533d63126bd042ce3dbf0feb91482`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b858156e16033fc7497c09956fac005c37a0f152b38074431dd9e5bf0d25ce`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:81cf97596c96bf2c8a7f16eec43b20e866143ae03a0cf8161f1f48263918269c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86b6487c29a72435af58323fd6eb163641668280416e87e7ee28eb55ea2b72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:20:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:20:58 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:21:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:21:15 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:21:19 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:21:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:21:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:21:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9351f6531fdc8fd4540a86dac5a66a5860f3985ed2e1e145f0eefecf312a4fc0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041f2592c836041c592a462e184775818c484807025efe56ec1473d2b13465d0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.4 MB (1361751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f71b1afe6f19e25c6412567f2ad476a7153baa201b4d75943e2cf9a041475`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 220.0 KB (220038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b30773a6064abc0c64614a42aca7bb8a0357867cd6ff0810d45240ab0de638`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edff0700419d6610c5b04cf162c75c7bccadfc322ab5c27f670963d1e7b1165`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:f8bed32d8fdba1fdb13b94080f008c65343ad2b3f05ae4cfffa6668cbe5eb52d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c98b6934770e5e69df9564d2c52b9f16c900aa31148984cc7a432c75a5f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:48:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 08:48:25 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 08:48:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 08:48:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 08:48:31 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 08:48:31 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 08:48:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 08:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:48:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b69c2be0d2e048804506af3efc37e709bf98661c409d99087d1184f0304631`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae960024d613c1bc136f3ae0b33c9fa92f11bdf496d5a2a40fe6c46f1132e06f`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.2 MB (1221481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1ec3a08579d63b87f03caf7152bed9ee8fda71ebaa41c5f0565b423dd6ec1`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 208.6 KB (208647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613853307ecba30c7c7f935ec69ed6aab0e74d6f261598b8e3504b156232c4ef`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c380a4795962e93d6ce5552fe1957ccbb666076846f911fe97fc8aa3b9513ec`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:73c463bbbd5f620dbb1aa0ab91b6f7973c8579ba6d720f3642f9b1550c8cca95
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
$ docker pull spiped@sha256:bbcb559f4d5d2f95adfeef51c918f2c078dcf991b30279a34be08e7614eda451
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e068a31dc93f7fbe323b521ca3e2dce275263b1eb366f065ef43b018191ac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:00:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 06:00:04 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 06:00:04 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 06:00:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 06:00:14 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 06:00:14 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 06:00:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 06:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc456d15d6c4f02d60102c7538cc196adfd3073fa382d3a6c9410c2acfa02238`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac40e9085148fd6ad0718c4bb551770cb399db60f6d9e0e6ae11e2af695afc`  
		Last Modified: Fri, 01 Dec 2023 06:00:26 GMT  
		Size: 1.4 MB (1433002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b55d95977f08a50d321f83fd17bb10e943234260c0d005d9596170d5ef3941b`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fa71cb099a874587efb2d18cba67b14c33ca2472939d01c1695f39e969163c`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1429def50f578086adeafeb1154a9f6683ab8f11715a60a8a1b321413c7c7f38`  
		Last Modified: Fri, 01 Dec 2023 06:00:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:56621f2fd5b22773d7a82548848c99caa44d7526774fccbff6db3e6cf6e2ed7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc63c886e4bd1a4b9a2c5f65cb983191d831e4c5e90b709a27b7ad0468306b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 11:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 11:13:49 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 11:13:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 11:13:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 11:13:57 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 11:13:57 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 11:13:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 11:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c3d326b144045f9766875844acf4350469a75b0a68c61aab0f7ff911f87c40`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39220be7b9073c1b18c05a3956edc927bf596eaf0d654d7b0056fd406cb2a9d9`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 1.2 MB (1236778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2272caa48ca2695c3ee259c5049bda74ac674fc0349ffce0eb63c15cbcfb373b`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 205.9 KB (205868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103f3bdb7f64e2684703c5f2a8310fa523b4b883c094984d24a0953897db969`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af16d05b1bfd95db714b4710e950d578ad3ded205b96654b373384e99c72a64`  
		Last Modified: Fri, 01 Dec 2023 11:14:06 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e20e033984b23e87d819762aa3be4ac888c7573b1fe380a37edc231668cabab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75811072665665f41fe5fd77242815ccd7ba1ada919ff4d133df4c010228f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:09:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:09:14 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:09:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:09:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:09:21 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:09:21 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:09:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:09:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776ef4d306aa7de299bd8db61e455d766a093b7f593b4cb003b7c7436d79d6b`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80582de4f02357b676b2af9cdb5e56aa702680fd50254af56c20b451949c4efb`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 1.2 MB (1163890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4fd5daf33693bf1e78930cd893f86c3b358b42b11140bad181d50be0636580`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 199.5 KB (199547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a963f13cfdeafcdd2c65f6a266762a0e9f1679aeba08b0ebe2f515f4188753`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfc83b30d29a5ba12424db7d486ed08e84ab517be2c9518f1cde49bb01a6853`  
		Last Modified: Fri, 01 Dec 2023 09:09:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b7bbfd15a130193c126e6305dde27ab1f812b1bde9bcdce939a472c991928997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a827ded63ac80140d8297b83d5b15fbe600917d04d811f7a104d5a81a45446f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:28:41 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:28:42 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:28:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:28:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:28:50 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:28:50 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:28:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:28:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a00b6b0251227c993c68fbac4ca61cbf6db9b390d4c9dfe2a005132c2c753`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c1951c258ad0eb59a0d4d33d432578b0760a47bef312a1e5bf8cccf477f47`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 1.4 MB (1362693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733da67e58e7549c947540df4ff581a3d9297a816340ca183083f623809e34bc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 215.7 KB (215687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f459526992eea15e16c15645ca376ef0435b204fc518f1fc404a1a1e2ebec6fc`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a81f75355f25a9bd668c3d651a02f8124af05c3fa0dfb1e2265074389ca80`  
		Last Modified: Fri, 01 Dec 2023 09:29:00 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:f975a9f3d41c92bff597add76b603827306ff8055d25df0b20f1186aa29b952c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c779ff3e48cf1e88a23dff62390543e9e2ab6c1b75a812f8d5dfa915323f58d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:03:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:03:26 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:03:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:03:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:03:39 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:03:39 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:03:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:03:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:03:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1d22c178557ad5427b2e2e39899f1ac5e8a7d3cbdbccccd75d44ef6c2ac2a`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f618f916fa34a39758083d0aea4bb87b1a9ac184745b09c642b66a0771671`  
		Last Modified: Fri, 01 Dec 2023 09:03:53 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88db827583d93974059d468003fccdeccfdcd9a21fc15a9286c04d5162b60f00`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 231.6 KB (231631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75849bdf81842f9eff8ef36f098d4df3977533d63126bd042ce3dbf0feb91482`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b858156e16033fc7497c09956fac005c37a0f152b38074431dd9e5bf0d25ce`  
		Last Modified: Fri, 01 Dec 2023 09:03:52 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:81cf97596c96bf2c8a7f16eec43b20e866143ae03a0cf8161f1f48263918269c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86b6487c29a72435af58323fd6eb163641668280416e87e7ee28eb55ea2b72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 09:20:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 09:20:58 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 09:21:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 09:21:15 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 09:21:19 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 09:21:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 09:21:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 09:21:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9351f6531fdc8fd4540a86dac5a66a5860f3985ed2e1e145f0eefecf312a4fc0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041f2592c836041c592a462e184775818c484807025efe56ec1473d2b13465d0`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 1.4 MB (1361751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f71b1afe6f19e25c6412567f2ad476a7153baa201b4d75943e2cf9a041475`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 220.0 KB (220038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b30773a6064abc0c64614a42aca7bb8a0357867cd6ff0810d45240ab0de638`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edff0700419d6610c5b04cf162c75c7bccadfc322ab5c27f670963d1e7b1165`  
		Last Modified: Fri, 01 Dec 2023 09:21:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:f8bed32d8fdba1fdb13b94080f008c65343ad2b3f05ae4cfffa6668cbe5eb52d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c98b6934770e5e69df9564d2c52b9f16c900aa31148984cc7a432c75a5f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:48:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 01 Dec 2023 08:48:25 GMT
RUN apk add --no-cache libssl1.1
# Fri, 01 Dec 2023 08:48:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 01 Dec 2023 08:48:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 01 Dec 2023 08:48:31 GMT
VOLUME [/spiped]
# Fri, 01 Dec 2023 08:48:31 GMT
WORKDIR /spiped
# Fri, 01 Dec 2023 08:48:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 01 Dec 2023 08:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:48:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b69c2be0d2e048804506af3efc37e709bf98661c409d99087d1184f0304631`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae960024d613c1bc136f3ae0b33c9fa92f11bdf496d5a2a40fe6c46f1132e06f`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 1.2 MB (1221481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1ec3a08579d63b87f03caf7152bed9ee8fda71ebaa41c5f0565b423dd6ec1`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 208.6 KB (208647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613853307ecba30c7c7f935ec69ed6aab0e74d6f261598b8e3504b156232c4ef`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c380a4795962e93d6ce5552fe1957ccbb666076846f911fe97fc8aa3b9513ec`  
		Last Modified: Fri, 01 Dec 2023 08:48:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:23f75f451120264e35f6fba4a2255e0d7c34c3fc14d8a1073eb3d9e76a48fbad
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
$ docker pull spiped@sha256:b9d410b612429c56c7bfc201428e054e133b3687a23c6ab56cdf78a8c9ad5c7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38188305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3c9d102eb55c2c6c87ed605fae08cffd0c4e04332b24fa0f37d59b2669e92c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:22:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:22:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:22:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:22:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:22:36 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:22:37 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:22:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:22:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e237e28b6c8479420ca602f6d9000c52b84b038600906da0b91c42da69a5a0`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4e443d4cd640e99746f86e1e59871a4ada3b96633f72d79fc6e6067891001`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 2.6 MB (2590190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d3e1422a236883c466850e64011b55a1b56e0c81a9545cfcd117adabeaab6b`  
		Last Modified: Thu, 11 Jan 2024 15:22:54 GMT  
		Size: 6.5 MB (6470596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e9783f12fe977d3c3fb97f2140d152d4a266d13d7d695ee4bae14ef8aff1`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babb199a86c149623a233c7dfb363392a7e6cb2ab371278c984af637a5d902c6`  
		Last Modified: Thu, 11 Jan 2024 15:22:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:48e3aec207f11f554d11f7cca3617dd0a20c63a99979dd52383f616781065e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34210288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6552c4cc72e079d96ac29b7b30f77891c4a148dd26b9214d8ad2127af31c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:56 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 11 Jan 2024 01:48:57 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:15:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:15:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:15:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:16:15 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:16:16 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:16:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:16:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:16:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efaf7aa15745e00ee1310cdd0c0a0fa04c9babc4b14f47a0511774e612c17cd`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef6770767dc97b364a92dd7e63c992849f75a389374a2b4a8e3d0b49171d840`  
		Last Modified: Thu, 11 Jan 2024 08:16:31 GMT  
		Size: 2.2 MB (2185812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9428fb70e931ef7456f037c3775b80a743f8c4408b0ba9e82f5b87746e30f8`  
		Last Modified: Thu, 11 Jan 2024 08:16:32 GMT  
		Size: 5.1 MB (5137399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8614ffef08a25ece6a906817bc2c8db1a70f645556aa00be2a766712227daa27`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7de8146f9a20caf7ce4138446d67ec581dda9f7a7c3b21a158483369b19f4`  
		Last Modified: Thu, 11 Jan 2024 08:16:30 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:649e6cc2ba661d32ef4256888cb13271ddbd95f30b237e8cd364585d269f95db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31643371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7652136d8cffbe4332d3b1d5eaa62b715afbddf4f65d40febad02fd1ded6ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:48:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:48:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:48:52 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:49:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:49:26 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:49:26 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:49:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:49:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc0d0a8576d9a44d6b4db5cc4f97e623d6bacb291afeb35f258395422a17c9`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1370755c9f61f9d8e5787bcf44b8c87a1f8ef8d4a4fb06ed5b875241ab8bab`  
		Last Modified: Thu, 11 Jan 2024 19:49:43 GMT  
		Size: 2.0 MB (2044341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f48cde4d3929bef49e5aa54ffc6d3b24ff2928a8064474cd99d88cb6ae755ac`  
		Last Modified: Thu, 11 Jan 2024 19:49:44 GMT  
		Size: 4.9 MB (4879298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9101dc3ba57dc33cf3f5784dd33320028deb6a8acea5608535f35068eebe01`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818ec00e89763b0bbe261764ee08b7fc2e910fcaf1e1c6b97d9e014aeff02444`  
		Last Modified: Thu, 11 Jan 2024 19:49:42 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8d46f6f1c78ff1ed0b3ad00a406bb7dfc11c6e39c7cc975822c2b6d102bd321c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37072116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76215eda00699b15fb0556eac76cf0a4af5d809749b14252b3334749d355379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:29:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:29:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:29:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:30:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:30:12 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:30:12 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:30:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:30:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:30:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a186769736ab6aafdd22af7f10d8e13a171d6f765babc242afde5b22f8e021`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89d5b689695e58a4b728e643310efd87f5b30b89d212f9f9805317e6d3d44e9`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 2.4 MB (2433129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20aa23ac8908dff126d96ec7cbe95309d0065002cc0f8ee4d20fe5be7294c11`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 5.5 MB (5480057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6694d2fbcae3e5b0c2c7144d4d8dd14321da5319438a3f43600f4a36b12f2977`  
		Last Modified: Thu, 11 Jan 2024 08:30:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5fbb626e824adb903fbe948e55bd6c1a28321f09b5cf69f0a200ed25471de`  
		Last Modified: Thu, 11 Jan 2024 08:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:fd98c9c853fa5a97230af82572ebcf43f560102c6df845a39886ad9916e747bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38673622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec415dd64331e77243cc53d1694750e9d873861a85647c362da7e4772d1852cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 15:14:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 15:14:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:14:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 15:14:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 15:14:35 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 15:14:35 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 15:14:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 15:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 15:14:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219d5afd5c80285ae297ac65047d682e4464a2bd13c5a0c40a0f9676f277503`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458658e0a88c324acd7e3779b7b9f2ef21f36e42bb8792755618eb54b652ad`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 2.6 MB (2586819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba0e8f8301c454ae49e2a06c26833a39423500fdea848c6a651431e4a7ffce`  
		Last Modified: Thu, 11 Jan 2024 15:14:52 GMT  
		Size: 5.9 MB (5941327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029a95a90cc76ed338c96fdbde9b3f8d8ae82fed8ed0638510a92e3cf2d53ee`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d585163d11cdefbc4f1aeed2629cd1f7d42248657db82a57065d9e9fd199f5`  
		Last Modified: Thu, 11 Jan 2024 15:14:51 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:8df4224500ebe6450955a361308a1477c405408c15fb18d78898367e96485845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36760029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608deccb69dd65cd1c30cfd92453f4110bfc407cb5eb90dea9359191bb51cd23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:46 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 11 Jan 2024 02:11:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:27:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 19:28:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:28:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 19:29:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 19:29:54 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 19:29:56 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 19:29:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 19:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:30:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd46628fd7683deb3e871331ca13e13a6a6b9f52e2b95664db3553ace5976072`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c440be7820b7f425d0f7805d8d998ba570bfe049ee58308256c53d7a4634cd`  
		Last Modified: Thu, 11 Jan 2024 19:30:22 GMT  
		Size: 1.8 MB (1834348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c992cb9fa388c0602093f4e7132009ce8dfa69d8b130db629e8c6827c1a6c5fc`  
		Last Modified: Thu, 11 Jan 2024 19:30:25 GMT  
		Size: 5.8 MB (5802770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ab8ad9c391168c89ebd0d8a1b2a01525859846b1f624563d7f17567f5a14a`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42164cb6fcc44321ff95e388bc7616373edf4d0c24d377f2285040857a541b4`  
		Last Modified: Thu, 11 Jan 2024 19:30:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:764b7df81dd7d86333ce5b7ca92010d23c2f3fc9c2d7dd13246be720993c2793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42313200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f14ae01ad7b8f3c003b12fbe2d899c5f4d8826a3abb0316ab4d31a9529a54fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:33:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:33:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 07:34:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 07:34:23 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 07:34:23 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 07:34:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:34:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ade73c36eccaaf1b719e4716d382e7a04b8d35d90350d3123d7a93d1137b54`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ccd0557a9cfbb9b7fd784f33b8cce1b87b02442b0536344db386a6c050e49`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 2.8 MB (2769149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4da6798029b0cbbf11779f41a9dc4093b5d0e4955383a8792705ad5f712e14`  
		Last Modified: Thu, 11 Jan 2024 07:34:39 GMT  
		Size: 6.4 MB (6421918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f5df5b7e161aec8d718577a51f297f7f7c55d711cfbf0e6d04f3a9a21c1944`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2770c2c06e8d52033f213a8302837f4f3fe92c7b17e4ee50393ffb59f18daa`  
		Last Modified: Thu, 11 Jan 2024 07:34:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:8460c43f50154dd2d81bcda32d49c1b2630492b81af7f6ef4234aa08d8ca6da1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35138721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96298ac6187d2c17e9ec5cd018bbbd064f59ad841cd21041e96356b347daaeda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:31:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 11 Jan 2024 08:31:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:31:26 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 11 Jan 2024 08:31:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 08:31:43 GMT
VOLUME [/spiped]
# Thu, 11 Jan 2024 08:31:43 GMT
WORKDIR /spiped
# Thu, 11 Jan 2024 08:31:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 11 Jan 2024 08:31:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 08:31:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc7df99d6feb97fc1b8c09e7cc15ed28a5c2044d90959ca6282d2e594155ba`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507bb72a5f4749be5f3b6839f7a19c8ad385c1010d7976be3eff7eb3d2b64d`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 2.3 MB (2260721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f29ec00eafde08f306e88d5c35bd960026ebbda97f7bd077a98d77b533efd`  
		Last Modified: Thu, 11 Jan 2024 08:32:08 GMT  
		Size: 5.4 MB (5384555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aebe89a49f2a8cfc48fac744b77c973d1991772b665f667bd7b22c50a2c5a3`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fed5b84874c5eb13bdb5054962a3292a66b05ff968423c916a0ea686dc5195`  
		Last Modified: Thu, 11 Jan 2024 08:32:07 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
