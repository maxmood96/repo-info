## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:ce9940c4f1138f1f35368dcbdaa9c8ed181ea45781bc027c27e4dd9793c79c0b
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
$ docker pull golang@sha256:f9ba3c0d8788c76374f47831b1ea1aeb3af095fb610c84350ebd503b6f98b2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88693784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425cb5fda151c68a6fffda36f0729aae6dce6980519f0a5c8099d346cb0bfd04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6d56e11053706c324d1aed9422637a5eae839388b3a34f2acd2108e15e8bfb`  
		Last Modified: Wed, 08 Oct 2025 23:40:03 GMT  
		Size: 291.2 KB (291159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a225db047f32dbd84f4590f2b6c32b9ffa9de20cb9b08f648341a3ad3cf52`  
		Last Modified: Wed, 08 Oct 2025 23:40:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d70f3eb8c4f6086c737a10d62ae37e8b49d0c18622840f53f04d42c58166add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364cda6a411d2358f63062f98314514a4a317068660123d83f945e664c5d316a`

```dockerfile
```

-	Layers:
	-	`sha256:27f728cc18f8a8f04dd90f25f94e2d9becf41c30a5e2e0d50a926ec6a9abeecf`  
		Last Modified: Thu, 09 Oct 2025 02:24:03 GMT  
		Size: 194.1 KB (194140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea83d94915eb483a9e9f9699ffaa11ac365dbdd47305870e0027f4a0eb2a4ad3`  
		Last Modified: Thu, 09 Oct 2025 02:24:04 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:270fb303422538c189c66beb7dd2840496fb1c5d603c25065aa22a3b66540f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91129818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfef6532782a4956724ed9dfc54057b9cc1000a8958e527fbf496fe14537b2a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc9ae1354d1b58919a2fea4e47174a010414a1cda645c0f6508c4be28687947`  
		Last Modified: Mon, 13 Oct 2025 18:33:51 GMT  
		Size: 292.3 KB (292311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74301a8b76982b257bb111ec9b6820a6de48153ddc455c61eafa801ef71fcc5`  
		Last Modified: Mon, 13 Oct 2025 20:24:30 GMT  
		Size: 87.3 MB (87333269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75709ed18f8dd74030d7724cdb2268de3ed22f380d8ee3591c8c108f5176acd5`  
		Last Modified: Mon, 13 Oct 2025 18:33:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:109d76aa666be259450619fd488225a8a121aba07e218b6488ac08c9959b260b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74755b4cdcd7ec63543e201d59e0a9fd8679e6309163c388bbcd00786e27b959`

```dockerfile
```

-	Layers:
	-	`sha256:a5e2f89358075512710eafae98d8ae68892fdd9296884cee73a5839a03c19df7`  
		Last Modified: Mon, 13 Oct 2025 20:23:49 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:630b77f5d8bc42a4749bce3b5bd8ebe8a67c42e1a626980043bb9a5fad5756a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90587418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54789d7536ba3d537589680d7cfe8ead6a0002557d30289666d0ca784327240`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78d0724f77b15cec7ddadba722b29dea43c4d61a6e61312987d794b80d2c1b`  
		Last Modified: Mon, 13 Oct 2025 18:25:09 GMT  
		Size: 291.2 KB (291206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b3f77f198194af8440022630b5f3555d19874bc1b8dcfcdeb4ff1346ed16b`  
		Last Modified: Mon, 13 Oct 2025 18:23:46 GMT  
		Size: 87.1 MB (87074499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f2c3963f4b0da8d0529e60bdfe284df442fb9770ad2b9dd1751e5c72d3bda`  
		Last Modified: Mon, 13 Oct 2025 18:25:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:bd25ff6cf66f6587bb5ee2a0751d063caf96f795662914ba1b746f85ca9dbf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f47775cd24d28aa1b7aec6baa31b5850a4004bd208252095092c31e9da550f0`

```dockerfile
```

-	Layers:
	-	`sha256:21effea2e058212b505ca05cb06873975efe3d0f31fba0fceb2bb727845366e4`  
		Last Modified: Mon, 13 Oct 2025 20:23:52 GMT  
		Size: 195.6 KB (195632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05943339b35ab8d1cbf5aebcfb10a38e46b09127b2e077b3be18d0dea59ab3f8`  
		Last Modified: Mon, 13 Oct 2025 20:23:53 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:60014d492919417fd5ec61d0f9d852b88bfd81067aa2a59e4862567ce70e7d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90474417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea49d64c7f0f3b0a12f241cba94c203b0351732d3ca4e177ebdc5fdb594d3263`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e96aebbea1fe54af9b503ca7c51165a0ad88fd062d4ba027a49ddd8f7fdae3`  
		Last Modified: Mon, 13 Oct 2025 18:26:44 GMT  
		Size: 294.1 KB (294097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad87b7b196d7850da55968ab4ea8d2e74337f796a2dda3e1e502c848906a7`  
		Last Modified: Mon, 13 Oct 2025 18:26:56 GMT  
		Size: 86.0 MB (86042092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b88516daa70bad04eeabe5f063ff0aa196f123a904663729b12be33549b88`  
		Last Modified: Mon, 13 Oct 2025 18:26:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:76850567a680caf6d2536e0f86a420f3f64d9e0d67833fc87827b3561dac8af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 KB (220965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328a634d193950f36beaaf1af5f43542607a4c44274b5397d8a35088c0a9891d`

```dockerfile
```

-	Layers:
	-	`sha256:e310475d590c074703723b3ce1aa9687901739daa2e6c3f2db38f015ad34b3e2`  
		Last Modified: Mon, 13 Oct 2025 20:23:57 GMT  
		Size: 195.7 KB (195668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b5363ca97a83113b72dcdd508133b7cfff4ca293ec3265884ffdd4ca06f27b6`  
		Last Modified: Mon, 13 Oct 2025 20:23:57 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:c2d25e64f7751807eaa3a9ea75c7e5e8e1f0164034e48714f9cd31ea0f8748e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92762810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a989e4df6c34c028e66a0d9fcae9c7365e789753c4e11062758c64e55dbc6e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e57dc913cd239f8a4ff63e9fd3e61a04004080639590170416e2cbdfb1d355`  
		Last Modified: Mon, 13 Oct 2025 19:08:24 GMT  
		Size: 291.6 KB (291625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc457dc23d2f2501ae16881398a5b91dd66079c5042a578bb1e723668e7c145`  
		Last Modified: Mon, 13 Oct 2025 18:22:29 GMT  
		Size: 88.9 MB (88852096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb84401d7985f795eccc632f43473be26aa741c2b667148622b5469f1236991f`  
		Last Modified: Mon, 13 Oct 2025 19:08:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:8a29f062d76578a854d02abaa334d5e7fdbe872dbe8bcbdc7a032692001f0445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c55bc3e32d9973e6f0d60e46429a66dcba0f2450bacd3106420c15d6378462`

```dockerfile
```

-	Layers:
	-	`sha256:957335d8fcc5ccdb41710534d819bcc4fc997acc4dc46a7e2662a30743e932e2`  
		Last Modified: Mon, 13 Oct 2025 20:24:01 GMT  
		Size: 195.6 KB (195571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19e2a4daefba2bedacb54dee2efef45ed2d3771d01b27e9395afcf30eea61d5`  
		Last Modified: Mon, 13 Oct 2025 20:24:02 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:f8d4106a696f6965244008330a4c5e8eb78540245a0165df6ee06d5315024d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91468867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7dd31ff6f18ba1650fdc1b99c158e9ac3995fa3ed63d8cda83fb93f62dde0d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34403a3833161e7317f5f43c031b3114df383a82ea83c5851edc4d5c8b921a`  
		Last Modified: Thu, 09 Oct 2025 04:12:57 GMT  
		Size: 294.6 KB (294579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb280635ff73067e450776ffb495ea1ad6245c60020ec72c47db59cab52504`  
		Last Modified: Mon, 13 Oct 2025 18:24:19 GMT  
		Size: 87.4 MB (87441889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27794a240a8ebaa9514ca85f3e87f0c8691eee2cc6b08253f2ba1537d630296`  
		Last Modified: Mon, 13 Oct 2025 18:33:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:1c4d874d159aa1ba61da1fbe35c87e77a85cb23b6f82a00516240fa6c83a9160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8a9b5ec006672ddd840618faa6358565c341189ec5e9eac4301d8fdd5c0735`

```dockerfile
```

-	Layers:
	-	`sha256:47337c08700db66ba3dde9e04c188adb0330ea7eb357a0155441c67cbc580b18`  
		Last Modified: Mon, 13 Oct 2025 20:24:05 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00e5dfdbaee03337fcf0f1f32ed3681f0d1b421536bbcba4f5999eeb01b5410`  
		Last Modified: Mon, 13 Oct 2025 20:24:06 GMT  
		Size: 25.2 KB (25195 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:c868d16d071fa22852bcabc1035552565d0c467e4e079086e7f1eb11ff383f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86040796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38212fc6bdcfc586ccd63e709f6137e6e6a3493a720236be0174597c1906880d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2055b904ba40ebefe03b802bf4885ac2708bb5c47a4294058815bff9a5ca3b`  
		Last Modified: Fri, 10 Oct 2025 21:04:20 GMT  
		Size: 291.5 KB (291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd0ce2ab28438bdf94f05f192ab71a6b801a6c5d6e3d4dc6d664c820e75f2c`  
		Last Modified: Tue, 07 Oct 2025 14:09:36 GMT  
		Size: 82.2 MB (82233887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e169cffe1fc87726d2b17399d782a2593334b6b8c29e809f0e1252d9e25d307a`  
		Last Modified: Mon, 13 Oct 2025 08:49:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:511e523f18830df3cc62fcf279ca8acdc4464aaad9d8d7ca84ebab982f854253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e805d1b0cd5e65b70d763861911c80200d2484ac5c9981d88fb1c51d34c342`

```dockerfile
```

-	Layers:
	-	`sha256:974fd0df2c79af2c7e3e3e4632ebbf417c4389182b122b1e6546150e51cdf7b8`  
		Last Modified: Mon, 13 Oct 2025 11:23:29 GMT  
		Size: 192.2 KB (192233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10904caaa772385b2371b4e97c30292f300a4adfacbd8c4972dc70d07db44ce6`  
		Last Modified: Mon, 13 Oct 2025 11:23:29 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:f87416599bdf677b1100f8fe0634de455548a5bbbcd34b21aeb130653c64c052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92733751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f783cb909064db852ca1e9781dcfa3a18ac0513c858bfc8c4f74c9f580f006`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2de0d30ada31da192f5016a4897bdd65bd1ab1a8a13dcbc1a8bf1e887eba8f`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 292.2 KB (292158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9327917e2dddfe4111d470e54a510bc92320cf661a5e14b0ac90c62acacad6e`  
		Last Modified: Mon, 13 Oct 2025 18:22:35 GMT  
		Size: 88.8 MB (88792191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f79809a704c146efe1be8d51acfefb2b2e6dda388827abaefe031b939c9ad6`  
		Last Modified: Mon, 13 Oct 2025 18:25:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:256819493c6091a222bf8c36dd55c79319b53b4cc12ee2f94e0cdd529114d6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecae0004e38fa4594cb7b6eca35badf1d3f6a56677ff480338debf7b94f3f684`

```dockerfile
```

-	Layers:
	-	`sha256:232e14f4435e3f1c1b5f5160efe15acce79221132dcaea6c2c3527e9f1002533`  
		Last Modified: Mon, 13 Oct 2025 20:24:09 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920683454befdb38609f2a6c548ce2d1dd25f863c384985ff2e1ac78b9e8f99f`  
		Last Modified: Mon, 13 Oct 2025 20:24:10 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json
