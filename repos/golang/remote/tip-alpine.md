## `golang:tip-alpine`

```console
$ docker pull golang@sha256:38937de1806ef220db08129ab4e5dc1ba1a89830dea0b126f96f44d1fa01bcca
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
$ docker pull golang@sha256:8326438bc7f49fad62058f966c9d98e6a14f034f64f9f38abecfd013dd7e1261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106034007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c639115e8ddb4c21d2ed2453b8c076d5392a9cbed2d7ced28f51d85520c181`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:20:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:22:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:22:24 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:22:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:22:24 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:22:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:22:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a6adf6de2e67c9ab33e159180487ae9b3244802c863e586396c6582696d9bf`  
		Last Modified: Wed, 27 May 2026 00:22:42 GMT  
		Size: 290.2 KB (290242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da848857ba8d560346623b29060265d568e3fd544a353c4d3226bc71f30e13`  
		Last Modified: Wed, 27 May 2026 00:22:37 GMT  
		Size: 101.9 MB (101879418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e641485bc7b0da72564449ad95f958bbda21eda1c49d84671922a52bec3d76d`  
		Last Modified: Wed, 27 May 2026 00:22:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fc7cfbf4f9cc4880d5d56ad2053b19b359fd524b2f9c2b0c03a4ed62fb53fea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba231ee62053425124e1200ea06e83d706d6ac40d40034e030b6ce6b23a65bb8`

```dockerfile
```

-	Layers:
	-	`sha256:e80dee59f912ca4302d069bc7633b2c09b0f1348ae50f25935bb165892bc286c`  
		Last Modified: Wed, 27 May 2026 00:22:42 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a615eeb3d4151c5c79c3f51a8101d9f501b4d89a04a91a13319d0d44376ee8ef`  
		Last Modified: Wed, 27 May 2026 00:22:42 GMT  
		Size: 25.1 KB (25098 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:88425388316b1c920dcac1826527408b667135956ffe261ad0c02416354690ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101748516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e082a7b4092a1a2e75acc8f7fa65529852ed6ef5500daff31745d5b6c14c92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:18:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:21:21 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:21 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:21 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e976785fb7544c209b05549d8cfce269da1f8f73e4f02d3d7b2e236b19ad06d7`  
		Last Modified: Wed, 27 May 2026 00:21:37 GMT  
		Size: 291.0 KB (291029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbc47c6937efdcec813236fc1a43a8627a2f5ce2335f3ef2107a3510692211`  
		Last Modified: Wed, 27 May 2026 00:21:39 GMT  
		Size: 97.9 MB (97885466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8e553aa991c218a32cb97d24ab23a4ffcf849b582c5d17aeeb73ab9d76632`  
		Last Modified: Wed, 27 May 2026 00:21:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:661928c7ac0ddeeee1c840d5a2e086a028bd7146b7dd7a552dc992ff0d9fc6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01fb69fe4fc8a898619be6914f2e6849eb6ac245d294a3109004fb20c41ed25`

```dockerfile
```

-	Layers:
	-	`sha256:e1f39ffcc1739849198a098e4887594b8119263fd87090f8386a2039d5cdccd2`  
		Last Modified: Wed, 27 May 2026 00:21:37 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:c71c4800960c33b2926ff7bfe4a3442faf30f868a31a4f7b488a11ad20a36d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101148252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0e003631a21562759e15d769afe343201a364ed211d8c727ecc7b58051a48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:18:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:21:17 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:17 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:17 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be22d06753bf44d0f1a52af08a58b5b08345438cbb0bf045e03c53a3a034504e`  
		Last Modified: Wed, 27 May 2026 00:21:36 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10970b698e6007676a0ddc85a9b7bd9dc803ec199aba70539ca19e2e26b490dc`  
		Last Modified: Wed, 27 May 2026 00:21:38 GMT  
		Size: 97.6 MB (97574805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c3a745b8bf718261527b15987a59a0301b8df6601c1073a31722c4a6de7dd8`  
		Last Modified: Wed, 27 May 2026 00:21:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7b4e25497c6a0e8988bfdc7362616452e96e66a598670b37e861ff7160bad0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f794036ee17c2dce1650bd5c34816db0742c7a6e26cd816f0584a383370fc31`

```dockerfile
```

-	Layers:
	-	`sha256:7f2527482b51373706bd32510957cc176766d9a3ac1bc9f24190163c0003dcac`  
		Last Modified: Wed, 27 May 2026 00:21:36 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ada0ef1ff6101376511366f2e3707a01c98587d4d4ae48b10918dd15b392a9`  
		Last Modified: Wed, 27 May 2026 00:21:35 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1d185a8339178f99192bc6104cf760a182679a29a2acde7d6843e637976ef20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100807468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c0c994ea15ae8b287b4bfec921717dac81f5f1e0cc1c747edfd3d1e92f148`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:19:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:21:19 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:19 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:19 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95cb083da4522b3d2742adabefdeda172ae9e8e78e4658a8bee9290fa0d7ea8`  
		Last Modified: Wed, 27 May 2026 00:21:38 GMT  
		Size: 292.9 KB (292875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11297bd411607a8b57c42b1e75c7973dc6c61df122e261576bba30bd7fe3ac`  
		Last Modified: Wed, 27 May 2026 00:21:40 GMT  
		Size: 96.3 MB (96314565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fcb59f819c284faa8b7c78d94e83e5a17975309ebeb7b522abe1b93e195015`  
		Last Modified: Wed, 27 May 2026 00:21:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e0f1d5a624088dd251a5bb69309fb5af88d965312f0814a4417c40d379a22882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e742f02878ca4f6d1b0df00d5474708792ec1a65b7781b3c3f9a53d5a4a0e383`

```dockerfile
```

-	Layers:
	-	`sha256:10ac48985323b0563e2dd0bd7b14192a988273b3903ee9f8aee1643599ad67b7`  
		Last Modified: Wed, 27 May 2026 00:21:38 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893cfcbf63abf36333db6e76048cc8ce4ae45a35d63bad364f3fea18e8ed5f19`  
		Last Modified: Wed, 27 May 2026 00:21:37 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:b2294a6e6ee094fd8eeafaec543fffb36436edd7dbc3de60827b1ce32255801f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103585314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf399cc329c8d7c5f3f683185523f8a52fdac199ea77abe1b71515a10a52211`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:26:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:28:23 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:28:23 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:28:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:28:23 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:28:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:28:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ad8e736eeaf2c8de3f6668b190df093be93b75436f4ddceafc01fdac2717b0`  
		Last Modified: Wed, 27 May 2026 00:28:41 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d403214e905076ef37eb9bf9b81fdb084f9e69d1847d3cf7505e9a15c9cfa`  
		Last Modified: Wed, 27 May 2026 00:23:45 GMT  
		Size: 99.6 MB (99604078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67957d8ac3e0f5dcbb31869770303f05140fc67395fb264ec2c9d464f2a4b7d8`  
		Last Modified: Wed, 27 May 2026 00:28:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:38d6e693533146cbcd984b590ec7880e864aa7de27fe5469259cc8c19905b9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1745b9f6793e40b47232b2afa16526cda3966f9165989412006afd6f4ff330b2`

```dockerfile
```

-	Layers:
	-	`sha256:f0e6f9cd71d7a8407e835af6d8d200cde3bfa857e8d43d8c0c78c7f13665fab4`  
		Last Modified: Wed, 27 May 2026 00:28:42 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9e0ddb0019290feaa9da031f87d18eed8d6067617706116eacaa85ecf5ec9d`  
		Last Modified: Wed, 27 May 2026 00:28:41 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:a287b2a747007d36e70577bc78016b993ee67eddb28a53719094c6824ca0bcfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102368611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108c8b424700c9edb955d2c3d5a47f0770ff5a926b95cfe1329323b10dcb482`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:47:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:33:54 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:33:54 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:33:54 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:39:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:39:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3404ddb9c665ea1e1f42e9894286fa3caedc18a9e1d221140b6a000d044639b4`  
		Last Modified: Tue, 12 May 2026 00:47:45 GMT  
		Size: 293.5 KB (293453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5d83b0a2acae5776f1d36a1951e6d604ad7e905260707ce03d30294ae6c508`  
		Last Modified: Wed, 27 May 2026 00:34:56 GMT  
		Size: 98.2 MB (98244071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c88a643e4dfe99136db49eb90aab4b4a838d7acc28ef2ab29eb3f0bbfecb6`  
		Last Modified: Wed, 27 May 2026 00:39:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:292c3b550e24404de2970c90fc33d6bffe736af5c065209fbe3899335324978a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 KB (218026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de5c7a591a7ed711c2542afa4200e57ea65a63d2c774ada016c5c36bd1e923e`

```dockerfile
```

-	Layers:
	-	`sha256:c6e6dce56e6df0b62ce706de446acfcc0eedb4f1533ddf6c8ddc7295baa030d6`  
		Last Modified: Wed, 27 May 2026 00:39:26 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1653901d2310341e0bbf3d24c4507ff5695bdaeaee63bcc8a151e70b504cfb9`  
		Last Modified: Wed, 27 May 2026 00:39:27 GMT  
		Size: 25.0 KB (24979 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:69a240971c4af022e04c74d5f58ab219f6f4c8013cc206f813a855eeeb399962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103040797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746d2353e4b01331a0fb0031923f7e9769bfa00bace397de4ca71d67e71a9378`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 28 May 2026 11:35:46 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 May 2026 11:35:46 GMT
ENV GOPATH=/go
# Thu, 28 May 2026 11:35:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 11:35:46 GMT
COPY /target/ / # buildkit
# Thu, 28 May 2026 20:30:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 28 May 2026 20:30:15 GMT
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
	-	`sha256:f9ba57acf5ba3d18b7eb9e4286139141d4a6480c2e9b8f4fd881334e86e5e1a9`  
		Last Modified: Thu, 28 May 2026 11:39:26 GMT  
		Size: 99.2 MB (99162424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb20ac87d29f824de6fab9598c6fd5a0880f18db7211c8ee556298a9b236cd3`  
		Last Modified: Thu, 28 May 2026 20:31:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:463b26775137a5917dafeb660baddbabe96106d659567ff79398571b8a8ce691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6d87bfc343670d667eca4af5fe3e7b7ebc505ce1ede15156db441c0990237`

```dockerfile
```

-	Layers:
	-	`sha256:ff62d029da4797ae66f0d7030539fb521319f66e71244d19ef54e9e918286f6e`  
		Last Modified: Thu, 28 May 2026 20:31:31 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92687eaa665ac6af13a90170c45d4a67616df7433e2948227c051f671b8ef4fc`  
		Last Modified: Thu, 28 May 2026 20:31:31 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:e0d2e4c290d52d57cb499d173d1ec08030bf0a8efd29122c2139a0fdbfbd7961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104311404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01f127e5be4ace432308b4cf38fba9fff0fd1fb22bed9c6a5ce6dff383ab259`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:27:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:27:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:27:22 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:27:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:27:22 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:27:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:27:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95f853eabb2533ec03a089c3a7c93466d9b3e95feb79fe7dbcd1b3ee93031d9`  
		Last Modified: Wed, 27 May 2026 00:28:22 GMT  
		Size: 291.2 KB (291158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def8ca56de94c50983811539154fa57356ce10e9aa7caf4558fbf0aca8e494c9`  
		Last Modified: Wed, 27 May 2026 00:28:25 GMT  
		Size: 100.3 MB (100293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4934fad0024c7b8f8aadece56fa42cb17686d0b8b3fbdce255cefed5ab25b4c`  
		Last Modified: Wed, 27 May 2026 00:28:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e9bc41aba1da7423891424916a485e2289d0604b77d12c25f327cbc04144e748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63da712f6c6ed59dc856c1aa3df2cb02698aeb018d099a37fd3b38a52908144`

```dockerfile
```

-	Layers:
	-	`sha256:d4bce72b1e08e33e7ffd96de39a898eaec54182227b1607d9f5bbaad58968d4e`  
		Last Modified: Wed, 27 May 2026 00:28:22 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2023f053ba97e3b9c8962b052d81824dd2457d4aed9c9eb5827a56ec57d6fa`  
		Last Modified: Wed, 27 May 2026 00:28:22 GMT  
		Size: 24.9 KB (24924 bytes)  
		MIME: application/vnd.in-toto+json
