## `golang:1-alpine3.23`

```console
$ docker pull golang@sha256:e58f92c51f4cc98f2ef4780ba8708fe914f20e6175720a19c1c85ff029a6b9fc
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

### `golang:1-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:f44b851aa23dfa219d18db6eab743203245429d355cb619cf96a2ffe2a84ba7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71439667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fbd9862b05789bb9e5462bf7d67300660e2ab5217aeb637b8db103ac45ea21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:36:58 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:36:58 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:36:58 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:36:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:36:58 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:37:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:37:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17423c887b377ec28c3923bc88337384a7a0c1f2b50b7faf4912760e8d503ebb`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 290.2 KB (290240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1512b43389a873b0519ae3d6c1a3c4d9b19295b8e3330b040d95d73c50ba2f9e`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f5fed3f8c50eb5aaf519c395c9b5eab00ac256522c55c1b338d65090147bc29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f218850ada7e7b643deda2d7aa2b46c6068ceb3ebb5acc28461a33f6c74c9d0d`

```dockerfile
```

-	Layers:
	-	`sha256:d0e37aca80016b1fdb4a73ff3fe88b6915ce5ef62de54ec8ced955c8c0287f42`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 195.1 KB (195068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcb22212809db82a5a09e485c1f61910ccb71af283340c0b4fd9664772668fc`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:0b9edb016c701fa174940fdf1dea18c8f0b32a00a9740c44f4d5af673efe993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69614065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1ad22b1f13b9e2b0dbe841db7d91bb7e7263580ebaf55a1feeb13acf65de55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:30:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:31:41 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:31:41 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:31:41 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:31:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:31:41 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:31:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:31:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c5793b7330baba2bdbdcfc15c9c30a01c808c080ac6caa02bf3b5585d2f0b`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 291.0 KB (291020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e327e2b14e32d059b1daa22f82c1fb7fa98060bc20d47dd6686da42229cba8b`  
		Last Modified: Tue, 07 Apr 2026 21:13:32 GMT  
		Size: 65.8 MB (65751024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff205b28ed383fd21ca44ed521626fb5d29207a307ecbcd118b32b80d9f4d7`  
		Last Modified: Wed, 15 Apr 2026 20:31:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:23aab7aec3d2a59b13c2712fbe39a0a077028219d9f1ad2ee3a6b598c2ec9641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d83ce3278127c1a28e8718fa8d6db86d3edf3992e8980967cc2db9d8a2eea78`

```dockerfile
```

-	Layers:
	-	`sha256:9b263a4b01262d528f836786801edea8142e8211a32ee12b9adf9fa3d1fe146b`  
		Last Modified: Wed, 15 Apr 2026 20:31:55 GMT  
		Size: 25.9 KB (25949 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:f608e2958f9aa09707c67854326298779d74a82c901427c3f7ef25f9662592e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084afa7b2c856ee1d8bfec679239809adc93b304ee1ba361219ccb843f285d29`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:38:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:38:57 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:38:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:38:57 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:38:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:38:57 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:39:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:39:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3ba670b4c9b2ddf01d859a649370597580dda4e52512417fb0791b9dee3e0`  
		Last Modified: Wed, 15 Apr 2026 20:39:14 GMT  
		Size: 290.2 KB (290155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4507fefe92406dc44db071c79b3b8d25445798810ce36b9e7f4459278f0b10`  
		Last Modified: Wed, 15 Apr 2026 20:39:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:db8319fdfe8bb62daca1187e9ea3a8152aeee5df1950b31d2bdc8460b70ce701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109df0bad6ff38ebd1585616888c5171f67191d4d761f73b351653d572fdec6`

```dockerfile
```

-	Layers:
	-	`sha256:cce5ee787c07bd8cdf39c1e7907f48559cbf05d6035fda0d8745dd534a82aff3`  
		Last Modified: Wed, 15 Apr 2026 20:39:14 GMT  
		Size: 194.5 KB (194470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8983151f5f689172c7ac443279c7fe40ca8f07ae8f265013aac2effd76550b8`  
		Last Modified: Wed, 15 Apr 2026 20:39:14 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:91dea08171115da4e00f7a5c74753c4e56f4e83e20b1e4065530b5d51d93742c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68660668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85526332edf09ad0a0c7acd875548d5b04a98e08ae64272efa724b244eb1c91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:42:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:42:16 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:42:16 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:42:16 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:42:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:42:16 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:43:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:43:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef948c355a7dc83c698cdbb853ce74cbea62b03bcdffec75a5ddd8453edb8fcc`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 292.9 KB (292856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e696fa36d88793f0869c86c611ba1d605ad3a2a7f60d00018579c8c2c9f935`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:a305b1da5eca73ac7d25e3dc8ea1734aa9a5533d165074bb0f449d62bd6984ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a41458ebb8c0d4e4db4126a9562316825236120eb86a232aba00bfd2cb203a6`

```dockerfile
```

-	Layers:
	-	`sha256:8f9b522dd6982502968f41aa37e38e8a3c8f7361e8c29f4e4b01f9297a199eeb`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 194.5 KB (194522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270caa600e6a9cde106c930b3d2a0a74333878a31f41dd3c19b66a6fb948cfc2`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:3a8f055e02fce9585d5e4ab5135d57f2e1a947a16e2a7e6a71a78e770c169e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69580386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff423aff05c212943d624a9fa8e6c44e45d506e06681eb8b3c52350e3baff1af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:37:59 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:37:59 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:37:59 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:37:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:37:59 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:38:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:38:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff356be0868643267e7ef13fa541a4ed3de24ebd1cefe71fd5fd4a40c12ef7`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 290.6 KB (290635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40fc8fcc10ee56c441c06327bcf95af166f71835205a4f4eff05758add1ec7`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 65.6 MB (65599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c134aaa6e81871cffc95032d2d94333ad68a39d4fb0570a177ed316490359c`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:388d5e136b25c992bc0ca2055a5a08b842fcdf22274fbeae5c65f34c44ad2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 KB (220978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7599c93ffa074c9fec66bb05ef7f72301b0745dd1ff9cbcedf68d4569f2674e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f2bb6e02ba8b65c9ca9d4c42153b747425053d1e4a9a437745a13088fa477be`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93de6a79e3a2990178addd1d86823a9cea257b2920f66486d3d83f23c451d7ba`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:a12dc8d3578346a24ef4bbe32dcbab3020bdfed9936b3db7e6e50eba6b224224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68882218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65568ed4286f49a7de9a801ffbd58a5a2bb68275613f83159bb082d74a59baf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:35:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:35:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0372cf4e623b54be68928792e5509486cabcf90908b531b460901e913b42b93`  
		Last Modified: Wed, 15 Apr 2026 21:35:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:1779e690095b09d21c655cd7a00d24b6c90685c6ea0bc6666a8fec14bfc6fdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75abb21aac5f6c5fb153eec9596463521410802b3a9b60210cb988b291b49ef`

```dockerfile
```

-	Layers:
	-	`sha256:ea51308687bbde9b6af157bff72b5bbc786db534ce199dfe0b1e217fa5a21697`  
		Last Modified: Wed, 15 Apr 2026 21:35:57 GMT  
		Size: 194.5 KB (194491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e568d3575c169a8ab16c182575242ee96db100fa3b94fbf1110b03ee7084e3d`  
		Last Modified: Wed, 15 Apr 2026 21:35:57 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:769bca04547432780c298e97e81d9b1ec7ea2c6e1e4cb0dc698e7666dc442177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68972227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d858cc547bf4d5ec68de0f9c55acbfdd2e9161b23493d6fb4be0d632deaba103`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOLANG_VERSION=1.26.2
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOTOOLCHAIN=local
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOPATH=/go
# Sun, 12 Apr 2026 09:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 09:58:49 GMT
COPY /target/ / # buildkit
# Thu, 16 Apr 2026 17:35:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Apr 2026 17:35:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fd72d900ad96a04e0615b341b3fedc269f4018f44079153195094e01751c01`  
		Last Modified: Thu, 16 Apr 2026 17:36:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:e7b88ee227c3190eb5c37765003f2dbd1d00659745898ece3948ab03ab0703dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4e9c5c66119fa4cead26535ffc4e4f079f320e7be3d096d72fc0b36e16b01e`

```dockerfile
```

-	Layers:
	-	`sha256:6cf1079ab59b22867b4438c628a1419be9122be84e96a205b28fc6db37ab2d5f`  
		Last Modified: Thu, 16 Apr 2026 17:36:46 GMT  
		Size: 194.5 KB (194487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284328c8d8808a15ba6d8092a15954ab5e5c226bf6802922c1623897ed32a881`  
		Last Modified: Thu, 16 Apr 2026 17:36:46 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:19a35024fb771d52a0343daecea0709dcd1831173db9049b3230d5ed7c20a2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70450020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b9068f1611ebd9380b16a2603c16c202a0a5df5116cbd1642a6df9607f46db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:49:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:49:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107efaa291b5f83372c13d97ab11aebdd260da2222cd795a4f56930ce905e525`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c34c0e0f61bfdc98564c02bc5b7b38c097bc93c1cc028e7ac08cced89a320`  
		Last Modified: Wed, 15 Apr 2026 20:49:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:2ca2d7041f45af49a29e98e14c32e642728b3fc98b68a4e7088be64e7b62703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 KB (220444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f028d190f6a03836687160b2270e7d87a7ac94cfac28fe59e015b12789f0a8d7`

```dockerfile
```

-	Layers:
	-	`sha256:79f6033a565d0cadbd0c05a12a3d2ccce2f100d6a7f17bd61b5b0538ff8ebed7`  
		Last Modified: Wed, 15 Apr 2026 20:49:40 GMT  
		Size: 194.4 KB (194417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81aee7997b047f0dcffe841bb17d6d2e8b16718ad38a8e5630c2afd63fc27107`  
		Last Modified: Wed, 15 Apr 2026 20:49:40 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json
