## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:641362b69325d87285774b6a7a655e19c4918c30b6282803a81b4eac94879958
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
$ docker pull golang@sha256:33023b9f2da35ede48d20c7e67a7ffabd8cd3e4c5a197d5c139a7e66a7e35c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97699538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf6465b505b70c7b6ec2f9fa3902072db7b1333543b766a7191acea5ca96549`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:02:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:02:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:02:13 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:02:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:02:13 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58a24c73d541d76a6709289c0d860b1ca26270d2009b8463665438de608acbb`  
		Last Modified: Mon, 02 Mar 2026 22:04:42 GMT  
		Size: 291.2 KB (291159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2e1ac27e72a185b3548ee8e61bfb4220af9dcad181f3bf51c4e1ac38e34fef`  
		Last Modified: Mon, 02 Mar 2026 22:04:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7aca1ff83ebff6278a60e0e33a9d1b0ac16a2f12e54a2ef5b2ee463f2da22d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc97d44de234744a37c6491875c1651045602f8071b4cd794398c6011a82f130`

```dockerfile
```

-	Layers:
	-	`sha256:f63e4829b2e1f319b775fad00ad8d7d3e3ce2d7de9234a3188865a88f3b68a0d`  
		Last Modified: Mon, 02 Mar 2026 22:04:42 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca79361341efab5deea1224228ccf3674f46b9e14a154921f91035f1c757856b`  
		Last Modified: Mon, 02 Mar 2026 22:04:43 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:99fc8e39e29b7f5d6adf99a2f8428785267650ea3cb094fcd08d49cfed463927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93768123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729409308712e79e73d58104eb0f4e4923e63e7ef7a44d5fc12b602112f16b16`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:02:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:05:06 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:05:06 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:05:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:06 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:05:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:05:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89e9294f2fe9982d97db67e2309f6b384047b31e1691c93945443765f8f2536`  
		Last Modified: Mon, 02 Mar 2026 22:05:21 GMT  
		Size: 292.3 KB (292315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f75482abeb648b9189b3f4696db6444fed715bf37c369ca85b2202c497f7c6`  
		Last Modified: Mon, 02 Mar 2026 22:04:54 GMT  
		Size: 90.0 MB (89970604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75dc722329dfb083a59bf827e1428b53c6085e3c6bb417d368bcdfae62bce68`  
		Last Modified: Mon, 02 Mar 2026 22:05:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5de25515b96e7f4076d03812ff3d046376b95d6965468e2839abf738bb132d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81d85875f783d72c0d084b75a93f4dfb08f1dfeb700ccd964775e0de52b20a7`

```dockerfile
```

-	Layers:
	-	`sha256:67a55c0a261549d3f6461c0cfe0424b92bdee293384386a378ce49ac49bf2c19`  
		Last Modified: Mon, 02 Mar 2026 22:05:21 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:6a8662f0765d6fdb42903c9a3f1dd405bf5f41fa5d7ed5a1f3a47c149c3d4b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93211661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76e1fc0ab6db76ad36ab9f7f75ea627ddaa7f4026342770a85e0ebd6723193c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:01:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:24 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:24 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf21e549b0b77423b9908c1bdee75eeb9594dd69b2e608b505ba5d865fc653`  
		Last Modified: Mon, 02 Mar 2026 22:04:41 GMT  
		Size: 291.2 KB (291211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03b9335d95cac58de30af4485b43f787d240b693c234dbf5e6ab219c90bee0b`  
		Last Modified: Mon, 02 Mar 2026 22:04:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:38510836b1a90ce7ec1ad9976acb939844b01de26bc4d2b8d71e8a5b02a2ff44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b22158779c52124ffc36794007fb1168cad7249c473d358d84dff815d29fed`

```dockerfile
```

-	Layers:
	-	`sha256:48f662c69d558919bd9d95692d7bac4d35c4dbe38f61b12e3447d9bf29bba1ae`  
		Last Modified: Mon, 02 Mar 2026 22:04:41 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a5deb103f1dce7076f5ed8e375cf471a21862d73cdb9d3692674352be15319`  
		Last Modified: Mon, 02 Mar 2026 22:04:41 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1d411fb54c7b9a22c01ed0e2621e77a80f071fba7d541d673696d82262fad5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93160627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f4de123df8035cd28267e3ab96e9df2e5de1f2b183f43221605c70cf12bd9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:28:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:30:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:30:44 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:30:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:44 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:30:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:30:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad0a773235657abd10a30353af8b0bdb01ea722f2b47af2b86c171be1495169`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991311643d5ba1266ad32d242c21d958ba93238b33b79d32fc0b23bd2b25b23`  
		Last Modified: Tue, 24 Feb 2026 19:30:15 GMT  
		Size: 88.7 MB (88726849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab94d3b61e1e6553f2b2324bcc0b93c5306cb0af77306bf61feb57c304ed10ae`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:fda7fa675f3273e265339f1020c00663da8268e93740277bf80ff5d8f01fdc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39256656452eec356780f59953c802f48481f5dfeeaf957cf517019dcff74480`

```dockerfile
```

-	Layers:
	-	`sha256:32b3de27f0d5fa7e284e5fce8610dcd2fec04d30d2941471d935912a00123a4c`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4569e0d123cb1602564737c88e9a8acba7bff72e662300579ef9b976ab929c9f`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:e70b4e706450caf91295f22abce10b2d9ed5c7254b505105112c18c8d2d5af98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95366954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b349f1d3b04e94546bdb0f1731f5ab78b5ae365da079e4446f133f431e8c2a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:25:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:27:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:27:41 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:27:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:27:41 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:27:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:27:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8ddc8c775d999d76ce891fe814ab4cfd850ab9fe6e09a1e99a801abab1207`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 291.6 KB (291618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70dcda3c127f8506d59d712159bc64c0b0ee6293dc7af8e7cd42a7bdd642799`  
		Last Modified: Tue, 24 Feb 2026 19:27:40 GMT  
		Size: 91.5 MB (91454447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3892b86546fb7a9abe3f1ebcc7c6a8c7b6b984a5bb1e848c6bc976ebed2a19`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:93a149fb7e96746c510e9fe2675f6cf97890bda2ff79bc84afc059a572f1db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b626432f261b4726536c4f204da7a5d666f6e25440facde9d285de2a13c36e3`

```dockerfile
```

-	Layers:
	-	`sha256:716cb631043ee2f217acff8f7b5a58b10e6f820f1a7ae56176be1de752fee08a`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36702427ae38e83acfa22ff0d6317b95c62ffe5c0f6ce19ed0d5da404b8a4779`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:85ac5b0eb6640d21b94a7972e8bc824441372b31997fc3b812471fc480139097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94277005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9b1830404ce2e4ba933dd7e1af4dc02a4901f0b614df49586ebd339ce389f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 21:37:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:37:06 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:37:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:37:06 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:41:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:41:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc2604b78642af0499cb3a1b9f782035bf72390be0d0d2b55d3e7523ce711e9`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 294.6 KB (294647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf61cfa0cf71c339b4513ee7439845e2a12d7a655ba1ebeafcd94af8061e69a`  
		Last Modified: Tue, 24 Feb 2026 21:37:48 GMT  
		Size: 90.2 MB (90247905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0581bdfd8d1a16e74c110212fafdde2559cb088b56a5494b40ecdf72135cd7e`  
		Last Modified: Tue, 24 Feb 2026 21:41:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e7fb90b9012d6b857d11c6d36d2bb0543ff348554ae2472f06666e34cde69457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69d1b3ddbadb1b346f27eb1fa9c622ba1b648848c9edbe751769d9255837882`

```dockerfile
```

-	Layers:
	-	`sha256:c13f3f5cad53802374b31b3b0cdc09163f009471b55b6ebbed57d2cea6df6a41`  
		Last Modified: Tue, 24 Feb 2026 21:41:44 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeecb0a852adaf8f657728480561157841e4c96f9bbaeff7169d666abc4403b8`  
		Last Modified: Tue, 24 Feb 2026 21:41:43 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:f44a43945064931168297ae08b0cf0982b2b49f55df00eacde3118a091ec2656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94539283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3cd63be06cd6a077fbae1b2bbf96d5768f5871a5151869d4227d017a1ab7ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:48:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:48:19 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:31:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:31:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5c9add62f2c1974f9d8b2a5b72c3c47a21eb3a147c7469bf123bb66cc26173`  
		Last Modified: Tue, 24 Feb 2026 19:51:42 GMT  
		Size: 90.7 MB (90730204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af8c8ae14ec8504d79a2aeb77487c21b453b367885a96c39f3b5b583073ab7c`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7e8999ba28fac140818207a22034efe5324a05f083b35b3e1d5273364e5d991c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9548093b02d94771f26ef28d1e30e82d4510bfb557234248aa3685a083fbaa91`

```dockerfile
```

-	Layers:
	-	`sha256:06b92ac97499145591a7afb2fd7f18bf93f4532412053df625c1c556d07c8b0f`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4605a8ffc603ad0421d6962a5b4fbcf5f4c9b3515aea23b5969596d213b17f`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:1bc0143a8507d5b0ae1ea8add294f8609ef5c81d34a25633e1c5700971bf51aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96745302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba7c3c1a87d5c6f304476eb7ef53e73e44cfae24d1f3d695f08f68048bac460`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:03:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:03:58 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:03:58 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:03:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:03:58 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e56a450b30eff197b13b7291a8a1cd969e7af83b7e3ef9927079233b1f47b94`  
		Last Modified: Mon, 02 Mar 2026 22:04:27 GMT  
		Size: 292.2 KB (292151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e334960e45bee3fcfb13e5c10ba6f93651558e8f25f4ba27e72fcb67b99aed2`  
		Last Modified: Mon, 02 Mar 2026 22:04:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5c6245bc2032163ee80f7a45025cd2adf998696f1d39a8e85eca795453b322d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a849f28ff797ebc130ac7c8dfabc6515a5bb183e72d2966c56cd775330d20`

```dockerfile
```

-	Layers:
	-	`sha256:12509b8f08815c76874c9b315568a5d7c6acb62422ad06f8f063d343103dd563`  
		Last Modified: Mon, 02 Mar 2026 22:04:27 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9743bac18167798538ca889194599f7fbfb290f7b4dccf6d8e0abf6f449a94`  
		Last Modified: Mon, 02 Mar 2026 22:04:27 GMT  
		Size: 24.5 KB (24463 bytes)  
		MIME: application/vnd.in-toto+json
