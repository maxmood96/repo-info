## `golang:tip-20251102-bookworm`

```console
$ docker pull golang@sha256:05250bf63fa8d6168e1bf6cf20cb13cda2abe4ac7f70b46701e87cbeaefa38d8
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

### `golang:tip-20251102-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:a8e02918302f674fcf105136c80cb0b283b520a2aeb732775e987e665a57bae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320935290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5877312a12033d34e34b22ebc558421fee5c33d85d3a86d94c404ce19dfcee7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:12:15 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:15 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:15 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:12:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:12:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbef13a1a2af12cdbf27569e5304050a7bd2faed946bcae63e27f6a6cf6831`  
		Last Modified: Wed, 05 Nov 2025 21:12:54 GMT  
		Size: 92.4 MB (92401964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecf9574c2c32de72ba0af7aaa9a80026807a9cc9433b3f3b0bae281deaa3ce9`  
		Last Modified: Wed, 05 Nov 2025 21:12:47 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9f18e63ec5372daefc6c351925f83881d1011efaed08836e5481fe1e12780b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33900f7c38b35141adc48d9e2fa7a613a822f5d275180f422d9cdbed8e6424c`

```dockerfile
```

-	Layers:
	-	`sha256:0c271c8389dcca9bdb6a3e99e6ee3a64f3a0fec3295119ed02b463439d98b60f`  
		Last Modified: Thu, 06 Nov 2025 00:25:30 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bcf290b0eee1adaf73d18d90a3cc7c10ee122ac5796e06a5be3c946a3b5d76`  
		Last Modified: Thu, 06 Nov 2025 00:25:31 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2857fb5f55dcf9d4381b1fa8d3c118d3d128a52db89ae243a8028ad9434e6c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279845723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e060f0ba56b73b20064ae127a281aeb21f0a561b6f7d8fd9bb0f9dc00ef92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:09:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:11:58 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:11:58 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:11:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:11:58 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:12:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4c6c96cff86026dfac835fc2d229a348ec06ff2d2c520014ac2aeb4555bd9e`  
		Last Modified: Tue, 04 Nov 2025 02:18:15 GMT  
		Size: 59.7 MB (59652141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7a46fa641c1544c20dbc645c2065f886e2df8381700e983415cd87a0af41f8`  
		Last Modified: Wed, 05 Nov 2025 21:12:58 GMT  
		Size: 66.3 MB (66255429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cea84e040c61769d28144a64e0a1b9b09c8ad8bd7598fbc6fcf7544df106763`  
		Last Modified: Wed, 05 Nov 2025 21:12:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6375d71d82edb7721424ed69eae12ea0dcc05a35ae291acc3d248421d878e969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2995aa68e14835fe0a5c91093a8abb71181706692f17208ffbce1467c98f1c00`

```dockerfile
```

-	Layers:
	-	`sha256:9ec8f9e768dc789705a72460c180b5248f8a3c03990914eadd194034a243274b`  
		Last Modified: Thu, 06 Nov 2025 00:25:38 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04630874f5a0298feb976f70a790bf314e33f7ab61fa94949de6a0e1edfd6fff`  
		Last Modified: Thu, 06 Nov 2025 00:25:39 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2f4f4b0b3b9bbd59f561d3305b395acabc694c529cbc50797340e152bd316b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309680161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52581e5b5cd48ce492f3eee1efe6ea89493575912d1c2f09bb31efb1d390c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:45 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:45 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:12:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:12:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142383afe3c283a8802ee0efe04b270ced628ae460cd37ae9ae5133d7fdb6f41`  
		Last Modified: Wed, 05 Nov 2025 21:13:31 GMT  
		Size: 86.5 MB (86472105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1726417a4c380bdf72f07feb74507dc0a9e2d16a47a742224bf65ca92c832`  
		Last Modified: Wed, 05 Nov 2025 21:13:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6cf300241c9b0f14519859070cfc2aaf79b524ba84cda0aa036106e5068f0599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543fd16df7c9145f35747d045fdffc633e7f827297deb8b0ef91fef3f16600fd`

```dockerfile
```

-	Layers:
	-	`sha256:7b3fdfa893030d90fb43b9e1d60e3a64377613dd4aa3f9f9c65d1c791a1fb280`  
		Last Modified: Thu, 06 Nov 2025 00:25:48 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96edfd82d37b210d2d60ba4a33649e7f59b00160c6212aad19de7dea144e0a61`  
		Last Modified: Thu, 06 Nov 2025 00:25:49 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-bookworm` - linux; 386

```console
$ docker pull golang@sha256:836d7e2968d9773f768d05f34deeed02ad7d5d83edfa7425e6982975fb58b988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320001910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f667dc2937c65449f9644355b06638353fe315d420ef500c9bcf9bebdd5822`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 21:12:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:59 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:59 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:13:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:13:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce6be8e6c76b859a7e1808f7c9de22684a829f5386b5bf2011b85482d4d192f`  
		Last Modified: Tue, 04 Nov 2025 00:26:27 GMT  
		Size: 24.9 MB (24864369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b596182a9b4836dc17a3bc5eadc1e2798b0aa5aa0c8f50fec56b60d802ddb375`  
		Last Modified: Tue, 04 Nov 2025 01:32:07 GMT  
		Size: 66.2 MB (66233815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86daf7c585fdfcca8473edf091bc585d356fb048a78bbad8f11fc2b7cd1cccb7`  
		Last Modified: Wed, 05 Nov 2025 21:13:39 GMT  
		Size: 89.8 MB (89823427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7650548a4c02bd43552c205b0842e655bb371fc64b8ca906823098dd03634181`  
		Last Modified: Wed, 05 Nov 2025 21:13:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:64e0f28b3387f96d587b2a94d4bea8dcea22854920d414b1cc41379d6ecc9af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6eccb67386067c1ea3b40f80afccfa30edcf34adc56481c8d21992b5b3c9d8`

```dockerfile
```

-	Layers:
	-	`sha256:6fbf90dbdc8fa267ac8042dec56c7b1aea0d35544be4a74730031ebec3bccb83`  
		Last Modified: Thu, 06 Nov 2025 00:25:56 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9ac7cc6189038ce2feeebd18e8462e783c3d2b87e8db20291432522b67884c`  
		Last Modified: Thu, 06 Nov 2025 00:25:57 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ab6a0bc91b5eb40e60cd8aec2fb52bb30f6d317924f9e344db5e2e6ad3bacd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291259673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddc47e0805e5a9180dea0462350319d09e4055e508d7319f299179f8b7c0cd1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 14:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 20:51:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 22:58:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 22:58:46 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 22:58:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 22:58:46 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 22:58:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 22:59:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4dda2a1b7438becfe8c22a70ae85ee418f80df0feba9ce91b9ffc92338d47792`  
		Last Modified: Tue, 04 Nov 2025 00:11:16 GMT  
		Size: 48.8 MB (48761282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6492253d4f5d673ee74abc9e254c218714a0737c4c244dcc729821fb543170`  
		Last Modified: Tue, 04 Nov 2025 14:04:51 GMT  
		Size: 23.6 MB (23614047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f9457e9c1a9cba16fc581959f009772a1561916f3cc0ea635018606420380`  
		Last Modified: Tue, 04 Nov 2025 19:50:51 GMT  
		Size: 63.3 MB (63309635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96817f9c963b6341e1b5f5447538613cbea1464e6f61848ae7af7c6e1ea82e01`  
		Last Modified: Tue, 04 Nov 2025 20:53:40 GMT  
		Size: 70.0 MB (69997094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb1ab417de53c45975d074e15d8a2784ffc35415dd457eb8b64a5003a76fa88`  
		Last Modified: Mon, 03 Nov 2025 18:33:12 GMT  
		Size: 85.6 MB (85577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c1842e4e5b7a74cd2c07d8e63305a0900f833945b2e19322550796e36173f7`  
		Last Modified: Tue, 04 Nov 2025 23:00:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3693fc7bacce6f7177368f13ba4ef2454a8291ea3cb7e08b62090d67fabb1a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97aa099cb7aa55e448f48e3eb11e2ddb63f69efd1a44c008eb3ce27e9069b712`

```dockerfile
```

-	Layers:
	-	`sha256:e5c564484e05b27fee213d129da596f57dc5b2b904c3634a73fe38921d43c2fd`  
		Last Modified: Thu, 06 Nov 2025 00:26:04 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f77ae9cb77c8ed0e711bb80016338e77f39fc8c883ea97d6652ba2b249c83bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326554808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd7571f74837cdd7b5e7472126b0a682540e30a3a275f8d69d03cb5d44e01f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 17:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 23:20:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 23:20:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f89c76b3026966e039b432e1b66b1655c47c97f236438dc626e5acdead5cd`  
		Last Modified: Tue, 04 Nov 2025 06:25:48 GMT  
		Size: 69.8 MB (69845633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae491da057a1ecedda719939edbf994746baaceebb2c65c80485f45477c5981`  
		Last Modified: Tue, 04 Nov 2025 17:30:12 GMT  
		Size: 90.4 MB (90417820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8b7c967451eddea5494193c38ad1eb6a350c3e77ca7b8752138c2b224d0c8`  
		Last Modified: Tue, 04 Nov 2025 23:23:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:28db886f2a34615b7026101ecb4a121cf400caa74ab7e51fdaa1a07606f41188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd69728080daf2247de5a8a1279579961abccde6bd89f499987c1ef6ca19c8c4`

```dockerfile
```

-	Layers:
	-	`sha256:5c538651ef6b205edb672556b6f6ad100ae69d8313a4cc1ed46b5189a41673bc`  
		Last Modified: Thu, 06 Nov 2025 00:26:10 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b69509d7827add25b8d23d35f95bd1d07862809f63b3bd9b6d3ec2eeadb4f0`  
		Last Modified: Thu, 06 Nov 2025 00:26:10 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:2a19172774b17f846167e24bce77b47ef0a2616cfd9606d223912633edafedd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293509834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928e7725608b38c67e5c5807987a9cdd32cd8f67e6099eb3091a0bb37510b140`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 15:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 20:16:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 20:16:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a580bca43f6d623617841d967d82ecc7cf55ebeb22ce79064b23dd0b4a10ce0`  
		Last Modified: Tue, 04 Nov 2025 03:16:55 GMT  
		Size: 24.0 MB (24027417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba91dbdb50f511980482385b36987be0332dae93638fc6697a70724b1e1e5c`  
		Last Modified: Tue, 04 Nov 2025 10:00:10 GMT  
		Size: 63.5 MB (63501365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2be7085694577e3fac80456fe4593cc47ab34cfe6e160c21357497ea26b1602`  
		Last Modified: Tue, 04 Nov 2025 15:26:49 GMT  
		Size: 69.0 MB (69006411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf8e5a3c606b40a1d9397f0a3c27dafa275cbcd76bf80221588b5693bf06248`  
		Last Modified: Tue, 04 Nov 2025 20:17:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:85e95fb55d30339b7623eb9cca0e114ca55a39770d6d166d181eef22536bc558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a52bd338244980b593a0f2072779aa7d556a157ee2376c6fa4f9ccdd1da2c`

```dockerfile
```

-	Layers:
	-	`sha256:bb72a79969cbbc9fea2245aa33af3f9918f0dfc50c71c49be24163a1beb6adcf`  
		Last Modified: Thu, 06 Nov 2025 00:26:23 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f641e32f24e4e5e5794bbc23e1a4aa554c203a3bcc6da38c076c92dc8b84b36c`  
		Last Modified: Thu, 06 Nov 2025 00:26:24 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
