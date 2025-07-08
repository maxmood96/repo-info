## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:c07f29dc2482a2784638d6f0edafa031d0187f3340f89da72177f0f3586c4d45
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
$ docker pull golang@sha256:84b7a03867e25b1d7fd5592f6de19426f0b92aea8e45c537932747c95c4615b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87023437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d38c482c9284cb29e3a8633ae33afd1c7dbcab6bc7fec8b4dc44e9a30c987c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f3141e0db3c814ff20e3d3c44350286b34cfb2da1b9ee65454cddfa5f64a4c`  
		Last Modified: Tue, 08 Jul 2025 21:17:44 GMT  
		Size: 294.9 KB (294905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9b1bf1df4ddb6cd2f3ba43fc263309f8c370fe86f15d3de62305a26c4885e3`  
		Last Modified: Mon, 07 Jul 2025 21:08:01 GMT  
		Size: 83.1 MB (83086126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a1d442cbc2515cda4a47020ab7f2396a087c2d1cf035ff4a8820cb6980e9c`  
		Last Modified: Tue, 08 Jul 2025 21:17:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1c3b6d9169e81c869d26849096e70f7ea1c63ee95f500a81fd8a8b523a12d94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 KB (219170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b926d70eec5f74a541ddc60acc417ecea2618a6f7d93d444bd0c265f4639e36d`

```dockerfile
```

-	Layers:
	-	`sha256:efcbec222e0c3f4206c70dfe459b3e75be90a96df08b796650a8d5b93fcb26ff`  
		Last Modified: Tue, 08 Jul 2025 20:30:20 GMT  
		Size: 194.7 KB (194662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ffb62ca77ca9506e8f053ffd1044e347ffa4261c85e89c5f3366f6e007614ee`  
		Last Modified: Tue, 08 Jul 2025 20:30:20 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:f6f8153e293d3bc062e8fd8759d5ccb512c597ddac5d0a2f0ff27cff98129d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84093646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f220300221ee0c473bc5653a9ad02bda3cf222158352590b3e591b50a37f287`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
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
	-	`sha256:100ca644ccef217b691cf701a2d3d00a0f16c7a7cbfa7f84fdba88c2b1a0747c`  
		Last Modified: Tue, 08 Jul 2025 01:56:56 GMT  
		Size: 80.4 MB (80432506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadea61c28715f13a43d021d5199aaae18e19f7b2e29bf094ce579461f585589`  
		Last Modified: Tue, 08 Jul 2025 02:01:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:24e0a72026dc30b6db4a8feaade0dd07aaa1b59e572ca80bddde9ea63bbf09b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59999cf2c3b9e290e2371fba6578ec4d27614751cbabfcbdd469ab6cd2ccd6b`

```dockerfile
```

-	Layers:
	-	`sha256:51519399e35d0425a9e592049b2104764512ac61ffa66904b2655d632f1c58f4`  
		Last Modified: Tue, 08 Jul 2025 20:30:23 GMT  
		Size: 24.4 KB (24400 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:eed6c5d7a55b5a1410688a071175b90db088f1af5dcbf7c2c1fa08a6e47936b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83574559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663a84ab05616b5b5934cd6f7f7175a47949a1b218ba5573610391ac03875476`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
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
	-	`sha256:d69fdb869efc0a02a2300329eae27592000268e157c8997d8c67d1e2518080e9`  
		Last Modified: Mon, 07 Jul 2025 22:02:14 GMT  
		Size: 80.2 MB (80181079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddddf6fe2f9b07df9c6ae8d795d02827139c119f2ec3eb1e994069a09be971`  
		Last Modified: Mon, 07 Jul 2025 22:18:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b4422bd4e4084185d5b7f86dd9973ba3653de6fb20e91e8115860cc14eab2d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154bc1cb462aa8afce33e77f4380c54b2bb1b75e721d8a62b166bdb74b5fc792`

```dockerfile
```

-	Layers:
	-	`sha256:15d697317ff5ea90722637b0d6c218a4fe587ba9da52b4f21dd59d7a62b02353`  
		Last Modified: Tue, 08 Jul 2025 20:30:27 GMT  
		Size: 194.7 KB (194668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2db31cf9daa47b5603422b3d51bc7d0860b9316abe1d1a33b2a4884dbfb0b37`  
		Last Modified: Tue, 08 Jul 2025 20:30:28 GMT  
		Size: 24.6 KB (24615 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:59acc94dce0186295ad37231980c2b93ab1ffdb3217dc656b8654fb4f0a2eef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83342252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1265cf6983cff47f713cf106365af9ab250a968dd06be05fd8e580cb6727a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b262260544cb39400e5dbb7647c5bec51158ea8b9b102d3b166fd952b3e386`  
		Last Modified: Tue, 08 Jul 2025 04:48:54 GMT  
		Size: 297.9 KB (297869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fe74c58f17b8638ab4c828f8d4b865821c43447e64c8cd4bfbde5a810c7b1`  
		Last Modified: Tue, 08 Jul 2025 05:43:08 GMT  
		Size: 79.1 MB (79051196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fa69b756f8485138a678c10a80dcc31210098ec27cdf2d3a518f32d3373c4c`  
		Last Modified: Tue, 08 Jul 2025 04:48:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:2e80795fffe0645f57a6256fb05670b226c89473a757546a5c165a02b9fd7e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdb4a9df3e9761481a4aa484eace4fa3aa134ccde1da437ab3f8f0fc99fd54`

```dockerfile
```

-	Layers:
	-	`sha256:0cf244730f794a3f093f73755e29e2b19778b739e435d75fded195829ab9d09c`  
		Last Modified: Tue, 08 Jul 2025 20:30:30 GMT  
		Size: 194.7 KB (194694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a692612483784d91ee58942af44b1919bc8a1f4d6c40e39bebba62cd4e5e07a1`  
		Last Modified: Tue, 08 Jul 2025 20:30:31 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:da964a21fcb35761ffe640c0696069f7f2394219067ef33e5098dc1df1201ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85579757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042e65a99064501a3416addfa34540abca8affdac0ed905510751c2c24191a19`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85ba82f1fa4e3e1c050af6a4622c2d983fc1d98aab3a6682fef2ac04071b9f`  
		Last Modified: Tue, 08 Jul 2025 18:11:44 GMT  
		Size: 295.6 KB (295597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fd65ade23887bad8cc24159556378a6549464832612b1c87e5e65754cc9685`  
		Last Modified: Mon, 07 Jul 2025 21:08:46 GMT  
		Size: 81.8 MB (81820379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44893312f83270467a0562d922c4988750af013ac2b65f2cf3a1c0e2e8eee75a`  
		Last Modified: Tue, 08 Jul 2025 18:11:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:542fb314ae8263573888fb6393eac9982181b5c5c629b1672cdf4f8709ac2cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 KB (219108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bcea0af588b570fe2794cfc3c299cf8ab13322a8b019194857a27f60147507`

```dockerfile
```

-	Layers:
	-	`sha256:41db5988fc0b3c9081da95ec924b482a3623e3b0f9d4c59185721d3062a4c3b4`  
		Last Modified: Tue, 08 Jul 2025 20:30:35 GMT  
		Size: 194.6 KB (194633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfbdde28942681baffe391898c691d55a12a8a60c7b4e88a150417ba1797e76d`  
		Last Modified: Tue, 08 Jul 2025 20:30:35 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:8ccf313711f21836de90e4ce3cc48ff52a86093a98ec8fa70e1f2aa3b2831ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84231883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef7678d1a57114a8328cd66d7ff018f1732519f0bfa951eee8260498ff59e0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c63a5fe94812205aea92afffb34bfadb77e3c0f3a3740a18e9d23511a8ba7c`  
		Last Modified: Mon, 07 Jul 2025 22:29:09 GMT  
		Size: 298.3 KB (298294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b55aa5c49337c93ecd39f723f408177c4f428404ab6858571184b51126cd1`  
		Last Modified: Tue, 08 Jul 2025 00:16:14 GMT  
		Size: 80.4 MB (80359086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034e0649256cb4208faab3fd412b04392640e85320834ac1aae6f3db1232901`  
		Last Modified: Mon, 07 Jul 2025 22:29:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:be1c7e03a09d39e806628ec98a31915605bfd231b49de9c1252c5b7c82825246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fe977c727cd2047d2903d14d1c1073e108cc984937e34dc3bac9d5c0f64189`

```dockerfile
```

-	Layers:
	-	`sha256:ec12d51d62afcfa75267d257b93b3c0649595e29a8484f4df9681bd84acbb423`  
		Last Modified: Tue, 08 Jul 2025 20:30:39 GMT  
		Size: 192.7 KB (192747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1215827541677b0d5222e6a7657821e6136d753bf17abbc16adedfa2f392da81`  
		Last Modified: Tue, 08 Jul 2025 20:30:40 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:5ad29dbe61ca8a1f4f1ece9430009c4e3bde4803b580f620a755b86eb35dbb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84201912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce40a51b9e1d12e4e3a85742e8422930e4e02e95d22209cd1c19a51d85b48657`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
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
	-	`sha256:950d2522679e808bf5b0d11b3e731c061e0d65a03b5eb65235ea8af4cb3df86f`  
		Last Modified: Mon, 07 Jul 2025 22:00:28 GMT  
		Size: 80.6 MB (80554969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4750c1bbe7733f027cc4aa1bb38aede5fae74a2db2a82927bb0245ab168e5c`  
		Last Modified: Mon, 07 Jul 2025 22:34:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d3e43aa9d66cabc83bebac0e2a3772dcb68bb7b11eba6ebecf5ab0a3198518bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebe6af9a922318ca13a7c7ba839858a6f2d246ad5b78bf4df90d2e8ae338972`

```dockerfile
```

-	Layers:
	-	`sha256:195e138d311438dcc1e5e438af2f76c50014487c2c4f720472cfb23b096ef651`  
		Last Modified: Tue, 08 Jul 2025 20:30:43 GMT  
		Size: 192.7 KB (192743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c540262605efbb498b0885145ab9e757174390a09614c87309a1bf2a76c84ea0`  
		Last Modified: Tue, 08 Jul 2025 20:30:43 GMT  
		Size: 24.6 KB (24552 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:928871a2ab0440aac0c584dba0e9587b776aaf448856dd9ca431941f048f549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e0f92266912ade908bbf875ca337761fc6f00885b91079292a13dc52ac34b8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a414ab9dfbde1973f254ba5fbf45d0f21227d9d3460aa7790f894fe7cc3001c`  
		Last Modified: Mon, 07 Jul 2025 21:34:42 GMT  
		Size: 296.2 KB (296193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff319e613d7718d33c97b2a4d68807464c2ed71607411d5eaa89b10ec085d5d5`  
		Last Modified: Mon, 07 Jul 2025 21:28:58 GMT  
		Size: 81.6 MB (81597964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce433a52336fe37a11275b83b911fdc8c37aebc3479ad1b4315603beafc054c`  
		Last Modified: Mon, 07 Jul 2025 21:34:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ec3a9a1cc59bdafedb9e87525bbbfb40765ba2386399a240290c411cf90f710a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa76cf358e08a743f31895c1a13e0d30dac8f33bc92c79c7e1a5c0220d212197`

```dockerfile
```

-	Layers:
	-	`sha256:efa48030fb11ab49e5273ab8fd9f67aa3de990722c45c187a5f8dab6a5087ba2`  
		Last Modified: Tue, 08 Jul 2025 20:30:47 GMT  
		Size: 192.7 KB (192711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea15a0e67bcf57b5bba989c56cf2b1fa32afdfaba9885ba8a24bafd9f5b0890`  
		Last Modified: Tue, 08 Jul 2025 20:30:48 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
