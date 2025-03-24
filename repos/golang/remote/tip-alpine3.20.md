## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:2a400a675d53911b8815650181024876a154983a1874a7de6dd837716afdebbb
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

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:c3c7657901947f97d87973cbef34a65e1b0e141bdf5eeba94f4f8d9819f6e098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129943481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15c015cd3fbf420fef17c12bfce285f2299af56ba4a8a1abec6186928216e73`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da77bef60dac2e89bfdec07fb487581d2aacc1a3560726f48f7a5685145ed7c`  
		Last Modified: Mon, 24 Mar 2025 21:23:16 GMT  
		Size: 294.4 KB (294396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cbe769fc954b1a5756fdf48e31713555a112012d07425d7d4a076ea9376a7`  
		Last Modified: Mon, 24 Mar 2025 21:23:19 GMT  
		Size: 126.0 MB (126022030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cde66dd6bf6789db001d0e16fd17a0e480c0e72a8dbb03ce2a79ec334b8d86`  
		Last Modified: Mon, 24 Mar 2025 21:23:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:0402a5613e39475348df8b9239d93010e38ed94316ed56a51e75d742effcadd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c22ded0e3bd0aa366168f98195fc614b2ab0c75e9253f845cda6f636c66753`

```dockerfile
```

-	Layers:
	-	`sha256:3691f773722b0ca4679efcb5c0d939b6e08d3f915f74e85d1e49b08c83ea401c`  
		Last Modified: Mon, 24 Mar 2025 21:23:16 GMT  
		Size: 205.4 KB (205355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edca85fbf807f26cf99d757c148d9124f5b81cd578c762a8e6ab135315c37850`  
		Last Modified: Mon, 24 Mar 2025 21:23:16 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:169b831e290f183d8d34e11eda9fb14d947f718a03136de56c596018645da76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124950024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2db35ff60c95d425cf1dca447ef5e6d595934b9dd46c2d2b89866d0f3acf6d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e6a0579c5ff3ee75a0b9bbce7a3f1ed648ca9daffbf53e165b1b1a72b4c26b`  
		Last Modified: Mon, 24 Mar 2025 21:23:09 GMT  
		Size: 121.3 MB (121281502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be3fdfbbdcb7a4c21994e205befcbe61bace308431104022ca8342ae521fa29`  
		Last Modified: Mon, 24 Mar 2025 21:26:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:16c1c0b09f0c947ee288e130f58e57c111002f3ee1d7c094b2aec77ee317d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6faefb78c8031050706d2f719b4d0d2008323d8c02a3d6703f9795edfa54d86`

```dockerfile
```

-	Layers:
	-	`sha256:7f97889a49fffa2f61ff5738348e4021649f9b91284254efe5c1e8e8903ddc18`  
		Last Modified: Mon, 24 Mar 2025 21:26:20 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:56f0b11475bf4783cc5c85d004054262c8c8be05e560d7076552c0b17c29c445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124336212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14125da7d7e287d022d8284a924a08a8807299d9a79f60c1db99250eb4c1946`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353e9c70d02c05f5d0756f45338b0d2910b536c139fce40d68a3d97077441d9`  
		Last Modified: Mon, 24 Mar 2025 21:24:23 GMT  
		Size: 120.9 MB (120945332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d82c7928326ca4330b9b5db9b6f4ad6febfb98b72690424c7ac795010ab068`  
		Last Modified: Mon, 24 Mar 2025 21:35:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3b2b982bc6a6dd88c118f3e2fad665a9b34694a2e94f3e1d484a363941b9308f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a36d476dd007d796d3d8a98ff80fe93cc2a4d231dc6347d0c27a0c1886c8b20`

```dockerfile
```

-	Layers:
	-	`sha256:c6ded34d9a45aee1d531566370ffc7c1418af7c61e0b4ba578a7fe276acacc70`  
		Last Modified: Mon, 24 Mar 2025 21:35:45 GMT  
		Size: 205.3 KB (205335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c2144cb878b6d5a3f8934f18b93628f39fd5e74e02986e401a49d704616622`  
		Last Modified: Mon, 24 Mar 2025 21:35:45 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d322ab7d100f3bff35e0dce21039e5e0cad50195646d4e1eda09ef8975c75c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122948023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1e396a7bd64dc4c1da927980775ca9e7c3dec6d5b8faa33cdbab8bb38d449`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634366ca850b96a5c7a0780daec3499faf6933b86acc8a8e99b70a5264f8f00e`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 297.5 KB (297463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa27b15393e951766b04748acddefa2554a614c3407abc8145f05a37f7e1559`  
		Last Modified: Mon, 24 Mar 2025 21:24:41 GMT  
		Size: 118.6 MB (118559237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afefdda03d63cbbf56660fcfc9afe299ade3d01284e79b8907ae6da58a05a66`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8b594dc139b97bc743bf4f2315565626461af42b4ae8de7304a0aa59850f7175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7018494f95d39547fb7408acb8c7505fb55ba2d1d51ed98887024ea4ed427eb7`

```dockerfile
```

-	Layers:
	-	`sha256:a847920845f5f0e1077f17bece82a4858054aa040246bcc2c34dd5025992af09`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 205.4 KB (205387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34057a791440d4686d793450953643b9ec9616ca6f9ddd721dd0532c4508c3da`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:80640939903892579eb67cda6acf7edf89f603d8dafda35b210f6f60a782e340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127879276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f778ddbfdc03820a674499dca206b681f8342262fe5d6f84d857ae7a51468791`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7195bdcd802b00d11d7cc5fdae126c735fed6c3bca56b124235b0a53a0961f`  
		Last Modified: Mon, 24 Mar 2025 21:24:00 GMT  
		Size: 295.1 KB (295131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76390dce495fb7dc13ff79afd09a2f809cad266d649bc9c2cf3aae32aea2ff71`  
		Last Modified: Mon, 24 Mar 2025 21:23:39 GMT  
		Size: 124.1 MB (124112320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be35575b8eabb6ba8966e0ee7bf3b8076119a67d3cb9c08529638131c64b46`  
		Last Modified: Mon, 24 Mar 2025 21:24:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e3aaea0937dfec0c55f2dfe01ff915b2df80dd4512c8caace01e422cca7ef5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 KB (229779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b30fafa69aa57db3e640696fd627f04b20852d7f5941f71291a3aa4001df7f`

```dockerfile
```

-	Layers:
	-	`sha256:29c3b80e57abaea11d02c084d69f195ef8aff0590c958b0cf96354c944f49ae6`  
		Last Modified: Mon, 24 Mar 2025 21:24:00 GMT  
		Size: 205.3 KB (205300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4f6dfeb56fe774c954ef0c4c7afb1491d3b8a7094c39239ef723b199b58104`  
		Last Modified: Mon, 24 Mar 2025 21:24:00 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:8a8f338309d56d585b2031e635bf4742f9e40c08af80f2a3fb9718086cb524b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124711981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee0cee8b6e13591564f482f442eeabefbd76bc03c0cc76bb9547a87942b7c7b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15784993a892df626148136e939e65b594ed2f1456345704a3272ec8fd984c53`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1867a2d294df0d3b21b808b4672bced3956fb4c495003b07361f0a8e9cb5d1`  
		Last Modified: Mon, 24 Mar 2025 21:44:58 GMT  
		Size: 120.8 MB (120838244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88814ca4460780fd54e1486eddd49e9d19cca00bb18675ceff6ac32bb674a7f9`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:943270bdba253ce60046c388a201e86c562ca29b2197b63c4301c5e27daef94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ec36e32005c48522f9c86276db1ce35efda6ae6aa1727ee75c5f8b73508231`

```dockerfile
```

-	Layers:
	-	`sha256:49746601eb9cf1d593b634e7a4707362ac2ced2dfc514d43b90f3153e0816abc`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 203.5 KB (203466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24666dadcfc0426cceda200eb5cda0985fdf1875e4ea58227842cb649c587ef5`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:e2b945074ab4f3fea36b93d8b6b89fb50695c23bdad7fdcff4f7c9b1179ba38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124891677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3139e6da04b034dd28b92a6cd00da605c5dd52a377a6add1e82efdfd2afcd6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d1dcd6a0865fdc41b8f9b0f05194766b10c2f89e1bc97978e63dd59f41eaa6`  
		Last Modified: Mon, 24 Mar 2025 22:01:06 GMT  
		Size: 121.2 MB (121222842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954f38c1d59f208f851fc797ac07eb9298834055cd78027e807667099f909b`  
		Last Modified: Mon, 24 Mar 2025 22:38:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:1c419eeaa6437b58c70759d26b772069db8d076d01ae75d5d42b2502eabf7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 KB (227225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f13fd3d9f1b851c7221605081f6f5948d8bcdcdb825da2fb48df2ef1a26b79`

```dockerfile
```

-	Layers:
	-	`sha256:970f7203943466d00e960ff02dbbbe712548586f9cec7f57abadb7e6d4a6af21`  
		Last Modified: Mon, 24 Mar 2025 22:38:32 GMT  
		Size: 203.5 KB (203462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b53a06e0e1a53f6603b535e37ec403949a4147662586a7fd1238d8c8d8f587`  
		Last Modified: Mon, 24 Mar 2025 22:38:32 GMT  
		Size: 23.8 KB (23763 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:c210f407891d45b6148c93b6c9a4a0bce5bebecd7bd3b3c2c0a47da37d10363a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127042889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb925c56bf1bdff2758fa27cb374d6c7e110a56f192eea7388dacadeb7a67d1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f378f0ab9f92249cab05739adecf3318eef414f2bb034b8f1580eac04a7de99`  
		Last Modified: Mon, 24 Mar 2025 21:30:12 GMT  
		Size: 295.7 KB (295703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f92bbf60c027242fd3e59fa4d4252eab4d7c2b21b8d05ba9b89f6a7dbd625f3`  
		Last Modified: Mon, 24 Mar 2025 21:23:38 GMT  
		Size: 123.3 MB (123282906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436f54526eee2d471926fae980e25641bf1ec5ed010f92ff78bd58fc38302f5`  
		Last Modified: Mon, 24 Mar 2025 21:30:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:2eae4741804e4970fc3f2477f8236e210551e0d945f6a33496f026cf897d7cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 KB (227916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cf01cde96ffcdab33e7e3dec7a909efdacc4edded8e81a9c337f48b4d37960`

```dockerfile
```

-	Layers:
	-	`sha256:2dd3e30ab8f07075cf615ba517e08a788294435190605af851ece4cd38f78839`  
		Last Modified: Mon, 24 Mar 2025 21:30:11 GMT  
		Size: 203.4 KB (203404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f8115ca7d30344137e4852493238d6d33b14b701b1dd7f5cde320a55b4eddd`  
		Last Modified: Mon, 24 Mar 2025 21:30:11 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json
