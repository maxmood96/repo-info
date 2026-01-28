## `golang:tip-alpine`

```console
$ docker pull golang@sha256:423a79cb31c3b5e65cf21d4919fc9310b0a0a631d9e045d63663cb18670c560f
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:38057ff609f66d21e9e5d4aed7497faaef9934a4408c3376d10ae42fcfd10742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97512592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666049f4424636f67887e3b9dcc54ad547fe6d455db03108b848c27b3508f55d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:50:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 04:52:34 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 04:52:34 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 04:52:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:52:34 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 04:52:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 04:52:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722ec003a261f2717edbc8d0a7c04578c36d9a18a209e010854bec9b0164e64f`  
		Last Modified: Wed, 28 Jan 2026 04:52:51 GMT  
		Size: 296.1 KB (296074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606b852e3c333533b6267cbada59c6fbc954cef2b3af5c4c84f2f9bd6ca56999`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 93.4 MB (93354538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759c73561b1e4c4086c54d63c1b4a864fe115a54fdadd6c976988222c343f614`  
		Last Modified: Wed, 28 Jan 2026 04:52:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b127b524070bc5e8da1e1fc691458b955353aca28205172f8eee7a7a4cc6ca64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccd6f15e074666aa8b09e26ae99044db23bb980adf0ec9808502b7aa8771c61`

```dockerfile
```

-	Layers:
	-	`sha256:19ae1be8a12f4fd745c4289567d258b82668a5714adb8438160c18d41a023806`  
		Last Modified: Wed, 28 Jan 2026 04:52:51 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7bd7b495f40a4dcbaeac2d0d87a947e7ecf293767fc87bad07b1e3eea37e63c`  
		Last Modified: Wed, 28 Jan 2026 04:52:51 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:6e86e23ebc44f6e0233a1cf49a17fcc8256182047b836c3906585ed9642ec171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93666271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c923edf6834d3cd5791f2deebc780e9388d797f72fcd7efa2af45c18e67712`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:57:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 04:00:34 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 04:00:34 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 04:00:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:00:34 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 04:00:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 04:00:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bbf175bfc50a923793e1e60c0a330e36a7925ee3865790f02949d3aafec2a9`  
		Last Modified: Wed, 28 Jan 2026 04:00:49 GMT  
		Size: 297.2 KB (297247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4ad1d715926b64a8f9ca2f7e3d6d0a5b04fcb12082a02013bdd6dc9c89d61c`  
		Last Modified: Mon, 26 Jan 2026 21:56:24 GMT  
		Size: 89.8 MB (89799045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ba01073858dbd1cf88cb98a42cee72e521b000c866069c1aaa7a41e06b979`  
		Last Modified: Wed, 28 Jan 2026 04:00:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f4dad9d6bae57a4a2beca249a26f24522fa0b5e0bf0a4b059d4a88ae2d2da1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9472170cb442aa039e4783a5004e807c04811b3558143d6cf79ad9c6b3e3c6`

```dockerfile
```

-	Layers:
	-	`sha256:d9c358729aff22f59539bb20389895e74a28355895f55a1ca7618de40a7fced6`  
		Last Modified: Wed, 28 Jan 2026 04:00:48 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:f62f0ee10f552684cf41909170a4b0f8decf5bc65ca92beeb997fdd04cc251fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93104829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffe01b1ce75a3b99c05aba864c424452e63d11d45cb8b8d42e5d9ff223cf408`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:02:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 04:04:45 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 04:04:45 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 04:04:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:04:45 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 04:04:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 04:04:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afd00d8e64374591da7b233b871153a2940bbae48f45707aa1314040689a114`  
		Last Modified: Wed, 28 Jan 2026 04:05:03 GMT  
		Size: 296.2 KB (296186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205fc7a73de56b4f5ea25cad036ec0f33fb7b33229a77437a24f71a2e0db125`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 89.5 MB (89526761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e58a618a4853419261d92c8ed23e5e226b229cd08a8313b02a28cd5905541f9`  
		Last Modified: Wed, 28 Jan 2026 04:05:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7dcdfed554787e2ee30e1b73fde1d6092c3aecb5d6637fc5385e8f1d638a0e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a3c9adeb2af9cac219f7361b3ed2c54d4586265a78ce107d42c4e3ebb91217`

```dockerfile
```

-	Layers:
	-	`sha256:2737f373da022c22f48dfcd42350838c1bcd0e024ac76fd537771ff2934b86a3`  
		Last Modified: Wed, 28 Jan 2026 04:05:03 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:777d80c03a46d9ae3f17d14304d84e16f02fafd2953de692144ea05c3f3da8b3`  
		Last Modified: Wed, 28 Jan 2026 04:05:03 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:028bd53a7732b25488db855ed94441030f90af69c9f23815b4e16edf95300e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92913345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd3729b9f35f09c09f39ca5026fbb91263ee9348d62e5fe893d816b71c68c9c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:32:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 04:34:08 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 04:34:08 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 04:34:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:34:08 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 04:34:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 04:34:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5276b7dd25c8812d0206113d994b597970f8f266260049bb5af2000543a8e407`  
		Last Modified: Wed, 28 Jan 2026 04:34:25 GMT  
		Size: 298.8 KB (298839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3fde52f4a9ce3ba79f004ba1b1e261e66970dc6baaa4a0f9b9bee7c6d5ab5`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 88.4 MB (88417257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a599cb4656a4d62c62a13d54c6873d7ca336150cacfd3cba7e6657b6be192e`  
		Last Modified: Wed, 28 Jan 2026 04:34:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:17f10a5a1e8d12bb8d13bf1131f599079d3e878f33259cd9f06c20cb1ff09161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b3c1cbb94b3fc24ec5534f5083e3d12e295b3557b54b1c5f93920f625e9cf`

```dockerfile
```

-	Layers:
	-	`sha256:c172db2750674253482dd971386aec953d71dc43b4ac9c143f3b7c74b29d97a4`  
		Last Modified: Wed, 28 Jan 2026 04:34:26 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd893b772e6da7e6c1c05b048fc5dbddf7b4cede56e2fa4c2e809b104a6e2c4`  
		Last Modified: Wed, 28 Jan 2026 04:34:25 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:efa241750f7ead4ae73b23cefe7ee36d92875a96a2442231045a16bdb68cf20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95421552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18995a65a1ee198e8845d4e5c071f0179c194be103147a2dc60b1fb4e4951841`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:47:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:58 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 03:49:58 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 03:49:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:49:58 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 03:50:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 03:50:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e4ac087a5005e02aac734a6b8c807703351195bb519875eb314797814891a4`  
		Last Modified: Wed, 28 Jan 2026 03:50:14 GMT  
		Size: 296.7 KB (296671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb24967b184a59692854afa79a294d0d5b0fa84b707a952b78449312c20956e`  
		Last Modified: Mon, 26 Jan 2026 22:04:59 GMT  
		Size: 91.4 MB (91437726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b320ae12e6179f2ac000a0a377872eae3648028a05cbc632ab787136b71c4d`  
		Last Modified: Wed, 28 Jan 2026 03:50:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d7445f88108bac6b7e3eebf7feaef67b6319b937c66fd23bff8feadd591763a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5a04d3f45b881858d550ea79be5a68d00f8ccb25a257a407146ef59fd47b24`

```dockerfile
```

-	Layers:
	-	`sha256:9e0937c708886d7ff3865c306a2eff31d285adcd01c8992d8b0cb4e18ed45f60`  
		Last Modified: Wed, 28 Jan 2026 03:50:14 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e65d3719a13f5170727c1a69eda16e476701a4876226ec079538da1fa8fc28a`  
		Last Modified: Wed, 28 Jan 2026 03:50:14 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:f61616e1d026e41d278d904ab08d90cdd5ffdef08b810cd481f16712ff2d7757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94179986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217a7f0fe49c07b5bb09606857c8091785f620085a5be57aabee735aef77b10b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:34:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:34:17 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 06:26:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 06:26:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd73d3916f2fedeed1c534628f9a66641a5e1350de62984f598c99fe3383aaf`  
		Last Modified: Wed, 28 Jan 2026 04:06:04 GMT  
		Size: 299.3 KB (299261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3fbdd047cc229947289d64050103b3f46ea0891f972e8e261f84917802eea`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 90.1 MB (90050925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0923d43ebb546de3f69b0e128d86f4ca1922573989afab77e98d984cf1ea1e7d`  
		Last Modified: Wed, 28 Jan 2026 06:26:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:765230e64a8d3d70a835722048b20928d1f032a98c1855faeb7973d7f638ad39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05d67faf06038bcdcd5a554c749adf2fc6f28c1218527c8d4804189c7e3bf1f`

```dockerfile
```

-	Layers:
	-	`sha256:7de0c0530248375de140b7354530603c7c6bca9c91a8f2b166366867fa0a3e26`  
		Last Modified: Wed, 28 Jan 2026 06:26:42 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911820d04eabee71f745d647e0a98d7ce5f43426780746da4b201a2b0007ab29`  
		Last Modified: Wed, 28 Jan 2026 06:26:42 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:e68648fac0d55ffb6b05634129822c46efe82034359cc0937c17970f3fd21707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94465415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba08815c2511f3674581c7de3d23ada67e038a3f6fbdcaf2648b3f4c1e1dbcd2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOPATH=/go
# Tue, 27 Jan 2026 04:27:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 04:27:07 GMT
COPY /target/ / # buildkit
# Tue, 27 Jan 2026 05:14:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Jan 2026 05:14:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:16 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336390632e3dab506cd0230c48180b8fdc0e8dcf2f397506712faf9caae798e8`  
		Last Modified: Tue, 27 Jan 2026 04:34:16 GMT  
		Size: 90.6 MB (90584800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a694671488bf2e9877e89d5b9da398a6699e157dda62cb71fe91c2720c5a5f39`  
		Last Modified: Tue, 27 Jan 2026 05:15:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a1fd609a9d8895cf5a8ce1528630bbf716e7340aa926163ca8db79ca44ac27d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e196b23dd0b32362bdd63901c3ec3216165463dc9336f3db632ad1b6a98c1b11`

```dockerfile
```

-	Layers:
	-	`sha256:1298ca67bca9f04eabd6e371058bc60510f0a30fbd130a6e3d895b21f5b086e9`  
		Last Modified: Tue, 27 Jan 2026 05:15:31 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67cec1b779f8d2c605b6e4e2cdd20acf2987a46e3c20da6dc0e9d87efa985ed2`  
		Last Modified: Tue, 27 Jan 2026 05:15:31 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:99fa74e4a1a426dc6d45bd31af617716659415cac306321c0c16db800e4b3cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96630684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e6e79b8cc5cdc3f4a9789c8443a43ba38adda2a85afa6767ea4f2f2f94508`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:09:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:12:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:12:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:12:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:17 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 07:12:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 07:12:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c254d4672aaab6950c71304b17b783faa6225bc21fb2e6a3d7c56fb735ffa71`  
		Last Modified: Wed, 28 Jan 2026 03:10:21 GMT  
		Size: 297.2 KB (297174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d1ebc1a42fde765fe01b70de439084ec52a344bfa25acb00b6d281dc10102e`  
		Last Modified: Mon, 26 Jan 2026 22:12:55 GMT  
		Size: 92.6 MB (92608018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8cf6bef0f813423e8d8cea26396659c53d94c72e25a0e8a9416a8c9832892`  
		Last Modified: Wed, 28 Jan 2026 07:12:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2c7236d464cbbb237bc17a82b29c34d4440f7d52470381a6271b55bf8daeeb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450d47fc34c6313d34fb30ad6c814f6552ea8ca22627fbb43d1bb63bd176e89f`

```dockerfile
```

-	Layers:
	-	`sha256:71fdcb8f65d167d9283c676492a5b1eccf2323173f5f7d76d4d91cbb86f72a2e`  
		Last Modified: Wed, 28 Jan 2026 07:12:39 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:003fa3d7220e9957d745d1b7306ef250655bc92dc43e3f03b937eb61d2f56151`  
		Last Modified: Wed, 28 Jan 2026 07:12:39 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
