## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:d8bae75d97c2550ac19975f95eac40b887edb38368c22351c937b416f54fbdcf
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:6f1a61de063122e39effbf104366e47a02d0c9bd9c175583d9dc5e649d7695fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86987832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71e232f4af0f2c5e8db4eb2d515e14326958a03b07a2a898ce9dd88dbae7e5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e964c3672912847fccd51f571bd810ab870c841ffb6e7e991bf936ee3afb8f`  
		Last Modified: Wed, 13 Aug 2025 18:31:47 GMT  
		Size: 282.4 KB (282423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70f62131fde5fdbd86a9a07a13b0d6d65a669fadfed0d46fc45a0e67fef05d`  
		Last Modified: Tue, 12 Aug 2025 18:32:41 GMT  
		Size: 83.1 MB (83067681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b5524c8e235d29ea9edf5bb3e2ea9ffbbab4e7dec6c3675d0e74136aed5142`  
		Last Modified: Wed, 13 Aug 2025 18:31:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:7d2ba333e756bfdec3f28a87a255cea97309586b2636ee8e1f880642f15028f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075151180e2f0a33121e3ab1ea94fc9aa08101b2666b37de3547fb6d912c73d0`

```dockerfile
```

-	Layers:
	-	`sha256:dd9fb33f54b9d774ead25c73e04e6e3b41f5cb3cfddbda8f1ed3baaab09f0bef`  
		Last Modified: Wed, 13 Aug 2025 20:25:10 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9900da5e84abe68a5a4afcade957cb756cfbee5fda1cfce16801ded85799ca6`  
		Last Modified: Wed, 13 Aug 2025 20:25:10 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:adaf6de490751697f85ce7b9be1f5d9815a89513ebac8124a5c7a27998c36fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83974519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff040fb97c4616e7e17f3abd8182aa6132cd5d2f00297b8c2a87c318b8e2cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4a214d6543aa5b234ca6b16aa4d8e27cbc22cad32bed5ef48890ed7409c406`  
		Last Modified: Tue, 15 Jul 2025 22:48:38 GMT  
		Size: 283.3 KB (283275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4874e979a2732f21fabc48aa296ed9fb88188b28b85ad587d534703aa9494a7b`  
		Last Modified: Tue, 12 Aug 2025 17:55:10 GMT  
		Size: 80.3 MB (80327273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2d3838c186bb995059461323b2c7f5fff4d8ec4649d1584d4c1453630acfda`  
		Last Modified: Tue, 12 Aug 2025 18:40:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1a72bf4ee1cc7227c6bfb0725fdbf7f45391938b95b7a274795527827fcfa599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edeb5c1fa914a720e6b092e4754086ac481ebc56bcf14be07bf68613e537798`

```dockerfile
```

-	Layers:
	-	`sha256:a18e81d1d2d236fff642198658b6dfd11f7d9e0e5d7d78c26b1282f8398eae28`  
		Last Modified: Wed, 13 Aug 2025 20:25:14 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:82038263a44335ec1d57acada417e626837fcf6587a3956aec12d6933fb5f9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83459934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e905e533bbd733c9174653edd44fb7f2900eba1ca2a4725812a860d6f6264`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce1ad2f4fb08bb90f837004e5025b472d374435573f34a4ee7d7287172cfa5e`  
		Last Modified: Tue, 15 Jul 2025 22:36:22 GMT  
		Size: 282.5 KB (282462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d10df13da6c65403fe5e3b6a9cc280dde2bb564435b287f2b85119c986cc8`  
		Last Modified: Tue, 12 Aug 2025 19:00:44 GMT  
		Size: 80.1 MB (80080443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda420816aaa74edc1dda2990da1e4dda01881f7c03d17f2ece4affe2a81735a`  
		Last Modified: Tue, 12 Aug 2025 18:08:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a195415a45c145b9e027432b25f7f63a2fd1d897ef01e1b052e23549678663ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a57812c7662883a8c24eb33b1d36ce29d63759712ad2328056b3273a7ad9b`

```dockerfile
```

-	Layers:
	-	`sha256:fe79c3a3ce1c4ee6acf68794095674993b27154726830c451bc6a69c06b2b53d`  
		Last Modified: Thu, 14 Aug 2025 08:23:51 GMT  
		Size: 190.1 KB (190126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0cb300eaaa232de8b2f0914dc118388a9202993d951c5ee17dfcf0025a4b5b`  
		Last Modified: Thu, 14 Aug 2025 08:23:52 GMT  
		Size: 24.6 KB (24616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ed1a10566bb6eef3cad232d2550af4d5701e0760b6ba27cce542bb17db5e4081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83277194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b4d2eeca7f5df44feaec3df462bbcbd6f778870d130136d26fc9043dacbd1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80bb7562bd7e03fda0615c89df2976c21bcf7fd34bd1bfa24010374df289e7`  
		Last Modified: Mon, 28 Jul 2025 20:57:12 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b7cf68665eac7cfd64f5bb944a8b17de913d4de7e1d26ec5a73f422afb207`  
		Last Modified: Tue, 12 Aug 2025 22:36:24 GMT  
		Size: 79.0 MB (79005413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9500d5659433fb46eee84660f0e23470b8994130ae93b8c80a5b69a18cf2a`  
		Last Modified: Tue, 12 Aug 2025 22:38:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:3fed1042d323cd681b9be2460c62cbf47e469eda9838357903b223d508c32c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac4146f17bb8926f9a4b429dd51f4173e65666e4a12c6e0fac5cb979f2d5dd`

```dockerfile
```

-	Layers:
	-	`sha256:d6c18d665b6baaf502f7caa972051f0a738e2518c218f108762b16cd320aa10d`  
		Last Modified: Thu, 14 Aug 2025 05:24:19 GMT  
		Size: 190.2 KB (190152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab8b776c3f0d608bbc8bd77cc32cf48471e2d1cf98caf42b6edbfce2691dfad`  
		Last Modified: Thu, 14 Aug 2025 05:24:20 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:2c96249da7f4aea031cac419c3514400619fb2fca3dcb5cdc52a449af2269bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85437601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9ea1ffd28333710350caeea6a6c053618b031b4096dc4dc7e22acfecf8445e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae823964c8c06ad4466a22f861f59504c29e0a74390c4efbbecae7ef6d562b06`  
		Last Modified: Wed, 13 Aug 2025 18:12:44 GMT  
		Size: 282.9 KB (282886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be820729530544d2d8ea257bf2456efd73f0f38ff4c7f538f538e091c491a7b6`  
		Last Modified: Tue, 12 Aug 2025 23:30:08 GMT  
		Size: 81.7 MB (81693831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968f8f20bc624093a62c9d2f1e1ce7685af176eb84f63eadb10e2c75fb6fbac`  
		Last Modified: Wed, 13 Aug 2025 18:12:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:85f089824fc8edf801d5fe3dba6c4681ae2c7c3a924ccef551afc4ecea3f775c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2a29f271628f7baa42292fdbf5f59697648e8b82eeffdf519a2467a920ad81`

```dockerfile
```

-	Layers:
	-	`sha256:e5b66e2e4b5749a568d7191a623d2b1d9da37c17167bed2bc86552d8f048fbc8`  
		Last Modified: Wed, 13 Aug 2025 20:25:22 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2cef26ba45ea6a8072d8cbb6426e9baee578daa702610b3758667e01f4c5c7`  
		Last Modified: Wed, 13 Aug 2025 20:25:23 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:65e4622c2d454d3890017b48d350b7676637d87aec28a1f34a54a4c1fc8115f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84257379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660d94f872af25a0f04efa158f5fadc6f89528d2fbeff0bfa88eddf9de7b8c8f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292e2d4d9d8706c1de48009e1d142646f4d2a8bd05fff7fc3f70c75ef02d1c0`  
		Last Modified: Tue, 15 Jul 2025 22:37:55 GMT  
		Size: 285.1 KB (285061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d949d12b56c803641dc1ee823fe0b4254f92598b51ea3dd4b12bbfc422e9b7`  
		Last Modified: Tue, 12 Aug 2025 23:22:22 GMT  
		Size: 80.4 MB (80403035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02f8d1ff57214caeb1d39b5669a8862a991d4ffb5476fb79df48c4e6dd09de`  
		Last Modified: Tue, 12 Aug 2025 23:25:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:da15affc33d6c97b7406589a78dedf9626f5ddb034f52317e95ace6d956d70aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700d62b717565c39c086184a9973ae9f6a1a6ea2c59edeff9a1e0126c52fb100`

```dockerfile
```

-	Layers:
	-	`sha256:e8e18d7754a624e918db253ceddbb30b677b707b44083e38cd4af23a17711958`  
		Last Modified: Thu, 14 Aug 2025 08:23:59 GMT  
		Size: 188.2 KB (188205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b040e8126730e5712b1653eaa5589cd56be3097c93fca6d6da5df21e75f6c87`  
		Last Modified: Thu, 14 Aug 2025 08:24:00 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:5747ca2d647f31fe4de8cc554ee2ed89e3503826d4386455a760746b780a853b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84099249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623353d9a27af7f0269d626ee0ad2187c0d6dccd89cb7be3e5740d62acdce8b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c1159826bb23e5196b06096f2b66ad808c31d84200f35d658ee413af6cd93`  
		Last Modified: Tue, 12 Aug 2025 21:35:10 GMT  
		Size: 80.5 MB (80467250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f136860aa750814ce15f6d4c53c6fae29021d6eaa3b69ba9691daadd8a2d568b`  
		Last Modified: Tue, 12 Aug 2025 22:07:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6f31a340b30dbdf457d1baf2b3ad3e3f4ad4327df58f1e8650c014bbdf58880a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea44710b6761c0dee688403c0f2ef5eed735aaa6a88197867c1a5579bbf6a95d`

```dockerfile
```

-	Layers:
	-	`sha256:1737cc99960ee1822c02e3e7ed8db2a566af0941113f1f0607048802a3fca6af`  
		Last Modified: Tue, 12 Aug 2025 23:26:07 GMT  
		Size: 188.2 KB (188201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9b8753b5121fb90e027367dc153f031161ce1cfd7f27d070ab4f59d56a0157`  
		Last Modified: Tue, 12 Aug 2025 23:26:08 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:04306bd5ba4017d47cb2adf8228899fee1b8697e7eaf541cf3dd91c8998930fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85367045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b60f7029a602ce1aa50b76b366918cfc0f2dc6609d683fba274b888d977c48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c2184ed1d560f97be7198cd6f9baa12de8a0aff6bbb89596217c942ed2797`  
		Last Modified: Tue, 15 Jul 2025 22:45:47 GMT  
		Size: 283.4 KB (283425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e557abe2162386c1768ffea94bd0b2e886c5afefd7b5aaadb4e3de900ee87e0f`  
		Last Modified: Tue, 12 Aug 2025 18:48:02 GMT  
		Size: 81.6 MB (81621362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff3c91e6e9c44924c332dad215f70cbcf26dac9017625820a6936625451dc5b`  
		Last Modified: Tue, 12 Aug 2025 18:54:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d94fda2c15b367555327843da0f53afd1bf1a708899561ce29ac334540089247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 KB (212676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7a864210d092f3fdf0f52dd76b0250f33b3083a1a2fad9ca8df38d5c89f115`

```dockerfile
```

-	Layers:
	-	`sha256:0ae10f7ca47520e81714946e8202487cb9099e0c0a62626848d4b29f1088d788`  
		Last Modified: Thu, 14 Aug 2025 05:24:29 GMT  
		Size: 188.2 KB (188169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9976df5000c675d4decb1a96facec7e192277b0cd7578ca441af6268e4abf6`  
		Last Modified: Thu, 14 Aug 2025 05:24:30 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json
