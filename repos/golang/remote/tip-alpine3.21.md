## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:607f50d4cc7e9ccfb649202288f5cc9e4e04eb5b9e3fda8cf5e3dac279698ec5
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
$ docker pull golang@sha256:49b4dcf705a1695280450009189965e524cd8cd6bd7d72135bdbd53c876a71a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87374491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4513818c580baa4cb6d30a4b675a1df696e31ac39a3f65666b3c7c51e48a7f15`
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
	-	`sha256:220d53a3f85db4ec5a87dd202af47d83ca7389ab97d619b6f5575d19ae03a2a7`  
		Last Modified: Tue, 02 Sep 2025 17:26:00 GMT  
		Size: 282.4 KB (282418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dff0c88890d852f1b6000c60fab1e5090230eba3301a46159a26dd4149cf4`  
		Last Modified: Tue, 02 Sep 2025 17:26:01 GMT  
		Size: 83.5 MB (83454344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3438b7fdbf3880d21664400d04457098d4376fbf823e0158e92a7383d012ee8a`  
		Last Modified: Tue, 02 Sep 2025 17:26:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:33afbce4751f9c53d2f6749713d26edbed9f9fa1b460a2335cb60e510570c1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d490636229c93f6ae02a60025dafbe1e5a065410a8b023caa6ba9123bf5a9bec`

```dockerfile
```

-	Layers:
	-	`sha256:9969f520e8d09b81e71803452774410f772e6762b45f0057dbbecc0281ecb3e9`  
		Last Modified: Tue, 02 Sep 2025 20:24:15 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9302360254dc8e6e3b84351fef850291cd1ed0e588adc3f38c8e11d4404d02`  
		Last Modified: Tue, 02 Sep 2025 20:24:16 GMT  
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
$ docker pull golang@sha256:05fa3b677e919b116660fe5736f55d0ac00f40b2d433046b98cd35bed62e92e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea549b0dacc11199e58c7de994e7c7cbb4f7b44d1d947903a5b3d0371078f18`

```dockerfile
```

-	Layers:
	-	`sha256:fd1388b70602b8c542f14e3d5ce0a2a2fdee2b06add044ada53b5b3c5a375de7`  
		Last Modified: Tue, 02 Sep 2025 20:24:19 GMT  
		Size: 24.4 KB (24401 bytes)  
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
$ docker pull golang@sha256:4cd6f842bae23d838daf5c3a165df5b468089800c893a9b2372c16574a6c0eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6348073db2304528b1633b82f46c5dc423e72cb0ccca505f38d8cb115042bbf`

```dockerfile
```

-	Layers:
	-	`sha256:4372863e39b0fed02275cb330214bf6c6edad8e4c14fc6e42ed9b914932de870`  
		Last Modified: Tue, 02 Sep 2025 20:24:23 GMT  
		Size: 190.1 KB (190126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2297c31b43cf14193e585b47a757168fcc346af7a63b1c58d66e7e8ecdfe44a`  
		Last Modified: Tue, 02 Sep 2025 20:24:24 GMT  
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
$ docker pull golang@sha256:aab5ae145ebd2c187c86c9241ad94868aa1da7ab2a011f7ebce1d2774baa8176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868d31dd258a46aff1e9c841a434dbd9651440e9f55161d7b60f20d95d4c30a1`

```dockerfile
```

-	Layers:
	-	`sha256:d8c512a01cb118ce45be31429b88573e2e278e55d1fa009a0db468f5cb335809`  
		Last Modified: Tue, 02 Sep 2025 20:24:28 GMT  
		Size: 190.2 KB (190152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11724d032d2c9742df6ff8fbbbdd608a3dfc4ead457925eca234143f82bdaf7`  
		Last Modified: Tue, 02 Sep 2025 20:24:29 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:cc76a4f03257403355d3efd97f293798c6dcbed8f1b69944529ee1e51734e9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85876547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9396ef0f0d6cd6cc41d6e9e7864453078ce31efd52be61b235027e80bcdd9fd0`
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
	-	`sha256:71ebd5c4c38fd7fee672ccfb4aebf27be334e097c78e2630284eb96091e8f3cc`  
		Last Modified: Tue, 02 Sep 2025 17:26:48 GMT  
		Size: 282.9 KB (282895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc969e7a30537f064821c7c82ed2000b4f696dfb82f12bececa0caf74f9469a`  
		Last Modified: Tue, 02 Sep 2025 17:27:09 GMT  
		Size: 82.1 MB (82132767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12523b551d1815be2f84d0b56ec27df981bc7e052e8d265a78a0de88b8ddf3e4`  
		Last Modified: Tue, 02 Sep 2025 17:26:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c37b60e11de4aa16dc0500cd9b64f297d91b6ee1a9243b5d80435c3df9b98ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff166e28952d807623b8e66a1756930f0309189b9fb1a4cb711c1f99d5dcfac`

```dockerfile
```

-	Layers:
	-	`sha256:034eb154c9762e5cef92702c7638f52f8f03cc214fa779cb54994a800d16b8fe`  
		Last Modified: Tue, 02 Sep 2025 20:24:32 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898fcba3e696939af24036ceb829015eb2d40bea2bf9c49f4233b829baf60a0d`  
		Last Modified: Tue, 02 Sep 2025 20:24:33 GMT  
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
$ docker pull golang@sha256:f2c85552447e5593056cad3895c2f1d447274da6552c1f83a637460b0a2b9df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bc8512d7270f561231be54c0b88375e429bf0cdab6c86d0348d3884826aafe`

```dockerfile
```

-	Layers:
	-	`sha256:a2ecd4919ab5ba307cb4d065f7c3965c58cd8e98ec1d9a6e6592a9c61357acba`  
		Last Modified: Tue, 02 Sep 2025 20:24:37 GMT  
		Size: 188.2 KB (188205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa4796db265bd514faa21077ec127519058ae48c938bed287869d426202f2b5`  
		Last Modified: Tue, 02 Sep 2025 20:24:38 GMT  
		Size: 24.6 KB (24553 bytes)  
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
$ docker pull golang@sha256:ed4d82eea30813b162ec05c874279d610982a6ab2cd02bb1f6af0d4b911d9eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85431007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5157f3b19cf03a81e56038118e2d208c2aadd783ba985c563d02313c02149e86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:c4bb0635d2e248956f88a4462ee973445c0bd3979670795027980550063343c5`  
		Last Modified: Mon, 25 Aug 2025 21:46:03 GMT  
		Size: 81.7 MB (81685324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab6b416d0fff881d6beaea8c8d2afe1fa95412ce01b9e99a87eba4b217870b1`  
		Last Modified: Mon, 25 Aug 2025 21:56:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:20f58b73c64420b5f36282d9539c8f151ab11ffd4a95475eba95a5d318faa7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 KB (212677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1db610a4025a44f597d4c4eaba39ffb2d3e96253d0739e8f6fe56596832a211`

```dockerfile
```

-	Layers:
	-	`sha256:af9eccd432da7007163ef372bb6d0e2f902b6a2f95ad467599067d5fa953b290`  
		Last Modified: Mon, 25 Aug 2025 23:24:44 GMT  
		Size: 188.2 KB (188169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a02a67360c975509f7c00aa1ab2105f5b9f708d9c7321c3cfb1d18a6233b83`  
		Last Modified: Mon, 25 Aug 2025 23:24:45 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
