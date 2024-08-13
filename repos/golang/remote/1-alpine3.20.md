## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:c744a197f23265cdd2f8a84c6f971a54ba5680b1fbe3394e39e39aca50000801
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

### `golang:1-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:ce1e987ea7759217351b74977a384cea8f44631f1c1add04d1703f13dd3ee850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77879252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c638dc5c33aa3a79896e3bb834515c99fe06396be96b7ecfeacbdb0560f165`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c27f9ec405fa049808e1419841775d2c973614041a03a8f3e6a2e85a297bde3`  
		Last Modified: Tue, 13 Aug 2024 20:02:20 GMT  
		Size: 290.9 KB (290884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b14fb4020d7e427735797bf663a02a5a028e40fae0f8993ed5dfe75f15417a`  
		Last Modified: Tue, 13 Aug 2024 20:02:18 GMT  
		Size: 74.0 MB (73965318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af28e06659b9d44e2f2f8b0e08b6a6bf1314d49a058037ffed2228ceaa8f10e`  
		Last Modified: Tue, 13 Aug 2024 20:02:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:0df891360a75f232c174975ce5f798a78ab5441c38889f188fac439948993d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 KB (232224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf479ac01ceed33ee4af7ef6111aed3b38932c123ee6197a65ea7677bc1a6d3c`

```dockerfile
```

-	Layers:
	-	`sha256:dee7005ec8a33a9f8f848792a6095e4af5af52c3e4c7aef4a68f4ba76158946c`  
		Last Modified: Tue, 13 Aug 2024 20:02:20 GMT  
		Size: 206.4 KB (206381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8415cd527fb64f9577951b1f77f14dfaa04a977b9fd767ea56151d1d79bde118`  
		Last Modified: Tue, 13 Aug 2024 20:02:19 GMT  
		Size: 25.8 KB (25843 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:149db0b60cd012d095f2b081a8579e9dc21f565bc71a7fec58312bf98c04dbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75784538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3149dc36c8808d49c465829fa5383410b5a1cc3d87259b6c127e5b72c7a477ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccab56a7828fccbfbf3c5386b666669245e0d8f93e53acce7ed8222093ae62a`  
		Last Modified: Tue, 06 Aug 2024 23:54:15 GMT  
		Size: 291.8 KB (291782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2264fd077e48bbe464da15268c0dc5d530f2daf4be4ca5923887f3657309c3`  
		Last Modified: Tue, 13 Aug 2024 20:04:23 GMT  
		Size: 72.1 MB (72127409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb51110e4d7abe6af8888f5b62192f97b10b4454badd1ccf2f428a09759f2d9`  
		Last Modified: Tue, 13 Aug 2024 20:04:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:661771ecf5178af9a0a7c99f6e071c3eb26065e81e20226e13e84e282fba745f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07819b2c346b82bb22e01bc2ac3b53a77c992539d04f681f67a00f38e24e718e`

```dockerfile
```

-	Layers:
	-	`sha256:f2dfeebabdd2b4e7a572c1113971d4624c35e7a2216c969d16c8aaab34a32202`  
		Last Modified: Tue, 13 Aug 2024 20:04:08 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:874f8b6f93cea528399301d710daeae4224bc2584ca45ea21c56a9f1489cc35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71115064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68645adf3d36c78ee568ba06fb250ff53af1d48dffcc3fc5f9824496abe786cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7318d3e5485ead98a8a7ffd1815df0d57c2d4e91ee5f14b79d688de1ab2cd`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 291.0 KB (290953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38353948ef7c4a85c3e42510197b5f321621d39f3094140f1496e3ba11d3156a`  
		Last Modified: Wed, 07 Aug 2024 00:08:57 GMT  
		Size: 67.7 MB (67728993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1e91c8c77a2673696ef7af8b778c14360bd4f987ac60f54ab9ed14d3768e1b`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3bc6b10f831e2105a3cfe5021e79a60d5eb2a04b759c06fe3069421f9c79dbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 KB (231981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d588250d03566ebd834d8d033e49989014fcd94fd9acc98d4913fe4699f31100`

```dockerfile
```

-	Layers:
	-	`sha256:a46ecc0fe3d5fe540f89a77c5672da2a5e75b36ca3ac952ffe6d13bbdb9d5fb7`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 206.0 KB (206010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbe652af751ee050a0383f4b83fb24ca2e1698e5927ad8a8ee385a341c35e5f9`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:22baacd172190c44b1e3570ef5dbe7193bdfa5e67d7cccd4fef47b7d474d84d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74988520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c7c392a1713c3d9e157ffb16530b5c0840987b56155cfad4fa3817d770dbe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171883aaf475f5dea5723bb43248d9cf3f3c3a7cf5927947a8bed4836bbccb62`  
		Last Modified: Tue, 06 Aug 2024 22:57:38 GMT  
		Size: 293.5 KB (293514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f9ed64c24993ada6c5d1b00ea7fbf5720c6cc30c9ae14d18134989fa7a08a7`  
		Last Modified: Tue, 13 Aug 2024 21:36:27 GMT  
		Size: 70.6 MB (70607916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e46708225bef299c0b34f0d1dead81d0c64ceefc65c63aa2be72a6d81574100`  
		Last Modified: Tue, 13 Aug 2024 21:37:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:da9e21eb389fdf9f2eab599d305f809a4c2108cbf91ee357e54a2d5bf3489f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 KB (232676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a2a378be109d6228faec5476a19787fd63b799003b344945784d837519bf7`

```dockerfile
```

-	Layers:
	-	`sha256:adb0adb8a913de3ad63d1f35dbf9815337f4b5eb299232890fd5b4def15e307c`  
		Last Modified: Tue, 13 Aug 2024 21:37:51 GMT  
		Size: 206.5 KB (206485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53cf207d563ec9058f56ea5adad05c43e5a723e3c039945b6c522183d49f477c`  
		Last Modified: Tue, 13 Aug 2024 21:37:51 GMT  
		Size: 26.2 KB (26191 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:d4c415dbaa973e539975e87fc2e939a37a6a50384daefe2f4f81c89193655f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75616229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57f269701790a8f7050542d5ff133b9a2386aa42923839731f9a955db83a8f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18225e14f52416ecea1dafd5c1c82973998f0f8301caadfb1bfcde61c81587e9`  
		Last Modified: Tue, 13 Aug 2024 20:02:36 GMT  
		Size: 291.4 KB (291367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a02128519d4902024135fc03b12145f389fd4b2b393eb6499f6f10486bc83`  
		Last Modified: Tue, 13 Aug 2024 20:02:22 GMT  
		Size: 71.9 MB (71856633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfe0f2dbd453270e017a67b9a96e6e61816322c63d576715363ca54255052`  
		Last Modified: Tue, 13 Aug 2024 20:02:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:1ed38f72e2ca20ed84691d20f401eca2aa0e8c047ae6f05500d70d5178f1733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 KB (232090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972b0f9c7ad122b518748cf236821b16205822c4b0688f74839d3b2ad2d10bef`

```dockerfile
```

-	Layers:
	-	`sha256:82530b0d835a306cdd12876a32618784a78a839faf34e832200e61ac64cd2ce0`  
		Last Modified: Tue, 13 Aug 2024 20:02:36 GMT  
		Size: 206.3 KB (206300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d8be65f84e00bb39c890476f8dbed3b22f00b08b939e7e0fff93676a1696629`  
		Last Modified: Tue, 13 Aug 2024 20:02:36 GMT  
		Size: 25.8 KB (25790 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:86181d26c58a80f5b533a0313b488c7fef5db9fc71697a30ccae14c77e66d6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70319628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd2ef13e06f69e7643732ca1e79526faf31e1b500b5e5c053c18e7cebd4cf83`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3799a78dfbed4f51d46b0331c523ca613f2dab716b4caeac0e3c3fc3a052197`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 294.0 KB (294033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa907a73ecb9721e6fd07eeff45b3daafd73705b1b26a4ab050075d2da72289`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 66.5 MB (66453881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3880e24cd21f53fd75298cf317970da7e553a2560ba8a3ef4724e2cee96c8971`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f7d6bfbde896280794546e2b91b485751b5c1ab7deb7f403086f6cee2229f42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db8db333a6f2d0888d1019cda6f6490579f2a61b34c6ec67119903320c0c402`

```dockerfile
```

-	Layers:
	-	`sha256:22d88ad523e95644256c4335009ed7601f3f1d17d5c5156508c8e55cd5680374`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 204.1 KB (204114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9e0578ac00706f004ddcddaa60d4859aa5d92a1c14149d562fa183be16ada8a`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 25.9 KB (25909 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:331e46874d5d49ea0d7dc94f7aa40e892b49f0d811487d6499ecd9b512f20a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74831214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5812f0b6d6dc29acafdfab755f7f5fc4f7a52d317b84ab1c28c794f926852ead`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a571abf33b31d34423d7fdec7f124b736d3b8c4bf672ec686abf087f11f88a`  
		Last Modified: Tue, 06 Aug 2024 23:01:07 GMT  
		Size: 291.7 KB (291678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c65b2c6673943bb3284431e3fcb32e4d0bdf1b157bf0552aefc2edff1c8be1`  
		Last Modified: Tue, 13 Aug 2024 20:15:28 GMT  
		Size: 71.2 MB (71168705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fe7a0d04a78b5333266ca5454ec9ab44ce1e290366d9fade5e98f5cee451f5`  
		Last Modified: Tue, 13 Aug 2024 20:15:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b60daa5c9ab03179ff1c0a0df5b9de240dc228e77b607c3b0f10e628e070021f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139eb0ffe4737337c027f09904549be8b239e76007588690ca458acc421fbf50`

```dockerfile
```

-	Layers:
	-	`sha256:9436dcce2176dc02ac491924ab4019837c940887c28d3f4883a6a7758f5b34a4`  
		Last Modified: Tue, 13 Aug 2024 20:15:19 GMT  
		Size: 204.5 KB (204517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195a4c07670457b0c447af2a15215fe3289b3dde6f122c11b274ba36746ff3db`  
		Last Modified: Tue, 13 Aug 2024 20:15:19 GMT  
		Size: 25.9 KB (25908 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:bf5efee4dafab3f3b61fd1b29366b678707df5fa32e40ca98a6013cae7ff6fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5e008b3c841c733b8d74d88ca77777bd021e0b3ba569e93167f771a73142ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c54ba5fba90bd52699c553f5c39c0b0ea45ac64b4d9ca09afb762001ab7bb6`  
		Last Modified: Wed, 07 Aug 2024 02:05:20 GMT  
		Size: 291.9 KB (291897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4f522c886389638258537d7ed45e62dbad030e5ed340cd291df30569fc9288`  
		Last Modified: Wed, 07 Aug 2024 01:54:06 GMT  
		Size: 68.4 MB (68420968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb91573b6ad53e5d8adc574aa13f3ecfdddb6225be1b5de558a4c4a087b2f23`  
		Last Modified: Wed, 07 Aug 2024 02:05:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:4e88e35c00f915b78862e861448aefef3c39d295f5418b0c951c030bdaed544e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c1cf72be02cc8439ffec7e7a44bacebd0da37eb52925d9e55dc9c8ec9a9210`

```dockerfile
```

-	Layers:
	-	`sha256:a6ca0bc3ac7fbb71bd07062cd527afcdfbc4dfe63d2e964dc61c6921dfba1f55`  
		Last Modified: Wed, 07 Aug 2024 02:05:20 GMT  
		Size: 204.0 KB (204022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3824dad8b429a32bd0b707ae9d3e3af33d40a18e27c0838abce1232e35b85188`  
		Last Modified: Wed, 07 Aug 2024 02:05:20 GMT  
		Size: 25.8 KB (25843 bytes)  
		MIME: application/vnd.in-toto+json
