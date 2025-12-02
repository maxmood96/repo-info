## `golang:tip-alpine`

```console
$ docker pull golang@sha256:ca63a15ce2dd8eb0dbcaf25074bbf51902519d1408e3c453256538ae64dea261
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
$ docker pull golang@sha256:59dcf194bd7538d31c6aec0480460b354dc9bd62005891c63e76ee2d3db7f16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98207005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee547011d9f612e4d22b131d2c8554120ec9e71039429e6de21f589107ffb52`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 23:55:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Dec 2025 23:56:58 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:56:58 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:56:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:56:58 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:57:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:57:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76d0deee6b2a91d0284a950c6ca882aa183fac4870ab6e74a8295759bc88a9f`  
		Last Modified: Mon, 01 Dec 2025 23:57:22 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a76f01eed12068791b9d01e6e1fac5e71a0eed9d59aaeeeaac959b8cd0d16c`  
		Last Modified: Mon, 01 Dec 2025 23:57:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6444fda6b985ba43358959296837cff8a484b45b02c10f0ccfa1e2651cdc4876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8d0489b4ad949c590d62ddcc346c484678330423e4bd18133fab2b35618b84`

```dockerfile
```

-	Layers:
	-	`sha256:60bcf71854f5e9a2e04e730b41ab20c7de99dcd4d2bf14db1ef41c421effa083`  
		Last Modified: Tue, 02 Dec 2025 00:23:43 GMT  
		Size: 195.6 KB (195614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee8cf30708a880e4cc40f1b985687dff73420f89317804cae76cc32d1cc684b`  
		Last Modified: Tue, 02 Dec 2025 00:23:44 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8667c5b1ea57be1e4f768d157132249aba7ec4345bcf01704ac0e5a439c54fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94275010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5f557cb3347b972a92f7b99ba5f4a45bf45dc2adb483602a7a72551d431ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 23:56:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Dec 2025 23:58:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:58:54 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:58:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:58:54 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:58:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3142aaf2c5c77e93555d78240afd739c031059d190a777f6de66818cbeb8e1`  
		Last Modified: Mon, 01 Dec 2025 23:59:19 GMT  
		Size: 292.3 KB (292316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cef798cb03bb0097c86699403eb8a58ab2cf9b985080b34f19c3c37355503d`  
		Last Modified: Mon, 01 Dec 2025 23:59:35 GMT  
		Size: 90.5 MB (90478457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7726863e1f8c71657e679d8975850b6335c3b4e6073fb207fc55237af9eaf831`  
		Last Modified: Mon, 01 Dec 2025 23:59:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4f9b71290ba82e81482b46087c4f50d33af4e2843f3a17fd87b5a8dadbb9cf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a8790004116160891a8f55b96a00c4caa889e7a58dae7728855ebcb487e779`

```dockerfile
```

-	Layers:
	-	`sha256:57df9b2d916fb49accf88567de592f0e3021f97adf4bb899d5a30d223fb6c098`  
		Last Modified: Tue, 02 Dec 2025 00:23:47 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:655a56b64a3119285275e8bc57603d4538e9aebcfb671fdd3bd6c9dd607897e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93711263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5951044a82ed637171eefa8268898bb69507ae73e9ae210a5408bae97994becb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 23:59:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 00:02:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:02:22 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:02:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:02:22 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:02:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:02:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5644d5621e2354ac8ecbf708665df181d28705ec64d6b0513c21a4936507b40`  
		Last Modified: Tue, 02 Dec 2025 00:02:46 GMT  
		Size: 291.2 KB (291207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de79893e3709464b3e3e102757ce18967655159897e2b8696825bfaa394349f9`  
		Last Modified: Tue, 02 Dec 2025 00:02:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:09c0c77c9b6fbb54965266a965b3d240c6e814f2399d3f1fcab8b6f83291ec67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df532f26e2d7ee47236bb795a526b38be979f40ab293c99456846a3489937a61`

```dockerfile
```

-	Layers:
	-	`sha256:34a6e946526d521e138fb8ea4bb84d50d5d1f2e3397b31a612963bddc110f16f`  
		Last Modified: Tue, 02 Dec 2025 00:23:50 GMT  
		Size: 195.6 KB (195634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fa7d362420953a5f648bd9f57c322fe00109181ce862ffe7178eed9ffa5775`  
		Last Modified: Tue, 02 Dec 2025 00:23:51 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:df20dc47f155d05149879423deeea4ab150a46bb71f6e0db93119d486c9fd648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93643742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d701cef7656d92508fa5ccdd34d5c30d71e055739b91405d12f533c5deb6e5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:01:41 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:01:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:01:41 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:01:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:01:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c771bc89a44a04a0a1b23d3cf647d94eb70c9dec6c80b013048aadea0b685f2e`  
		Last Modified: Tue, 02 Dec 2025 00:02:04 GMT  
		Size: 294.1 KB (294108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e97f6ff525280b208c77082ded9603cb55d420b78300b8914bee1772480847`  
		Last Modified: Tue, 02 Dec 2025 00:02:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8b6a8fc6b68c3437c2e5fda2bee44c621ae3d2488fbe0b81c2c18065622732d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4e460d24d95f4470084fc2311e52198369cdc447712dfca9a572deca8d57f`

```dockerfile
```

-	Layers:
	-	`sha256:54a68796a0a89ec5a6567b1a30438e97c751ce08dcd0148ee6e3d0cb360e22c5`  
		Last Modified: Tue, 02 Dec 2025 00:23:55 GMT  
		Size: 195.7 KB (195670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71e7f9065303e92b700cde29f99e6522531e37b2154b53176afb23bf2213ee3`  
		Last Modified: Tue, 02 Dec 2025 00:23:55 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:4c171930466bf7d5a59b3ec6e6aea4a9195e4c8c72aabafceaf7f665f480cf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95939134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d940b0d6262ee491df90846e3f22485e7ca1173bb6964b05957a8bcc72b8bee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 23:58:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 00:00:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:00:37 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:00:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:00:37 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:00:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:00:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72da5a375f3d8489dbc71eb46bee0e36b3ea58825f47d7e54c12f0a544fb4e3`  
		Last Modified: Tue, 02 Dec 2025 00:01:00 GMT  
		Size: 291.6 KB (291640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e141ca9cc7d077e9c0894f7cb0e007cd1b68902d92e284cad49f898cc6053ce`  
		Last Modified: Tue, 02 Dec 2025 00:01:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6b5963c30f6a909507376d3d9e5175d5463892bbb49974962752e45e9c594370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecac1229ccbcff651f710ae9ff696f9268561b0187145b8f67536b7dad306b8`

```dockerfile
```

-	Layers:
	-	`sha256:6087d99d07198884928705b6f0abf56fadd92955ccffd0a21b02f075262e7ef2`  
		Last Modified: Tue, 02 Dec 2025 00:23:59 GMT  
		Size: 195.6 KB (195573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d569ba6f4dda8b81ca5a3b62df74ffeda4a59695456b8d4b275e72a7c8f3e10b`  
		Last Modified: Tue, 02 Dec 2025 00:24:00 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:8a3168247d6928be82610060561eee43475a533d92c2e132fb496e6ecfd95919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93099419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a67589f04fc0c3c54a0f7f03e6a7d28f970aa043ce79df5190f693d03afd35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:36 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:43:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:43:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c192b4221bdae7479c6a0a0cefbefa83b4b143b2a4b40e323ae02e100ce6102`  
		Last Modified: Mon, 24 Nov 2025 22:46:59 GMT  
		Size: 89.1 MB (89072428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96f85f10c579e3515aef85e4242cce954fc4198af1df0a2adb67e1a1229dd28`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d420a861887cd2ab0b0a749534546f1bdcae036758134a1e1cdac4713bc9165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a69ba61a4694ce542354767b29576c6670f0e9d43ba3e94cdd06f63c14638b7`

```dockerfile
```

-	Layers:
	-	`sha256:1badc52f16f92da332bd46df0d6fa19408693ddd6410d957b98fa51a31a82a33`  
		Last Modified: Tue, 25 Nov 2025 00:24:18 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f9c028adb500f8789cac3b879d94397754fc0ddcbfd2a63e17d912fb7ec6ad`  
		Last Modified: Tue, 25 Nov 2025 00:24:18 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:89ee7fa654e7aaba3761f29a71eda5b7e42e293c2541b3cc170bb87f8b22c095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93485658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c43e3df6c706bd2c2bc06baa6e33574b4f1af4e3ce68721dae2fc3adf3284a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOPATH=/go
# Tue, 25 Nov 2025 06:38:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 06:38:29 GMT
COPY /target/ / # buildkit
# Tue, 25 Nov 2025 07:20:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Nov 2025 07:20:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737de4a2a89a200a514c4bb9d33946647ec30322b982a3272843e60840a135c`  
		Last Modified: Tue, 25 Nov 2025 06:45:54 GMT  
		Size: 89.7 MB (89678738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c6b198d7ab1fcafec20f7a56dfed62dc07de66bc50d2dc83c90a2b97fa7c4a`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9c9393f6cf5ba4a74fe09030fbb9a473773a88c6ad451601bb66737db2f9ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1f625e14eb9b5d031f7aa0a317eea09fae59e954dc210e307f18b78f2979a`

```dockerfile
```

-	Layers:
	-	`sha256:2713188e5e934129b909cf0818dc4f63b7a411b95431cdbdc33229de22b850e3`  
		Last Modified: Tue, 25 Nov 2025 09:23:28 GMT  
		Size: 193.7 KB (193707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1692df96fdc1ecdfc72d431bedc6ec909d026edee14a0a0a99795b5ca33939fb`  
		Last Modified: Tue, 25 Nov 2025 09:23:29 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:c10574c882c8235b2bd9b904f1ba3675720de2a0d5110dd91ac6125c6084b4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94565505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750365b752e8e821592dc6aa69965161a0aa58c9187f85089cbf52df02589e93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:54 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:54 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94177cc1b10be488b5d187dad00f1ccc030bc5cd416e55c943d85498ded2fbfe`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 292.1 KB (292150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00d64c48f24f624221defe9715cae4847baad7ac3f98d927259b00270c75f2`  
		Last Modified: Tue, 25 Nov 2025 02:17:38 GMT  
		Size: 90.6 MB (90623953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5972f3f34169707e5c58e3df4a5be77c45f4684c08dbe468461feac27f0c83`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6c402ee5a1c6b60dcfc85399aa86c9a3df37ed4b47c1e2af670e740aaa5bcd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fc47251cfc4b5aeeacef43a99e06df0010b9576a7b65221cea24fefe33f`

```dockerfile
```

-	Layers:
	-	`sha256:db34393df4e0e3e8f4e877cd165c7cc140b859f820526916f640e03653a39fc8`  
		Last Modified: Tue, 25 Nov 2025 02:33:18 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f983bb0674d81d42917523e40310510dfbebf3db9c49680d3996002768ddd58`  
		Last Modified: Tue, 25 Nov 2025 00:24:22 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json
