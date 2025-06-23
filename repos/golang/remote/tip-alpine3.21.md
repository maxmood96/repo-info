## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:91073100709034753f62da1217d5911faf927bc86a082d22683e0055221c9824
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
$ docker pull golang@sha256:71e2a090e2fd4bee24b9e37722434f1bb526ebf4d63983c94ee19d647cbd4036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87130458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5fae55a6b83b8601238479d5c48b3ffa7730029f12f23168fd87cf7636eb7c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514d47c8e735902f215d398f133bb31982a29c06262a0811a06c3ce715545a63`  
		Last Modified: Mon, 23 Jun 2025 17:35:41 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553943e6d01c9acd45d693254df521c1e8dd5f2af99f49bd85cc6c44cbb632b8`  
		Last Modified: Mon, 23 Jun 2025 17:35:46 GMT  
		Size: 83.2 MB (83193149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d141b25cf0d8979091b904dad3335d1893281bdda0ae9999bc0f1acc86ea65`  
		Last Modified: Mon, 23 Jun 2025 17:35:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:7f4249b8d26add83cccca34cbc5faaf3f9ffdcf5f74401537cfb51b263086fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 KB (219170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d6c2b10e480f7ee5f6e1a05996539db7fbc07fb27d4758ed04d7a1a4e9373e`

```dockerfile
```

-	Layers:
	-	`sha256:5fa096a1c8342abe1ad6ab77f093a312745c946b2eb49cb3e7079ac63e33f9d4`  
		Last Modified: Mon, 23 Jun 2025 20:24:39 GMT  
		Size: 194.7 KB (194662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69dbf842d1d250f82b9ff5e3760a99aff87234d7f52adf12d776d96c37c4e9c4`  
		Last Modified: Mon, 23 Jun 2025 20:24:40 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:0c74946fc494d4d95a5dc1eb2bdcac5c31eff1b94ebca82f3089e3620aa311c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84184165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1acce53d7ba480f7a90cb643788a98d8575e8bfd7cda43e7e1ad65421b6942a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:1ab9a7a30deb311a783c5365d0931a1351ca72ae7fb5143ad20974e441e0182d`  
		Last Modified: Mon, 23 Jun 2025 17:36:02 GMT  
		Size: 80.5 MB (80523024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f7a4ade5f0df8a42a8aa8a311e111ff64318667ad85efe63e671be75d2a50`  
		Last Modified: Mon, 23 Jun 2025 17:39:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:2f0c7949e51cc561a432b364f545b9051bd35dda010fb95e40243cf430afec21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13717cf44fa3fdb47edb7531539ec759b168257ff23cd77c88f9161aa399f03a`

```dockerfile
```

-	Layers:
	-	`sha256:8192e6139a6c5268c295ea7d6f495173c52935992a2f1957c5e6e08975d3c5fa`  
		Last Modified: Mon, 23 Jun 2025 20:24:44 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:7e090e152e5be4029569bfda0aa35d737a746b50bd746f51b0eee30b89a1ead6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83669921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c23642767f56b2600cde8c63f42e8a32c9679b12e7e179ae89ee4cfaf54fe2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:9f2c23b36edc595b524e22ac037644488010f16b51c7c2741b5377b0b7319594`  
		Last Modified: Mon, 23 Jun 2025 17:37:09 GMT  
		Size: 80.3 MB (80276441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394acca446925b1ef5805601c2a2830d963f54f6dc0d75c93b7a529dcc0b7f98`  
		Last Modified: Mon, 23 Jun 2025 17:48:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:34ac97bcb3112709fa01e9c39c0771fc7c84e622bda88e4e8b887939b2807ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10494b233c51dbe99e02a2044856b44156d837c681ea08ecad3d6d7d4d12c056`

```dockerfile
```

-	Layers:
	-	`sha256:842e6d44f085e747c737bd55e9399ae3811f0c56f04607f74980b71dd5f9347c`  
		Last Modified: Mon, 23 Jun 2025 20:24:47 GMT  
		Size: 194.7 KB (194668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedfe8bb4757b17520c57f58984236e23256a651cf696b9401591362fd82549f`  
		Last Modified: Mon, 23 Jun 2025 20:24:48 GMT  
		Size: 24.6 KB (24616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:86d034841574d8493692b617d13e1eac3d1a96b7c561597669d65cfcd40ff311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83459474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d20dc04a57baf12df64525c61c38830d8e94ed543152be37b65e040d585cd5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:c5b77692401f3ea137343bd9363ea145d89603d5742a3fff804ed8b3a2b6ef06`  
		Last Modified: Mon, 23 Jun 2025 17:54:19 GMT  
		Size: 79.2 MB (79168414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c3380a1a6bc98007b1c887949580c488c145188255fd288dfd956f959a2914`  
		Last Modified: Mon, 23 Jun 2025 18:08:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b2bd7319326d4202ebaba96d7debb5a08ab3836c82b74663c26e519cf78985b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c164ac3aac1c254eb14fbab1369097ffdba8119a67d0135eb0156f473ca64d3`

```dockerfile
```

-	Layers:
	-	`sha256:29b51939b891af51f6e9b2ab5b8b73265ba3cb426b0ec1544eaa156250d33fb5`  
		Last Modified: Mon, 23 Jun 2025 20:25:02 GMT  
		Size: 194.7 KB (194694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4707f06d417b7378c5d15d29870b64f4386727a11b09d950279bbaa596651279`  
		Last Modified: Mon, 23 Jun 2025 20:25:03 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:83ce3b0be321fac3728ec5a2d3500c97e8fc735b35fe1eaeb4d0c2b536e828db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85687727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e1c8cc767198fabad667108039c56d2fc4de2ee7deed13410d93df2656b0c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89033e401844d0680dd3ed2a3b01b542c48048fc8a674bce0c3da9412ba4a286`  
		Last Modified: Mon, 23 Jun 2025 17:36:19 GMT  
		Size: 295.6 KB (295606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c3a68cf208e712d48fe5a3cca6178d38afd0dcfcac42ede03f6220d712b15`  
		Last Modified: Mon, 23 Jun 2025 17:36:27 GMT  
		Size: 81.9 MB (81928340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9242ef880600d68cf51e98d34ebc893097431b125f323dc4a13517de2b4fabc5`  
		Last Modified: Mon, 23 Jun 2025 17:36:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:3d494b39b4217846c3c894b466ae66605d22568e824e0661e7d09011d98fc11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 KB (219108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59c41bdaf2a30d844ac1c90f57dc8b8f4b2a82558d80541f138059fb695482`

```dockerfile
```

-	Layers:
	-	`sha256:56bbf7c69bd35c096365d621f4618ccad98bc33df4b7000db7fdf21800925ec6`  
		Last Modified: Mon, 23 Jun 2025 20:25:07 GMT  
		Size: 194.6 KB (194633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18159806525a34050a82ee70ae474db080143e107dd9d15dbd449fdbb01bcdad`  
		Last Modified: Mon, 23 Jun 2025 20:25:08 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:a43faeb7f31b625230701f189edcc03c945973ece4eba40ed538becce021311a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84335950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d1862659fac9e3589ebd28ebb8b06db1d0d615615f839ef5acef6eef71bc10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:a51f6a9436457535ac561521e5803267cfa96280c8bee442d726995d270b958c`  
		Last Modified: Mon, 23 Jun 2025 17:51:06 GMT  
		Size: 80.5 MB (80463156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3052e17f6df320ec3e4a8c53f7460289762da82f634ee57e0255952465f36f1a`  
		Last Modified: Mon, 23 Jun 2025 17:57:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:458940db7c21e6d8d007fee17279d84fc40d426317b109a1b87eb3e035eb6458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7ff0f5d14ea85de15a33c5eb5b21492f6619361af35c9ea9093352bb460271`

```dockerfile
```

-	Layers:
	-	`sha256:ace676deca0a450b117399ee47f2cd0f50eab4d3980b42c9cfd95ccedde37190`  
		Last Modified: Mon, 23 Jun 2025 20:25:12 GMT  
		Size: 192.7 KB (192747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340bf1a580f6994e5644199ab1d57b8c39fd0eed445f56ec2390e669471eb464`  
		Last Modified: Mon, 23 Jun 2025 20:25:12 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:e4b74433efad48d01533f62be012343869b1a24c7f615ebf60fe6df526d1b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84308934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0b50527fbb83d56f2b32aa716ccf111768e154b7a452130b718e4a8e626da1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:7ca371f3980f40fcf4092a1b2596a15254585a582ae996faee1dffc84f633fec`  
		Last Modified: Mon, 23 Jun 2025 18:20:54 GMT  
		Size: 80.7 MB (80661991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fa7d054cdff16aba97efbbc6e2dea6b56447b2b74dcfacc73e3a86880f1d5e`  
		Last Modified: Mon, 23 Jun 2025 19:02:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:fdd52825789c008fc6b1dddb26aa5b049a5f2e6a0de07e5ff914ed60b218585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88acec6687be91dcbf903075e8269fedf85758a4b92027b4466a629b24e1f1`

```dockerfile
```

-	Layers:
	-	`sha256:86ff27633bb613876f5344ef7705a94693c1af068970f893b23e889724756508`  
		Last Modified: Mon, 23 Jun 2025 20:25:16 GMT  
		Size: 192.7 KB (192743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8396fb806ec71a06c9298fb9cf53ca2ec083f4780611f0ac0a40539125f11d3d`  
		Last Modified: Mon, 23 Jun 2025 20:25:17 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:50562a82dfcedd174e86898a6f76df8cb83a8d1d1002d1ffec22d412b9a4c466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85472926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5988fe48d2551f05f605f64c5cd70370c69f05c93ae487c9e3a2b92b9574fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:87c4e9ad813ce53948d9016f3d50242da725640f347f8b2bb02b8db89e7d0980`  
		Last Modified: Mon, 23 Jun 2025 17:41:29 GMT  
		Size: 81.7 MB (81709009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500b293477c857ab9f924b408627c0e27960bbc17c72682e215f651043a08029`  
		Last Modified: Mon, 23 Jun 2025 17:47:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:79eeee4aae97ddb5164f6c17118cb8531921dcea9162e79e5a44bdcb324b2b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4900d5e63a667e8d1b9cfb084d05720849b9d9e58f285c1d9bdde453f2ce704c`

```dockerfile
```

-	Layers:
	-	`sha256:ed30d6d0a5081c5473d41350a19e8e1f77459b96aca60d93fb450b96c2f8c708`  
		Last Modified: Mon, 23 Jun 2025 20:25:21 GMT  
		Size: 192.7 KB (192711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01faa2ce79729aabc1b3eac4a14452ab1647305a902229a9f1c2271502add0dd`  
		Last Modified: Mon, 23 Jun 2025 20:25:22 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
