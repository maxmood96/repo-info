## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:bbe9f1b0311d38dd7f34f85b1fb6f62d28428dfc6465b9dff1603dc560f9fd41
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
$ docker pull golang@sha256:16f147ebb60861900e6e03189d22b900841117930891e39f4cc648d4962bdacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97448304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57acc6c77b343edf8b2e47f60322e8a5ebe8d8900a93188ac86cf9c760b5b92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:05:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:07:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:47 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:47 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a0117187a3b1d2f6c56076ff2847c410a352e7e3acb538d19abfe0640be58`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 291.2 KB (291156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606b852e3c333533b6267cbada59c6fbc954cef2b3af5c4c84f2f9bd6ca56999`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 93.4 MB (93354538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b88caea71b17666e9f7995e07d2d72872e7c033c698893702826dd07d47c82`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3a335972aa6a5a8634f07fd7c3a3bfa0f10ccdfcc09b129b640203dde4b5fc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bc82862810cbb2d5215afe6b14e1acd3e5e207e461dd7102ba9d4f0a3acaf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ad538f0ec5dd2445d154d2ca61e918c9c697eddbea6a0ee321be36372c69108`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae883095ad31a0db444bd9582225d5d780c6cce767c17c01f89f7c4142fdaf28`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:ce3cfe00b8b87e4e5746de17454e450bd6037ddf2d6d55b726f808b8144ff2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93595606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6ae33d5da838123437f0d0448a452fad1a98e2c8fa3bdb1c2fbda07af5228a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 21:53:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 21:56:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 21:56:33 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 21:56:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 21:56:33 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 21:56:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 21:56:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faabb96d630e457558de78b68ac0f3f5aacd51e4e069d6afe06f032667c2166a`  
		Last Modified: Mon, 26 Jan 2026 21:56:47 GMT  
		Size: 292.3 KB (292322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4ad1d715926b64a8f9ca2f7e3d6d0a5b04fcb12082a02013bdd6dc9c89d61c`  
		Last Modified: Mon, 26 Jan 2026 21:56:24 GMT  
		Size: 89.8 MB (89799045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfb8773616f76173895fe5fc61aeaac996778f2226f8829056702f3ef032138`  
		Last Modified: Mon, 26 Jan 2026 21:56:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:db5914078cbb2ae608cee296df5fd33d6ca36248538e9ba03fa40f469f11dc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd2bf1297211b9e28bdd8eb8dd1a897d1bd95a1c9e896f0d539d571af18699`

```dockerfile
```

-	Layers:
	-	`sha256:e704143aaa51684d10c9bb4cc4950732d0740d3fe797b16d73f4ee24103359dc`  
		Last Modified: Mon, 26 Jan 2026 21:56:47 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:f0863aa40912eae2e071a2f2afc60a833c2177924d0f4995a4f95c8f7274e6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93041749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593f246344b28ecd10bc40a5e084304f7eaaf4533af5a58589cb95617885605b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:03:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 04:05:51 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 04:05:51 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 04:05:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:05:51 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 04:05:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 04:05:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be78f6b99340dddbdfccffb09a2fdea1e7bdb9a8706eb1f76c8c5a0698f0610`  
		Last Modified: Wed, 28 Jan 2026 04:06:08 GMT  
		Size: 291.2 KB (291201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205fc7a73de56b4f5ea25cad036ec0f33fb7b33229a77437a24f71a2e0db125`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 89.5 MB (89526761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b72c878c3f0350320fab0594e7778ec25547541fadd9e45a611bc1337289f9`  
		Last Modified: Wed, 28 Jan 2026 04:06:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2bbd1086b61b6ca939f156afadaed3973cd1d025e87a31f09e17c2680e2f33e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d16fafcec2e68eaf861de75c55f7ab585d7b39ed6d0b1736908075fdd47831`

```dockerfile
```

-	Layers:
	-	`sha256:63366b61679a2ad855ed7ee0731ecc19511d278e592186314393f076474a360b`  
		Last Modified: Wed, 28 Jan 2026 04:06:08 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c38b6cbbd8bab9fc8ac94dcecdb65355cbee8a16d9857bc0412ecece94f341b`  
		Last Modified: Wed, 28 Jan 2026 04:06:08 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d9cefebf44b0e8dc2b51a3526bdba259dee9a680d44f4617d2f028ff00820953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92851026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770a86ffa58d322ed066f151c54dfab61a6cccaf461b3be49951536a8b19303a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:32:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 04:34:21 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 04:34:21 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 04:34:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:34:21 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 04:34:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 04:34:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a51e77e12fc68dc25b08da383438c51b2a899889703461d5ad1bc3b6a13ec3`  
		Last Modified: Wed, 28 Jan 2026 04:34:38 GMT  
		Size: 294.1 KB (294093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3fde52f4a9ce3ba79f004ba1b1e261e66970dc6baaa4a0f9b9bee7c6d5ab5`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 88.4 MB (88417257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ebadee70a20da0807de6090f3ed183dd4ea70d3ad3df34c458a32e9b44e11e`  
		Last Modified: Wed, 28 Jan 2026 04:34:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:bddaadbc6a126d2a77897f3d06ee9a2345d9041e1a61f502dc3aa3422f69bc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f04719cdf6dcd77610c6047db27795489c5ed32dba7debc3b7532f5d056076`

```dockerfile
```

-	Layers:
	-	`sha256:a84046db62b5684cfec989291f6813e6eac49fba70bafe7bfe6d7be0de524223`  
		Last Modified: Wed, 28 Jan 2026 04:34:38 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fea8b296274cb79365ac32f529bbec4e6979f7b488afe716a0b7b096390daef9`  
		Last Modified: Wed, 28 Jan 2026 04:34:38 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:f208e02724664d4b20b00ca0ce986f7b2787952cd2cc498bf9ff3b4b6d357a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95350242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e98169a2d3b185701e67333087b024f243370b02771628177b52ca4df7b629`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:50:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 28 Jan 2026 03:50:24 GMT
ENV GOPATH=/go
# Wed, 28 Jan 2026 03:50:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:50:24 GMT
COPY /target/ / # buildkit
# Wed, 28 Jan 2026 03:50:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 28 Jan 2026 03:50:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa2b5e458308a10cd5429f154e9a7a7b710cc35cd19a12791bbd59150cc5fd0`  
		Last Modified: Wed, 28 Jan 2026 03:50:40 GMT  
		Size: 291.6 KB (291626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb24967b184a59692854afa79a294d0d5b0fa84b707a952b78449312c20956e`  
		Last Modified: Mon, 26 Jan 2026 22:04:59 GMT  
		Size: 91.4 MB (91437726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa369449a57c43e5667d6d24d82f737f9f6d239573fa3b93587942bc459f23d`  
		Last Modified: Wed, 28 Jan 2026 03:50:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:eef5e66430e67ee61aa140bf0a916c6842f07b26c5eacd181c20b93c7e56a2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09503a424d764fa0bf98130c15e21054bcae777cc01112f7a156cf2aecd4ea25`

```dockerfile
```

-	Layers:
	-	`sha256:ec3351b556c766b553df8c24a26555574f7e622b8d782d6be58cea825ea457fb`  
		Last Modified: Wed, 28 Jan 2026 03:50:40 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:932ba7fe35dc02ce6771da3ed479f8c53a7624663a449a5491c4fa799fd03737`  
		Last Modified: Wed, 28 Jan 2026 03:50:40 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:6db698f6e17f248d2e4292e407f2a6fa30df8bfe4ab2316c4ffb33c4da34b700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94077905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ab147a9c4c3d7dcef2312c96e80d0219396043e57145ace95933bd709f9c48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:40:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:34:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:34:17 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:40:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:40:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:06 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2557aad8b74dd54bbe1d3e83db11c2c0a23753c7fbd8d9d8e9290439c86b03b2`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 294.6 KB (294581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3fbdd047cc229947289d64050103b3f46ea0891f972e8e261f84917802eea`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 90.1 MB (90050925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86820cb770a7373ada56385e91308e5606b527b51c6abbd187183ce5327ad29`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5102d4c9242b8f9239b59df20fead1330e2b34a75cc14bab25a362eb5674a37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96116b20088d935477e9fcdd098f3309a0b910c7e77e0ed657d844066c2010f1`

```dockerfile
```

-	Layers:
	-	`sha256:6bf8cfad05246f8fd229d5f3e507a196f03c8c73079491a06ba0b81e559494a2`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd59bb6f0a38dc34570775f2c0a563e7bfd736fcd456f61c0c7c8276f93d3392`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:176fe7a1a6aed8aa382ed2c23359b26b8fe8a0e5047786a6ab1c408acc0941ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94391721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6568574b5618e1f4f132bf87c4f7545332356f095d95a0907ff76fb7db2d51c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOPATH=/go
# Tue, 27 Jan 2026 04:27:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 04:27:07 GMT
COPY /target/ / # buildkit
# Tue, 27 Jan 2026 05:52:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Jan 2026 05:52:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:12 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336390632e3dab506cd0230c48180b8fdc0e8dcf2f397506712faf9caae798e8`  
		Last Modified: Tue, 27 Jan 2026 04:34:16 GMT  
		Size: 90.6 MB (90584800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbe5d407cf8c06b2fda05295e281b8d17ecbbb03f5c1004f58de30ba25ebb12`  
		Last Modified: Tue, 27 Jan 2026 05:54:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b809730a83ed089f7e089c329e00fba6664bc85e8d0de2acf4ba389caecc0da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827e74253925c885b9a8c56c24104c95509d649ea09d7e09d1966a4f926cc5c4`

```dockerfile
```

-	Layers:
	-	`sha256:4bc139fbb45055abe9c41734d7d66445bf9a6d511913390fd370a45173b27f20`  
		Last Modified: Tue, 27 Jan 2026 05:54:07 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a463aabb6dcf6bcdf9c8d42043f55b02117f2e9b82048449673c0f4ee7d1c278`  
		Last Modified: Tue, 27 Jan 2026 05:54:06 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:00c9fb4e71cfbbe10cc145356ed5da12e3fc5e7c41ca1199e39aeec9aba3dce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96549572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d55a43f6f8146b8bbbe5ed341bfad447c160fb287390462792ef3e5d5d2b4d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:31:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:12:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:12:13 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:12:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:13 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:13:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:13:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4477625ae0958d0e9b2655402cac23110eb0328923e9ab75f1482f7e600bb6`  
		Last Modified: Thu, 15 Jan 2026 19:31:42 GMT  
		Size: 292.2 KB (292153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d1ebc1a42fde765fe01b70de439084ec52a344bfa25acb00b6d281dc10102e`  
		Last Modified: Mon, 26 Jan 2026 22:12:55 GMT  
		Size: 92.6 MB (92608018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77f1debb55d5f0d900955c2ffc9c999a449ed8900473f89080bf673ebfb919`  
		Last Modified: Mon, 26 Jan 2026 22:13:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:aea9ee02db25c606a8c317537fdae3c98946a575996b5f4516f51a1cb979dfdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2ff823ec15b09f046855cd269d337ecdf6d30cb4f81751c0b7c84034aba14`

```dockerfile
```

-	Layers:
	-	`sha256:8f8a4cce3cf53522b6a90bb8d71de30c2cec087d18ececd252bfbc5f4c68eb5a`  
		Last Modified: Mon, 26 Jan 2026 22:13:31 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c1c363e39aa2201c2496e7a984e64cf90dac5cfd77c58998582759d30a1002`  
		Last Modified: Mon, 26 Jan 2026 22:13:31 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
