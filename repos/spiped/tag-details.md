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
$ docker pull spiped@sha256:862cc3f862cc8485517ddae23f0011c8077ff7e8af04033ea81bdf7b1da1a9c6
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
$ docker pull spiped@sha256:cf4ddd6a6c44691ed6859d574a20ef59ef698ae3f037b7df1ebfa28b8b8bd1f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf52c9298823b1f18acb17148cc5b3ebdbd75089de16ae1130205dbb9aafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:16:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 14:16:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 14:16:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 14:17:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 14:17:03 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 14:17:03 GMT
WORKDIR /spiped
# Tue, 14 May 2024 14:17:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 14:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 14:17:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a82628b598b9cce8ec64537611dcedbe90af99841cdb49e58d721b32483729`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1143c09313a2d7e6f5baee62a732edda947d3623f822103d7a0d387b3d5b79`  
		Last Modified: Tue, 14 May 2024 14:17:19 GMT  
		Size: 2.6 MB (2592087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55108b9e1b391323c605eb1ee0685ffba653fb2af66003cffdecdff25ae3a56b`  
		Last Modified: Tue, 14 May 2024 14:17:20 GMT  
		Size: 6.5 MB (6475264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80206eeb4def215391eef90fe876b1c36cf988e9541137626622f3dfe617fc`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e3cf85dc49c2c5b7913c7eccbeb21a31572d56162310926d29b4a4da4f727d`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:80cea41eb10539a9614cf8d3bce942e421a8d4bbe7afcc76a184794f2e90e0b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f9030fa7ad2788e7b672a14a95c165cb3f2fcbf6d4a1a1476c8ee00af7a593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:42:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:42:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:42:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:42:37 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:42:37 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:42:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6777bbed6c805551e42c47e87032e740c5eedc8cadbf77dad9b8e8ce511606f`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417f02f1db7a09b0e9d5825f84ee133a3f893a14453713c8ff8bdd0ae044aa2`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 2.2 MB (2186969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464ba5d70c3dca39b17e559d73d2d6487a5b2e8bd876d640e4c5b0ec69b24159`  
		Last Modified: Tue, 14 May 2024 07:42:49 GMT  
		Size: 5.1 MB (5142325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9019ad88684b9f4c3d1f49972424b0293510ab9e06d759775629fc6b0e24b`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdf89f322e59ce594f65f2ca1a07971adc5c5c87caa1596e860953c16477bf8`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:735a8a603975528c3c97c5d7d9483954e59479d5dfd9d004de05b9a8c21b10eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31672192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa20a67e38ed4bead4a3dd6430fd2f1c3769bdef70b0cf5fb931f2c84d572d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:28:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 09:28:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:28:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 09:28:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 09:28:54 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 09:28:54 GMT
WORKDIR /spiped
# Tue, 14 May 2024 09:28:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 09:28:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a4cf67b1b0dbe745e9aa40fa5f87e52c1c82885299efbbc72f32c0cee35433`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dd0b66ddc27047a4a5855335209c7516484db200e84db320f73729200a97be`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 2.0 MB (2046404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e382aa9af357b420a0175272654caba9cccb79f1e60eb7046e58e8254bb449b`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 4.9 MB (4883986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fea207b8cc3f715368994f5d85c6fcf99dab41e6011c51316c4c824e3e304`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe8d5d653b76bafa5139bf4f66f348e0018600f0c4f700257f9321a9426e9fc`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:2d26a994ce529bacb0c6a4582bd38f688cf540b418a9891ee25758ab72e8c9c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab23d111d60dd2cf3472be5b49d62f48d5ee126f0eb0b1c00c0feeabfec0820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:34:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:34:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:35:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:35:06 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:35:06 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:35:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:35:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c383b8fe43238b1fad5f3e216bd4661862b04dca14f2f6c25ba2ddc8f76a3910`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a6bfc68a06eaa7e7db9542db2e0b93ea49bdb46dc931a06c449b56e49bbb2f`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 2.4 MB (2435061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1914712040941e6fe19a7257a9d1f780dd56d7d8d98ccc2a5e1d4be2fa36e7ec`  
		Last Modified: Tue, 14 May 2024 07:35:22 GMT  
		Size: 5.5 MB (5485266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262a48740e860bd3d023e3526fe6eea2a5b156dafb90337e0e9e719ae03914e5`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efec22567cdd2ff09d813eb9509399603c62df9074669e4d4f72608d7d1063b4`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:d118a30f85973d9624c09d24791175edadcf7bd64daa760de5433d37ffff4267
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38697698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d6cb7c219e62868baaca89c97d2082759b1b34f4c1b33904bd06687f78ef39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:59:24 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 08:59:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 08:59:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 08:59:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 08:59:58 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 08:59:58 GMT
WORKDIR /spiped
# Tue, 14 May 2024 08:59:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 08:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 08:59:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b467928807c0e563a54f8670c91eca71e6fd926ffa244c927c62d0db86a39d82`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2177ea79a0f66474ae7a368cea82d1058ead17203d1ce58d4c971d7b3caaf`  
		Last Modified: Tue, 14 May 2024 09:00:16 GMT  
		Size: 2.6 MB (2588290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c20f7da89678592d46e8ebeeb4f876239229f927e886826e9f1c570f3c2769`  
		Last Modified: Tue, 14 May 2024 09:00:17 GMT  
		Size: 5.9 MB (5945172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4522d4f258a1969fb9e707a784d8b90b7051f3c02ee3cc80873d216ea3857`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e536d0d133fe4da2515e6ce89465a852fa25d4a16286ad6af8bb449723fdf1a`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

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

### `spiped:1` - linux; ppc64le

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

### `spiped:1` - linux; s390x

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

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:6e421e250586c16849e386519b6835425c114526c56dd8bbd77d6cedda957f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:07e3b4b9207f89998e572bed22a7f7954cc6492c8d8f21be279963f2cff7fc9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3855418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9201d18866bb1ce0bb8b2535a09c9746ee4710bbfc2f2c1ab380e1ab464c476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 02:34:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 02:34:48 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 02:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 02:34:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 02:34:59 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 02:34:59 GMT
WORKDIR /spiped
# Fri, 24 May 2024 02:34:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 02:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 02:34:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b65a0cef07ed27e2dfa105666ab73da30ede8da8ec1d6a4aff22c6d64a5905`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 984.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79dadf24bbac85056299fdc71ca82aa8bdc1d5e88edfbaded02869e0b489815`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef14f04bed6dd2107fa0c48cff8ac4c26d9c72582967c37fba6b6641ee53628a`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 224.3 KB (224301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512d6a117eb4435d549b47b5d8cae78953c96f8a91d9420fa806decbd655936`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b384b7559504371850eed3815c8be24a48bbf848e4f8181a30e96853c6af3f1`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5d9da313669f8f0048ec2e9eab6bf853600283a81b4ca96e692b10bdb3c72bdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ca2a16641057fa841612e468f82aa3487de7f1198cfad469dcf99446926816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 00:49:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 25 May 2024 00:49:30 GMT
RUN apk add --no-cache libssl3
# Sat, 25 May 2024 00:49:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 25 May 2024 09:53:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 25 May 2024 09:53:05 GMT
VOLUME [/spiped]
# Sat, 25 May 2024 09:53:05 GMT
WORKDIR /spiped
# Sat, 25 May 2024 09:53:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 25 May 2024 09:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 May 2024 09:53:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc224dd751252e9181a8cfc90f8cc478007dd80c5fcaf9c0e7365c5c5690cd6`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d844205e2c4ed91d86c9d3b93ba94f73a6802f7d95e2637329e3171f1596051`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf50783437084d308ea037a336c6b2adde912eb87c2d0910d52f8259d2ccd361`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 209.0 KB (208990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e446f34a875f7f58e4f0ff44cdfc7c4fa476269342e24e5cd4b066bf0fd56db5`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973efe8383e26e010949975c4c577788da3b889331852a53e975fdd74591d73`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:25599ac7da2bbcb6630557d1d39c0d42ba4e82abb1faca8c8d5416b6c9355639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e776a6cafa9ea09db267caf77626a5486302739cab2a69c06021f6f020bc38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:08:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:08:47 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:08:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:08:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:08:59 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:08:59 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57dde9a22f05f8d3d8c1a8a13dc73487a9cde1413d04a2f0921d0b629c3e8`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b15fc10ac651a8f9a2a48b8fa00251a8fac4dcb9d04570226980e7f64e8f09`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c206c9d5ca56d7e0dfb79bbf3513d4b64cd649c95da66330942faada9b5be4c`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 202.6 KB (202557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb12eda4f30ee29354c5c954d72d1201f6189aa39214e279ea95a1139d20706`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3301f3fd425a130e1103ae1c59693e259c0aa61c4457150fbb86acf87164bb9`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ee22a4376163469a5478a77d3dd086da10e96bab2415e92cb213ce08dee1701e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7161188ee6d2c07e0c2f1fc2a6fb5a02c590873473230245a1f9a46ad49f8791`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 01:17:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 01:17:10 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 01:17:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 01:17:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 01:17:18 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 01:17:18 GMT
WORKDIR /spiped
# Fri, 24 May 2024 01:17:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 01:17:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 01:17:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f90aa9bfc773d7ce92ca3bf50d8ae635c7d9f78892f0b93b65803c9d33b1a`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b9605849ac73a8379695848d7a0520038c21b1c2ebf31e40beda1b53f9fe9`  
		Last Modified: Fri, 24 May 2024 01:17:30 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099b3f4d764b8b79d94713e5d3320da1b4822ef27f9af0f3149655d12aa47d`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 219.0 KB (218970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b21ae2d8249251716fb673e50c2e09cda47bc565d7eebd5fe3efa053d5eac6`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236abc558b7bcb1712f41161eaaaecbf399e7eaf1b2aa8094cddd334c4f6872e`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 337.0 B  
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
$ docker pull spiped@sha256:f7be193e91b7536b291aff1af811715f1994df5d1ff50e7e01ac61438ce971b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6123bf450568ccf383fc60e3066c5d8216950f96a0d14b76f8751ddc829569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:09:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:09:15 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:09:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:09:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:09:25 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:09:25 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416f94511c6e98b05f9acca81a2233b2167b904c9be9084f8782e7fee8c030da`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afb72e562d3649f63864604b0551f222f5fe0fd3061dc2d2039e65aa5873a2e`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 7.6 KB (7590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8756affa07ec356f000450e4e65d82e98d038ff03a81c67470272d6e4f30e72d`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 222.9 KB (222928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b978619b6227e9697ca0875eb4b8b47a1b84aa7b4cc5f9eb6e8c5aebf8921`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d5f1d461a5a0e946207612f37d9fdecbffe6ff7b8a528dd00968ac1594b162`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:cd5a4621afff483f36101ea9ebae88f7dcf25f86c2309d723bbd483be19ceafe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e812e801b6ae16522a84a7ab6f7556c16c0a15341d272fce6510208bf865f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 04:22:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 May 2024 04:22:11 GMT
RUN apk add --no-cache libssl3
# Wed, 29 May 2024 04:22:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 May 2024 04:23:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 May 2024 04:23:18 GMT
VOLUME [/spiped]
# Wed, 29 May 2024 04:23:19 GMT
WORKDIR /spiped
# Wed, 29 May 2024 04:23:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 May 2024 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 04:23:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c0c4f99ba3a3946abd6a4741459ac597ecf8393da29611c0c72c127c3c8fc6`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5b031480a0383a5f02d1f22612813b1ffa3cfb8ac50bda5bca486fdbf7499`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e17de0f3b7417191ea5c8f7779379c7965a389e87d7fddba3c8d28d6f854c`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 215.3 KB (215290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7d27f6c07e7feb513acf854ddaee65e51ce92daf7c3918f1625aaec5fa14b`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e20db4a7ebcccd41cb86827aeddf9cb92dfc787970bf9623b4779f5bf8559`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8dec41cbe81f417096082fdaa31bb95bdd7e36dfec4cc462a7e9462205ed2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee6531c62c7ffe07b640d5ab5b763be7303e38a61c81bb6524855dec0ca243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 00:57:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 00:57:59 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 00:57:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 00:58:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 00:58:05 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 00:58:05 GMT
WORKDIR /spiped
# Fri, 24 May 2024 00:58:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 00:58:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d2acf9b7465edffd5a10fedbf230b30c81cb8b13eb3c7d97b4ba3dc542d17`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbc970af29f74dd00097324a2d43d0cd4ea77aee3bf1217ffe3b76397a889`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec7c94b7827b61d57438499589e4d6f5b1320a6bd0eee1a2226d3f8d22d81aa`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 211.7 KB (211719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad9a1996f006554091faad0788cedfe9c37ce442aefa430c0d7b7a7eb402280`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531998ea71dc30b5a286d51c478a1a6f9ff8db7afc074c302dfe6bef2f5da69d`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:862cc3f862cc8485517ddae23f0011c8077ff7e8af04033ea81bdf7b1da1a9c6
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
$ docker pull spiped@sha256:cf4ddd6a6c44691ed6859d574a20ef59ef698ae3f037b7df1ebfa28b8b8bd1f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf52c9298823b1f18acb17148cc5b3ebdbd75089de16ae1130205dbb9aafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:16:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 14:16:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 14:16:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 14:17:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 14:17:03 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 14:17:03 GMT
WORKDIR /spiped
# Tue, 14 May 2024 14:17:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 14:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 14:17:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a82628b598b9cce8ec64537611dcedbe90af99841cdb49e58d721b32483729`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1143c09313a2d7e6f5baee62a732edda947d3623f822103d7a0d387b3d5b79`  
		Last Modified: Tue, 14 May 2024 14:17:19 GMT  
		Size: 2.6 MB (2592087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55108b9e1b391323c605eb1ee0685ffba653fb2af66003cffdecdff25ae3a56b`  
		Last Modified: Tue, 14 May 2024 14:17:20 GMT  
		Size: 6.5 MB (6475264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80206eeb4def215391eef90fe876b1c36cf988e9541137626622f3dfe617fc`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e3cf85dc49c2c5b7913c7eccbeb21a31572d56162310926d29b4a4da4f727d`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:80cea41eb10539a9614cf8d3bce942e421a8d4bbe7afcc76a184794f2e90e0b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f9030fa7ad2788e7b672a14a95c165cb3f2fcbf6d4a1a1476c8ee00af7a593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:42:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:42:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:42:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:42:37 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:42:37 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:42:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6777bbed6c805551e42c47e87032e740c5eedc8cadbf77dad9b8e8ce511606f`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417f02f1db7a09b0e9d5825f84ee133a3f893a14453713c8ff8bdd0ae044aa2`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 2.2 MB (2186969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464ba5d70c3dca39b17e559d73d2d6487a5b2e8bd876d640e4c5b0ec69b24159`  
		Last Modified: Tue, 14 May 2024 07:42:49 GMT  
		Size: 5.1 MB (5142325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9019ad88684b9f4c3d1f49972424b0293510ab9e06d759775629fc6b0e24b`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdf89f322e59ce594f65f2ca1a07971adc5c5c87caa1596e860953c16477bf8`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:735a8a603975528c3c97c5d7d9483954e59479d5dfd9d004de05b9a8c21b10eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31672192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa20a67e38ed4bead4a3dd6430fd2f1c3769bdef70b0cf5fb931f2c84d572d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:28:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 09:28:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:28:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 09:28:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 09:28:54 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 09:28:54 GMT
WORKDIR /spiped
# Tue, 14 May 2024 09:28:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 09:28:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a4cf67b1b0dbe745e9aa40fa5f87e52c1c82885299efbbc72f32c0cee35433`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dd0b66ddc27047a4a5855335209c7516484db200e84db320f73729200a97be`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 2.0 MB (2046404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e382aa9af357b420a0175272654caba9cccb79f1e60eb7046e58e8254bb449b`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 4.9 MB (4883986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fea207b8cc3f715368994f5d85c6fcf99dab41e6011c51316c4c824e3e304`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe8d5d653b76bafa5139bf4f66f348e0018600f0c4f700257f9321a9426e9fc`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:2d26a994ce529bacb0c6a4582bd38f688cf540b418a9891ee25758ab72e8c9c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab23d111d60dd2cf3472be5b49d62f48d5ee126f0eb0b1c00c0feeabfec0820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:34:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:34:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:35:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:35:06 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:35:06 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:35:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:35:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c383b8fe43238b1fad5f3e216bd4661862b04dca14f2f6c25ba2ddc8f76a3910`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a6bfc68a06eaa7e7db9542db2e0b93ea49bdb46dc931a06c449b56e49bbb2f`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 2.4 MB (2435061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1914712040941e6fe19a7257a9d1f780dd56d7d8d98ccc2a5e1d4be2fa36e7ec`  
		Last Modified: Tue, 14 May 2024 07:35:22 GMT  
		Size: 5.5 MB (5485266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262a48740e860bd3d023e3526fe6eea2a5b156dafb90337e0e9e719ae03914e5`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efec22567cdd2ff09d813eb9509399603c62df9074669e4d4f72608d7d1063b4`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:d118a30f85973d9624c09d24791175edadcf7bd64daa760de5433d37ffff4267
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38697698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d6cb7c219e62868baaca89c97d2082759b1b34f4c1b33904bd06687f78ef39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:59:24 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 08:59:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 08:59:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 08:59:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 08:59:58 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 08:59:58 GMT
WORKDIR /spiped
# Tue, 14 May 2024 08:59:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 08:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 08:59:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b467928807c0e563a54f8670c91eca71e6fd926ffa244c927c62d0db86a39d82`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2177ea79a0f66474ae7a368cea82d1058ead17203d1ce58d4c971d7b3caaf`  
		Last Modified: Tue, 14 May 2024 09:00:16 GMT  
		Size: 2.6 MB (2588290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c20f7da89678592d46e8ebeeb4f876239229f927e886826e9f1c570f3c2769`  
		Last Modified: Tue, 14 May 2024 09:00:17 GMT  
		Size: 5.9 MB (5945172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4522d4f258a1969fb9e707a784d8b90b7051f3c02ee3cc80873d216ea3857`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e536d0d133fe4da2515e6ce89465a852fa25d4a16286ad6af8bb449723fdf1a`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

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

### `spiped:1.6` - linux; ppc64le

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

### `spiped:1.6` - linux; s390x

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

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:6e421e250586c16849e386519b6835425c114526c56dd8bbd77d6cedda957f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:07e3b4b9207f89998e572bed22a7f7954cc6492c8d8f21be279963f2cff7fc9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3855418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9201d18866bb1ce0bb8b2535a09c9746ee4710bbfc2f2c1ab380e1ab464c476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 02:34:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 02:34:48 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 02:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 02:34:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 02:34:59 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 02:34:59 GMT
WORKDIR /spiped
# Fri, 24 May 2024 02:34:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 02:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 02:34:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b65a0cef07ed27e2dfa105666ab73da30ede8da8ec1d6a4aff22c6d64a5905`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 984.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79dadf24bbac85056299fdc71ca82aa8bdc1d5e88edfbaded02869e0b489815`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef14f04bed6dd2107fa0c48cff8ac4c26d9c72582967c37fba6b6641ee53628a`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 224.3 KB (224301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512d6a117eb4435d549b47b5d8cae78953c96f8a91d9420fa806decbd655936`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b384b7559504371850eed3815c8be24a48bbf848e4f8181a30e96853c6af3f1`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5d9da313669f8f0048ec2e9eab6bf853600283a81b4ca96e692b10bdb3c72bdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ca2a16641057fa841612e468f82aa3487de7f1198cfad469dcf99446926816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 00:49:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 25 May 2024 00:49:30 GMT
RUN apk add --no-cache libssl3
# Sat, 25 May 2024 00:49:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 25 May 2024 09:53:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 25 May 2024 09:53:05 GMT
VOLUME [/spiped]
# Sat, 25 May 2024 09:53:05 GMT
WORKDIR /spiped
# Sat, 25 May 2024 09:53:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 25 May 2024 09:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 May 2024 09:53:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc224dd751252e9181a8cfc90f8cc478007dd80c5fcaf9c0e7365c5c5690cd6`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d844205e2c4ed91d86c9d3b93ba94f73a6802f7d95e2637329e3171f1596051`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf50783437084d308ea037a336c6b2adde912eb87c2d0910d52f8259d2ccd361`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 209.0 KB (208990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e446f34a875f7f58e4f0ff44cdfc7c4fa476269342e24e5cd4b066bf0fd56db5`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973efe8383e26e010949975c4c577788da3b889331852a53e975fdd74591d73`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:25599ac7da2bbcb6630557d1d39c0d42ba4e82abb1faca8c8d5416b6c9355639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e776a6cafa9ea09db267caf77626a5486302739cab2a69c06021f6f020bc38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:08:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:08:47 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:08:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:08:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:08:59 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:08:59 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57dde9a22f05f8d3d8c1a8a13dc73487a9cde1413d04a2f0921d0b629c3e8`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b15fc10ac651a8f9a2a48b8fa00251a8fac4dcb9d04570226980e7f64e8f09`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c206c9d5ca56d7e0dfb79bbf3513d4b64cd649c95da66330942faada9b5be4c`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 202.6 KB (202557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb12eda4f30ee29354c5c954d72d1201f6189aa39214e279ea95a1139d20706`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3301f3fd425a130e1103ae1c59693e259c0aa61c4457150fbb86acf87164bb9`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ee22a4376163469a5478a77d3dd086da10e96bab2415e92cb213ce08dee1701e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7161188ee6d2c07e0c2f1fc2a6fb5a02c590873473230245a1f9a46ad49f8791`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 01:17:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 01:17:10 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 01:17:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 01:17:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 01:17:18 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 01:17:18 GMT
WORKDIR /spiped
# Fri, 24 May 2024 01:17:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 01:17:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 01:17:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f90aa9bfc773d7ce92ca3bf50d8ae635c7d9f78892f0b93b65803c9d33b1a`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b9605849ac73a8379695848d7a0520038c21b1c2ebf31e40beda1b53f9fe9`  
		Last Modified: Fri, 24 May 2024 01:17:30 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099b3f4d764b8b79d94713e5d3320da1b4822ef27f9af0f3149655d12aa47d`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 219.0 KB (218970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b21ae2d8249251716fb673e50c2e09cda47bc565d7eebd5fe3efa053d5eac6`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236abc558b7bcb1712f41161eaaaecbf399e7eaf1b2aa8094cddd334c4f6872e`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 337.0 B  
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
$ docker pull spiped@sha256:f7be193e91b7536b291aff1af811715f1994df5d1ff50e7e01ac61438ce971b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6123bf450568ccf383fc60e3066c5d8216950f96a0d14b76f8751ddc829569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:09:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:09:15 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:09:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:09:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:09:25 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:09:25 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416f94511c6e98b05f9acca81a2233b2167b904c9be9084f8782e7fee8c030da`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afb72e562d3649f63864604b0551f222f5fe0fd3061dc2d2039e65aa5873a2e`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 7.6 KB (7590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8756affa07ec356f000450e4e65d82e98d038ff03a81c67470272d6e4f30e72d`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 222.9 KB (222928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b978619b6227e9697ca0875eb4b8b47a1b84aa7b4cc5f9eb6e8c5aebf8921`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d5f1d461a5a0e946207612f37d9fdecbffe6ff7b8a528dd00968ac1594b162`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:cd5a4621afff483f36101ea9ebae88f7dcf25f86c2309d723bbd483be19ceafe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e812e801b6ae16522a84a7ab6f7556c16c0a15341d272fce6510208bf865f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 04:22:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 May 2024 04:22:11 GMT
RUN apk add --no-cache libssl3
# Wed, 29 May 2024 04:22:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 May 2024 04:23:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 May 2024 04:23:18 GMT
VOLUME [/spiped]
# Wed, 29 May 2024 04:23:19 GMT
WORKDIR /spiped
# Wed, 29 May 2024 04:23:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 May 2024 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 04:23:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c0c4f99ba3a3946abd6a4741459ac597ecf8393da29611c0c72c127c3c8fc6`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5b031480a0383a5f02d1f22612813b1ffa3cfb8ac50bda5bca486fdbf7499`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e17de0f3b7417191ea5c8f7779379c7965a389e87d7fddba3c8d28d6f854c`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 215.3 KB (215290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7d27f6c07e7feb513acf854ddaee65e51ce92daf7c3918f1625aaec5fa14b`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e20db4a7ebcccd41cb86827aeddf9cb92dfc787970bf9623b4779f5bf8559`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8dec41cbe81f417096082fdaa31bb95bdd7e36dfec4cc462a7e9462205ed2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee6531c62c7ffe07b640d5ab5b763be7303e38a61c81bb6524855dec0ca243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 00:57:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 00:57:59 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 00:57:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 00:58:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 00:58:05 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 00:58:05 GMT
WORKDIR /spiped
# Fri, 24 May 2024 00:58:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 00:58:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d2acf9b7465edffd5a10fedbf230b30c81cb8b13eb3c7d97b4ba3dc542d17`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbc970af29f74dd00097324a2d43d0cd4ea77aee3bf1217ffe3b76397a889`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec7c94b7827b61d57438499589e4d6f5b1320a6bd0eee1a2226d3f8d22d81aa`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 211.7 KB (211719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad9a1996f006554091faad0788cedfe9c37ce442aefa430c0d7b7a7eb402280`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531998ea71dc30b5a286d51c478a1a6f9ff8db7afc074c302dfe6bef2f5da69d`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:862cc3f862cc8485517ddae23f0011c8077ff7e8af04033ea81bdf7b1da1a9c6
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
$ docker pull spiped@sha256:cf4ddd6a6c44691ed6859d574a20ef59ef698ae3f037b7df1ebfa28b8b8bd1f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf52c9298823b1f18acb17148cc5b3ebdbd75089de16ae1130205dbb9aafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:16:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 14:16:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 14:16:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 14:17:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 14:17:03 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 14:17:03 GMT
WORKDIR /spiped
# Tue, 14 May 2024 14:17:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 14:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 14:17:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a82628b598b9cce8ec64537611dcedbe90af99841cdb49e58d721b32483729`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1143c09313a2d7e6f5baee62a732edda947d3623f822103d7a0d387b3d5b79`  
		Last Modified: Tue, 14 May 2024 14:17:19 GMT  
		Size: 2.6 MB (2592087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55108b9e1b391323c605eb1ee0685ffba653fb2af66003cffdecdff25ae3a56b`  
		Last Modified: Tue, 14 May 2024 14:17:20 GMT  
		Size: 6.5 MB (6475264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80206eeb4def215391eef90fe876b1c36cf988e9541137626622f3dfe617fc`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e3cf85dc49c2c5b7913c7eccbeb21a31572d56162310926d29b4a4da4f727d`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:80cea41eb10539a9614cf8d3bce942e421a8d4bbe7afcc76a184794f2e90e0b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f9030fa7ad2788e7b672a14a95c165cb3f2fcbf6d4a1a1476c8ee00af7a593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:42:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:42:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:42:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:42:37 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:42:37 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:42:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6777bbed6c805551e42c47e87032e740c5eedc8cadbf77dad9b8e8ce511606f`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417f02f1db7a09b0e9d5825f84ee133a3f893a14453713c8ff8bdd0ae044aa2`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 2.2 MB (2186969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464ba5d70c3dca39b17e559d73d2d6487a5b2e8bd876d640e4c5b0ec69b24159`  
		Last Modified: Tue, 14 May 2024 07:42:49 GMT  
		Size: 5.1 MB (5142325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9019ad88684b9f4c3d1f49972424b0293510ab9e06d759775629fc6b0e24b`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdf89f322e59ce594f65f2ca1a07971adc5c5c87caa1596e860953c16477bf8`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:735a8a603975528c3c97c5d7d9483954e59479d5dfd9d004de05b9a8c21b10eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31672192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa20a67e38ed4bead4a3dd6430fd2f1c3769bdef70b0cf5fb931f2c84d572d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:28:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 09:28:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:28:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 09:28:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 09:28:54 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 09:28:54 GMT
WORKDIR /spiped
# Tue, 14 May 2024 09:28:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 09:28:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a4cf67b1b0dbe745e9aa40fa5f87e52c1c82885299efbbc72f32c0cee35433`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dd0b66ddc27047a4a5855335209c7516484db200e84db320f73729200a97be`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 2.0 MB (2046404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e382aa9af357b420a0175272654caba9cccb79f1e60eb7046e58e8254bb449b`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 4.9 MB (4883986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fea207b8cc3f715368994f5d85c6fcf99dab41e6011c51316c4c824e3e304`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe8d5d653b76bafa5139bf4f66f348e0018600f0c4f700257f9321a9426e9fc`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:2d26a994ce529bacb0c6a4582bd38f688cf540b418a9891ee25758ab72e8c9c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab23d111d60dd2cf3472be5b49d62f48d5ee126f0eb0b1c00c0feeabfec0820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:34:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:34:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:35:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:35:06 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:35:06 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:35:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:35:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c383b8fe43238b1fad5f3e216bd4661862b04dca14f2f6c25ba2ddc8f76a3910`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a6bfc68a06eaa7e7db9542db2e0b93ea49bdb46dc931a06c449b56e49bbb2f`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 2.4 MB (2435061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1914712040941e6fe19a7257a9d1f780dd56d7d8d98ccc2a5e1d4be2fa36e7ec`  
		Last Modified: Tue, 14 May 2024 07:35:22 GMT  
		Size: 5.5 MB (5485266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262a48740e860bd3d023e3526fe6eea2a5b156dafb90337e0e9e719ae03914e5`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efec22567cdd2ff09d813eb9509399603c62df9074669e4d4f72608d7d1063b4`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:d118a30f85973d9624c09d24791175edadcf7bd64daa760de5433d37ffff4267
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38697698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d6cb7c219e62868baaca89c97d2082759b1b34f4c1b33904bd06687f78ef39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:59:24 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 08:59:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 08:59:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 08:59:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 08:59:58 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 08:59:58 GMT
WORKDIR /spiped
# Tue, 14 May 2024 08:59:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 08:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 08:59:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b467928807c0e563a54f8670c91eca71e6fd926ffa244c927c62d0db86a39d82`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2177ea79a0f66474ae7a368cea82d1058ead17203d1ce58d4c971d7b3caaf`  
		Last Modified: Tue, 14 May 2024 09:00:16 GMT  
		Size: 2.6 MB (2588290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c20f7da89678592d46e8ebeeb4f876239229f927e886826e9f1c570f3c2769`  
		Last Modified: Tue, 14 May 2024 09:00:17 GMT  
		Size: 5.9 MB (5945172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4522d4f258a1969fb9e707a784d8b90b7051f3c02ee3cc80873d216ea3857`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e536d0d133fe4da2515e6ce89465a852fa25d4a16286ad6af8bb449723fdf1a`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

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

### `spiped:1.6.2` - linux; ppc64le

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

### `spiped:1.6.2` - linux; s390x

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

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:6e421e250586c16849e386519b6835425c114526c56dd8bbd77d6cedda957f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:07e3b4b9207f89998e572bed22a7f7954cc6492c8d8f21be279963f2cff7fc9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3855418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9201d18866bb1ce0bb8b2535a09c9746ee4710bbfc2f2c1ab380e1ab464c476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 02:34:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 02:34:48 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 02:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 02:34:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 02:34:59 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 02:34:59 GMT
WORKDIR /spiped
# Fri, 24 May 2024 02:34:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 02:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 02:34:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b65a0cef07ed27e2dfa105666ab73da30ede8da8ec1d6a4aff22c6d64a5905`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 984.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79dadf24bbac85056299fdc71ca82aa8bdc1d5e88edfbaded02869e0b489815`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef14f04bed6dd2107fa0c48cff8ac4c26d9c72582967c37fba6b6641ee53628a`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 224.3 KB (224301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512d6a117eb4435d549b47b5d8cae78953c96f8a91d9420fa806decbd655936`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b384b7559504371850eed3815c8be24a48bbf848e4f8181a30e96853c6af3f1`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5d9da313669f8f0048ec2e9eab6bf853600283a81b4ca96e692b10bdb3c72bdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ca2a16641057fa841612e468f82aa3487de7f1198cfad469dcf99446926816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 00:49:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 25 May 2024 00:49:30 GMT
RUN apk add --no-cache libssl3
# Sat, 25 May 2024 00:49:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 25 May 2024 09:53:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 25 May 2024 09:53:05 GMT
VOLUME [/spiped]
# Sat, 25 May 2024 09:53:05 GMT
WORKDIR /spiped
# Sat, 25 May 2024 09:53:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 25 May 2024 09:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 May 2024 09:53:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc224dd751252e9181a8cfc90f8cc478007dd80c5fcaf9c0e7365c5c5690cd6`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d844205e2c4ed91d86c9d3b93ba94f73a6802f7d95e2637329e3171f1596051`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf50783437084d308ea037a336c6b2adde912eb87c2d0910d52f8259d2ccd361`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 209.0 KB (208990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e446f34a875f7f58e4f0ff44cdfc7c4fa476269342e24e5cd4b066bf0fd56db5`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973efe8383e26e010949975c4c577788da3b889331852a53e975fdd74591d73`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:25599ac7da2bbcb6630557d1d39c0d42ba4e82abb1faca8c8d5416b6c9355639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e776a6cafa9ea09db267caf77626a5486302739cab2a69c06021f6f020bc38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:08:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:08:47 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:08:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:08:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:08:59 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:08:59 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57dde9a22f05f8d3d8c1a8a13dc73487a9cde1413d04a2f0921d0b629c3e8`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b15fc10ac651a8f9a2a48b8fa00251a8fac4dcb9d04570226980e7f64e8f09`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c206c9d5ca56d7e0dfb79bbf3513d4b64cd649c95da66330942faada9b5be4c`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 202.6 KB (202557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb12eda4f30ee29354c5c954d72d1201f6189aa39214e279ea95a1139d20706`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3301f3fd425a130e1103ae1c59693e259c0aa61c4457150fbb86acf87164bb9`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ee22a4376163469a5478a77d3dd086da10e96bab2415e92cb213ce08dee1701e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7161188ee6d2c07e0c2f1fc2a6fb5a02c590873473230245a1f9a46ad49f8791`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 01:17:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 01:17:10 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 01:17:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 01:17:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 01:17:18 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 01:17:18 GMT
WORKDIR /spiped
# Fri, 24 May 2024 01:17:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 01:17:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 01:17:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f90aa9bfc773d7ce92ca3bf50d8ae635c7d9f78892f0b93b65803c9d33b1a`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b9605849ac73a8379695848d7a0520038c21b1c2ebf31e40beda1b53f9fe9`  
		Last Modified: Fri, 24 May 2024 01:17:30 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099b3f4d764b8b79d94713e5d3320da1b4822ef27f9af0f3149655d12aa47d`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 219.0 KB (218970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b21ae2d8249251716fb673e50c2e09cda47bc565d7eebd5fe3efa053d5eac6`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236abc558b7bcb1712f41161eaaaecbf399e7eaf1b2aa8094cddd334c4f6872e`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 337.0 B  
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
$ docker pull spiped@sha256:f7be193e91b7536b291aff1af811715f1994df5d1ff50e7e01ac61438ce971b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6123bf450568ccf383fc60e3066c5d8216950f96a0d14b76f8751ddc829569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:09:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:09:15 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:09:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:09:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:09:25 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:09:25 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416f94511c6e98b05f9acca81a2233b2167b904c9be9084f8782e7fee8c030da`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afb72e562d3649f63864604b0551f222f5fe0fd3061dc2d2039e65aa5873a2e`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 7.6 KB (7590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8756affa07ec356f000450e4e65d82e98d038ff03a81c67470272d6e4f30e72d`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 222.9 KB (222928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b978619b6227e9697ca0875eb4b8b47a1b84aa7b4cc5f9eb6e8c5aebf8921`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d5f1d461a5a0e946207612f37d9fdecbffe6ff7b8a528dd00968ac1594b162`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:cd5a4621afff483f36101ea9ebae88f7dcf25f86c2309d723bbd483be19ceafe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e812e801b6ae16522a84a7ab6f7556c16c0a15341d272fce6510208bf865f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 04:22:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 May 2024 04:22:11 GMT
RUN apk add --no-cache libssl3
# Wed, 29 May 2024 04:22:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 May 2024 04:23:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 May 2024 04:23:18 GMT
VOLUME [/spiped]
# Wed, 29 May 2024 04:23:19 GMT
WORKDIR /spiped
# Wed, 29 May 2024 04:23:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 May 2024 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 04:23:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c0c4f99ba3a3946abd6a4741459ac597ecf8393da29611c0c72c127c3c8fc6`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5b031480a0383a5f02d1f22612813b1ffa3cfb8ac50bda5bca486fdbf7499`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e17de0f3b7417191ea5c8f7779379c7965a389e87d7fddba3c8d28d6f854c`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 215.3 KB (215290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7d27f6c07e7feb513acf854ddaee65e51ce92daf7c3918f1625aaec5fa14b`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e20db4a7ebcccd41cb86827aeddf9cb92dfc787970bf9623b4779f5bf8559`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8dec41cbe81f417096082fdaa31bb95bdd7e36dfec4cc462a7e9462205ed2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee6531c62c7ffe07b640d5ab5b763be7303e38a61c81bb6524855dec0ca243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 00:57:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 00:57:59 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 00:57:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 00:58:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 00:58:05 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 00:58:05 GMT
WORKDIR /spiped
# Fri, 24 May 2024 00:58:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 00:58:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d2acf9b7465edffd5a10fedbf230b30c81cb8b13eb3c7d97b4ba3dc542d17`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbc970af29f74dd00097324a2d43d0cd4ea77aee3bf1217ffe3b76397a889`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec7c94b7827b61d57438499589e4d6f5b1320a6bd0eee1a2226d3f8d22d81aa`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 211.7 KB (211719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad9a1996f006554091faad0788cedfe9c37ce442aefa430c0d7b7a7eb402280`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531998ea71dc30b5a286d51c478a1a6f9ff8db7afc074c302dfe6bef2f5da69d`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:6e421e250586c16849e386519b6835425c114526c56dd8bbd77d6cedda957f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:07e3b4b9207f89998e572bed22a7f7954cc6492c8d8f21be279963f2cff7fc9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3855418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9201d18866bb1ce0bb8b2535a09c9746ee4710bbfc2f2c1ab380e1ab464c476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 02:34:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 02:34:48 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 02:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 02:34:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 02:34:59 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 02:34:59 GMT
WORKDIR /spiped
# Fri, 24 May 2024 02:34:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 02:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 02:34:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b65a0cef07ed27e2dfa105666ab73da30ede8da8ec1d6a4aff22c6d64a5905`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 984.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79dadf24bbac85056299fdc71ca82aa8bdc1d5e88edfbaded02869e0b489815`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef14f04bed6dd2107fa0c48cff8ac4c26d9c72582967c37fba6b6641ee53628a`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 224.3 KB (224301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512d6a117eb4435d549b47b5d8cae78953c96f8a91d9420fa806decbd655936`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b384b7559504371850eed3815c8be24a48bbf848e4f8181a30e96853c6af3f1`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5d9da313669f8f0048ec2e9eab6bf853600283a81b4ca96e692b10bdb3c72bdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ca2a16641057fa841612e468f82aa3487de7f1198cfad469dcf99446926816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 00:49:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 25 May 2024 00:49:30 GMT
RUN apk add --no-cache libssl3
# Sat, 25 May 2024 00:49:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 25 May 2024 09:53:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 25 May 2024 09:53:05 GMT
VOLUME [/spiped]
# Sat, 25 May 2024 09:53:05 GMT
WORKDIR /spiped
# Sat, 25 May 2024 09:53:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 25 May 2024 09:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 May 2024 09:53:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc224dd751252e9181a8cfc90f8cc478007dd80c5fcaf9c0e7365c5c5690cd6`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d844205e2c4ed91d86c9d3b93ba94f73a6802f7d95e2637329e3171f1596051`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf50783437084d308ea037a336c6b2adde912eb87c2d0910d52f8259d2ccd361`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 209.0 KB (208990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e446f34a875f7f58e4f0ff44cdfc7c4fa476269342e24e5cd4b066bf0fd56db5`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973efe8383e26e010949975c4c577788da3b889331852a53e975fdd74591d73`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:25599ac7da2bbcb6630557d1d39c0d42ba4e82abb1faca8c8d5416b6c9355639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e776a6cafa9ea09db267caf77626a5486302739cab2a69c06021f6f020bc38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:08:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:08:47 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:08:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:08:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:08:59 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:08:59 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57dde9a22f05f8d3d8c1a8a13dc73487a9cde1413d04a2f0921d0b629c3e8`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b15fc10ac651a8f9a2a48b8fa00251a8fac4dcb9d04570226980e7f64e8f09`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c206c9d5ca56d7e0dfb79bbf3513d4b64cd649c95da66330942faada9b5be4c`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 202.6 KB (202557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb12eda4f30ee29354c5c954d72d1201f6189aa39214e279ea95a1139d20706`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3301f3fd425a130e1103ae1c59693e259c0aa61c4457150fbb86acf87164bb9`  
		Last Modified: Wed, 05 Jun 2024 23:09:16 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ee22a4376163469a5478a77d3dd086da10e96bab2415e92cb213ce08dee1701e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7161188ee6d2c07e0c2f1fc2a6fb5a02c590873473230245a1f9a46ad49f8791`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 01:17:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 01:17:10 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 01:17:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 01:17:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 01:17:18 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 01:17:18 GMT
WORKDIR /spiped
# Fri, 24 May 2024 01:17:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 01:17:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 01:17:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f90aa9bfc773d7ce92ca3bf50d8ae635c7d9f78892f0b93b65803c9d33b1a`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b9605849ac73a8379695848d7a0520038c21b1c2ebf31e40beda1b53f9fe9`  
		Last Modified: Fri, 24 May 2024 01:17:30 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099b3f4d764b8b79d94713e5d3320da1b4822ef27f9af0f3149655d12aa47d`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 219.0 KB (218970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b21ae2d8249251716fb673e50c2e09cda47bc565d7eebd5fe3efa053d5eac6`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236abc558b7bcb1712f41161eaaaecbf399e7eaf1b2aa8094cddd334c4f6872e`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 337.0 B  
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
$ docker pull spiped@sha256:f7be193e91b7536b291aff1af811715f1994df5d1ff50e7e01ac61438ce971b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6123bf450568ccf383fc60e3066c5d8216950f96a0d14b76f8751ddc829569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 23:09:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 05 Jun 2024 23:09:15 GMT
RUN apk add --no-cache libssl3
# Wed, 05 Jun 2024 23:09:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Jun 2024 23:09:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 05 Jun 2024 23:09:25 GMT
VOLUME [/spiped]
# Wed, 05 Jun 2024 23:09:25 GMT
WORKDIR /spiped
# Wed, 05 Jun 2024 23:09:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Jun 2024 23:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 23:09:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416f94511c6e98b05f9acca81a2233b2167b904c9be9084f8782e7fee8c030da`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afb72e562d3649f63864604b0551f222f5fe0fd3061dc2d2039e65aa5873a2e`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 7.6 KB (7590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8756affa07ec356f000450e4e65d82e98d038ff03a81c67470272d6e4f30e72d`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 222.9 KB (222928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b978619b6227e9697ca0875eb4b8b47a1b84aa7b4cc5f9eb6e8c5aebf8921`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d5f1d461a5a0e946207612f37d9fdecbffe6ff7b8a528dd00968ac1594b162`  
		Last Modified: Wed, 05 Jun 2024 23:09:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:cd5a4621afff483f36101ea9ebae88f7dcf25f86c2309d723bbd483be19ceafe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e812e801b6ae16522a84a7ab6f7556c16c0a15341d272fce6510208bf865f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 04:22:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 May 2024 04:22:11 GMT
RUN apk add --no-cache libssl3
# Wed, 29 May 2024 04:22:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 May 2024 04:23:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 May 2024 04:23:18 GMT
VOLUME [/spiped]
# Wed, 29 May 2024 04:23:19 GMT
WORKDIR /spiped
# Wed, 29 May 2024 04:23:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 May 2024 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 04:23:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c0c4f99ba3a3946abd6a4741459ac597ecf8393da29611c0c72c127c3c8fc6`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5b031480a0383a5f02d1f22612813b1ffa3cfb8ac50bda5bca486fdbf7499`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e17de0f3b7417191ea5c8f7779379c7965a389e87d7fddba3c8d28d6f854c`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 215.3 KB (215290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7d27f6c07e7feb513acf854ddaee65e51ce92daf7c3918f1625aaec5fa14b`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e20db4a7ebcccd41cb86827aeddf9cb92dfc787970bf9623b4779f5bf8559`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8dec41cbe81f417096082fdaa31bb95bdd7e36dfec4cc462a7e9462205ed2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee6531c62c7ffe07b640d5ab5b763be7303e38a61c81bb6524855dec0ca243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 00:57:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 00:57:59 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 00:57:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 00:58:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 00:58:05 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 00:58:05 GMT
WORKDIR /spiped
# Fri, 24 May 2024 00:58:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 00:58:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d2acf9b7465edffd5a10fedbf230b30c81cb8b13eb3c7d97b4ba3dc542d17`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbc970af29f74dd00097324a2d43d0cd4ea77aee3bf1217ffe3b76397a889`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec7c94b7827b61d57438499589e4d6f5b1320a6bd0eee1a2226d3f8d22d81aa`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 211.7 KB (211719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad9a1996f006554091faad0788cedfe9c37ce442aefa430c0d7b7a7eb402280`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531998ea71dc30b5a286d51c478a1a6f9ff8db7afc074c302dfe6bef2f5da69d`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:862cc3f862cc8485517ddae23f0011c8077ff7e8af04033ea81bdf7b1da1a9c6
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
$ docker pull spiped@sha256:cf4ddd6a6c44691ed6859d574a20ef59ef698ae3f037b7df1ebfa28b8b8bd1f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf52c9298823b1f18acb17148cc5b3ebdbd75089de16ae1130205dbb9aafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:16:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 14:16:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 14:16:39 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 14:17:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 14:17:03 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 14:17:03 GMT
WORKDIR /spiped
# Tue, 14 May 2024 14:17:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 14:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 14:17:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a82628b598b9cce8ec64537611dcedbe90af99841cdb49e58d721b32483729`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1143c09313a2d7e6f5baee62a732edda947d3623f822103d7a0d387b3d5b79`  
		Last Modified: Tue, 14 May 2024 14:17:19 GMT  
		Size: 2.6 MB (2592087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55108b9e1b391323c605eb1ee0685ffba653fb2af66003cffdecdff25ae3a56b`  
		Last Modified: Tue, 14 May 2024 14:17:20 GMT  
		Size: 6.5 MB (6475264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80206eeb4def215391eef90fe876b1c36cf988e9541137626622f3dfe617fc`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e3cf85dc49c2c5b7913c7eccbeb21a31572d56162310926d29b4a4da4f727d`  
		Last Modified: Tue, 14 May 2024 14:17:18 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:80cea41eb10539a9614cf8d3bce942e421a8d4bbe7afcc76a184794f2e90e0b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34240807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f9030fa7ad2788e7b672a14a95c165cb3f2fcbf6d4a1a1476c8ee00af7a593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:42:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:42:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:42:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:42:37 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:42:37 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:42:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6777bbed6c805551e42c47e87032e740c5eedc8cadbf77dad9b8e8ce511606f`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417f02f1db7a09b0e9d5825f84ee133a3f893a14453713c8ff8bdd0ae044aa2`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 2.2 MB (2186969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464ba5d70c3dca39b17e559d73d2d6487a5b2e8bd876d640e4c5b0ec69b24159`  
		Last Modified: Tue, 14 May 2024 07:42:49 GMT  
		Size: 5.1 MB (5142325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9019ad88684b9f4c3d1f49972424b0293510ab9e06d759775629fc6b0e24b`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdf89f322e59ce594f65f2ca1a07971adc5c5c87caa1596e860953c16477bf8`  
		Last Modified: Tue, 14 May 2024 07:42:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:735a8a603975528c3c97c5d7d9483954e59479d5dfd9d004de05b9a8c21b10eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31672192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa20a67e38ed4bead4a3dd6430fd2f1c3769bdef70b0cf5fb931f2c84d572d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:28:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 09:28:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:28:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 09:28:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 09:28:54 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 09:28:54 GMT
WORKDIR /spiped
# Tue, 14 May 2024 09:28:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 09:28:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 09:28:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a4cf67b1b0dbe745e9aa40fa5f87e52c1c82885299efbbc72f32c0cee35433`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dd0b66ddc27047a4a5855335209c7516484db200e84db320f73729200a97be`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 2.0 MB (2046404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e382aa9af357b420a0175272654caba9cccb79f1e60eb7046e58e8254bb449b`  
		Last Modified: Tue, 14 May 2024 09:29:08 GMT  
		Size: 4.9 MB (4883986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fea207b8cc3f715368994f5d85c6fcf99dab41e6011c51316c4c824e3e304`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe8d5d653b76bafa5139bf4f66f348e0018600f0c4f700257f9321a9426e9fc`  
		Last Modified: Tue, 14 May 2024 09:29:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:2d26a994ce529bacb0c6a4582bd38f688cf540b418a9891ee25758ab72e8c9c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab23d111d60dd2cf3472be5b49d62f48d5ee126f0eb0b1c00c0feeabfec0820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:34:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 07:34:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 07:35:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 07:35:06 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 07:35:06 GMT
WORKDIR /spiped
# Tue, 14 May 2024 07:35:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 07:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 07:35:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c383b8fe43238b1fad5f3e216bd4661862b04dca14f2f6c25ba2ddc8f76a3910`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a6bfc68a06eaa7e7db9542db2e0b93ea49bdb46dc931a06c449b56e49bbb2f`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 2.4 MB (2435061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1914712040941e6fe19a7257a9d1f780dd56d7d8d98ccc2a5e1d4be2fa36e7ec`  
		Last Modified: Tue, 14 May 2024 07:35:22 GMT  
		Size: 5.5 MB (5485266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262a48740e860bd3d023e3526fe6eea2a5b156dafb90337e0e9e719ae03914e5`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efec22567cdd2ff09d813eb9509399603c62df9074669e4d4f72608d7d1063b4`  
		Last Modified: Tue, 14 May 2024 07:35:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:d118a30f85973d9624c09d24791175edadcf7bd64daa760de5433d37ffff4267
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38697698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d6cb7c219e62868baaca89c97d2082759b1b34f4c1b33904bd06687f78ef39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:59:24 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 14 May 2024 08:59:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 08:59:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 14 May 2024 08:59:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 14 May 2024 08:59:58 GMT
VOLUME [/spiped]
# Tue, 14 May 2024 08:59:58 GMT
WORKDIR /spiped
# Tue, 14 May 2024 08:59:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 14 May 2024 08:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 08:59:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b467928807c0e563a54f8670c91eca71e6fd926ffa244c927c62d0db86a39d82`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2177ea79a0f66474ae7a368cea82d1058ead17203d1ce58d4c971d7b3caaf`  
		Last Modified: Tue, 14 May 2024 09:00:16 GMT  
		Size: 2.6 MB (2588290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c20f7da89678592d46e8ebeeb4f876239229f927e886826e9f1c570f3c2769`  
		Last Modified: Tue, 14 May 2024 09:00:17 GMT  
		Size: 5.9 MB (5945172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4522d4f258a1969fb9e707a784d8b90b7051f3c02ee3cc80873d216ea3857`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e536d0d133fe4da2515e6ce89465a852fa25d4a16286ad6af8bb449723fdf1a`  
		Last Modified: Tue, 14 May 2024 09:00:15 GMT  
		Size: 341.0 B  
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
