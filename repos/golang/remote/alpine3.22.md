## `golang:alpine3.22`

```console
$ docker pull golang@sha256:3587db7cc96576822c606d119729370dbf581931c5f43ac6d3fa03ab4ed85a10
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

### `golang:alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:18a5f71675ef62af731b00ac0bd22dd54133365ec0558bd93e203c578afc7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64245080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60343179d354cc763b5b4ab89f5093bfeb7a6846549ba266783ff13595994f77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:12 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca2393419fe3a74cd2335a6f38c974ac4018810e984e58d4eb9f8504e71be1`  
		Last Modified: Tue, 02 Dec 2025 17:47:38 GMT  
		Size: 291.2 KB (291156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09615bee918a0a1913f982926164fe321067b4ae8a2bd5e632e16e062e052073`  
		Last Modified: Tue, 02 Dec 2025 17:47:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:643fb7521bc79798337d659313090c02ad30c836fdddb8a100918117a3ad8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d931aacbdee9bee2b47af78087893500ae45943bf7991e694098609dd28598`

```dockerfile
```

-	Layers:
	-	`sha256:a7e0d6d5ddecc543c05757425f153607ed9a85c0b437441bed990cae153a83bf`  
		Last Modified: Tue, 02 Dec 2025 18:09:22 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbe145edc7f49601bba4f7dafa25ee206d8fcb6f380189c2c4590b3b4efa4b28`  
		Last Modified: Tue, 02 Dec 2025 18:09:23 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:f8629c643ffe4b76e09be0b3609b48d45a8527732d6acadbc8e532bf77f3e537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62868496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6547d37cb106cc6b59150972ae8312b6239cea43889c9757cb744866fbbc3f03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:46:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:35 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:35 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:35 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:35 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018d563333bae8e633faf8bab936767992815a7a24d1f1c4c31fb84f26f383a2`  
		Last Modified: Tue, 02 Dec 2025 17:47:58 GMT  
		Size: 292.3 KB (292303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43dd4211ee5273ca0c5772840c1a03b86bde39c606d1c608d88cc81d6d76501`  
		Last Modified: Tue, 02 Dec 2025 17:47:55 GMT  
		Size: 59.1 MB (59071955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5368840f9d54bdcc8859d425dd09f7810866f7c939caf326919e8738ca36bb`  
		Last Modified: Tue, 02 Dec 2025 17:47:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:79f5e352a6ce99b56cc1b87c927fc9b1a07f0791af024d3dbffa8676d3022c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fefe574ce19ddc0d843ea0dcaa27e6d643a7f8052ab6aea6a78b7b2adeef2ca`

```dockerfile
```

-	Layers:
	-	`sha256:04f7ef1987b8a8b01bebbe36eb249cd34b27edd39bc5a7949d1babf8040360a0`  
		Last Modified: Tue, 02 Dec 2025 18:09:26 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:13941f39a6717f6ed9c9b60a9b799eb132eb6add05fe2a7d91ee68ec99f16169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62584992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb46ca954a3ba1e670363d6b47e2b7717ff60bbb5f598600ce28dfb7c17f691`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:48:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:36 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:36 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:36 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:36 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c503d8216e3d83c88f2e6fa55a973a50afa1ea035ad31e9d6a22606d88f7ea`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 291.2 KB (291216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24644c9c8d72b7eeaac69d4fd6498522e17774698cf1d50b5fd84284b60cf43`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d70b6fa1dcc39bb797867970d7cb11fd38e3f751295ef0ac6d0734c4a67734da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 KB (221781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220874011f81cf297f7b613c683416324a4b2ca97e6508b614a75473d8621e2f`

```dockerfile
```

-	Layers:
	-	`sha256:f8861c6afe071f40737ace997f100992e3624b89b6234365254b4bcde88bcfdd`  
		Last Modified: Tue, 02 Dec 2025 18:09:30 GMT  
		Size: 195.6 KB (195616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7c69c3adabea96d959dc896ad78080cd7b8b56b73fd8dc42c1e910c058566d`  
		Last Modified: Tue, 02 Dec 2025 18:09:32 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:162d2b7f956842f19c797c1e2d8ef63bdf331eb55f61b2e4cf8a82e0cb1db56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62083255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90383087b977e545de714b2b7f4fbbdbf1135856e5f47483623bfcb3f3538782`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:18 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:18 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:18 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1cfd108ccaf6f7d493ade1fc03b1d84d7ee4dfb9aa1572d2e2701af0cf91a1`  
		Last Modified: Tue, 02 Dec 2025 17:47:56 GMT  
		Size: 294.1 KB (294111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f7ff8173cdfbdd6ef409a95240bce9a61c2cd8cea2f9896f405a86dbf6a54c`  
		Last Modified: Tue, 02 Dec 2025 17:47:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f1e873d097b6904e4cfd929773c32de338893d07eb2fd6033441c2705fd9dea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 KB (221875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f6f7ff0b441f8f19e1bce1ca96caf3f3a2cee19e7c666be01bcc523f0221d5`

```dockerfile
```

-	Layers:
	-	`sha256:6352607ad64b855d3429ed0b6bb3a46a93eea5045a5ff45950bd95cad5f72303`  
		Last Modified: Tue, 02 Dec 2025 18:09:35 GMT  
		Size: 195.7 KB (195666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba30108032755d50a6a8c67912ee5bdb9d0764bfcd0f4326b8848b4c2664662`  
		Last Modified: Tue, 02 Dec 2025 18:09:36 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:470550f3af8ab6bf93a5cd5c0cc61c67084f3ad9f5e9357263fe9f217f4bc00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62782664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0221a81a484900f37b960de340b5cbf9d76565580effab65036399b8223a50b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:49:23 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:49:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:49:23 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:49:23 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:49:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:49:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d26f109d271775642bb52c5ca8e4127de7fe26da9efa068f074533d442cb797`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 291.6 KB (291636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa81b16a0bef06e2443d5428328742fb73b3e08aadd327bcf33564f3220a8cf`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:635636f3912939b19b4c98c52d90faf892ba6274351c72dac4c43ed2043bc9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d10d5c7020b21197edcc17cec23bf2daa3670d2873623fea4a6f0e65774b328`

```dockerfile
```

-	Layers:
	-	`sha256:fc10ee6b2559d500499d00da4fad9db9bd7108e443024b86921c054a722e3937`  
		Last Modified: Tue, 02 Dec 2025 18:09:39 GMT  
		Size: 195.5 KB (195503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc6f324a54cd5621e7802fdb3c7f2906544a7f686a18c19dfd99ac18e377f52`  
		Last Modified: Tue, 02 Dec 2025 18:09:40 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:4be0b66e0fc6f3149b64824922dd3bc35b8f0c845bf8026497d6be8324cc9983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62161937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da061ca29d1fc4102e9292c02328647057d7ca0c3fb8cd143379b9bd03b92fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:09 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe3074abc6346584ebb7d175a96261ddfaf687149e8a47e8c83b0d8c9e1691`  
		Last Modified: Tue, 02 Dec 2025 17:49:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4dff481e3c86e98c977c3c115d1da6bfb1dcb4274261e19b503ac13815d08814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bfd2f7d7141027dd80e38ca1989bffda2558489ab862e0f1bf10ccf11f736c`

```dockerfile
```

-	Layers:
	-	`sha256:c5a7f9cf5ae8df8239a0ab06c68c435e67ca9cfe0260182a02cb7001538cc971`  
		Last Modified: Tue, 02 Dec 2025 18:10:03 GMT  
		Size: 193.7 KB (193683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ec1ae99c25e732134da15c8ebf8fb9ece180ba98bb5410bd465e3393075f7d`  
		Last Modified: Tue, 02 Dec 2025 18:10:04 GMT  
		Size: 25.9 KB (25925 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:c4aa409006c5b85299a463c39b3e87a53ba69dda4e41e9c337eed979ef7d46ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62479364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6730f401d97c7cb241e66007640e5287aceda7b05ec6d9878ef443a07754eea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:55:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:55:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dece81b84dd08929374b6e8e9e38b7015785ac31adf38602fb02b1dbd442d0ce`  
		Last Modified: Tue, 02 Dec 2025 17:57:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d5fc590691ec32a3769e307af9bb31c0037594f9bf6084f25091b20ca320bda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 KB (219778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7880ae1625aa53baf54393e352efabf436e717831f17c1f8441ba1344cda5891`

```dockerfile
```

-	Layers:
	-	`sha256:b6cf13527ca00989a5d63e78ef3266a49f2b23a54f33cb3507c0c61d9ff4343f`  
		Last Modified: Tue, 02 Dec 2025 18:10:08 GMT  
		Size: 193.7 KB (193679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6be714a9e7134a8298eb33541e9b38ab1910dd8add1b2c5f056712f4642b033`  
		Last Modified: Tue, 02 Dec 2025 18:10:09 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:f4f13bf3977116e623a55e92501ca7bdec4cc1cb243519fbc37894b2e76f829c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63428770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e02973f916fa9dcbf329af4a38e0033af80a0a97890749250d7477acb35c49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:28 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94177cc1b10be488b5d187dad00f1ccc030bc5cd416e55c943d85498ded2fbfe`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 292.1 KB (292150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d419ba7d33a7aff89f4f162d7f80f73a4b62020a51e81530406474b71e63be`  
		Last Modified: Tue, 02 Dec 2025 17:49:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4fa589042cbe32ac54453900d034066e9380d78fda4825afb52c61269dc1ffa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 KB (219464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872cbb30e45e83b1b2b60527ee4f09d1f0b02b660ad09608fe1744f297338fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a68574a948ab8f603a17a59272758390f5cf7ac20157d1ea067516cb482bf90`  
		Last Modified: Tue, 02 Dec 2025 18:10:12 GMT  
		Size: 193.6 KB (193611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcb39426bccc4c8fe5b3e80390583fefc2f121054e0bcde58105742bdeca2ff`  
		Last Modified: Tue, 02 Dec 2025 18:10:13 GMT  
		Size: 25.9 KB (25853 bytes)  
		MIME: application/vnd.in-toto+json
