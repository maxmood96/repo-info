## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:aa54274f672b786d8452bc355ba2c1d21707d91858d73c83cafbee0ea58b6197
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
$ docker pull golang@sha256:6b037ee8db73417663f4db3e17734d6954add60b320b83b11baa7bb9b3eed9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87546794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3347f7f4b4093996c4226ef2715d07ec140d9b5f718297681d872641368266d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaddba19329518428807a7f97ac94eb1905281a1d808dbd851f40dec4f634aab`  
		Last Modified: Mon, 08 Sep 2025 22:12:10 GMT  
		Size: 282.4 KB (282425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ded06cd7fc4272134c8fd8dd6fe01e98f582c7adaa60ab9166ea8bfd71723`  
		Last Modified: Mon, 08 Sep 2025 22:39:32 GMT  
		Size: 83.6 MB (83626642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f53ba0d3cdfda0408e3ad92b99a4e91114f05543f2210111e10c13a224ce09`  
		Last Modified: Mon, 08 Sep 2025 22:12:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:dab8c0098a022dff913b6547fd4a371dd39bf934668d0761e27a8058faf51097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032df454f0e60fbd1bfb9fbc2652903bce17a5df6f9d7d221e87d92a39572655`

```dockerfile
```

-	Layers:
	-	`sha256:43dab870dadccb7ab84c11f8494519573dd04c615f5e0c9315c2577ae19cd7f2`  
		Last Modified: Mon, 08 Sep 2025 23:24:34 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5bd6bbac82a3db9236820df346cb5bb680aa9c00ae4ea260baf950ad04cdf5`  
		Last Modified: Mon, 08 Sep 2025 23:24:34 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:3bd5119690bdf158b3b90a210889295eb18b8c30969af03649687ee57793de7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84542758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546abe4d77098a223700c4e135a5dd4520f156822e87b7a76765931cca3e4a99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355cb49f6d62a0602e21370a5159383ad8ada7a0c094cb57bbf04fc9c2f4927`  
		Last Modified: Tue, 09 Sep 2025 02:00:03 GMT  
		Size: 283.3 KB (283281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcbe18c0f889b22c938684b528ef1c3ed22f9b8e65f539809799c450b1bf80a`  
		Last Modified: Tue, 09 Sep 2025 01:19:49 GMT  
		Size: 80.9 MB (80895506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116995a16a38d1a2f33e562f6da517fd692f433b29c9312ba39bf5a141738c68`  
		Last Modified: Tue, 09 Sep 2025 02:00:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:50cac6f9befee5274050abfdcf5984fa12c79a921b0543986e848b8782f30917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823a12cd17576d36b7d93400895925c80085a3b52b85654382386f92ecbad26`

```dockerfile
```

-	Layers:
	-	`sha256:221194a2aaed907cd79961520e3d02500b8d327e26375aa98e42f27826af6a6f`  
		Last Modified: Tue, 09 Sep 2025 02:23:18 GMT  
		Size: 24.4 KB (24405 bytes)  
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
$ docker pull golang@sha256:83553b57d139e6dff9445e95eecd1830d1ef4c65e1c2a915ba2f160e226a4ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86034306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2b9cc52a41811368fc7561bc757e83aff87fc69c36c60ca0b89e46f19d79c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24739a97cc4ec65c733a396ecb14b0924dec258f3bd652c64ddfdc2e2247d`  
		Last Modified: Mon, 08 Sep 2025 22:30:34 GMT  
		Size: 282.9 KB (282879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518dceeeab292a9ac96f797a930543374e02f8a442c539c30c018a2f30d27fff`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 82.3 MB (82290543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9b5982fa559aab5f88b4b5433a42b3e863192c33cbc264a01ea41ffe06ebe2`  
		Last Modified: Mon, 08 Sep 2025 22:30:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c4e87384fc719009a3db2ad74eba2a489382c25f7e25d5e4f915cc97f67ca26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ed5f89d2f56ba91fc511300de98586ab2ad35e8fe6e63bd3084d5df8f3df35`

```dockerfile
```

-	Layers:
	-	`sha256:1a7b3c0c44d79dd5b5fc36130bfcea6aa8121f7f755d9d1c77df95847682393b`  
		Last Modified: Mon, 08 Sep 2025 23:24:38 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a9e350dfe93127f6e4a2d660d12b2f30db4c1f7d28dfcc9ad8501d9386b7f7`  
		Last Modified: Mon, 08 Sep 2025 23:24:39 GMT  
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
$ docker pull golang@sha256:7ac46e222f4817ce379641bcdc40d94c8808aed13af42389340525066acb03fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cfbff5f74186a195b4aeff38f892560e006e681f09c344d7ed80e09b26c2d7`

```dockerfile
```

-	Layers:
	-	`sha256:4749b0f1e5ca29cd859f5b0fb4fe2f8259200c12d3e9f227de41aae448c70167`  
		Last Modified: Mon, 08 Sep 2025 08:23:34 GMT  
		Size: 188.2 KB (188201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22490922ed46f236750af8da010d1dd63114a985df219ec80c80145706ca49d6`  
		Last Modified: Mon, 08 Sep 2025 08:23:35 GMT  
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
