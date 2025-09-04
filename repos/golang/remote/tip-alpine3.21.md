## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:198f32b51145fd7e9ae558c1fe1bcba041c1b4dcb6c8b2fba9b49c6be7d6046a
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
$ docker pull golang@sha256:a024aa133823b8f85dc5bc314295c249d2fb8b9e359bcbe5d0708564b098538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87374494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8760418b74bc5daa4df7bbe49b4b4a1fe086239db0913874121c9d735c4876df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146570fadf64efc0b9549bcb4feeb33f2dc95ce85e6ffeb8db1f6f3055a84e4`  
		Last Modified: Wed, 03 Sep 2025 19:07:18 GMT  
		Size: 282.4 KB (282422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dff0c88890d852f1b6000c60fab1e5090230eba3301a46159a26dd4149cf4`  
		Last Modified: Tue, 02 Sep 2025 17:26:01 GMT  
		Size: 83.5 MB (83454344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d7a7ffb4ba599ce119dc44e1d0034e243463bb22983259bdda8dd6454e580`  
		Last Modified: Wed, 03 Sep 2025 19:07:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b7ddd5747e74b850bc330303f2a6ba6793d5930e645c1df944f0c2f320c59734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bbbeafb76dcab2010b80e4b2c8163145053318f9391e8d6cc248f212688d42`

```dockerfile
```

-	Layers:
	-	`sha256:d10b92ac6b8dacfbfbafecadf3976356077590c77514ed17bba67b2ec5545032`  
		Last Modified: Wed, 03 Sep 2025 20:24:12 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b29fcd872060006efe9f2f1b0841f1f15f73066d840c2f299102508b6b38ef6`  
		Last Modified: Wed, 03 Sep 2025 20:24:12 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:a26d275f62ba881cb711ac2f40aa749e7f7d7d8c80104d4ef749dc609e26c0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84381662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fabc17a40c11f35f0b687279263a3d4076a888c2c89ec3feb80c5efeef1034e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:1c4f8085d3112f423ea1896156056d65bf494bfe035c7f45a8b926d0806a425b`  
		Last Modified: Tue, 02 Sep 2025 17:25:15 GMT  
		Size: 80.7 MB (80734416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441de33427440ebbb61e586657478056a8cf66c14d5df14d2a1e2640f5ec5ce0`  
		Last Modified: Tue, 02 Sep 2025 17:28:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0e10d5c6da815fb29ea91dae620e674e9f59ce8042afb3cc569d315416fc7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7faa3c655bd5eb3ba8e2e9acbbd913a3dc5e1365f3188557f7e2baf3db0de508`

```dockerfile
```

-	Layers:
	-	`sha256:343569dbc4d077fdf169f04edf7faaf6d0bd8abaf6979ff8eaf6c0e202b67849`  
		Last Modified: Wed, 03 Sep 2025 20:24:16 GMT  
		Size: 24.4 KB (24399 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:c4a7e037944a55f9152c645a8da216fa2c6d419c668d9be75fc758a63f0500c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83891781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ee861c8322f375c5608dd0136ed9dfa26672e65d04847eeb8298d934895e4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:c8183d7d02c47a9b085b3d0bc6d67309b7fa4b7ef97cac1694dc0b5ea8b6ce9c`  
		Last Modified: Tue, 02 Sep 2025 17:26:14 GMT  
		Size: 80.5 MB (80512289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706c9a46ed9caec58fa10d3543fe76d11c6bc5aa8d3de98b08b221c55657474`  
		Last Modified: Tue, 02 Sep 2025 17:35:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d7a45298661ae3633777d1826ceb43fcdcf261d72fd71b24dd5c1458864bc4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e934f1fcc4a8fab3b3168c051bb1e1dec0cc34913e16acc07a7c00b96f1beaa`

```dockerfile
```

-	Layers:
	-	`sha256:cef7b8d1b4234f439569935b6fc84cc4ff37ac6dc24602e35f11828bc9800512`  
		Last Modified: Wed, 03 Sep 2025 20:24:19 GMT  
		Size: 190.1 KB (190126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f330bdbf94011b509e923d0507b8d7d0cd8ff812c812d7ded125f2bedd5cd6e`  
		Last Modified: Wed, 03 Sep 2025 20:24:20 GMT  
		Size: 24.6 KB (24616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6c7ad52224e073b91da1d86a99c8eba8e8d3f7465acda7d9b418f2d09b63ceaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83735241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859840ff5297d51566288c10de30290e450f9fe975539e0b6eb4e842b502ede9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdac3bedee6d0b6d28da346629f79543b5f724ed01d0d3967167b284e2b25b2`  
		Last Modified: Tue, 02 Sep 2025 17:31:51 GMT  
		Size: 284.7 KB (284681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948ccd09d5c498d3bdd3015babafec64e8e01106fe6a739f268b131403fa7cbb`  
		Last Modified: Tue, 02 Sep 2025 17:24:20 GMT  
		Size: 79.5 MB (79463464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be30583a2fbdfbe30cca6313097faa555964ccaf7165939a93d91a224489042`  
		Last Modified: Tue, 02 Sep 2025 17:31:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:008664eb5dc7d396a2a6482c53b820b011ce33a177c96e4c46d0ef5fbc3e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8845b14c2a1f8081c2dd0677cd1ed605656ce69476ff5392ba9e6119dec8851`

```dockerfile
```

-	Layers:
	-	`sha256:47d77d5e0c5165e153db2f2fc9c150a51ad580ff49bfb0b7e3bd4a23cf8afc05`  
		Last Modified: Wed, 03 Sep 2025 20:24:24 GMT  
		Size: 190.2 KB (190152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01dfe2c8b9a12cc1b0d4c30133c2392b7991e49ad4473a80ad1e66c6bcb5c82b`  
		Last Modified: Wed, 03 Sep 2025 20:24:25 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:a02c64d98dba9a883955cc2ba7c1c6ef04410428047255168bdc21c27ad94cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85876539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488bf2f4ac9a7cb26aa4fcc7a6fd9123d27914f68e0535dcb1609726352418ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c7a39f2fadaca5e27ade178ff13da862661cfd9faeb84975347fcf4099b827`  
		Last Modified: Wed, 03 Sep 2025 19:08:10 GMT  
		Size: 282.9 KB (282888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc969e7a30537f064821c7c82ed2000b4f696dfb82f12bececa0caf74f9469a`  
		Last Modified: Tue, 02 Sep 2025 17:27:09 GMT  
		Size: 82.1 MB (82132767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd95941e21881edf30a2ad77929bd48defdabeb819e49bb5327e5b69dc3b85`  
		Last Modified: Wed, 03 Sep 2025 19:08:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d68776cb74832b9c7dd4a91175f093447a63eead1391eab34aa1cb1d1ec2b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0eff372b9cc9c48f7aa3d236b88228e1ea09ea114566eab00f70bcc9c9e35d`

```dockerfile
```

-	Layers:
	-	`sha256:0c9969d6fd2e0e0bb2a3966c55abe646e6e42a08cdc893087f83ff2ea256e710`  
		Last Modified: Wed, 03 Sep 2025 20:24:29 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee4c990d5f38bd675cb7851a3f85937121c0d8e91c14b82606cb25af6f19390`  
		Last Modified: Wed, 03 Sep 2025 20:24:30 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:c0e7707e45b69ec07befa5b60fb71d674a9ac7c633b8e60ac020218e182d3831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84670273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb7e1aa7dfe5226d964d1cd8f8cd1ec5743ff028c009e39ed411e652636b9c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05343cbd8895ac16fca565a0ad3f2f6a0dc20e79a602738d4d6b870a682cd2cb`  
		Last Modified: Tue, 02 Sep 2025 17:40:55 GMT  
		Size: 285.1 KB (285075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65adef97a585f4d6f34375efc6b453ef50bc737c051ef6eb9403cedd2e831eb9`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 80.8 MB (80815917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d11c89250f1e83f21fc4f86762015147955e516c92ccd49988c86dff73c5e74`  
		Last Modified: Tue, 02 Sep 2025 17:40:55 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:35b6a3822466f732fc95dceae636fa35c35df65eb87975471e1f727df469dc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ce0474826f6f82cf45bb71820de1b199279f190b4022a01d7d5ebdc9adc1d4`

```dockerfile
```

-	Layers:
	-	`sha256:76981d0cc2ead7bcfd33e21054b6d13a8cd9f3601fab72dcaeb5a4d1bfae0ec3`  
		Last Modified: Wed, 03 Sep 2025 20:24:33 GMT  
		Size: 188.2 KB (188205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efcee28be36b18ff6ae65987b25f2ffb7792ec26d09fc32ef3751c781b78f9dd`  
		Last Modified: Wed, 03 Sep 2025 20:24:34 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:4b2013ea1f804d87b731f07c1b342d2ad3d64b73054c652a6860bf100803c45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84523133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f1131478e025036c9f3f89052319df8d57789b3a8d3911f2a74d2593c03055`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:293eb689539c18522b5644ece27c44567aa0a4ab5ae7b74edd76c1cea9f0f71c`  
		Last Modified: Wed, 03 Sep 2025 05:13:46 GMT  
		Size: 80.9 MB (80891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be84f9f90c54b08b873a4928864560378146cf4019ba69629c073626813b9d`  
		Last Modified: Wed, 03 Sep 2025 06:37:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:f2a90b528bd92660bb37d8a43f16a5c3ce74d3a8dd2a23845b752f9bf9aef06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3780fd9cefa60e24a2c6a30fa112acb0831572ef5ca01f6a93d27d5f02b27db6`

```dockerfile
```

-	Layers:
	-	`sha256:67a4271a07b44f43bf22f37231e11c329a15d6ce68e435d21594f12df4b54927`  
		Last Modified: Wed, 03 Sep 2025 08:23:41 GMT  
		Size: 188.2 KB (188201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6045099696beec1dac0cb91b4044becacefb7565817c1c2cc13f1d6b767c289f`  
		Last Modified: Wed, 03 Sep 2025 08:23:41 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:b3f2b25bb2fa9089384be2bec78f6a00a78bbe478dfbb86e6a7577cd6c5e61bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85776749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715045172fba88edca7c523573fa38a347ad1f3405501500c950f6bbad3d62b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baeff4e12a448b03c9a0556e687e666d81fee45be531e32b6b5f75090e58bce`  
		Last Modified: Wed, 03 Sep 2025 20:25:47 GMT  
		Size: 283.4 KB (283440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d5b2317c0e6d0b707d21864c7e46b8277ee225d4365f7839ca2960a88e985a`  
		Last Modified: Thu, 04 Sep 2025 01:06:05 GMT  
		Size: 82.0 MB (82031053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34378821d9c0366467d75fac0b053b8bc75ad605bd464577a87dd3cafdcbcb07`  
		Last Modified: Wed, 03 Sep 2025 20:41:43 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c6634b253fcfaf4cc1c4dd7c25f1c7015379f8bab783200c449ea8cd8fcab05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 KB (212677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e0a0677dd4645210d5f35082f8fd0c48db9a0dbfff54e92c66eff5a5fe09d`

```dockerfile
```

-	Layers:
	-	`sha256:9c4c63c80fdfbb427ef0d7027ba39918cba31f1db216b4415e3ab1dd265ba585`  
		Last Modified: Wed, 03 Sep 2025 23:24:37 GMT  
		Size: 188.2 KB (188169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82370ceac62870042d88812ab598d5eec03f36860316d2deaf56971d7adb31e3`  
		Last Modified: Wed, 03 Sep 2025 23:24:38 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
