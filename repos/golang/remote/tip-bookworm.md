## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:215c3c818ea6d6c9f54e11fdb6a3bed3bdbed541cd7dd15fbcbcc88848db9d9e
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:24378af30dcb2db3ef65e13c9dc0608a01e60115834ddf504966876df1237b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355277082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2bd41131bf95acd72525253d834e06088d408ec97a290b9fafe4e95cbb281b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9302ab9a7724420a6bb45d089230c1619c95ead37ad5c8c46201642c7da7dce8`  
		Last Modified: Tue, 08 Apr 2025 04:14:06 GMT  
		Size: 92.3 MB (92333008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc044b4e18e8d70a1ecc203412289673855869397177339cdff79099bda4d2f`  
		Last Modified: Mon, 07 Apr 2025 22:40:51 GMT  
		Size: 126.0 MB (126045817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9929c4697adbb2d587529b6e7a96408ca358c108c2a05f3477c021bdb038ae`  
		Last Modified: Tue, 08 Apr 2025 04:14:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c1f6f8e5c58b5dae5ca91aed0c2bb3fd30fea87f28504bf6c1790cb5cf345cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a0e2a94b7a8ab48bbe4e39934f6767f115d8cf4dc095c86f147fa8325d749e`

```dockerfile
```

-	Layers:
	-	`sha256:843cd081cd579bc322c8c9562189eacad4ff80343ed15810ba262efa2e061246`  
		Last Modified: Tue, 08 Apr 2025 04:14:05 GMT  
		Size: 10.3 MB (10271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a8eab6d8a1c6f026b6420f5242b906316dbe8dc811cfdf7ea829e77834266d3`  
		Last Modified: Tue, 08 Apr 2025 04:14:04 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:b855503a06ac44f1f4c7484ae6425c738ea9ce96ca90458c505b9e3400f4e73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312994082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e82f0f9ee58d49820fc1fb67f2af7c63c74c17f795e38f0fb848b04566437a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00519b34344176105ca045ed023ebae6a0a5c6298dc42892bd398946022f439c`  
		Last Modified: Tue, 18 Mar 2025 16:42:48 GMT  
		Size: 66.2 MB (66197750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1290dc10baba6632fd5e083ce70494036c9bdcaeb42c9719e7ebc2bbe45fe3`  
		Last Modified: Mon, 07 Apr 2025 22:57:05 GMT  
		Size: 121.1 MB (121060891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767a7afa1fade28312db859907b89a2c6256ea2dcb34a521275737b22eb268b`  
		Last Modified: Mon, 07 Apr 2025 22:57:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:662603ecd125b15862a936cdc966d577abf15e84f9911bdd7935928ae490c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10106639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bc5da2c3b5fa10a1af7928d99c14cc51aa0fa8306f273f388341d8696d42c`

```dockerfile
```

-	Layers:
	-	`sha256:1610bf7ac87ebd94c8e1e720e0f18025bd93de6e8d66c656e54dec0429859127`  
		Last Modified: Mon, 07 Apr 2025 22:57:02 GMT  
		Size: 10.1 MB (10078852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ea409c7c848deb4fafc8952825e3f516ca4341b6bc07a45d7d3dfbff34e89e`  
		Last Modified: Mon, 07 Apr 2025 22:57:01 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e95d2e19c00fe38a3d79e004d3ddacc44828667cbd4987128d151854a309e81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341346285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d1533368b101b494da03ab0ea3b63d14c74eb68e79800ea676c45a167f489b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7d0b299d26ce0f065a1fac5d6ad12aaa605ef18f04114a5b9e048f7d59782`  
		Last Modified: Tue, 18 Mar 2025 14:43:52 GMT  
		Size: 86.4 MB (86397409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c040252f366631b10d12c85c56edda99c15cbe025d4e4abe3b2a7e0736ae53`  
		Last Modified: Mon, 07 Apr 2025 22:45:10 GMT  
		Size: 118.7 MB (118743723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc1bcac5a146d71eb5f79cb6aa9c34a05c5a78dc4cf38b38d1ab919110812ba`  
		Last Modified: Mon, 07 Apr 2025 22:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9bb023032dbb47e3d49515f5c9759320ab098b1510b13e572b5f638d26c483e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9af7b9c621f8ded5435bca04f50b30442bc03d70009a48d560a2df4c30806`

```dockerfile
```

-	Layers:
	-	`sha256:70fc050799260c01c691317bb14e204710bad24d9318ac09748df3787f9c1c92`  
		Last Modified: Mon, 07 Apr 2025 22:45:05 GMT  
		Size: 10.3 MB (10298377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8400a2f867904b7b0be6147e544c9d05e947009a867aa50f4eb5c5275d04ff2`  
		Last Modified: Mon, 07 Apr 2025 22:45:04 GMT  
		Size: 27.8 KB (27822 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:8bfa0ab44682e6c1335d4f9646e95d7dfdb3bd6ec575ec646619614dc34034a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354511176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07df79634a23164606f5dbfd6133ce48793c193741cb9c6f45b493271ce3aa02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38df34719080b4a5d1322a751afee0fe679c18aa327eda32daa312b1c48334fb`  
		Last Modified: Tue, 08 Apr 2025 04:14:52 GMT  
		Size: 89.8 MB (89752953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae3c30c1a3e04c667c09570d32c4fdc5fb10965c2ae3c7c8d16fb2e127e055f`  
		Last Modified: Mon, 07 Apr 2025 22:41:19 GMT  
		Size: 124.2 MB (124195306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e9b036343e3af9da19f4951d37f815b0f382dfaf547097b56d61650b64bcf`  
		Last Modified: Tue, 08 Apr 2025 04:14:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6f62e3ed3b307d4d1a8884e54c24a4c602bbffdf6417906e210c4d53c2cc981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba00b1fa02ec6e69d52b6b9694f1864c52c0a0cd6dc5ffe1e6eff3aa47cea569`

```dockerfile
```

-	Layers:
	-	`sha256:290e63ef0bc3da70e58014c5c27712bb4ace82deb4d3c61c279f867705d0b6d5`  
		Last Modified: Tue, 08 Apr 2025 04:14:50 GMT  
		Size: 10.3 MB (10251942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fbd996d81210c869678495447c1f3adb1130f9976406d54447e6481eeead029`  
		Last Modified: Tue, 08 Apr 2025 04:14:49 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:4fbaf217ec02459e75aa4a8cc0364df8cb6608a23531d29cbb1f3cc8d5efd5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321959229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec00c3e4fa5df95858ae0fc1ca998486e06c4e2f1a49bd3f681714c9ee35b223`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a4688093ff24a7c0a47c52d04ce08c1411187824a95dc1fb509b4ab01c8c4`  
		Last Modified: Wed, 19 Mar 2025 05:02:22 GMT  
		Size: 63.3 MB (63308534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2231f6ba5c37aa271ccac7a0771657978751e91d524c076449ab434853b6fbd6`  
		Last Modified: Wed, 19 Mar 2025 09:15:32 GMT  
		Size: 69.9 MB (69916047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217715ff223da784f1dfef1ab407185f2f404c6c9eafd7fec335ed813e934ce2`  
		Last Modified: Mon, 07 Apr 2025 22:59:57 GMT  
		Size: 116.4 MB (116382730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c029078241c4a43830f8ea0e7954d91c5fb19385dab73478aa4c917d332f63`  
		Last Modified: Mon, 07 Apr 2025 22:59:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e422a45e52512dd12b63d0a186116d0e5d70205172672ed333fce27cfecc0c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd6fb979524d055da6a392c2b16d31c5aa12749cd45e6e776da31e83521a96b`

```dockerfile
```

-	Layers:
	-	`sha256:92badfd7c5e2360d3c4fb0c286fee703b9a3583b311b103942cd2b8b99fb161e`  
		Last Modified: Mon, 07 Apr 2025 22:59:46 GMT  
		Size: 27.5 KB (27533 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:78ca7b8fe5f35235d84577a40141db1410d88032607ecf782ee51dc4f851c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359024710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861727352be34d5d5e7addc3c11cf45d7de0ce40eb465109eafddef61707d0ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae46de5b9b1bff7a4ad47fdc2c2eaee788abd87244f4992fa97aa13f80c83e`  
		Last Modified: Tue, 08 Apr 2025 15:44:42 GMT  
		Size: 90.3 MB (90334402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff7c926c5215703e9cc5f378e25970c1665c6647a6d87c93d8dedc53c595868`  
		Last Modified: Mon, 07 Apr 2025 22:42:14 GMT  
		Size: 120.9 MB (120864404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cd38de6a73dc8b9a0d7c98243e1f0990e3d73744453a85586edacfece679fc`  
		Last Modified: Tue, 08 Apr 2025 16:45:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:87c368c6f289f7750fe27d50c5d7adac38e0d94a8481d69f74651403f8924070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9987642ff1feb47f6aec8b89c3a9bc3fad6c3b371ec966c484aee9d7873c8927`

```dockerfile
```

-	Layers:
	-	`sha256:4f5aba6aaaf80fedee0dba01403c944decdd8f72d34a334cc21a28ffa4f66db2`  
		Last Modified: Tue, 08 Apr 2025 16:46:00 GMT  
		Size: 10.2 MB (10244561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30bff397b4f735c1dda2a4798c7657306cb19066b0c157d613788dd82a4e9d2`  
		Last Modified: Tue, 08 Apr 2025 16:45:59 GMT  
		Size: 27.7 KB (27720 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8b4f9f640a3dd4327ae56489780ba0fb48852c4a8966d1db8c02a1270683667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326863795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7639b44629ef50fc340695e8ca54b668319fb404195a43f8edb475f610ff2bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b90f4963e2742395335d2bc5e908f7c9081649b808703a7348aa8213d7b75`  
		Last Modified: Mon, 24 Mar 2025 21:23:36 GMT  
		Size: 68.9 MB (68922898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422ac8743b3d8d2ff96125eac5437f0e522f00570e50d835f0fcd015b8c6cee0`  
		Last Modified: Mon, 07 Apr 2025 22:47:48 GMT  
		Size: 123.3 MB (123306442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a6723d52e4d9c6b2a1ef9ccd332fc5d3fc88d236fc2d204ac20b990590f21`  
		Last Modified: Mon, 07 Apr 2025 22:47:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5f3e48f381cf7e94469bcb079894cdf60b38a76a2ff203aaffa8ad299287f17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39519d4b4ba67fcd0a96c930111ed8f87e7472a6977cdce179b01bbe80070a5`

```dockerfile
```

-	Layers:
	-	`sha256:a493d54d4cc4665faf0774238fc70fc54bb1c885bf28cde1085eecf1381f037a`  
		Last Modified: Mon, 07 Apr 2025 22:47:46 GMT  
		Size: 10.1 MB (10106510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d81cfa09626b48d20d0cf45fdd40e79089400d734668034982f8921e3680fc`  
		Last Modified: Mon, 07 Apr 2025 22:47:45 GMT  
		Size: 27.7 KB (27661 bytes)  
		MIME: application/vnd.in-toto+json
