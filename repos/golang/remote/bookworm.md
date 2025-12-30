## `golang:bookworm`

```console
$ docker pull golang@sha256:67deea7cdb4830535ec78c364749e644c3bf526fd38711075b9fe84cf2bb0124
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:cfacfe031d4eb1c1ad50593e4988cc9e8286ff1ca5f33bf357eb863fddc08073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289468544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e245162a1e8c394cb350e743daa23f3d4ef7e0391c75c49e195c84b98f77d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 00:46:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:46:16 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 00:47:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 00:47:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b18210496c0a859458bb2304c5fd1c1e099de8c927f7030f1bce471f5361bf`  
		Last Modified: Tue, 09 Dec 2025 00:47:59 GMT  
		Size: 92.4 MB (92410480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1aed72b746091f7129c5e483dae161d20c9f3092262292f6f8993779531c60`  
		Last Modified: Tue, 09 Dec 2025 00:47:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:87ae66b51171764a067baf15ec4feed14b7a5528f022cdaa2953b7b44fd0da3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687d4ea612b261ce91ae6c255a984ae80bf3a7b6e54c3dc0d3ea633d68c2b47f`

```dockerfile
```

-	Layers:
	-	`sha256:c22df4569f017be27de20cc98ee8a0fef93b6aaee4a7a13e012855f442da6e73`  
		Last Modified: Tue, 09 Dec 2025 03:23:30 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ddf431b12e9e281ec2da71a87f2042b612219afc37536fec5293968ed2c83b`  
		Last Modified: Tue, 09 Dec 2025 03:23:31 GMT  
		Size: 27.8 KB (27796 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:45136b9daa9c60443e6671a50bda5a2078c3a17841e17329e28711a500f70735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251131919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fff599e9f5e3fd1cb487cd70884d319c6d3c1f824a88029e571c75eb3a78bdb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:56 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 30 Dec 2025 02:35:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:35:56 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:35:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:35:56 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:35:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:35:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c47e6d209a48429f83d84da46efa5b9cf3f213484d98aa41c979735c76b6bc`  
		Last Modified: Tue, 30 Dec 2025 02:36:30 GMT  
		Size: 66.3 MB (66276422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1be9bdcbed6827d0f555f9543e27d0fc34ecef160a205bfb7ba501b5006bea`  
		Last Modified: Tue, 30 Dec 2025 02:36:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1ff611930f478afcb918c16ccdd0ee100634d64f6566617deeaafe6530e73ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cd84369f83aa5741aea4dd1af1708b11b6ccd36a9fc90f7669110757029239`

```dockerfile
```

-	Layers:
	-	`sha256:e1d14dd0c5676c202fcc1964a4b69064948c86a61cf126e81828e5429cff70f3`  
		Last Modified: Tue, 30 Dec 2025 03:23:29 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0806e11f19f822d598771653a32565ff0539eef8ad975ca33eabf61b7002eb`  
		Last Modified: Tue, 30 Dec 2025 03:23:29 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:38f61e632fb494c99162aff0a04ca364c471f66da84d1e588bfefb143f06b52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280470881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a623116632f708a04a469b04d8f15684e890b5fbee8f31b1f2bd5be3b099b593`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:17:05 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 01:17:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:17:05 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:17:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:17:05 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:17:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:17:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1d7b2841bed83e94cfc06e675eae22d6e1ccaf8af5c3432f5a731b73586622`  
		Last Modified: Tue, 09 Dec 2025 01:17:47 GMT  
		Size: 86.5 MB (86490999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c9f644e5b0bca4a0dc6f08736ac4de9ebf80e4d45ab5df9500fe29747adcb`  
		Last Modified: Tue, 09 Dec 2025 01:17:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:38bf793e006e6e66fa8fa68efa6626ffb7f52e3f1fb1807158b704957c7f2085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6818b1c899a413646dd4a14aaaad8c344805f189e70ee201bebb0baa0c35f8d`

```dockerfile
```

-	Layers:
	-	`sha256:c800f3e2ed304dc45527c10d6710eee5e5b7f36638db63d8f723deed82c4bdfc`  
		Last Modified: Tue, 09 Dec 2025 03:23:50 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9a5d0b64d3207492cece84445bcfc5214e69eb797ebf481582f0f9a6b8e237`  
		Last Modified: Tue, 09 Dec 2025 03:23:51 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:47c9be99ca0f72c811eb18b123f6bfa58fc504a4ebbe677088c27695ed39cfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289276919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f33c5dc17b42fcc7c44ca6fadf1cee26671d9893c85fdafd77f20d3bbc9c90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:52:04 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 30 Dec 2025 01:52:04 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 01:52:04 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 01:52:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:52:04 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 01:52:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 01:52:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10eedb7d741cb151d52259302acf62c6c98590a9a4168d4370619e890f15715`  
		Last Modified: Tue, 30 Dec 2025 00:32:36 GMT  
		Size: 66.2 MB (66233282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fbbde9b3324b993c83c24fcb23c687fa3682d37dd772e6109542a7b4ab7617`  
		Last Modified: Tue, 30 Dec 2025 01:52:44 GMT  
		Size: 89.8 MB (89840196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea63b97c6a2eec0cc38594ddf76bf0e913038ab82202131cf29221fa54788473`  
		Last Modified: Tue, 30 Dec 2025 01:52:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8974f9f32e9d81761408707d197b87c0c26cf97bc7186476c4c37b888bdfaccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035fd7891ef34bcdad909b7c0af477a27f4cc5f61b33528d688bd49fd1328f6`

```dockerfile
```

-	Layers:
	-	`sha256:fee390fbad6f905d34ae4388e6c011e8113b281cdf02ee58ad25334b912b85ff`  
		Last Modified: Tue, 30 Dec 2025 03:23:46 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94623cb36419bb642e584f66635210d2c87f7fce82821d6206fa580a1466479`  
		Last Modified: Tue, 30 Dec 2025 03:23:46 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:0f0692020ad37f779944469da018b4007343e4c5009f298abf4f470d871b727a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262276160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18a82c8b46ea2430acfabc415ab319e51734f22d69446c6f1577da228f67963`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 15:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 21:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:31 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 21:59:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 21:59:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39c87c0b77499147a54de9b3e5bae714c175e6e770a910d9f420c4e6fb61ba58`  
		Last Modified: Mon, 08 Dec 2025 22:14:39 GMT  
		Size: 48.8 MB (48760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1571bb35c4ff72a581f317370ae35a4e1c5896fc868d9d6a6a545382b80d1b1`  
		Last Modified: Tue, 09 Dec 2025 15:10:23 GMT  
		Size: 23.6 MB (23613949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7e7f53e0184cfbc8481d8bf6e3898908651f4106389843dddb844d4e45ba75`  
		Last Modified: Tue, 09 Dec 2025 20:10:46 GMT  
		Size: 63.3 MB (63309593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c4012ce2cba975e6e5e0c4498492dadfcd953fd94bfbda58e546a544114552`  
		Last Modified: Tue, 09 Dec 2025 22:01:04 GMT  
		Size: 70.0 MB (70017142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a811f73ff0cb3df64f15904472d8c052172a4266c947c138019cab5cd2bb575`  
		Last Modified: Tue, 02 Dec 2025 17:48:38 GMT  
		Size: 56.6 MB (56574424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d5c5a34d40dd752ec4dffb6adc5d0be728bbd9918afa08f9c5d6498c11b31`  
		Last Modified: Tue, 09 Dec 2025 22:00:57 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e376c4db3bc5f768252f6e6982027b9747b4cf33ebfb9fe532062a39ace78eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6352337d4d29bae81704366f34a7c26fb32d3bc46daca20152a48dec75081f`

```dockerfile
```

-	Layers:
	-	`sha256:2d8b79014e5ec19502bc90199afa809e583a372b553c42b18b67340c11d913f9`  
		Last Modified: Wed, 10 Dec 2025 00:22:54 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:7be8e0eb4743fe5ddea75f00797a0249e041a91f857803ce90dc0aec4d6a66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296400242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7843922480b6d0e44719be61547fb74ad98114a908936e1f5af6bc8f2499ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:12:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:12:05 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:12:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:12:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fcf0300c06237c12ec60c09556f95a6b8c833ba82bfc5828beb977742de538`  
		Last Modified: Tue, 09 Dec 2025 02:13:29 GMT  
		Size: 90.4 MB (90419946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a20f8398526b7e32e5610cbaf93e2d1dc9ef12fe14e2f40d8981cbf322083f`  
		Last Modified: Tue, 09 Dec 2025 02:13:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:26f6b8379232a27c484820400b1d8f4aed4033968a8ea21ba0f8221e7d6f19eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6f5c90c55d3f98b3e3134a332c426d11b6cbfc21b5050509fc7e9bbb85dad`

```dockerfile
```

-	Layers:
	-	`sha256:a9cce1234d409d1894452021b7e8872ff49b9855f41f46b8e5079291672e81da`  
		Last Modified: Tue, 09 Dec 2025 03:24:12 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc991258b0b5f35f2d2a8630acdfc640f89cdf40bb6fb47d6a78752739fa826`  
		Last Modified: Tue, 09 Dec 2025 03:24:13 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:da54e6a866547deb3c3fa8bc4fe77b540683cdc7292230b262ebfe3fc92b67af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263163415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b636998ac43873427e196eeff14300ed60d3edd4c8b88789763d207e14c56c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:59:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:59:32 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:59:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:59:32 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:59:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:59:32 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:59:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:59:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4635598f3b0f128359fc25d526138bfeb1cfd50aa2df3f8a5a9214cdae1551f`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 24.0 MB (24027286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85977b1427cc2c2afbab15cfdcc745e64492465bdc1299648a91c7787a768`  
		Last Modified: Tue, 09 Dec 2025 01:46:34 GMT  
		Size: 63.5 MB (63501228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c78d8ef4c672ad3a1b17951daa282f21316a1dab32f99d9430a850ba86084`  
		Last Modified: Tue, 09 Dec 2025 03:00:20 GMT  
		Size: 69.0 MB (69009858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9caad544c3834ba0a3a1c507df39d82fa12eda45b7621ee781a25f1640f424`  
		Last Modified: Tue, 09 Dec 2025 03:00:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d63d532373ca382e3375a6e7fcbc47f9c086f0f7889cf700a12e1b42d81a4419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8072f5902460707ad585de1b270ad06efb3e9b5941416d413e909eaabed2bc`

```dockerfile
```

-	Layers:
	-	`sha256:e7b02ac9ef323744c4f39980bce6f20f316f16dde9681f8a48d51adb5d45a928`  
		Last Modified: Tue, 09 Dec 2025 03:24:23 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac87caa068e7bee2415443f00e7afdb38b73203596024d2a4c50585c3648349`  
		Last Modified: Tue, 09 Dec 2025 03:24:24 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
