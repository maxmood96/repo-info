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
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
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
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
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
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
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
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
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
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
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
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
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
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
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
