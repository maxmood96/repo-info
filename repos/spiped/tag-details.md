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
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
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
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
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
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
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
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:39a83d33d159f195029258c4b2f0b1071b886fc4f896554b5a046ce55b6e9e05
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
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
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9fd87268d09ea1b26486f155294d0b6f48bdffa6d2c205cbc5053eef7487cfe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aeaff450dfe5f24cec848e858eaa6c3915bad30abd15082ec0b6c23d06795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:42:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 22:42:24 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 22:42:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 22:42:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 22:42:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 22:42:30 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 22:42:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 22:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 22:42:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71169b8b2b22fc0c4a5fbf4c96cd876c8ce6b26beb724b80e17790abc67dc9b7`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb94937dc469250ad8e4bb9adeb55585854d5f364518959c7b996f9d9f8a53`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 1.2 MB (1221495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f434acef5237b2162bda5a532bf9e53b1f99ec8aba26e919487f4b2e923577`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 208.6 KB (208644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f359de674f97e161c3447839d262cc4b15930b2c79d39853371852c6ea64fa9`  
		Last Modified: Sat, 16 Mar 2024 22:43:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c5f9156e70d491cf1b9c5d39ef773f50bc189d6bc53a6a1fbfda351828a18`  
		Last Modified: Sat, 16 Mar 2024 22:43:39 GMT  
		Size: 341.0 B  
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
