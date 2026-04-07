## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:c15892d24bfadd381ee42de3f7f0dff5edf294352eadb4f4ef088b4b40c46b5f
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:a781e217da0782606433db7e7baa61b89e00f099970a56026e73351f81744efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98096599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d764c791a66cef78ebbd38caac72d6db68e81ccabc757610f20aa8ab11830d67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 06 Apr 2026 18:43:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 18:45:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:45:10 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:45:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:45:10 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:45:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:45:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5ff4fe06bcc752065f506654867234ef4abcbacb0bdba579fa66cc5d3be626`  
		Last Modified: Mon, 06 Apr 2026 18:45:27 GMT  
		Size: 291.2 KB (291154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8966583daebf02f7188b966cc8cfaaff27cf5fc1ff9b30af37d939f77e22335f`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 94.0 MB (94000413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72da44ee3d8c3933e51b00632cf67781320f10a1dd8944b4de3b780827e69522`  
		Last Modified: Mon, 06 Apr 2026 18:45:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a7febb7eb49e4f2681fcd11b23c1aa2f2e398d12f0b8566b3440324a539e6637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70983f3df8bac9259516d6af23c924c2a9d1a26d33a047a7cd19c939a1b68ee7`

```dockerfile
```

-	Layers:
	-	`sha256:7599f228fb1404b93a5d40387ff064904b5c18ae93527d87200015852e360359`  
		Last Modified: Mon, 06 Apr 2026 18:45:27 GMT  
		Size: 195.0 KB (194984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f6ce4ecab78f50864b0f4491a793c3161e061ac11b90ba162f87a2f356b767`  
		Last Modified: Mon, 06 Apr 2026 18:45:27 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:183ebdd86ddcbf91c6f6053baac40e77d4b7746d0f360e1c918ac586a28172c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94213697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6691825bd1766b837e60e744db152354d9443b83ced07d07e0ade3fb0c83f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 06 Apr 2026 18:38:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 18:41:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:41:21 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:41:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:41:21 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:41:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:41:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac1455a99606bd13d608469b9b35cb7554f7ee76e84407078c9253b00a2fd9`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 292.3 KB (292299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393680f702bf36f995f3d05ba855c679536e58106a81ae55184686e8496850ed`  
		Last Modified: Mon, 06 Apr 2026 18:41:39 GMT  
		Size: 90.4 MB (90416194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4554053a194d342dfe4f7f1cce8d0832436370a27c76bda3c648d75f8b00f`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9e7bf1cb51a45efdfa5e2e9eafa2d7a105e4ec8aff78246c54f9044542597cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0473d825c08063fdbe5c2b2cd16b0482dbdd6dc134b1f0035a038e7184f8b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:9efc62c4536757eb5f45993f136abdd0670a44df2513784f579d8d14de0126fa`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:8d6dd6a17cbb64d771103953a100b955cda2dcfa27b3c0a30115db580b67cdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93651696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056e225697bf374cba1f0e35621bc68069dec86a0e3287d0ada4a7192aa5160`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 06 Apr 2026 18:40:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 18:43:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:43:05 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:43:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:43:05 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:43:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:43:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816b80dd0db35fbc756f00e76d4dc7eb40baa502d2625cb2e80755c840f68b66`  
		Last Modified: Mon, 06 Apr 2026 18:43:22 GMT  
		Size: 291.2 KB (291202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866705b29d2f18b79748f9fadfbe79c21fa37d231a94fa79b6aae3edf75ac398`  
		Last Modified: Mon, 06 Apr 2026 18:42:37 GMT  
		Size: 90.1 MB (90136708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64afdb7fac07eb60d6761efcd12b84ce4beb528770ce4191cf2130d09154cf5`  
		Last Modified: Mon, 06 Apr 2026 18:43:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:714b5643bce9406bbe0806cdbb50325803c103fdce46a5bdb5cd4fb167c1b813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f504945110efdf3bbc142040a19f6f520076493241ab65f967712f5c1504cdc`

```dockerfile
```

-	Layers:
	-	`sha256:2ec7dc1d0d4e75527b0151ea6b5f8dc98c2786e460c5c8b614dbc73826f8c885`  
		Last Modified: Mon, 06 Apr 2026 18:43:22 GMT  
		Size: 195.0 KB (194988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d02096f3850b4d39e87337f50eded68ade4ddd48484f02dadbba035eeabf34c`  
		Last Modified: Mon, 06 Apr 2026 18:43:22 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c56d8215eb9ee51798acbc9e4f66f470492b7a35b76f6339446af77fe5574d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93518725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396d96c73f2c7b4814d39b60be0232d8f4e119d94518f33337faeae1438b9b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 06 Apr 2026 18:41:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 18:43:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:43:27 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:43:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:43:27 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:43:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:43:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fd9b43fc867c5acbdb7d3133ec0ea8cfb1d10b6ef3c3ac74f44d8d816807e9`  
		Last Modified: Mon, 06 Apr 2026 18:43:44 GMT  
		Size: 294.1 KB (294093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffa2ba5933aea1f1c364c6a791a91c9e49057e35639f30985503d0547a7466`  
		Last Modified: Mon, 06 Apr 2026 18:41:04 GMT  
		Size: 89.1 MB (89084955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165be6f65351892574ba04734d601e9990dd9c935c27e2216ea6b3e8a133d250`  
		Last Modified: Mon, 06 Apr 2026 18:43:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:eb3b933b3e990fa44961de64eced5ce44f826741ff054e6dd5520154125347f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c116475edb31f5e537a7148c4bd7a6fe862a8c0463a7e7b128724c4b1dadd14`

```dockerfile
```

-	Layers:
	-	`sha256:8e420380ce4a2774afb728a55d958fbf12ef5cb9d400054f0f0be12c96f68a41`  
		Last Modified: Mon, 06 Apr 2026 18:43:44 GMT  
		Size: 195.0 KB (195016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805942e2ec413ea9b0051a6b8d55dc2dc2a942d76c6dd785e893f93afcba9012`  
		Last Modified: Mon, 06 Apr 2026 18:43:44 GMT  
		Size: 24.6 KB (24599 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:4572d44f2957a40466d7974cc5fb027eb481b01a528a3592081270c03e717999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95754271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece8ec88d08147e998ba08bdd88219bc0cedccda2b9fc70854f64cbedfc0b96`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Mon, 06 Apr 2026 18:41:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 18:41:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:41:09 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:41:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:41:09 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:44:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:44:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61ec01a3d8bd62d544e43bcb5c363fb63376875fec4e3cbce5e09be3665ad6`  
		Last Modified: Mon, 06 Apr 2026 18:44:19 GMT  
		Size: 291.6 KB (291614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b82e2680f4d14426f015346712b6e5f30c486655039ad7e1ec71d21151434`  
		Last Modified: Mon, 06 Apr 2026 18:41:48 GMT  
		Size: 91.8 MB (91841768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db4465e63222e7d1d6b3c40d5ba112d3c7d3ecec23a5f3606c01d501d468074`  
		Last Modified: Mon, 06 Apr 2026 18:44:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4c23903b5983f37f0f1bc29ff5dcbd2825314da0817d54b3daef6ba4fc796925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba933a088069a077e2e057ef305fa23c6fabf1fd206ecc5a408ce64dbcb5a88`

```dockerfile
```

-	Layers:
	-	`sha256:cfa53dbd2d9f2412b6306b92a1ca8ccb612f8a40b71e16d2dea06fe05e7e7293`  
		Last Modified: Mon, 06 Apr 2026 18:44:19 GMT  
		Size: 195.0 KB (194953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72b8cb683bf4571f02a71c1cbf487aa6c7cb24eb44cc5b31c95aa64bd6165ed`  
		Last Modified: Mon, 06 Apr 2026 18:44:19 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:f24ae94860158cc322fa9cf7868cced6cc2bff35baf0439bc3cbd76e936d23f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94831823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eebe642b46b78aa28b762c49660905aacd69416d11a5ae7e33d50f58a17588e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:55:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 18:57:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:57:14 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:57:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:57:14 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 19:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 19:02:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64720ac2efbc7914d888806578c44302c9086937591f15a9af7c799c3227865a`  
		Last Modified: Mon, 30 Mar 2026 17:55:20 GMT  
		Size: 294.6 KB (294572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc368d4f4523089f91977c543e8d1f1e4d28e3b0d524ab4ee1d1ce21debe4d`  
		Last Modified: Mon, 06 Apr 2026 18:58:20 GMT  
		Size: 90.8 MB (90802796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f5a8b2579b8761959ebd88ebca321c30fc3e42855638563f58121c1c8dc6e4`  
		Last Modified: Mon, 06 Apr 2026 19:02:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a5692a83e5e5c3b6af135654d23ae34364b00cd8f2d8351d879502529f8b5fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb9209916ed6006ccda0208f3153a300d0367842b1172b1ce4ea0b9bf021cf0`

```dockerfile
```

-	Layers:
	-	`sha256:5060517cde4655de01ed1c407927f63efc7cfab0c375451f5fdc0e2d05929a84`  
		Last Modified: Mon, 06 Apr 2026 19:02:58 GMT  
		Size: 193.1 KB (193071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bc23540c994d5db2841025dba8856f1cac6414a414318d0e31300448884e21`  
		Last Modified: Mon, 06 Apr 2026 19:02:58 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:c955abdb6e76cb8fddba272c204f50209c338a139527142b529171de2e48cd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94978187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a909ba6f3875fa167aec26a4f3ebf070408bd3031cabbb18c58570aae6520848`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 09:33:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 00:07:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 00:07:49 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 00:07:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 00:07:49 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 01:34:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 01:34:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffd6ced4c894ab06d11bb63b601a98fc1d0536c2ff8bedffe653c521058ea`  
		Last Modified: Tue, 24 Mar 2026 09:34:58 GMT  
		Size: 291.5 KB (291515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54965d042f5518ecbbacb568db6d4c79f2db392d6bb595ff62396d66c4a52e68`  
		Last Modified: Tue, 07 Apr 2026 00:14:41 GMT  
		Size: 91.2 MB (91169092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afab4a7a7c3a6581c8131dae4bd5edeac041294eda66d1f29c5fdc471b6360a`  
		Last Modified: Tue, 07 Apr 2026 01:35:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:42378a4874167b34827c59acb392215c7423830fe2bb8ffa5229aadd2982c173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea321dc07109c2cb670ef43f5a1bb278e2c6882a7f3b19e61299e543715c108e`

```dockerfile
```

-	Layers:
	-	`sha256:2fe17c057c79c0d4a23cb2c695cd758503ca42448c6866257f025608a29479e4`  
		Last Modified: Tue, 07 Apr 2026 01:35:50 GMT  
		Size: 193.1 KB (193067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6da8b370c5748495e5e7d66d8112345e5b45703d5c5f3fb50e8107e8248803`  
		Last Modified: Tue, 07 Apr 2026 01:35:50 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:a36f4695b9152d3113fd12fc436e840613901ad3535148e79041a67fd1f969dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97125599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94def3f06a1f0f433e48b949a8b06f9ff25a927233ae8787e57a544cdca56b6c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:53:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 20:02:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 20:02:24 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 20:02:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 20:02:24 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 20:04:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 20:04:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7637877693e4289d6df99aa29346872829e90442ce4345fc60826a40b78f22a`  
		Last Modified: Mon, 30 Mar 2026 17:53:53 GMT  
		Size: 292.1 KB (292140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7bb14b36d862c74817ebfb57b26695332f89670a6fc97f1c869402d1de33e`  
		Last Modified: Mon, 06 Apr 2026 20:04:12 GMT  
		Size: 93.2 MB (93182867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47b59d1c63a84b7de96a78fe55de9acee3ce2f312c775c8e8ac6cf0362a73f`  
		Last Modified: Mon, 06 Apr 2026 20:04:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f9e71370a08dd4bde0e51e8b9294e3386ebbb8ead4ea7801c1d86f5f1cb151f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f2298a2d09fcb344b342caac5af1b11f002a0e16189ed6b3ba4a3031f7cb7f`

```dockerfile
```

-	Layers:
	-	`sha256:144a298e10aa6bf4114337a9bd54941944157f29f99bddf8f3250347c4576c4a`  
		Last Modified: Mon, 06 Apr 2026 20:04:41 GMT  
		Size: 193.0 KB (193033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f693dea5ce8c2922bd2f81e689568dc5bfef43fe7f5671fb638b90d4d4b69a`  
		Last Modified: Mon, 06 Apr 2026 20:04:40 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
