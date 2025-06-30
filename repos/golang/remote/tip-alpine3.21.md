## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:21820ed3fc6c2b61ceb46e1100848dff1a7b1de559f68c5c6be7165402a7a33c
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
$ docker pull golang@sha256:a8d277f7de72a1df5c1a052f3a54d67ca5b947190f3fa28961b4f40c7c5e2668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87022368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7268a642bbb713f474ca5f222d64d37abcfceb9c4b851ab9c9c240f29c7bd5d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360404e0f8e7ecc3f0ee26d089e605fdb20238ad10abd42427be7b0d6641f5cb`  
		Last Modified: Mon, 30 Jun 2025 17:30:28 GMT  
		Size: 294.9 KB (294908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8f8c49f445d30fa7cd4c028a18d5365e5bdfe97436ef61eb7709425c99cad`  
		Last Modified: Mon, 30 Jun 2025 17:30:36 GMT  
		Size: 83.1 MB (83085055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4994e97d2b7529955330c2646cf1e2160e10b0fa15bf82521760db3bfadb5d`  
		Last Modified: Mon, 30 Jun 2025 17:30:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:186b0cb209c05f8c4fd313d17afb1f1fadff4a338cee24899431fc87b61a1817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 KB (219168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acaefe91d7133296839520a5c3c6f3c6729ac90185865a9a8beabd6b670e8ba`

```dockerfile
```

-	Layers:
	-	`sha256:7a753db52d721c923affe602c9460210ed73011e5acd553ca765ed2bef3b654d`  
		Last Modified: Mon, 30 Jun 2025 20:24:48 GMT  
		Size: 194.7 KB (194662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedc0e4820ba0799c79214adf67e819c5d28e277a54b0a4de6dbc551c9ef6903`  
		Last Modified: Mon, 30 Jun 2025 20:24:48 GMT  
		Size: 24.5 KB (24506 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:3b29c96fec150c7c7201f374a269d443fc39ce17802b90dd23ab77eeecd3c1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84067840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ed5e56f7d2453b2cc884e3546fc38a3b6a52ac67dd146f13be09165f088b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a033f7a855efa81f3c3e4821d12fee8d5403f75f7ae4938295059761c5792682`  
		Last Modified: Mon, 30 Jun 2025 17:35:02 GMT  
		Size: 80.4 MB (80406700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3859c2612acdec00a15bf0245a29fa2d72b9df693ad786df99db50a3236a5`  
		Last Modified: Mon, 30 Jun 2025 17:38:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a275bab86dd6829fea7914c8e8e0920d9703d7a130b2472469345deae3cf73ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cfd83f0ad3a14b9a072aff387abca371b8154525baf736056f03c33b4a66ce`

```dockerfile
```

-	Layers:
	-	`sha256:951cc29e2626b1472c1f309e00d4776073600b667f595c5204ebf5b309c3c08a`  
		Last Modified: Mon, 30 Jun 2025 20:24:52 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:ee6920ae585ecd18f7b4b68ed3a2a14a2fde75c99c8d5608a84e7510ab7c2224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83556849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bba891e63fc85df8283e16c63a3c9aa13013dfa17f81e8d59258be294979efb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6586f6a3b72edca5355ba2231baded357cf799f55b8944edc8ae75b0c7b67acf`  
		Last Modified: Mon, 30 Jun 2025 17:31:46 GMT  
		Size: 80.2 MB (80163369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee95f2653346ea067c93ec1d03cf0e3e4215b6221b04d36bdc81162f2e1bf700`  
		Last Modified: Mon, 30 Jun 2025 17:43:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b10344149303a5fc3ef5b5142132d8ec7babf4f1e99d40cabd51d629a0ce0e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa94c5131f0ad74315b9fb3462d49b150410eca8284c0ff140eb45f349b90aa`

```dockerfile
```

-	Layers:
	-	`sha256:0cb6977870c0c9b9fd29d53444e748915d9e954ab7802702efd1ac5dfd0f23ea`  
		Last Modified: Mon, 30 Jun 2025 20:24:55 GMT  
		Size: 194.7 KB (194668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a91611b1f2e78de8405c616625c959c6cddcfea6da39c35158a0a5d23f1974`  
		Last Modified: Mon, 30 Jun 2025 20:24:56 GMT  
		Size: 24.6 KB (24616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3f2da3250eb61f796dc837127b0100fe9cd180e7dede32a6afee1a90b85a8ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83348831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a085bc95bbf61df61e2c72b8e221e46e52787dae0670fbe86931bcc3e4263`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2f34450ab6893f9de21e818c13da20ab31676614598eac0352797a074049df`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 297.9 KB (297874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f0e5c856fb20135c901f955406b40129ab946b3615cd5e0d5839e969930423`  
		Last Modified: Mon, 30 Jun 2025 17:34:31 GMT  
		Size: 79.1 MB (79057770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7a69f99dfe16fa7141505539b267aa82af8325cb211b8de09e4dba6ed3f61`  
		Last Modified: Mon, 30 Jun 2025 17:40:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a3ee2c22a3916d677639a8c8510fcb919b721d7574c5865178d7dbed50b7b0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c8d7991dbd1400bed8062356f3afc1ba5b537f6ab6066d319dd5224b63fe9d`

```dockerfile
```

-	Layers:
	-	`sha256:521629ea4225a599c51388b7136f3cc2a6f2c48c500c103a28e03c004aa7834f`  
		Last Modified: Mon, 30 Jun 2025 20:24:59 GMT  
		Size: 194.7 KB (194694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19473dba66c46e6f5e7c03e096ba1f4aa11089b9a47ea4271b25d8464ee92c74`  
		Last Modified: Mon, 30 Jun 2025 20:25:00 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:ce871c238917ae1100328de92920bc4d00c61e63955ff4c215a56668b84baefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85569531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61e81e9c3c4a6c919a7a87b0613030ec84231cccbb4ed2615e1a50566560731`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f144ef8fabcec01aae45b617b6a44ccc07d1cb4d3fa760283cadd349bd7b358`  
		Last Modified: Mon, 30 Jun 2025 17:31:08 GMT  
		Size: 295.6 KB (295608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2781a7c01ceed520d1e8478386c7e0683cbeab9ca6a32207c24229a367897`  
		Last Modified: Mon, 30 Jun 2025 17:31:11 GMT  
		Size: 81.8 MB (81810142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d78178103459a0b9e28049e6b2986f5e2764e474168d99930410d585b7444c`  
		Last Modified: Mon, 30 Jun 2025 17:31:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c110bffee6bf6187c85318347be39a9fd9444dc37712659affd7d9bc4dd357aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 KB (219106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cbe4d4defbd33095c3a9dc0be9831386062a1d15c13c7c64364dcb97487394`

```dockerfile
```

-	Layers:
	-	`sha256:6abe587ce61fc3d9d66055ce4a5c640688b2ec8da3390a857692655d9c39cc2d`  
		Last Modified: Mon, 30 Jun 2025 20:25:04 GMT  
		Size: 194.6 KB (194633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf2ef74acbf15fe683abd5f472d47d3ab776db7edc349d157c7011a57e40762a`  
		Last Modified: Mon, 30 Jun 2025 20:25:04 GMT  
		Size: 24.5 KB (24473 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:e49735065ad030efa4ea7191bf56e270bbe9160cea115530473e4cf0d0c9cb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84223831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540be1ce8dc9829c69376a084b6eb78b090d036a145c5b5b4581443e891985b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07c13e49694099e3952065321ca0fc45938d3a118b16ce109a83e147045f6`  
		Last Modified: Thu, 08 May 2025 18:21:43 GMT  
		Size: 298.3 KB (298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90415633da1367f6a55f0b20986162d53698245a02ffb8afb2ac26988cca44e`  
		Last Modified: Mon, 30 Jun 2025 17:31:50 GMT  
		Size: 80.4 MB (80351038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47ffee21f4aa08263b916f2c9348b5191e5b5efa870a70811fcd0d06f6def91`  
		Last Modified: Mon, 30 Jun 2025 17:38:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4840824754f596795ea00aa8955db99d8d92781e0b13b6844d51a1c010791d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daba0deef76ac7a559366e1e0b119d2eec3eaac57b255bf109bafdb55b27f9a`

```dockerfile
```

-	Layers:
	-	`sha256:38c689ab1af0f85502c581aaa5a82749c068ea5e387fc7fb1b45044568e61bd3`  
		Last Modified: Mon, 30 Jun 2025 20:25:08 GMT  
		Size: 192.7 KB (192747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc07bb4a4ff59fc88c0d5cfcd5d08a680e86f58ed67f4e924a33165c43a58d2a`  
		Last Modified: Mon, 30 Jun 2025 20:25:09 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:061c579f3cdd6a2a6cef19a7c3d806ddf23ee31ea013e82d8c7df74ed847a688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84194593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81bfdb092252c8d75cc9aa381e27f710eb06d00a9fed6cc760189383255328f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7713f67b0d70bfaa134a3e1854dcff25f4a9e8874d07fc34ea756eb284febc`  
		Last Modified: Mon, 30 Jun 2025 18:10:31 GMT  
		Size: 80.5 MB (80547650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a93068dcddd48b3c07ecd4463a12303aa9c126c8604a43055421d208eee5c2`  
		Last Modified: Mon, 30 Jun 2025 18:44:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:7cb229780502b2ae7ebc621ce94e98722b8edc348eb71c6a96acf4fb1836f99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52260cdc69a1075e4506f25bfde1bd1daef3861b24b75e0c27626b667bb4e962`

```dockerfile
```

-	Layers:
	-	`sha256:967d7b953f800dbd005107fea673d6c6bc2816a40167a98869453812e6998ad7`  
		Last Modified: Mon, 30 Jun 2025 20:25:12 GMT  
		Size: 192.7 KB (192743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eeb0248afa3bcdf49923d26618c9b8ada1db85976e26b93a8e3b19e01ecda8f`  
		Last Modified: Mon, 30 Jun 2025 20:25:13 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:745984cf77317fff48c3adddb23e9b0efe17ab3b6a11fdb63bedf97c80c6a2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85359354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc133be14d212b1c9abcb0afbd98f04fae28cf38faea2fbface12beb8479a89a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd99af01c56b56dd8b4b638222a30d969ae806a266626016d5a030517f57428`  
		Last Modified: Thu, 08 May 2025 18:21:45 GMT  
		Size: 296.2 KB (296192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1d310562389511c34710f540a5f40a96841fcdf844e9a2742b152e861d58d`  
		Last Modified: Mon, 30 Jun 2025 17:32:00 GMT  
		Size: 81.6 MB (81595438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3859c2612acdec00a15bf0245a29fa2d72b9df693ad786df99db50a3236a5`  
		Last Modified: Mon, 30 Jun 2025 17:38:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:7c80769dfe48a1cf378dfcacd8e00bfee3fe1fdb8a44629d757adaad1d66fbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbe28026991713931028c2e165341c4e9180b9327858a9392d11a0b62ec7b19`

```dockerfile
```

-	Layers:
	-	`sha256:fed36afb40c52635f27f0cec1f32d94158265474f89bb6bd3a56718ee93d5460`  
		Last Modified: Mon, 30 Jun 2025 20:25:16 GMT  
		Size: 192.7 KB (192711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32364524b64ee64e0f8e56625294d6b08289ec253c789721050f1cab1b317263`  
		Last Modified: Mon, 30 Jun 2025 20:25:17 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json
