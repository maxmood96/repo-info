## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:40eac4098652065ecf3ed6d1f45670cbe614fcc756b2099ef8f60cbfef9440d3
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
$ docker pull golang@sha256:7910ea69555038ed4fdd80dad5b29f01d077326e8639a7d54c51e6f588b264cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98678133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e2766fc1e62e49ad4d25492365affeb1ffe73ef79fcbd16da21aeb06591735`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 23:59:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:01:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:01:33 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:01:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:33 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:01:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:01:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d41c3ab079f5340df1e5e4fb596421733f9296d41e4926e474ab5fc80395ad`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 291.2 KB (291154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab04cb4a8e454fc7559b5ebb652cf17e60070b889bacf79f9339f14ac23b48e`  
		Last Modified: Tue, 14 Apr 2026 00:01:54 GMT  
		Size: 94.6 MB (94581946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0e6d4fce7e51d4c8017757579ba045175f1c033be6c22bdeb6bfd4fa3ec0ce`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:67a66c0302e5f7ff2c0a47824efc8a064325e0594b078043ddc5fa4cf80d1929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cd67164d969aeae55b2895bb506ae395743015294d1adf5f125b9b68846ae3`

```dockerfile
```

-	Layers:
	-	`sha256:4416d9dbdc201b02bb59105f80b890a89b924d43aefc2e0d9e1d1ae99d2699ed`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 195.0 KB (194984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d586fd4857ea015dd60fff1441268aa263e366c6307f98f432ec108811b1c7fa`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:37c9be6ccd9f3433630832f2cce056afe775ad57b948dfc52852e68bd9a5e875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94984365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d36055664f203378c6302e0113a701487c4fde87dec69208b69bc10c23199`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:04:36 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:07:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:07:24 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:07:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:07:24 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:07:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:07:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fba4fb29b14ba03caf9d3c3315f296373ba8dfc031a3af488d751397be5fc1e`  
		Last Modified: Tue, 14 Apr 2026 00:07:38 GMT  
		Size: 292.3 KB (292302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b805d56aa0bb12df6840037301a097e9d8c991b01763b634df28890710475e8`  
		Last Modified: Tue, 14 Apr 2026 00:07:36 GMT  
		Size: 91.2 MB (91186859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6537e54b8b1fc5767808a572520f68d4811c7407ac2d7288b536057741fd3ce4`  
		Last Modified: Tue, 14 Apr 2026 00:07:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e8b2e9829690c76cd26791dd6be42ace753dd02ad5fb4f660b3fc185eaf18733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47333eebe5bb9bdfea1b2d6fbc6d3d4baeb71fe244828701e90bed973589cfe`

```dockerfile
```

-	Layers:
	-	`sha256:ea46eb35af247da90b72caa2369cdda12fb21a72f85fa39caec220dde8374254`  
		Last Modified: Tue, 14 Apr 2026 00:07:39 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:7e102f63159d44b46b837760c2290e3b7d18a0453f18a6147017a4d2de6c031c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94407465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e8d33ebfcd759f28422d072b45ca2117ad2f14a342b77a8a05e6e6cd40fe75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:02:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:01:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:01:42 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:01:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:42 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:05:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:05:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beaa020a0214275ac2626a754279595a366dc16e073255f399d093a889a8542`  
		Last Modified: Tue, 14 Apr 2026 00:05:15 GMT  
		Size: 291.2 KB (291209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5edd4ff2dbd145648193fafaa3d5f04805713affd95a7e7d9d0029f6ec1270`  
		Last Modified: Tue, 14 Apr 2026 00:02:12 GMT  
		Size: 90.9 MB (90892470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24999fd0299e95442d4c54486b6fcf1ab9083cc7aa417fdd146804188eae3d5e`  
		Last Modified: Tue, 14 Apr 2026 00:05:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:03b1575d526edee7a343432a1cb9cc5ebb380c649f56b6ff67931046089320f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624f8cb4cca258f80d21da90b7fef5f368520adfff2cc1437f3ab5dcd21b999e`

```dockerfile
```

-	Layers:
	-	`sha256:1791d5accc7a17917a6947875d5ea976a6cbf16cd44afd3e8d0fce1120afce38`  
		Last Modified: Tue, 14 Apr 2026 00:05:15 GMT  
		Size: 195.0 KB (194988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1de5ba6f1107297f3cc81fd55357a269a30889607c8f48b7599585b5c279eae9`  
		Last Modified: Tue, 14 Apr 2026 00:05:15 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:05c96ffee77dc9deb392f96f1e870a3507e4588449c8de9de9ad8288fbed9df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94134669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ba027bcb1a2d6a2b8beb02162f707314dd94f9c6dba17890f236909fe69849`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:01:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:02:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:02:49 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:02:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:49 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:02:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:02:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58827dd5b19b63e0ecc9236d338bd8cb955a08685bfebeaf879b643b5c5192d2`  
		Last Modified: Tue, 14 Apr 2026 00:03:06 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ee12e748379dfc7e49600a21d46479ed1f62dbf74c0006b5ec77222dadb`  
		Last Modified: Tue, 14 Apr 2026 00:03:08 GMT  
		Size: 89.7 MB (89700892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca484d49ac1466f323c2adb797b70f7bc8bd0a793de7d45625d88ef46939de8`  
		Last Modified: Tue, 14 Apr 2026 00:03:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f4fc7fe410b214a1ab0c0d9a1db7622562e70164df3537a2dd957fe5eeca699b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a65b0c233017464a5aab9af9a1d066167f28ab3111b2cb271f65c277f5ab26a`

```dockerfile
```

-	Layers:
	-	`sha256:503b42585c10132e28a17e0214d82005f6f0a99611481f83ebf88803ea30cb2f`  
		Last Modified: Tue, 14 Apr 2026 00:03:06 GMT  
		Size: 195.0 KB (195016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b360a1cb2bab75bc599be817433246598d940a2ed104874e278c4be204b0d6a`  
		Last Modified: Tue, 14 Apr 2026 00:03:06 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:0ac9754e6a554531adc84990feea73ecb8946917deecb3466c0568b72a5989e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96533772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31c85267b80bfec31c6e0f5bb7618b6068d57e410e1c14ef049ce79692f76b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:27:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:29:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:29:15 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:29:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:29:15 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:29:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:29:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78704937db5725a398c40db3b03d1411a8b5771f86aee3327c7a0241a8665a87`  
		Last Modified: Tue, 14 Apr 2026 00:29:31 GMT  
		Size: 291.6 KB (291624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5425bebab36322e26303eb33424df1802209b7a6b3dc6b986570aca912bfd`  
		Last Modified: Tue, 14 Apr 2026 00:29:28 GMT  
		Size: 92.6 MB (92621258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b0048a1616fca525730f7e4e6561881af5ad4f001955bd6078f26d77ad6147`  
		Last Modified: Tue, 14 Apr 2026 00:29:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:64d14504164db31635f5cfcab83bd787e8ad64cba8d37ab777f96b45b6f32fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40a44806ef600aa0e2e42e5518c214fbcafd9fd814965a602c511ecba42b827`

```dockerfile
```

-	Layers:
	-	`sha256:62a51660a0d529aba8981937d5e8976b1e90612a577f9611f7cde87a6fd2c528`  
		Last Modified: Tue, 14 Apr 2026 00:29:31 GMT  
		Size: 195.0 KB (194953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e5caecadd2b6eeca3d0ec8e218c6cd59cc74f28d063c480441cf035acdfb3d`  
		Last Modified: Tue, 14 Apr 2026 00:29:31 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:8a3962f53ca289d7e37c9737f76bd7d6b43a469fc78015ab2976cd2a59bb69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95374253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6b7077b10ac4be108889f98fa067dbb4c94f0c9e644b8e531eee98bf9a23f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:28:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:06:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:06:08 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:10:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:11:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e1ebafd39830591510ded21f3f10c22801e3e344d366979450ab6f748be747`  
		Last Modified: Tue, 07 Apr 2026 21:29:10 GMT  
		Size: 294.6 KB (294576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0175a2939aed372a8574a3f30ca86be23817fbc044f643da506137d0f0ef397`  
		Last Modified: Tue, 14 Apr 2026 00:07:09 GMT  
		Size: 91.3 MB (91345222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017d6f0ce725090487940411ece9030ab783d866629b23234f73250649f6eb7d`  
		Last Modified: Tue, 14 Apr 2026 00:11:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2ef05bbcd0e82c6ad99a2298f534c692df7dd24742424f3b067d9696f84606e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d136ef82741318aadfde92410a3b2fc3463f74264e9e5149e767aa1308db0875`

```dockerfile
```

-	Layers:
	-	`sha256:0dc338220b0ce7011ce765fc7cbaa781a14266cd40c3ec5db8005c61abf6809b`  
		Last Modified: Tue, 14 Apr 2026 00:11:18 GMT  
		Size: 193.1 KB (193071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6125897d450792c93e3fa9d4355533e4f90b81025d99f2392a90e4eb2d01add`  
		Last Modified: Tue, 14 Apr 2026 00:11:18 GMT  
		Size: 24.3 KB (24337 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:1776eda487025a03f8ae9ffb7e5b3e7e4d80f61d63bc24185026127acf5eb8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94978185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6ed5a04942b0725be74c59e642f67857bc3dc47042c0b74c9b6ff294d22001`
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
# Sat, 11 Apr 2026 05:51:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 11 Apr 2026 05:51:51 GMT
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
	-	`sha256:b8929825aafb1a4d74b71f3e7ced0899ed99cb315069c41e05706547a7e40bb5`  
		Last Modified: Sat, 11 Apr 2026 05:53:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:32d03ad7b80f604d4f5243c9a9b66aa07c819a7b1bd06437148b966b4ef004cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c22a22cfa978c4703cd810040e265d44728fa18f34b33df88dd01a751bc232`

```dockerfile
```

-	Layers:
	-	`sha256:4c8db77eddfb22cc5e846f04b0362a621a6604c79a6429fe940f5eab94ce28ee`  
		Last Modified: Sat, 11 Apr 2026 05:53:06 GMT  
		Size: 193.1 KB (193067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1787aec60faef63fce7c249b600fddc4d85397a7bc302b3f3ceba63476f41430`  
		Last Modified: Sat, 11 Apr 2026 05:53:05 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:5856edea1b8c0a43e746a07cb66262766d25149cbbb0d01b63526611150db2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97720932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0174d13156f9e13d787d46bbb50bb35627cd22419259d93e6e3d12dfea248f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:22:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:26:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:26:50 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:26:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:26:50 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:26:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:26:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0559230bb041f05f42d3054e6c9126e6ad9c9580e7fc9bc739bb1a5f80acd`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 292.1 KB (292150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5aaa70187b5fa60b40f4f6aa959f778263834bd8f55472a34e3a940460eef6`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 93.8 MB (93778190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fbbe191b9852366a821b0f1008c57263a90f76c9f3f3d7ee2420fd01fd2546`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:78f8ecb07ab5f6b5b29e934c2ce165af80e4a46298a2d75d99ee27eaad9d66d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bed4d4f33b1f1aca699a7a1cc02f49b2df5dae63875a5e20db21082bd9cbb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f31c386f76c38de0a1dc680dee6328375df5d6661ac371c7e4baa3b2e1bfdc6c`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 193.0 KB (193033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5636ff544be7e6be615772963fc785de7e3b9bbc600ea68a41c9ad00746bf4`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 24.3 KB (24291 bytes)  
		MIME: application/vnd.in-toto+json
