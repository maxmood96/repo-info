## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:6b2f33a26a6ad28720a32bdd711d14fb7a96079e5583f4e0456ee767d61ebfb6
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
$ docker pull golang@sha256:f3d223b58a20916c687c96e4d58489659dddd7c4745f24d0e4db367c5e5c2b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131456582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5108fb2519348f49f08dd800e3d84c745281aa04c14562433d598d1e107815`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986f8823f9eb1f33cc216497901a64ead469436c45c7532caedf941d2081bf2`  
		Last Modified: Tue, 13 May 2025 19:20:59 GMT  
		Size: 294.9 KB (294928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a030b6acdb6db93394700b17a9f3cc951920ccdced1afb5118ff9ea25b238acd`  
		Last Modified: Tue, 13 May 2025 19:17:15 GMT  
		Size: 127.5 MB (127519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed444f6928c0efb75f1690c3575063c6fcc8319be83ddfc0be68e8c70826a26`  
		Last Modified: Tue, 13 May 2025 19:20:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:30fe59a91461a98e5b38582936cb8b1ff697fe7976b610a3931c6dd538dff94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2a8feeeef26ac5abbe06f905bacb30cd31362d4434b5f97055fc67674b2dba`

```dockerfile
```

-	Layers:
	-	`sha256:a005ca0ea96af8b4b1422efc9f441342fa8acd514f1cf56200e4fb972ac11473`  
		Last Modified: Mon, 12 May 2025 19:15:37 GMT  
		Size: 211.8 KB (211831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb9370e25c820928e973165f50fb14492b28700e48a5cfed453e47ac890ae3b`  
		Last Modified: Mon, 12 May 2025 19:15:37 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:bc18b98442ddb37d379e25a2cd11ec805c91a45358febc02b60b73526300f3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126469143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03db5e31b70a606951b35ff0f30a0c63dc6b466183f517fc98dc2859b2fc4822`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:cf4282a86be70f8e1a4d046254c770e7b2183496ad61e66fa1ae91c1abfd1471`  
		Last Modified: Mon, 12 May 2025 19:44:12 GMT  
		Size: 122.8 MB (122808002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da604da46927f4c6eac8caf8a4394830073b32c72a8b0b003070ff9c9472838c`  
		Last Modified: Mon, 12 May 2025 19:44:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e484ec3745662bc58f17016a4fe8041a75c9f6a938caa7fcbf6bbc9a8641790c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2d9fb9b88b88dc5bdad7c434a7da59ec12fa969f42f0a0f26fb0a968c78e7f`

```dockerfile
```

-	Layers:
	-	`sha256:dba998bbdef9ce327bc54dc8e043e79bd059b2943b4648f1ab7900a668eaa799`  
		Last Modified: Mon, 12 May 2025 19:44:08 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:95be963674b2caacd6c90c2ceeb77270ec8a8fc5a5c62ada106eeae42f66ec50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125882136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9dd910fe0bbbf88fac20d65c9e7e92f5e6b1cf22b6cd8b1ad478baefbf4aa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:8433d2a5af6a5a0cd9e0774121856fe6f3adabe483560b233f2a94fde92edb03`  
		Last Modified: Mon, 12 May 2025 19:24:40 GMT  
		Size: 122.5 MB (122488656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03afb96dd57f2bb86e9de12da6596ffcb394a467c2609e46e3aadff55e0425be`  
		Last Modified: Mon, 12 May 2025 19:34:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:30665e87d31511aa5d65dfe4da05e3f5a0fd266324eb4bcee60627831bf56d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052631b4fe28df03b76598eb0f4df3ade47e3f2b7480e93c53046942fb3ea9be`

```dockerfile
```

-	Layers:
	-	`sha256:01e8afd930e4e72ca13addbeafd9576ea2d569ce1b867be374301058daaf64d1`  
		Last Modified: Mon, 12 May 2025 19:34:50 GMT  
		Size: 211.8 KB (211827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d186727e26cd3534f29ab21de6315086fe8dffb5ab1de5245a414d7224070d0`  
		Last Modified: Mon, 12 May 2025 19:34:50 GMT  
		Size: 25.3 KB (25265 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f2d51f5b2ba5b3f3d0233116938fbc7a2f9e49f69e6eb730fabb352f0a80aa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124442777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d4464fb54e0b392c7855a19cf0c1c91e02a3b12fe38fc9c7271b60795d2345`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:c5330a97dbc92942ba37ce2bac7d5253897166c49acf8935c0dc87f91eec5803`  
		Last Modified: Fri, 16 May 2025 13:26:20 GMT  
		Size: 120.2 MB (120151716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8dadda6a333da8212e9fc097213e0555416f8dafff90ac52f4b09f89d77051`  
		Last Modified: Tue, 13 May 2025 19:20:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:cc8d056492a2545b08e7698be58360e2af24af2940d284b04231061575e35505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 KB (237189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb858439d6647be2fcb321ba3f940b156b189a3e371cd1b159446105711065b0`

```dockerfile
```

-	Layers:
	-	`sha256:435c347147d3970c5cc03222e416ef7c0f4a2694081564bdd2953d56d8bae4a7`  
		Last Modified: Mon, 12 May 2025 19:18:21 GMT  
		Size: 211.9 KB (211887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4235a0145aa447afd2f71e3406882392911c713f24d6b2a7e54ad5fe7211473d`  
		Last Modified: Mon, 12 May 2025 19:18:21 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:78b8b20c0b7a889c577cfb1dfa4a6213fe1181b2701e3f94fe615d8354a89b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129411118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05d717bda2a91b5a3288665dab8ae7b046a4e84e6dc01a44e3f55e36743cb10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59122b3cf5684e4fad08b5dd6a4e6b15fcdbcef1e4932361f7e20bd2f4e8b75`  
		Last Modified: Mon, 12 May 2025 19:15:52 GMT  
		Size: 295.6 KB (295604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d7e22db058c2c925ae80e0e254d251aaeb04c6161e3b31757924fb81096b47`  
		Last Modified: Mon, 12 May 2025 19:15:56 GMT  
		Size: 125.7 MB (125651733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8fe384ea72dcaacd0471be2e7769f408f159d67e6b7ebc94fd2de9a7ba06e9`  
		Last Modified: Mon, 12 May 2025 19:15:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:379c66bed605a68d2f4d61ad7178f08030e0dcb4afc984e05e052cb80e0af571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3608a5b824c93a3edd52a9bece177c20579c4bfe57d3763696559b8f281ac6e8`

```dockerfile
```

-	Layers:
	-	`sha256:025f0bc371aa14d01f7e2e55e2e917f47e5da24088eac79aab25e645162b5676`  
		Last Modified: Mon, 12 May 2025 19:15:52 GMT  
		Size: 211.8 KB (211766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae3b1ac59ae7e6c5be6079f969d679b549492ef93401dff82ad5e0aa72338e2`  
		Last Modified: Mon, 12 May 2025 19:15:52 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:89ece499214a9f58578b5065938edf776a8f14d4a15e5d166f657319e5532907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126161865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c7336964b6778c22a7e813d6c5401a8e9a9905908041f4d6d2f9f1d53ae41f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:67ce9d7585ca139e17d7229c72e5e4b665cf0442ad17458746abe1ac1f1118c4`  
		Last Modified: Mon, 12 May 2025 19:15:34 GMT  
		Size: 122.3 MB (122289073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90921dc583caff4643236bdfaa34da691b48a69e8d89f739e0df1af0c251701`  
		Last Modified: Mon, 12 May 2025 19:18:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b14983228d9365de2e44828c78517885f45f3868fcbd1cee962578bff7d3cea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 KB (235154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27227c50e4206fe4f50a8749de3cc635db09f474a1ef42b53f082d34d37ab435`

```dockerfile
```

-	Layers:
	-	`sha256:3d7cbbd407469e13720e1f52940d7ed3790beab5ae3e2a02c76e7b217e6cf130`  
		Last Modified: Mon, 12 May 2025 19:18:42 GMT  
		Size: 210.0 KB (209954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a58cc7a495eca084960ea72f74483255def8d19c0b561a165cc49a599a955c2`  
		Last Modified: Mon, 12 May 2025 19:18:42 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:e6a3b8cdcf4ed4f63567becce0de595989a4da3121ccf3bfa41b61112cbeabf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126274342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbdcc2d501da83d23f9e2e0e49b5e2cbdc543a403624765452f22017cafe3249`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:ba6fb6b5563dabdad76b739d3338fefd5b6192bd70358c744c534995868ad289`  
		Last Modified: Mon, 12 May 2025 19:53:04 GMT  
		Size: 122.6 MB (122627399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb98dae830de04d5f983165f2bc759113168a7942c548eddb0be1bb3f011d9a`  
		Last Modified: Mon, 12 May 2025 19:52:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d806f2be279b1cbd36e15a5534afdc3e11c928b18e92ce0daac5c145c0085846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 KB (235150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cf5d830f8fe8c1fc21fafb1decc310e607b914894f9e9a9b6077cc1863196f`

```dockerfile
```

-	Layers:
	-	`sha256:03323c6c73a76b1ebcf1c13acbc8259a230d89ae166997302bcf7489eb9f52ee`  
		Last Modified: Mon, 12 May 2025 19:52:46 GMT  
		Size: 209.9 KB (209950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a12b019c0d0d47a59f88ad61116a795889b8e566fc390f9e22f62fd5f022b6`  
		Last Modified: Mon, 12 May 2025 19:52:46 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:83b128574bd674a44e86c7109d93ee24688916bf144a0c3e88db7ad2f76dd20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128512560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc466bec9e26d8e5975ae51568914bbae478ac0bf127b1229670eedb4e6e8018`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:05f6707b6ea1615397f3ca5bfff811b917ce5218f2246275a6ac50ada31e70be`  
		Last Modified: Mon, 12 May 2025 19:16:07 GMT  
		Size: 124.7 MB (124748643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a93968b8724c53edf8d4f5aa989b81566ee84dfd2d54e0273c4b14a37bf1ea7`  
		Last Modified: Mon, 12 May 2025 19:19:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ae351b6a8f1ef666386b3b80e33204b1585edeefcccf98d882a535583aa7e1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007930c6fdab4d59f44cbae29b336dadb05ce9cc4ca98eff955499706b753e99`

```dockerfile
```

-	Layers:
	-	`sha256:1420894dd929b327c21e6f2f87648681be70432805b441c2010b13302acb8db6`  
		Last Modified: Mon, 12 May 2025 19:19:03 GMT  
		Size: 209.9 KB (209880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343168715be2167047b3b676e656f97866e610f80816657f1138105c6533f8c9`  
		Last Modified: Mon, 12 May 2025 19:19:02 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
