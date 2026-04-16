## `golang:1-alpine`

```console
$ docker pull golang@sha256:27f829349da645e287cb195a9921c106fc224eeebbdc33aeb0f4fca2382befa6
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:80fbb8f9b2fa541a7d34378f1ad10f4f1c433817c4ed39ddb3e2f3ec3e961271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a932cac16c0188b9a431afa69b0f64063cba293bb362177242913cadbb94bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:35:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:35:25 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:35:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:35:25 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:35:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:35:25 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:35:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:35:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3aca1499f06ff02939c8f744463049feecb3965f1319b86b5e91790a9631e6`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 290.2 KB (290242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f1b4898e9c2c22c54ff9d1bc2e2d45d59d4c2e53c60281dde84ef43df4c79`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:727cc7b15e20dec3d0314cbeadea4e505bbe10661ae58dfcc96294e873379a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57601b0cc8fec4db728fc8112bffccc405c515daf9ee5891ecc948fde3ba02dc`

```dockerfile
```

-	Layers:
	-	`sha256:3aadff5e5dbdd4fb3119daa0f64455d4662b4188fa085e7a4e320d5ae7690970`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 195.1 KB (195068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d8c1e7bb7fe688f0ddea241b98ed52bb907b8d4375cb10ebcaf79a1d152c472`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

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

### `golang:1-alpine` - unknown; unknown

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

### `golang:1-alpine` - linux; arm variant v7

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

### `golang:1-alpine` - unknown; unknown

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

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:cd092644fdf413d14a09baf952d5851dfe5d423983fe1bbbd19595f70fb939e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68601627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1ae4813de385c97632ceae841760d7f3a8a5cce14811ba5aab12332f35b6c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:35:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:35:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:35:40 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:35:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:35:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89244935705494e38d5fa051ae5221080d8446b496516d3888d3cb64c7a7d51f`  
		Last Modified: Wed, 15 Apr 2026 20:35:57 GMT  
		Size: 292.8 KB (292841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e813a1647e7ea7745c1c15436c1f86a82eadb5436933163091db860d16ed923d`  
		Last Modified: Wed, 15 Apr 2026 20:35:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a85433bfcc3fc910b19716abc87a734815b0b121a3484530b067cf8482f54aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e5275c27258d2b2d303fc2f49af3db86c82f344cd2c7badd75409d28d449c1`

```dockerfile
```

-	Layers:
	-	`sha256:e1de3e9a1d3d48696244574d706ff8f8d214501782f3287338f1d543cf04da68`  
		Last Modified: Wed, 15 Apr 2026 20:35:57 GMT  
		Size: 194.5 KB (194522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3968e82055b7357f491ed307a3007ac774ab9e5204c021e601f0d7f8c8bec0b7`  
		Last Modified: Wed, 15 Apr 2026 20:35:56 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:dcd42605f7f4432904156be77580f9c2ea1d48a6db4ce818b52f9db72cfcb3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69523019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7873477350068c62f253730752451d0a0947f235deff785312a0fce6ec9a8ed2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:27:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 22:27:14 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 22:27:14 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 22:27:14 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 22:27:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:27:14 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 22:27:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 22:27:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa77d2183379a6ee28394aa8bd3aa604f063629b4eb811e67b917ecc84acb6c6`  
		Last Modified: Wed, 15 Apr 2026 22:27:30 GMT  
		Size: 290.6 KB (290649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b29d109e367ac43f3e67c104c046d01b1c6cca80443b728b2d38a262b476`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 65.5 MB (65541767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c837ac97b92d85b3521aa4480a7d341a92d1f9dc216a780d4b991e9802e92c`  
		Last Modified: Wed, 15 Apr 2026 22:27:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e2743ce191c525ddb5f1613ed92ee1e286ffa3ae946095a7950402b796e4116a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 KB (220978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a850fabdfcb3f53a911d1b1c53c495122bc0190de1c2ac7708a9367182728a3`

```dockerfile
```

-	Layers:
	-	`sha256:ea2647b73cb5885fdc804884457fa5cc7cd8f06217a52c054d7736d2fd9d743b`  
		Last Modified: Wed, 15 Apr 2026 22:27:30 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574e1196fbc6d4dca83d4e6b1337d2eb60fc36859383978271d3762fc40a10f1`  
		Last Modified: Wed, 15 Apr 2026 22:27:30 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

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

### `golang:1-alpine` - unknown; unknown

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

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:cefa96c59339c74d73f51703a41a24cc3b520a736236bf7a6580df1b2883e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68975814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bb46fbe4d3e2609f55fc4ed147fb2108d70c9bb8ab52fa217b20363b1ee942`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:31:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:31:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18820a12075d850af6085d052799ca6c42481c33ddc318143f5caa48480e4d17`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4c346f825e10059298946e2fc2011feafc007183fa7b2c3f0269d07e78f1f8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 KB (222541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871bdf797d0720526445af2dec7fd4adcc741cc9941d795f8947b167307df50`

```dockerfile
```

-	Layers:
	-	`sha256:4de9839b9b099497236b198e6f2afcfca248cee87330100e021cf732d6d601cd`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 196.4 KB (196442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66388c961ddc07d76c8debaa85b64b168abbe9790e2387fe6042c4b012ff0e53`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

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

### `golang:1-alpine` - unknown; unknown

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
