<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.4`](#spiped164)
-	[`spiped:1.6.4-alpine`](#spiped164-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:ce16a3780001f91acee7a5318152cf2fdb7f77a9f9efbdf7c9d42624b7d9c398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:fea99c454ce0fbe794959c712b9aa8211a59ec36d96ba4ec47e615983a02df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61044b76967f0bfbd214c3f0c337a70e34bd5e0113b94ee6aee969afe8ae0c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc238e6158ba23ca3c78f09a916e5b8debcb8fc98435ef72ed1372e4a10d36f0`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631db32462bfbb6f6adbfce206c84ea557ef848ce2db5acbc296919b1e2fb8`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfab92e44961e7c708e76600cd2a58da46309cb1585752de3faf3cf12144b9b`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 7.0 MB (7048278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723c6fe89d1ee4486ae7f1aba339a847174340058a9aafba610b8f5d08c392a`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc283d4e51af75c91b14cfc4325a4b783724ecdd9ac3d936db49437b45069`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:9c5b20ad1230caec7f7f817835a32a8e84c0749bb0cec2f1338c9f94d9cafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39fc5ab26c741f2fadea946a1e3f5f8d5f57b2c46254f39a4cf3dec01016afc`

```dockerfile
```

-	Layers:
	-	`sha256:6162c674076105e040975f2f9084082ad1c95d3491863ccfc1a758ad44af0f88`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e718aeb59e0ddcdc8ae0d260d22d1e426d5f84484cbe07357ab801c3c2ae2ac`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0ae5335373d50afd2ebe6afcfa6f6be07e82a19bded4d420d96db3555cf6df5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33737857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1987049a10433f61f985c8a961f2a43c8f01aec18c6d80152fa3fbc3c38a2bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e9eedd2de38e34f9c3259b80e737fa7ffbfb18c38b1f08d50dbb49345eb0d7`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c241ba477fd0194fc32c7ae4f77367d65f7cc4dc492ba06ee414e5e2e1769`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62532e7e306eaf6c857c1dcac69b720b1f9d66d14712934fe28bf0a4be73f567`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 5.8 MB (5789345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfaf6902331c4ccad828cfb4d679d658a030950d2c261496bd7e99ee3522ce2`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe9a7ee86cc167f3246c7ccbaca7e78f1107bcb72fdff9d7524c789bdafd50`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:505d2a98a8941d45aca76abca0104a7e8d398561b1ae7927db969818fbfe2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444672c549748ba8acd59e1603ca69ca9739f52248e1194cd651561d40623efa`

```dockerfile
```

-	Layers:
	-	`sha256:5fb828ad140b7db9b7197a184f66219daa0cac03e3e22a9ec8a4419674b5f497`  
		Last Modified: Tue, 30 Sep 2025 07:04:22 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadb488ef6180819b4864740433eb5e2bd6a3c663387cd05aea5ae85c0d45596`  
		Last Modified: Tue, 30 Sep 2025 07:04:23 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e1cbc8dd0e0dd1d11dcd2e91b74f72b061b6f7a0e9866f8db6c6d01e53d0cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31799710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b584a05bc5a36361a150d614c57ef195e48343081cadd05fe2b0d359e8222`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797f6a658761eae62ed9bd79e1c2e88e731aa6bfefc3880e9b1db206648e59d`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6f0ef72b36a4c660b1f283e3b24a699e315d67f621b453e96e9409d81cc56b`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540e53f5a976b4fd01fcdbb30203a9b777b0f90275315ec34c995a73d288d6b`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 5.6 MB (5584592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b18fa5e02aa57bd7e2669c537eab73247a3828b4525b21b63efc33fc4fe383`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3424719f3c5ef07c1120d5ec07677a2845f8b2d0ef696b2d0c6df065e7256365`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:c23578978a201a21a792164719d8288c21cc5bd23ee2f2edbc21e35c712f002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fe98bdde4a887388e84e89c0aacdf7acb8eb5d8f584a9d0bbb8d6657033d3`

```dockerfile
```

-	Layers:
	-	`sha256:238ce2a67002b5d15d9cfb00195afa1ff16e285c1ce5686c02a79faa79411471`  
		Last Modified: Wed, 01 Oct 2025 22:04:31 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949b594d27935fbfd7f4a1995c730838a20f5c97e5dde2310a58c62179762e49`  
		Last Modified: Wed, 01 Oct 2025 22:04:32 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9c14d801535964b9856cc995b5cc1d953e664d4d36a29226d0b525ebd12fc23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3760e5d3e931c335d1ba762156bad16c786221e38cc064a049bffad16061ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138cafb84902697aa37bc68f6f860c44a9a11d9b9a83a6c59384a6946bfb5073`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a73645b11d1149fdeaeb95abee773ad6067bb95726c22f35387d4b849d93568`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2201eaba239855e7b70ec7db2b53e68c5437be9fc29a5048b5cec95d4357005`  
		Last Modified: Tue, 30 Sep 2025 00:13:19 GMT  
		Size: 6.2 MB (6231836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b71e07b92ddd3ea16e307a436f84f0862f6d41ce6e60c918112b5004eacd7`  
		Last Modified: Tue, 30 Sep 2025 00:13:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c64c105923c5d37d4fa6700dee51a52780c755bfba3de0ac42ccf55d9c80ce0`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:9bc13bf85136708d05c74af3dfc16259959b0610a6cae025c7f9013c1e36d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb9ea2712f520f693ab118515cba89588115d9457cb6fc3051b4f69abe0cb5`

```dockerfile
```

-	Layers:
	-	`sha256:67ff2bdb0f88eae236c4d226ffb071064078a72edf0c36dbc9605931b2873702`  
		Last Modified: Wed, 01 Oct 2025 13:04:28 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa507c4eeada3b5ef073dc36105783217730a9444ef304a477a6297a951cebe2`  
		Last Modified: Wed, 01 Oct 2025 13:04:29 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:3483553c118f803d7dc6a6c85ba75a6757cf336c0fcdce07857d0a1ca40b5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fb778095be09981fa712b92b08229fb6c016edeac9681a10e3d7ceaa3d67e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b683a27da0ff4f41706867fe165539c8b1d4170671892b8376bb380a96382`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16959a1fc618d2ae9b84f6d83c71e630edc85d191636b48932f2f1aa95ecf3ae`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd39dff5263a0f9cae965c7539aca9f51ec3b9f5224265f80015a145df9f2cc7`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 6.4 MB (6442337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41989a27b3616713951399c9446e9fedc876ac4bae34f2143fa0833b64bd5886`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e5b5f97c64972331e5b1e53b8a01934b0013551e3c28790fc7e13f0dfebd`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:5c3bc443e4a2f479f89ee155cbe841e2d63cc9294c3aa888fc64457bea94a474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a6fde58a78a8df0407f92615908cc35805714e3a1671a66bdd5d5353c72832`

```dockerfile
```

-	Layers:
	-	`sha256:480cb796d2b5b5d888e607bb45d255e462c4690fb64e54f2721250e19ed909aa`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a547b0a456597261657868e2d4ae927c47a163fda68183e21e9e32adb52c96f5`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:c5b3f79371b3d7ff8f9e4bbc41f348539977b5654f1de79061ec53da86a2563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab34c773cbd45451d188b0fc586243e9ddabeba95f34d0a3fe2ab3eb9668073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a521cfb00afa1f22bd5d97b85ad1720879ee5c0b1baab105f52e4860ec7cb`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ff4669d4781473da0924bb50912f548111551b9b5f03299c1b3c476c31795`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77cbf7134214650d99819f0a9af3301695acf4eaa87494d06ed137216f6dd03`  
		Last Modified: Wed, 01 Oct 2025 19:48:07 GMT  
		Size: 6.8 MB (6840251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f16a31134cd2b56611423f586a6bf111aa53bd8afd8bdaafa3815fbae142d`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b21ea73e2977d5c531615088cb9bf1fa9b673f9a4a73159745d3775b9be25c`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:c1257c6861ac64a590f57df8457c5341ce92804291bcf17f2e526d6cf56f30e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a512f85e4c6debb71b1588d50653364b97ef66ecf26e492d16906c6f02d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:2e693f388098945d670d6d7401d2c73d30208c04a9c434f89128a9257051cad6`  
		Last Modified: Wed, 01 Oct 2025 22:04:41 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fe9e313181c313debecbb9cfd10ea888761ba52ba83d75c155e7f24b2c4c0`  
		Last Modified: Wed, 01 Oct 2025 22:04:42 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:63c81e7a01da08fe2456c4fe9380a75306824b5e09e202e7c8c48a955ef67681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d07a35af2ecef1d379d7de3e2682368da4fbefb910ec3cd0543c9702ba1cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fdd8b049eb029577d94c03617e2a21858508fc5e580623cc21f55413af7350`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2785eaaf3b19c0d99a6cd261f54682df997b7f9e8accbab631417bedbbe11e`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e4c78f116c60eebba9d5a01de232d21fdc151c6c160765cdd45131ac57266d`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 9.4 MB (9358166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5280abb5bee4d4bac9b5e9874666be22133b46530de1b9bfdf616d9bbefaa34`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a4b562d5e2bd3a63858fa9ad791651dc993419da3712ec490f3c0437d9c81`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:fefbe28311f558c8f0bd34fd6ae277e561a9fba8dccbb5c370b5ae8d06f0ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946cc255ef0e663aba1c9b13f58f3e2ef6b22802d595e60c1a905b7c9f8d81e`

```dockerfile
```

-	Layers:
	-	`sha256:0f8800600e75cda5489b2d17ddd9ec37a58ad1f1223410df7742af5d2f47beaa`  
		Last Modified: Wed, 01 Oct 2025 19:04:43 GMT  
		Size: 3.6 MB (3613221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea670935804f907c5c8108973c916a79cd259c3ef65e26b1505d0e684c44599`  
		Last Modified: Wed, 01 Oct 2025 19:04:44 GMT  
		Size: 15.1 KB (15072 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:0f938721daf08c239ba32eb210482941a1f07269b403c500e3eb132911dcb44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35960783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a850e3bdd587415e9e20969ef6ce52c0faccac714e602b10f9bf1d2b0dfb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470e100e87fb0737d8813ad701db233de34e7eda3bc7a5e347182edb96fc07b7`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef1e4cab10fc5f2a92736f192b67f9fc080966aa9ed2c1f50b7e11829520c0`  
		Last Modified: Tue, 30 Sep 2025 09:24:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df0b2c4d2fdf31e6e7d55fa1d672759b5244e49159f022163b746b96993bca3`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 6.1 MB (6121187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b089a06826b0a24ec162778fc2d01554cd54c34862516f04dcd2dd9ccd403`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d77df7c01beee6fc002cc7aa3c14a701e7f5700b06926f27e143c76a4b4ad2`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:989260bf82df9044c638bd7e2ffd082c84c055e6978c4b777f7ff712cdd195fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e624bfadefdc72db4094fd7c89b27c542616642506962d12a9866c5e9c9829d`

```dockerfile
```

-	Layers:
	-	`sha256:e8ce284c6273618f8501626aaf90218d5b7c16d53c5504f820ceb8845d9247d6`  
		Last Modified: Wed, 01 Oct 2025 22:04:48 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1078258bc1376211e434d54b32dc2978a4b4a468f55cf19901220469ca2edb4f`  
		Last Modified: Wed, 01 Oct 2025 22:04:49 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:ce16a3780001f91acee7a5318152cf2fdb7f77a9f9efbdf7c9d42624b7d9c398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:fea99c454ce0fbe794959c712b9aa8211a59ec36d96ba4ec47e615983a02df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61044b76967f0bfbd214c3f0c337a70e34bd5e0113b94ee6aee969afe8ae0c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc238e6158ba23ca3c78f09a916e5b8debcb8fc98435ef72ed1372e4a10d36f0`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631db32462bfbb6f6adbfce206c84ea557ef848ce2db5acbc296919b1e2fb8`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfab92e44961e7c708e76600cd2a58da46309cb1585752de3faf3cf12144b9b`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 7.0 MB (7048278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723c6fe89d1ee4486ae7f1aba339a847174340058a9aafba610b8f5d08c392a`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc283d4e51af75c91b14cfc4325a4b783724ecdd9ac3d936db49437b45069`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:9c5b20ad1230caec7f7f817835a32a8e84c0749bb0cec2f1338c9f94d9cafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39fc5ab26c741f2fadea946a1e3f5f8d5f57b2c46254f39a4cf3dec01016afc`

```dockerfile
```

-	Layers:
	-	`sha256:6162c674076105e040975f2f9084082ad1c95d3491863ccfc1a758ad44af0f88`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e718aeb59e0ddcdc8ae0d260d22d1e426d5f84484cbe07357ab801c3c2ae2ac`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0ae5335373d50afd2ebe6afcfa6f6be07e82a19bded4d420d96db3555cf6df5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33737857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1987049a10433f61f985c8a961f2a43c8f01aec18c6d80152fa3fbc3c38a2bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e9eedd2de38e34f9c3259b80e737fa7ffbfb18c38b1f08d50dbb49345eb0d7`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c241ba477fd0194fc32c7ae4f77367d65f7cc4dc492ba06ee414e5e2e1769`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62532e7e306eaf6c857c1dcac69b720b1f9d66d14712934fe28bf0a4be73f567`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 5.8 MB (5789345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfaf6902331c4ccad828cfb4d679d658a030950d2c261496bd7e99ee3522ce2`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe9a7ee86cc167f3246c7ccbaca7e78f1107bcb72fdff9d7524c789bdafd50`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:505d2a98a8941d45aca76abca0104a7e8d398561b1ae7927db969818fbfe2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444672c549748ba8acd59e1603ca69ca9739f52248e1194cd651561d40623efa`

```dockerfile
```

-	Layers:
	-	`sha256:5fb828ad140b7db9b7197a184f66219daa0cac03e3e22a9ec8a4419674b5f497`  
		Last Modified: Tue, 30 Sep 2025 07:04:22 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadb488ef6180819b4864740433eb5e2bd6a3c663387cd05aea5ae85c0d45596`  
		Last Modified: Tue, 30 Sep 2025 07:04:23 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e1cbc8dd0e0dd1d11dcd2e91b74f72b061b6f7a0e9866f8db6c6d01e53d0cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31799710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b584a05bc5a36361a150d614c57ef195e48343081cadd05fe2b0d359e8222`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797f6a658761eae62ed9bd79e1c2e88e731aa6bfefc3880e9b1db206648e59d`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6f0ef72b36a4c660b1f283e3b24a699e315d67f621b453e96e9409d81cc56b`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540e53f5a976b4fd01fcdbb30203a9b777b0f90275315ec34c995a73d288d6b`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 5.6 MB (5584592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b18fa5e02aa57bd7e2669c537eab73247a3828b4525b21b63efc33fc4fe383`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3424719f3c5ef07c1120d5ec07677a2845f8b2d0ef696b2d0c6df065e7256365`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:c23578978a201a21a792164719d8288c21cc5bd23ee2f2edbc21e35c712f002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fe98bdde4a887388e84e89c0aacdf7acb8eb5d8f584a9d0bbb8d6657033d3`

```dockerfile
```

-	Layers:
	-	`sha256:238ce2a67002b5d15d9cfb00195afa1ff16e285c1ce5686c02a79faa79411471`  
		Last Modified: Wed, 01 Oct 2025 22:04:31 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949b594d27935fbfd7f4a1995c730838a20f5c97e5dde2310a58c62179762e49`  
		Last Modified: Wed, 01 Oct 2025 22:04:32 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9c14d801535964b9856cc995b5cc1d953e664d4d36a29226d0b525ebd12fc23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3760e5d3e931c335d1ba762156bad16c786221e38cc064a049bffad16061ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138cafb84902697aa37bc68f6f860c44a9a11d9b9a83a6c59384a6946bfb5073`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a73645b11d1149fdeaeb95abee773ad6067bb95726c22f35387d4b849d93568`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2201eaba239855e7b70ec7db2b53e68c5437be9fc29a5048b5cec95d4357005`  
		Last Modified: Tue, 30 Sep 2025 00:13:19 GMT  
		Size: 6.2 MB (6231836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b71e07b92ddd3ea16e307a436f84f0862f6d41ce6e60c918112b5004eacd7`  
		Last Modified: Tue, 30 Sep 2025 00:13:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c64c105923c5d37d4fa6700dee51a52780c755bfba3de0ac42ccf55d9c80ce0`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:9bc13bf85136708d05c74af3dfc16259959b0610a6cae025c7f9013c1e36d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb9ea2712f520f693ab118515cba89588115d9457cb6fc3051b4f69abe0cb5`

```dockerfile
```

-	Layers:
	-	`sha256:67ff2bdb0f88eae236c4d226ffb071064078a72edf0c36dbc9605931b2873702`  
		Last Modified: Wed, 01 Oct 2025 13:04:28 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa507c4eeada3b5ef073dc36105783217730a9444ef304a477a6297a951cebe2`  
		Last Modified: Wed, 01 Oct 2025 13:04:29 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:3483553c118f803d7dc6a6c85ba75a6757cf336c0fcdce07857d0a1ca40b5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fb778095be09981fa712b92b08229fb6c016edeac9681a10e3d7ceaa3d67e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b683a27da0ff4f41706867fe165539c8b1d4170671892b8376bb380a96382`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16959a1fc618d2ae9b84f6d83c71e630edc85d191636b48932f2f1aa95ecf3ae`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd39dff5263a0f9cae965c7539aca9f51ec3b9f5224265f80015a145df9f2cc7`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 6.4 MB (6442337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41989a27b3616713951399c9446e9fedc876ac4bae34f2143fa0833b64bd5886`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e5b5f97c64972331e5b1e53b8a01934b0013551e3c28790fc7e13f0dfebd`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:5c3bc443e4a2f479f89ee155cbe841e2d63cc9294c3aa888fc64457bea94a474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a6fde58a78a8df0407f92615908cc35805714e3a1671a66bdd5d5353c72832`

```dockerfile
```

-	Layers:
	-	`sha256:480cb796d2b5b5d888e607bb45d255e462c4690fb64e54f2721250e19ed909aa`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a547b0a456597261657868e2d4ae927c47a163fda68183e21e9e32adb52c96f5`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:c5b3f79371b3d7ff8f9e4bbc41f348539977b5654f1de79061ec53da86a2563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab34c773cbd45451d188b0fc586243e9ddabeba95f34d0a3fe2ab3eb9668073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a521cfb00afa1f22bd5d97b85ad1720879ee5c0b1baab105f52e4860ec7cb`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ff4669d4781473da0924bb50912f548111551b9b5f03299c1b3c476c31795`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77cbf7134214650d99819f0a9af3301695acf4eaa87494d06ed137216f6dd03`  
		Last Modified: Wed, 01 Oct 2025 19:48:07 GMT  
		Size: 6.8 MB (6840251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f16a31134cd2b56611423f586a6bf111aa53bd8afd8bdaafa3815fbae142d`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b21ea73e2977d5c531615088cb9bf1fa9b673f9a4a73159745d3775b9be25c`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:c1257c6861ac64a590f57df8457c5341ce92804291bcf17f2e526d6cf56f30e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a512f85e4c6debb71b1588d50653364b97ef66ecf26e492d16906c6f02d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:2e693f388098945d670d6d7401d2c73d30208c04a9c434f89128a9257051cad6`  
		Last Modified: Wed, 01 Oct 2025 22:04:41 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fe9e313181c313debecbb9cfd10ea888761ba52ba83d75c155e7f24b2c4c0`  
		Last Modified: Wed, 01 Oct 2025 22:04:42 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:63c81e7a01da08fe2456c4fe9380a75306824b5e09e202e7c8c48a955ef67681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d07a35af2ecef1d379d7de3e2682368da4fbefb910ec3cd0543c9702ba1cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fdd8b049eb029577d94c03617e2a21858508fc5e580623cc21f55413af7350`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2785eaaf3b19c0d99a6cd261f54682df997b7f9e8accbab631417bedbbe11e`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e4c78f116c60eebba9d5a01de232d21fdc151c6c160765cdd45131ac57266d`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 9.4 MB (9358166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5280abb5bee4d4bac9b5e9874666be22133b46530de1b9bfdf616d9bbefaa34`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a4b562d5e2bd3a63858fa9ad791651dc993419da3712ec490f3c0437d9c81`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:fefbe28311f558c8f0bd34fd6ae277e561a9fba8dccbb5c370b5ae8d06f0ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946cc255ef0e663aba1c9b13f58f3e2ef6b22802d595e60c1a905b7c9f8d81e`

```dockerfile
```

-	Layers:
	-	`sha256:0f8800600e75cda5489b2d17ddd9ec37a58ad1f1223410df7742af5d2f47beaa`  
		Last Modified: Wed, 01 Oct 2025 19:04:43 GMT  
		Size: 3.6 MB (3613221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea670935804f907c5c8108973c916a79cd259c3ef65e26b1505d0e684c44599`  
		Last Modified: Wed, 01 Oct 2025 19:04:44 GMT  
		Size: 15.1 KB (15072 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:0f938721daf08c239ba32eb210482941a1f07269b403c500e3eb132911dcb44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35960783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a850e3bdd587415e9e20969ef6ce52c0faccac714e602b10f9bf1d2b0dfb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470e100e87fb0737d8813ad701db233de34e7eda3bc7a5e347182edb96fc07b7`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef1e4cab10fc5f2a92736f192b67f9fc080966aa9ed2c1f50b7e11829520c0`  
		Last Modified: Tue, 30 Sep 2025 09:24:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df0b2c4d2fdf31e6e7d55fa1d672759b5244e49159f022163b746b96993bca3`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 6.1 MB (6121187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b089a06826b0a24ec162778fc2d01554cd54c34862516f04dcd2dd9ccd403`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d77df7c01beee6fc002cc7aa3c14a701e7f5700b06926f27e143c76a4b4ad2`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:989260bf82df9044c638bd7e2ffd082c84c055e6978c4b777f7ff712cdd195fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e624bfadefdc72db4094fd7c89b27c542616642506962d12a9866c5e9c9829d`

```dockerfile
```

-	Layers:
	-	`sha256:e8ce284c6273618f8501626aaf90218d5b7c16d53c5504f820ceb8845d9247d6`  
		Last Modified: Wed, 01 Oct 2025 22:04:48 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1078258bc1376211e434d54b32dc2978a4b4a468f55cf19901220469ca2edb4f`  
		Last Modified: Wed, 01 Oct 2025 22:04:49 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:ce16a3780001f91acee7a5318152cf2fdb7f77a9f9efbdf7c9d42624b7d9c398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:fea99c454ce0fbe794959c712b9aa8211a59ec36d96ba4ec47e615983a02df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61044b76967f0bfbd214c3f0c337a70e34bd5e0113b94ee6aee969afe8ae0c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc238e6158ba23ca3c78f09a916e5b8debcb8fc98435ef72ed1372e4a10d36f0`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631db32462bfbb6f6adbfce206c84ea557ef848ce2db5acbc296919b1e2fb8`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfab92e44961e7c708e76600cd2a58da46309cb1585752de3faf3cf12144b9b`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 7.0 MB (7048278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723c6fe89d1ee4486ae7f1aba339a847174340058a9aafba610b8f5d08c392a`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc283d4e51af75c91b14cfc4325a4b783724ecdd9ac3d936db49437b45069`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:9c5b20ad1230caec7f7f817835a32a8e84c0749bb0cec2f1338c9f94d9cafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39fc5ab26c741f2fadea946a1e3f5f8d5f57b2c46254f39a4cf3dec01016afc`

```dockerfile
```

-	Layers:
	-	`sha256:6162c674076105e040975f2f9084082ad1c95d3491863ccfc1a758ad44af0f88`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e718aeb59e0ddcdc8ae0d260d22d1e426d5f84484cbe07357ab801c3c2ae2ac`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0ae5335373d50afd2ebe6afcfa6f6be07e82a19bded4d420d96db3555cf6df5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33737857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1987049a10433f61f985c8a961f2a43c8f01aec18c6d80152fa3fbc3c38a2bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e9eedd2de38e34f9c3259b80e737fa7ffbfb18c38b1f08d50dbb49345eb0d7`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c241ba477fd0194fc32c7ae4f77367d65f7cc4dc492ba06ee414e5e2e1769`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62532e7e306eaf6c857c1dcac69b720b1f9d66d14712934fe28bf0a4be73f567`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 5.8 MB (5789345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfaf6902331c4ccad828cfb4d679d658a030950d2c261496bd7e99ee3522ce2`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe9a7ee86cc167f3246c7ccbaca7e78f1107bcb72fdff9d7524c789bdafd50`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:505d2a98a8941d45aca76abca0104a7e8d398561b1ae7927db969818fbfe2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444672c549748ba8acd59e1603ca69ca9739f52248e1194cd651561d40623efa`

```dockerfile
```

-	Layers:
	-	`sha256:5fb828ad140b7db9b7197a184f66219daa0cac03e3e22a9ec8a4419674b5f497`  
		Last Modified: Tue, 30 Sep 2025 07:04:22 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadb488ef6180819b4864740433eb5e2bd6a3c663387cd05aea5ae85c0d45596`  
		Last Modified: Tue, 30 Sep 2025 07:04:23 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e1cbc8dd0e0dd1d11dcd2e91b74f72b061b6f7a0e9866f8db6c6d01e53d0cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31799710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b584a05bc5a36361a150d614c57ef195e48343081cadd05fe2b0d359e8222`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797f6a658761eae62ed9bd79e1c2e88e731aa6bfefc3880e9b1db206648e59d`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6f0ef72b36a4c660b1f283e3b24a699e315d67f621b453e96e9409d81cc56b`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540e53f5a976b4fd01fcdbb30203a9b777b0f90275315ec34c995a73d288d6b`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 5.6 MB (5584592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b18fa5e02aa57bd7e2669c537eab73247a3828b4525b21b63efc33fc4fe383`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3424719f3c5ef07c1120d5ec07677a2845f8b2d0ef696b2d0c6df065e7256365`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:c23578978a201a21a792164719d8288c21cc5bd23ee2f2edbc21e35c712f002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fe98bdde4a887388e84e89c0aacdf7acb8eb5d8f584a9d0bbb8d6657033d3`

```dockerfile
```

-	Layers:
	-	`sha256:238ce2a67002b5d15d9cfb00195afa1ff16e285c1ce5686c02a79faa79411471`  
		Last Modified: Wed, 01 Oct 2025 22:04:31 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949b594d27935fbfd7f4a1995c730838a20f5c97e5dde2310a58c62179762e49`  
		Last Modified: Wed, 01 Oct 2025 22:04:32 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9c14d801535964b9856cc995b5cc1d953e664d4d36a29226d0b525ebd12fc23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3760e5d3e931c335d1ba762156bad16c786221e38cc064a049bffad16061ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138cafb84902697aa37bc68f6f860c44a9a11d9b9a83a6c59384a6946bfb5073`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a73645b11d1149fdeaeb95abee773ad6067bb95726c22f35387d4b849d93568`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2201eaba239855e7b70ec7db2b53e68c5437be9fc29a5048b5cec95d4357005`  
		Last Modified: Tue, 30 Sep 2025 00:13:19 GMT  
		Size: 6.2 MB (6231836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b71e07b92ddd3ea16e307a436f84f0862f6d41ce6e60c918112b5004eacd7`  
		Last Modified: Tue, 30 Sep 2025 00:13:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c64c105923c5d37d4fa6700dee51a52780c755bfba3de0ac42ccf55d9c80ce0`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:9bc13bf85136708d05c74af3dfc16259959b0610a6cae025c7f9013c1e36d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb9ea2712f520f693ab118515cba89588115d9457cb6fc3051b4f69abe0cb5`

```dockerfile
```

-	Layers:
	-	`sha256:67ff2bdb0f88eae236c4d226ffb071064078a72edf0c36dbc9605931b2873702`  
		Last Modified: Wed, 01 Oct 2025 13:04:28 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa507c4eeada3b5ef073dc36105783217730a9444ef304a477a6297a951cebe2`  
		Last Modified: Wed, 01 Oct 2025 13:04:29 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:3483553c118f803d7dc6a6c85ba75a6757cf336c0fcdce07857d0a1ca40b5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fb778095be09981fa712b92b08229fb6c016edeac9681a10e3d7ceaa3d67e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b683a27da0ff4f41706867fe165539c8b1d4170671892b8376bb380a96382`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16959a1fc618d2ae9b84f6d83c71e630edc85d191636b48932f2f1aa95ecf3ae`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd39dff5263a0f9cae965c7539aca9f51ec3b9f5224265f80015a145df9f2cc7`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 6.4 MB (6442337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41989a27b3616713951399c9446e9fedc876ac4bae34f2143fa0833b64bd5886`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e5b5f97c64972331e5b1e53b8a01934b0013551e3c28790fc7e13f0dfebd`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:5c3bc443e4a2f479f89ee155cbe841e2d63cc9294c3aa888fc64457bea94a474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a6fde58a78a8df0407f92615908cc35805714e3a1671a66bdd5d5353c72832`

```dockerfile
```

-	Layers:
	-	`sha256:480cb796d2b5b5d888e607bb45d255e462c4690fb64e54f2721250e19ed909aa`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a547b0a456597261657868e2d4ae927c47a163fda68183e21e9e32adb52c96f5`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:c5b3f79371b3d7ff8f9e4bbc41f348539977b5654f1de79061ec53da86a2563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab34c773cbd45451d188b0fc586243e9ddabeba95f34d0a3fe2ab3eb9668073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a521cfb00afa1f22bd5d97b85ad1720879ee5c0b1baab105f52e4860ec7cb`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ff4669d4781473da0924bb50912f548111551b9b5f03299c1b3c476c31795`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77cbf7134214650d99819f0a9af3301695acf4eaa87494d06ed137216f6dd03`  
		Last Modified: Wed, 01 Oct 2025 19:48:07 GMT  
		Size: 6.8 MB (6840251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f16a31134cd2b56611423f586a6bf111aa53bd8afd8bdaafa3815fbae142d`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b21ea73e2977d5c531615088cb9bf1fa9b673f9a4a73159745d3775b9be25c`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:c1257c6861ac64a590f57df8457c5341ce92804291bcf17f2e526d6cf56f30e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a512f85e4c6debb71b1588d50653364b97ef66ecf26e492d16906c6f02d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:2e693f388098945d670d6d7401d2c73d30208c04a9c434f89128a9257051cad6`  
		Last Modified: Wed, 01 Oct 2025 22:04:41 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fe9e313181c313debecbb9cfd10ea888761ba52ba83d75c155e7f24b2c4c0`  
		Last Modified: Wed, 01 Oct 2025 22:04:42 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:63c81e7a01da08fe2456c4fe9380a75306824b5e09e202e7c8c48a955ef67681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d07a35af2ecef1d379d7de3e2682368da4fbefb910ec3cd0543c9702ba1cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fdd8b049eb029577d94c03617e2a21858508fc5e580623cc21f55413af7350`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2785eaaf3b19c0d99a6cd261f54682df997b7f9e8accbab631417bedbbe11e`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e4c78f116c60eebba9d5a01de232d21fdc151c6c160765cdd45131ac57266d`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 9.4 MB (9358166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5280abb5bee4d4bac9b5e9874666be22133b46530de1b9bfdf616d9bbefaa34`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a4b562d5e2bd3a63858fa9ad791651dc993419da3712ec490f3c0437d9c81`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:fefbe28311f558c8f0bd34fd6ae277e561a9fba8dccbb5c370b5ae8d06f0ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946cc255ef0e663aba1c9b13f58f3e2ef6b22802d595e60c1a905b7c9f8d81e`

```dockerfile
```

-	Layers:
	-	`sha256:0f8800600e75cda5489b2d17ddd9ec37a58ad1f1223410df7742af5d2f47beaa`  
		Last Modified: Wed, 01 Oct 2025 19:04:43 GMT  
		Size: 3.6 MB (3613221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea670935804f907c5c8108973c916a79cd259c3ef65e26b1505d0e684c44599`  
		Last Modified: Wed, 01 Oct 2025 19:04:44 GMT  
		Size: 15.1 KB (15072 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:0f938721daf08c239ba32eb210482941a1f07269b403c500e3eb132911dcb44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35960783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a850e3bdd587415e9e20969ef6ce52c0faccac714e602b10f9bf1d2b0dfb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470e100e87fb0737d8813ad701db233de34e7eda3bc7a5e347182edb96fc07b7`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef1e4cab10fc5f2a92736f192b67f9fc080966aa9ed2c1f50b7e11829520c0`  
		Last Modified: Tue, 30 Sep 2025 09:24:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df0b2c4d2fdf31e6e7d55fa1d672759b5244e49159f022163b746b96993bca3`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 6.1 MB (6121187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b089a06826b0a24ec162778fc2d01554cd54c34862516f04dcd2dd9ccd403`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d77df7c01beee6fc002cc7aa3c14a701e7f5700b06926f27e143c76a4b4ad2`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:989260bf82df9044c638bd7e2ffd082c84c055e6978c4b777f7ff712cdd195fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e624bfadefdc72db4094fd7c89b27c542616642506962d12a9866c5e9c9829d`

```dockerfile
```

-	Layers:
	-	`sha256:e8ce284c6273618f8501626aaf90218d5b7c16d53c5504f820ceb8845d9247d6`  
		Last Modified: Wed, 01 Oct 2025 22:04:48 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1078258bc1376211e434d54b32dc2978a4b4a468f55cf19901220469ca2edb4f`  
		Last Modified: Wed, 01 Oct 2025 22:04:49 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.4-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:ce16a3780001f91acee7a5318152cf2fdb7f77a9f9efbdf7c9d42624b7d9c398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:fea99c454ce0fbe794959c712b9aa8211a59ec36d96ba4ec47e615983a02df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61044b76967f0bfbd214c3f0c337a70e34bd5e0113b94ee6aee969afe8ae0c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc238e6158ba23ca3c78f09a916e5b8debcb8fc98435ef72ed1372e4a10d36f0`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631db32462bfbb6f6adbfce206c84ea557ef848ce2db5acbc296919b1e2fb8`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfab92e44961e7c708e76600cd2a58da46309cb1585752de3faf3cf12144b9b`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 7.0 MB (7048278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723c6fe89d1ee4486ae7f1aba339a847174340058a9aafba610b8f5d08c392a`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc283d4e51af75c91b14cfc4325a4b783724ecdd9ac3d936db49437b45069`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9c5b20ad1230caec7f7f817835a32a8e84c0749bb0cec2f1338c9f94d9cafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39fc5ab26c741f2fadea946a1e3f5f8d5f57b2c46254f39a4cf3dec01016afc`

```dockerfile
```

-	Layers:
	-	`sha256:6162c674076105e040975f2f9084082ad1c95d3491863ccfc1a758ad44af0f88`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e718aeb59e0ddcdc8ae0d260d22d1e426d5f84484cbe07357ab801c3c2ae2ac`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0ae5335373d50afd2ebe6afcfa6f6be07e82a19bded4d420d96db3555cf6df5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33737857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1987049a10433f61f985c8a961f2a43c8f01aec18c6d80152fa3fbc3c38a2bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e9eedd2de38e34f9c3259b80e737fa7ffbfb18c38b1f08d50dbb49345eb0d7`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c241ba477fd0194fc32c7ae4f77367d65f7cc4dc492ba06ee414e5e2e1769`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62532e7e306eaf6c857c1dcac69b720b1f9d66d14712934fe28bf0a4be73f567`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 5.8 MB (5789345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfaf6902331c4ccad828cfb4d679d658a030950d2c261496bd7e99ee3522ce2`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe9a7ee86cc167f3246c7ccbaca7e78f1107bcb72fdff9d7524c789bdafd50`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:505d2a98a8941d45aca76abca0104a7e8d398561b1ae7927db969818fbfe2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444672c549748ba8acd59e1603ca69ca9739f52248e1194cd651561d40623efa`

```dockerfile
```

-	Layers:
	-	`sha256:5fb828ad140b7db9b7197a184f66219daa0cac03e3e22a9ec8a4419674b5f497`  
		Last Modified: Tue, 30 Sep 2025 07:04:22 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadb488ef6180819b4864740433eb5e2bd6a3c663387cd05aea5ae85c0d45596`  
		Last Modified: Tue, 30 Sep 2025 07:04:23 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e1cbc8dd0e0dd1d11dcd2e91b74f72b061b6f7a0e9866f8db6c6d01e53d0cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31799710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b584a05bc5a36361a150d614c57ef195e48343081cadd05fe2b0d359e8222`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797f6a658761eae62ed9bd79e1c2e88e731aa6bfefc3880e9b1db206648e59d`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6f0ef72b36a4c660b1f283e3b24a699e315d67f621b453e96e9409d81cc56b`  
		Last Modified: Tue, 30 Sep 2025 01:01:32 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540e53f5a976b4fd01fcdbb30203a9b777b0f90275315ec34c995a73d288d6b`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 5.6 MB (5584592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b18fa5e02aa57bd7e2669c537eab73247a3828b4525b21b63efc33fc4fe383`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3424719f3c5ef07c1120d5ec07677a2845f8b2d0ef696b2d0c6df065e7256365`  
		Last Modified: Tue, 30 Sep 2025 01:01:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c23578978a201a21a792164719d8288c21cc5bd23ee2f2edbc21e35c712f002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fe98bdde4a887388e84e89c0aacdf7acb8eb5d8f584a9d0bbb8d6657033d3`

```dockerfile
```

-	Layers:
	-	`sha256:238ce2a67002b5d15d9cfb00195afa1ff16e285c1ce5686c02a79faa79411471`  
		Last Modified: Wed, 01 Oct 2025 22:04:31 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949b594d27935fbfd7f4a1995c730838a20f5c97e5dde2310a58c62179762e49`  
		Last Modified: Wed, 01 Oct 2025 22:04:32 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9c14d801535964b9856cc995b5cc1d953e664d4d36a29226d0b525ebd12fc23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3760e5d3e931c335d1ba762156bad16c786221e38cc064a049bffad16061ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138cafb84902697aa37bc68f6f860c44a9a11d9b9a83a6c59384a6946bfb5073`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a73645b11d1149fdeaeb95abee773ad6067bb95726c22f35387d4b849d93568`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2201eaba239855e7b70ec7db2b53e68c5437be9fc29a5048b5cec95d4357005`  
		Last Modified: Tue, 30 Sep 2025 00:13:19 GMT  
		Size: 6.2 MB (6231836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b71e07b92ddd3ea16e307a436f84f0862f6d41ce6e60c918112b5004eacd7`  
		Last Modified: Tue, 30 Sep 2025 00:13:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c64c105923c5d37d4fa6700dee51a52780c755bfba3de0ac42ccf55d9c80ce0`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9bc13bf85136708d05c74af3dfc16259959b0610a6cae025c7f9013c1e36d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb9ea2712f520f693ab118515cba89588115d9457cb6fc3051b4f69abe0cb5`

```dockerfile
```

-	Layers:
	-	`sha256:67ff2bdb0f88eae236c4d226ffb071064078a72edf0c36dbc9605931b2873702`  
		Last Modified: Wed, 01 Oct 2025 13:04:28 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa507c4eeada3b5ef073dc36105783217730a9444ef304a477a6297a951cebe2`  
		Last Modified: Wed, 01 Oct 2025 13:04:29 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:3483553c118f803d7dc6a6c85ba75a6757cf336c0fcdce07857d0a1ca40b5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fb778095be09981fa712b92b08229fb6c016edeac9681a10e3d7ceaa3d67e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b683a27da0ff4f41706867fe165539c8b1d4170671892b8376bb380a96382`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16959a1fc618d2ae9b84f6d83c71e630edc85d191636b48932f2f1aa95ecf3ae`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd39dff5263a0f9cae965c7539aca9f51ec3b9f5224265f80015a145df9f2cc7`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 6.4 MB (6442337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41989a27b3616713951399c9446e9fedc876ac4bae34f2143fa0833b64bd5886`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e5b5f97c64972331e5b1e53b8a01934b0013551e3c28790fc7e13f0dfebd`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5c3bc443e4a2f479f89ee155cbe841e2d63cc9294c3aa888fc64457bea94a474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a6fde58a78a8df0407f92615908cc35805714e3a1671a66bdd5d5353c72832`

```dockerfile
```

-	Layers:
	-	`sha256:480cb796d2b5b5d888e607bb45d255e462c4690fb64e54f2721250e19ed909aa`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a547b0a456597261657868e2d4ae927c47a163fda68183e21e9e32adb52c96f5`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:c5b3f79371b3d7ff8f9e4bbc41f348539977b5654f1de79061ec53da86a2563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab34c773cbd45451d188b0fc586243e9ddabeba95f34d0a3fe2ab3eb9668073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a521cfb00afa1f22bd5d97b85ad1720879ee5c0b1baab105f52e4860ec7cb`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ff4669d4781473da0924bb50912f548111551b9b5f03299c1b3c476c31795`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77cbf7134214650d99819f0a9af3301695acf4eaa87494d06ed137216f6dd03`  
		Last Modified: Wed, 01 Oct 2025 19:48:07 GMT  
		Size: 6.8 MB (6840251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f16a31134cd2b56611423f586a6bf111aa53bd8afd8bdaafa3815fbae142d`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b21ea73e2977d5c531615088cb9bf1fa9b673f9a4a73159745d3775b9be25c`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c1257c6861ac64a590f57df8457c5341ce92804291bcf17f2e526d6cf56f30e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a512f85e4c6debb71b1588d50653364b97ef66ecf26e492d16906c6f02d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:2e693f388098945d670d6d7401d2c73d30208c04a9c434f89128a9257051cad6`  
		Last Modified: Wed, 01 Oct 2025 22:04:41 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fe9e313181c313debecbb9cfd10ea888761ba52ba83d75c155e7f24b2c4c0`  
		Last Modified: Wed, 01 Oct 2025 22:04:42 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:63c81e7a01da08fe2456c4fe9380a75306824b5e09e202e7c8c48a955ef67681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d07a35af2ecef1d379d7de3e2682368da4fbefb910ec3cd0543c9702ba1cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fdd8b049eb029577d94c03617e2a21858508fc5e580623cc21f55413af7350`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2785eaaf3b19c0d99a6cd261f54682df997b7f9e8accbab631417bedbbe11e`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e4c78f116c60eebba9d5a01de232d21fdc151c6c160765cdd45131ac57266d`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 9.4 MB (9358166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5280abb5bee4d4bac9b5e9874666be22133b46530de1b9bfdf616d9bbefaa34`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a4b562d5e2bd3a63858fa9ad791651dc993419da3712ec490f3c0437d9c81`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fefbe28311f558c8f0bd34fd6ae277e561a9fba8dccbb5c370b5ae8d06f0ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946cc255ef0e663aba1c9b13f58f3e2ef6b22802d595e60c1a905b7c9f8d81e`

```dockerfile
```

-	Layers:
	-	`sha256:0f8800600e75cda5489b2d17ddd9ec37a58ad1f1223410df7742af5d2f47beaa`  
		Last Modified: Wed, 01 Oct 2025 19:04:43 GMT  
		Size: 3.6 MB (3613221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea670935804f907c5c8108973c916a79cd259c3ef65e26b1505d0e684c44599`  
		Last Modified: Wed, 01 Oct 2025 19:04:44 GMT  
		Size: 15.1 KB (15072 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0f938721daf08c239ba32eb210482941a1f07269b403c500e3eb132911dcb44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35960783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a850e3bdd587415e9e20969ef6ce52c0faccac714e602b10f9bf1d2b0dfb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470e100e87fb0737d8813ad701db233de34e7eda3bc7a5e347182edb96fc07b7`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef1e4cab10fc5f2a92736f192b67f9fc080966aa9ed2c1f50b7e11829520c0`  
		Last Modified: Tue, 30 Sep 2025 09:24:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df0b2c4d2fdf31e6e7d55fa1d672759b5244e49159f022163b746b96993bca3`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 6.1 MB (6121187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b089a06826b0a24ec162778fc2d01554cd54c34862516f04dcd2dd9ccd403`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d77df7c01beee6fc002cc7aa3c14a701e7f5700b06926f27e143c76a4b4ad2`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:989260bf82df9044c638bd7e2ffd082c84c055e6978c4b777f7ff712cdd195fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e624bfadefdc72db4094fd7c89b27c542616642506962d12a9866c5e9c9829d`

```dockerfile
```

-	Layers:
	-	`sha256:e8ce284c6273618f8501626aaf90218d5b7c16d53c5504f820ceb8845d9247d6`  
		Last Modified: Wed, 01 Oct 2025 22:04:48 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1078258bc1376211e434d54b32dc2978a4b4a468f55cf19901220469ca2edb4f`  
		Last Modified: Wed, 01 Oct 2025 22:04:49 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json
