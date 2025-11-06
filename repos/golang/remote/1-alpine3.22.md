## `golang:1-alpine3.22`

```console
$ docker pull golang@sha256:8b6b77a5e6a9dda591e864e1a2856d436d94219befa5f54d7ce76d2a77cc7a06
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

### `golang:1-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:96f36e77302b6982abdd9849dff329feef03b0f2520c24dc2352fc4b33ed776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64245641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86e735e7a39c546c1f105f637c63efcf44f4d6d285f9d8f524c1c62d9125377`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:18:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:17:49 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:17:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:17:49 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:17:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:17:49 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:18:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:18:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005175e490b0ff92097d506946bbecbb38ca5479503236dcb3350f2da29b1cb`  
		Last Modified: Wed, 05 Nov 2025 20:18:45 GMT  
		Size: 291.2 KB (291160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9d4a4eea0de466b378fec1876ea74acd9465fc6a1d15368a117eeacaa21b7d`  
		Last Modified: Wed, 05 Nov 2025 20:18:32 GMT  
		Size: 60.2 MB (60151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae96bccb6682de86f077a4ef76a3024218e06114ae177db9ad565f2be5a0e423`  
		Last Modified: Wed, 05 Nov 2025 20:18:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:451c5169d54d2a6d928014db595624018d652b0472edafd094a1a877a0b8f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf957e09f2b674a27745dadaabf25905d707e28e8c9ed81829a835bd50d1b74`

```dockerfile
```

-	Layers:
	-	`sha256:edc85e085b36c960c096c3ecb77035653310919fd0bda1c66d41c9e45c074e61`  
		Last Modified: Wed, 05 Nov 2025 21:23:05 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199a7113bc5f2e777f4b7f89f21d96317597e9c19d436ca408bf9121c0ada9a0`  
		Last Modified: Wed, 05 Nov 2025 21:23:06 GMT  
		Size: 26.0 KB (26026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:a24c381d0383b237be8a4dfc38858883e40737d62ada3f2af2180ccc8da1893a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62868600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ee3af206e4f065943e3397807ae0b82917fd570bc7373baf9e4302da438a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:15:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:15:22 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:15:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:15:22 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:15:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:15:22 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:15:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:15:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07afe75e6854373e30caf12c0d6e46cce3030ab72c031b93f11155b2e58891f3`  
		Last Modified: Wed, 05 Nov 2025 20:15:46 GMT  
		Size: 292.3 KB (292317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82229606d045e3bf5b3d666cc06b953ca48f62773919b720b3dfdeb45e64bc8e`  
		Last Modified: Wed, 05 Nov 2025 20:15:52 GMT  
		Size: 59.1 MB (59072045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e302011fea114ca069efc60577762159427692541e9be15f7af04f1b6c3a8b70`  
		Last Modified: Wed, 05 Nov 2025 20:15:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d132f68828970e76d55d6a8d8e8e26d14794beddf77fc583b0c3b3031d04677e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43e3f34b8def0fa2b534b0f5cdef18e736bce3209e33bf5e8c9c8c48d7c9251`

```dockerfile
```

-	Layers:
	-	`sha256:822a6c36acaf82781c12316e14d88cac08f9632ca5d8597d15a4600864086cd6`  
		Last Modified: Wed, 05 Nov 2025 21:23:10 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:18993b4792ff5c94147a07c749d0fa93ebb9ddb64710a70be55b2f78a2d19669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62585107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3b6c4028546ca3552dacb06115ca2170e2b2e118086ff00858b9568fd3eec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:17:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:17:32 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:17:32 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:17:32 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:17:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:17:32 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:17:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:17:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1cbd4d00de10f1ccd8e9cd575f313cf0834eaf5e9a79f150a6890d42f5bc98`  
		Last Modified: Wed, 05 Nov 2025 20:17:54 GMT  
		Size: 291.2 KB (291214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005e5e3f870b603812d4e2b76f2d3cd35fb32a7d8a09fbbc4d31d3610a5033ab`  
		Last Modified: Wed, 05 Nov 2025 20:17:33 GMT  
		Size: 59.1 MB (59072180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a246aed21745c7139016120f286dc8eac916f4e8188ded36960e3ef1f52507d`  
		Last Modified: Wed, 05 Nov 2025 20:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:cd48ed13965c1de3e1f44b121854adf1a9329d1087c71730b3cfdd6d8363a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 KB (221781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681697df84ba61fd5cf57f4d6f2dcc973a2001b3772eb040b4cefc3a12c84966`

```dockerfile
```

-	Layers:
	-	`sha256:b2cdcfa940bc036afe338415b531ca1e413a1e0a50f91d1aebf7b2212c3b5811`  
		Last Modified: Wed, 05 Nov 2025 21:23:14 GMT  
		Size: 195.6 KB (195616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dafb43cf06d1e054233cf23c72885c1560076d2980f8ac6be2d0ddbf65841de9`  
		Last Modified: Wed, 05 Nov 2025 21:23:15 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d1a86de5b6e2f63d4aa907f104045b9676081bae999fdec8f43b238b45819a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62083992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dd1848490fd7a0716ba94b718a2496e061e8f428b329c02c8b24b9191cc013`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:20:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:20:36 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:20:36 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:20:36 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:20:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:20:36 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:20:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:20:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f1ad36a5a83c5a5f7482a06aefd78ca2e2c575913005ca05bbcf64fec9b080`  
		Last Modified: Wed, 05 Nov 2025 20:20:57 GMT  
		Size: 294.1 KB (294093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cd0526a95aa822822b8c4a246e8d3cb0ad0abd58b11c3ff2e34a74e1ffe9b`  
		Last Modified: Wed, 05 Nov 2025 20:19:33 GMT  
		Size: 57.7 MB (57651672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b381f593327825af561f9a2d04f44104c8ad3ae820768cbd9a7acbed30f1fac5`  
		Last Modified: Wed, 05 Nov 2025 20:20:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9bcb0a8f0682a07a57be7ede58709c007c33e6aeb3e721949078b2a5d65dd3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 KB (221875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e2d8ef759668d3dbf57855099ed6c8ca45d9b75cf6954b992af03298e5b4`

```dockerfile
```

-	Layers:
	-	`sha256:d9b8b33acdb9ebc2da94558bf724ef507e34a85333e209967d5f7a2a8753def2`  
		Last Modified: Wed, 05 Nov 2025 21:23:19 GMT  
		Size: 195.7 KB (195666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:858aff4856ccb94b97a6256c21eae3bc12e604ed3c6f83ea7287ac713c322e09`  
		Last Modified: Wed, 05 Nov 2025 21:23:20 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:154a3d4ba5a80316771e042c706e5e0f84e01e80d3ccba6bc7df6ea93702e93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62781727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0cecb290ae5202f8f2735b3820daaf1c9ac5a40dbe29290fbb690a46585411`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:16:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:16:13 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:16:13 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:16:13 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:16:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:16:13 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:16:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:16:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe051471f0c1169368d558e6cb755aa3cbec075c33e08fa0cf32fd3c2218b1a`  
		Last Modified: Wed, 05 Nov 2025 20:16:34 GMT  
		Size: 291.6 KB (291634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb3e80f5b54e127a93e5c4d633621083cf9b0a94288cc3bff72b650fbb53f1c`  
		Last Modified: Wed, 05 Nov 2025 20:16:54 GMT  
		Size: 58.9 MB (58871003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca987d550a5416b49d67d32a5c17e1308c0f978fd39973b9bb3bc62a40c3964`  
		Last Modified: Wed, 05 Nov 2025 20:16:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:507d8b400511a43436f9d58b0b07106ad40c99028e4181bf4bcd75629d1fe9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e385708d19c303cba689e67417ec12a614ec99d2807eeee6d77969762a1148`

```dockerfile
```

-	Layers:
	-	`sha256:c3e9f9f2524de6e2b6b8b6291fa0bb1158ef665363aeafc35e68e994366e52ec`  
		Last Modified: Wed, 05 Nov 2025 21:23:23 GMT  
		Size: 195.5 KB (195503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36884360e60182760930b79644aa01a079a5b12bf4e5736558e99d0219d90bd`  
		Last Modified: Wed, 05 Nov 2025 21:23:24 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:80c2c1b4239e8400643db42891bca3d1b65ea242a452cfbca27c0755d982d752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62160101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985dec420a9d772bf06c1ecb5a1aea1e2b1df4d262cb97e66c88081516c9f535`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:17:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:14:57 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:14:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:14:57 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:14:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:14:57 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:18:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:18:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c8bd62217b855f213063830cb5c2b3ccc4717b8ba91afea33b4f12c5e23dcc`  
		Last Modified: Mon, 03 Nov 2025 18:18:26 GMT  
		Size: 294.6 KB (294587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2470fe8e729e39478adbcf0e2206e2b0fe316cbf8e73d84d0bf464e839a1aa00`  
		Last Modified: Wed, 05 Nov 2025 20:16:13 GMT  
		Size: 58.1 MB (58133115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0834934dea77468ae0e5189e36b259141d724ddc3580509a4fa1548db653bef9`  
		Last Modified: Wed, 05 Nov 2025 20:18:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7dcf14d2f8bf2bc357b334ec1933051bdcaef4479352c09ac9b8c850ea47f9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 KB (219782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bafca8c5e8632e623fea53ad6b27ee6379c2b5792f4a50e2f9a34f5415b35e3`

```dockerfile
```

-	Layers:
	-	`sha256:a3dfe7965b51c1449e27a6e40a196a16cf1ba579ae6d16193aab54b7a9f47337`  
		Last Modified: Wed, 05 Nov 2025 21:23:27 GMT  
		Size: 193.7 KB (193683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c994c002455422262f57101195e99969eba1c8f578f1a0eaa12fadf061a069b1`  
		Last Modified: Wed, 05 Nov 2025 21:23:28 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:ed107a1ff1bed41cd66fe7fc939408b432bc2eefbfc9bb718b175588dd5e05f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62477153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c193ba18f3dad789262f2392788980eebcf521df16e1bc3b218e295d18ee8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2055b904ba40ebefe03b802bf4885ac2708bb5c47a4294058815bff9a5ca3b`  
		Last Modified: Fri, 10 Oct 2025 21:04:20 GMT  
		Size: 291.5 KB (291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7738f55d50b335f992c80eaabcdddcb36c67eae2749a3858d5261b9c2e4d583a`  
		Last Modified: Wed, 15 Oct 2025 07:20:46 GMT  
		Size: 58.7 MB (58670244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d07361f03b2c716f1b16e3f9b2bcc0ffe616e2758f085c2adda69bbd0f351`  
		Last Modified: Wed, 15 Oct 2025 07:26:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:496c12aa18c612ae9c14c95cedcbc4a1970cf332eecd05be02012ad38e16d8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 KB (219821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831c6b0f7aa5c566df541431435bba4b3929cfc671abe7790e55dcee57301ee`

```dockerfile
```

-	Layers:
	-	`sha256:7fea5de439ef43bb22ba71dc7fc69ed5a8d3cdd83177f031254e03a42f810b48`  
		Last Modified: Wed, 15 Oct 2025 08:22:39 GMT  
		Size: 193.7 KB (193679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0285513fb5ac76e3e6cca621c90be6dcbf819ebb301f0c48bede2bfb5bd2d7b`  
		Last Modified: Wed, 15 Oct 2025 08:22:40 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:05497917d64fc62a3c20aa0c4f87c77e86c149064273e255a06f736b13fe69eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63425212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762450a14f52ae1d5556fa4287bcaea0858b96063265cdb847f6a617945936db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:14:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:15:38 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:15:38 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:15:38 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:15:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:15:38 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:18:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:18:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce53ff9bf2eef5053eb507e6c4a528322e0535fda9d363fa7b72a5259d021f2b`  
		Last Modified: Mon, 03 Nov 2025 18:14:51 GMT  
		Size: 292.2 KB (292156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe2a4ea5a438feafc93392d55b50ea8eee2e47563087161685963824d4cb40`  
		Last Modified: Wed, 05 Nov 2025 20:16:44 GMT  
		Size: 59.5 MB (59483654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77654748a1a8b65734bda7544ee4f147fa0796982fc7bdf802e5662bf1bc5801`  
		Last Modified: Wed, 05 Nov 2025 20:18:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6722dd057031593cbb78ce8b7f332878a3cd62f30f61539622eef10caa382dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b7a9fa3d7ccfaee832e80f6277dc5fee7a54f23318741e8d1c17c154d9f7f0`

```dockerfile
```

-	Layers:
	-	`sha256:36573ee6b25342f0f0a6a25fbef1eb992b6790b83e3770bb8680bdefb4e7fb7b`  
		Last Modified: Wed, 05 Nov 2025 21:23:35 GMT  
		Size: 193.6 KB (193611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1933fa0fa08ac374a5ce3be57bd5b2833da07a1822c479aba8c4bdc623e719f6`  
		Last Modified: Wed, 05 Nov 2025 21:23:36 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json
