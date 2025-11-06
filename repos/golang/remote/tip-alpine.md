## `golang:tip-alpine`

```console
$ docker pull golang@sha256:1fca5370dc9c60bc35cf98ddff2200aa3a9490f775c1baf59f3f75d0b30a21c5
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
$ docker pull golang@sha256:bf5183b87b2aaa101c891f20807e88b6d8e75b84f0012351f12fd7b2aa97fbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95720433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc0d00baae56b34555bd059386c2e646fa9d379a33987a67703404b348688a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:10:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:12:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:44 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:44 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:12:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:12:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe566dd680e32f6abe466be233c6c2307949e21dc3c58edf1283bc0ffe25182`  
		Last Modified: Wed, 05 Nov 2025 21:13:06 GMT  
		Size: 291.2 KB (291155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2585e489df1dd8b8e8ac0b521f0fc78bcf765b672ba54091dcb4fc74c26cf949`  
		Last Modified: Wed, 05 Nov 2025 21:13:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ed3aff7cf8e2aa5689104e62d9cd452762383a75f075263977ce71b591e1d089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd66455ad132353dbd1692ff997d70017273d5de2830cea59258735262d28be`

```dockerfile
```

-	Layers:
	-	`sha256:8700127bd896659e1320651ca2e15d369a93a41a26fd2275618811e3bd2e6b72`  
		Last Modified: Thu, 06 Nov 2025 00:25:08 GMT  
		Size: 195.6 KB (195612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edff98fb6ed6219586fa31917d1141d60ed4f69f99ccb7229816263491e9637e`  
		Last Modified: Thu, 06 Nov 2025 00:25:08 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:e6ad16e1a0d460230fb2d44d2f2cf6f6e75c767351478158fbc2d2f37ca5bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91861151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43db007b4b2e7fe7f55592ee75f3d6dd7c9fe0f924bdc747dd5feae0ff6ac8b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:12:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:15:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:15:22 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:15:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:15:22 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:15:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:15:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25b9fdf7e0e6a3191398141a8420d4d141eaaeeb6e2029bc83f5c4a96190f16`  
		Last Modified: Wed, 05 Nov 2025 21:15:46 GMT  
		Size: 292.3 KB (292321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518140b1232c759e1bbff002fa828b3b3a5b3d09a55146300b06356a080e134`  
		Last Modified: Mon, 03 Nov 2025 18:08:08 GMT  
		Size: 88.1 MB (88064592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c8a4a7dd633b6614c7d8d78f4eb35fdfcd6b4bcef3b2a08523a9c770650057`  
		Last Modified: Wed, 05 Nov 2025 21:15:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:886f8b493e2d6cb77e11b47e4f0e9cba6f712bfe416d7efe9f4fc02dc10b3afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f163499a69f7223af367b23c50478c35f9543450284c5b08dad81a781407d2e`

```dockerfile
```

-	Layers:
	-	`sha256:ee631494963ef00e500b9941c33e521e98dc5672dfd47bc538996275a5790de6`  
		Last Modified: Thu, 06 Nov 2025 00:25:12 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:55565f04b33638009041edcf2d5c46883aaf04a96c6e9c142fc3c68a4fe97a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91319603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ebccb2ea37f92fd89312c222fa4b967374224e7b336ceec084741b7de767d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:09:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:12:00 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:00 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:00 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:12:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:12:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89905c84ebce06a1c76599cfb04d36bc55756647766c066b1b8bff22ab132b6b`  
		Last Modified: Wed, 05 Nov 2025 21:12:25 GMT  
		Size: 291.2 KB (291210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e0430e906cb419cbda2fd21c65fecaaa3ea6c25a47ea01dcf40105fe2f2d2`  
		Last Modified: Wed, 05 Nov 2025 21:12:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d10460efe87f85bc1f07979a969c34003063b9d1fcaca8123b1b79f544a09e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68cb921b4d86ee05a80bf822299002ef3b820a4057f0707d7bec2b158e12c84`

```dockerfile
```

-	Layers:
	-	`sha256:00bad73d4e8883f1e5fc0666e313741be8a70f66a841749c8c93fd909a8acb5a`  
		Last Modified: Thu, 06 Nov 2025 00:25:15 GMT  
		Size: 195.6 KB (195632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1340d94c4158e2bc44bb21a18395a96e82a0f32139eabd13ea6c124e1d270a32`  
		Last Modified: Thu, 06 Nov 2025 00:25:18 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:75088d1f2a79e7f5b0092d4e0add69de3bdac0a6f289f2396e04c189f2d6d4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91310919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c8715babbe131d8ad8817d36558d89f11ce6eeb87b56c567b49118e95250c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:11:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:12:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:57 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:57 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:13:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:13:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f637e4090bf812ec6d0f061b0f0f6f72edcaa414892ef902d9268e5033c16a16`  
		Last Modified: Wed, 05 Nov 2025 21:13:18 GMT  
		Size: 294.1 KB (294121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49166298bd3a0e50e95901f29d771814c8c02a88e53a27df017fecb63a21692`  
		Last Modified: Wed, 05 Nov 2025 21:13:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f338205ed37109ca242c26c7eb5f1bd70cc4e756de8afca9354eb2e417992fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757a8008f430e7067a58a633f7fee28ca576f302f1d89714b594d1976abf3027`

```dockerfile
```

-	Layers:
	-	`sha256:c18463f29c2462485216fa197d05e5e27a8e4ecd6e131e97e5ea021cb741775d`  
		Last Modified: Thu, 06 Nov 2025 00:25:21 GMT  
		Size: 195.7 KB (195668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de2cef6b1870d0d43c02f6e684b5f6d786e0ec576cc5112b24ae047af840b99`  
		Last Modified: Thu, 06 Nov 2025 00:25:22 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:16f5de4408af3d54dae7e18c5ce334f73724222deb4c5bded7688f69ae9ded44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93523749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a67cb045391694b8cab59d5a4455df957db9e298b90861c54514564f4be35b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:11:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:13:05 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:13:05 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:13:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:13:05 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:13:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:13:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd4d0a54f2c4b0761c7b224b8b23e6bcdba43a55d933622589da524f08d5e8e`  
		Last Modified: Wed, 05 Nov 2025 21:13:25 GMT  
		Size: 291.6 KB (291632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8057ce024163dfe9e87a3179b6cc00d4e6a36dd6ea54e1165466c61bca9af82`  
		Last Modified: Wed, 05 Nov 2025 21:13:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:22fed35a6aecaf75792c3edef4a3409a93f4e14d9816420e88d9cd7705ee1050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89016ae5ca4ee39863141257b27d47da5d5f4bd371ce3597cb99e999604e6c73`

```dockerfile
```

-	Layers:
	-	`sha256:9eb95fd7436d22a60865909af5f074ce278a54f88c693cf7446c8d17cffa4229`  
		Last Modified: Thu, 06 Nov 2025 00:25:25 GMT  
		Size: 195.6 KB (195571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9f3fc462397aa12b47460e405e21b697c0cf574b449e5aa9f24752a951f827`  
		Last Modified: Thu, 06 Nov 2025 00:25:26 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:5fdc2c9ecaf01c714d1c52a856207ad940a8531edb7fc58dffaefc2c41b24140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92318849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54e5299bb7dc661508ae18ba12d640099b68c0810883852d616f1743717caa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:17:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:18:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:18:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c8bd62217b855f213063830cb5c2b3ccc4717b8ba91afea33b4f12c5e23dcc`  
		Last Modified: Mon, 03 Nov 2025 18:18:26 GMT  
		Size: 294.6 KB (294587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceec0e4d5de5dea09954f1a27c8249b0a35d8d279f74fc99310146c6bcff3247`  
		Last Modified: Mon, 03 Nov 2025 18:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a9d805a9914cf6749bc4bd4cd9c67af15d5e9419d51e35a7f7726c7f6130e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fe2d7d93a230913fe556dd11d35c4bcb41bb73dcc10659a91f722938391b54`

```dockerfile
```

-	Layers:
	-	`sha256:f715830bf038c894892ba4d43ca86c5b9828394955c136c0833747e56dcc1dc6`  
		Last Modified: Thu, 06 Nov 2025 00:25:30 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f2fc07e3ca7851c406df25bbcd8d4b72b991b2e8a6ec4ef9e562e0dd310331c`  
		Last Modified: Thu, 06 Nov 2025 00:25:30 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:8aa91784989093b0769adc0d6ebaedfc552abbc40240199053f39e0b9ca7d166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92603327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8028cbd3d0c27838a7b86746dabbfb030aa63a2dffa25b0e5433a29161c33649`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 21:01:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 19:28:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 19:28:57 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 20:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 20:10:31 GMT
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
	-	`sha256:568766c8d70cce8f34aaf3713ad1c1267acad6ccddf02bbbe3d428a4c87f11f0`  
		Last Modified: Mon, 03 Nov 2025 19:36:15 GMT  
		Size: 88.8 MB (88796418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3236c2890d28de5a1f8962dcb6d7f862419dd8e282b861a7ba427e2dbb8ede7c`  
		Last Modified: Mon, 03 Nov 2025 20:11:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:55dd17edda325de76a9d1ae239ceacbfd94c86ace999bdcca04123c53beced95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49928298dea6620117dc2803bd653f216c12113a58c63ad85177d1885051ec8d`

```dockerfile
```

-	Layers:
	-	`sha256:a5bdf00f40ab6cfb051bf3ae39d1654972fec35e5648d84b02d762055ba97903`  
		Last Modified: Mon, 03 Nov 2025 21:24:21 GMT  
		Size: 193.7 KB (193707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f74ff09450842c19cdb49f8d159bcfd368b22643ad8d81711621f2e4e41d2e6`  
		Last Modified: Mon, 03 Nov 2025 21:24:22 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:95f24aea1f16fa9a368aba4e13d06ef8e875b4a80e636ab947ed39f8f8f70163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93777947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d9affe333b124be142042b43da5b7348619b24d4aa89283e7dc9af3b2ebe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:14:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:14:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:14:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce53ff9bf2eef5053eb507e6c4a528322e0535fda9d363fa7b72a5259d021f2b`  
		Last Modified: Mon, 03 Nov 2025 18:14:51 GMT  
		Size: 292.2 KB (292156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c84c0a2b8c3becb9b5fae9dc0218be8d82025dbb521618694049793d9e42c`  
		Last Modified: Mon, 03 Nov 2025 18:14:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:64f7d659115071cd4941a89c251c9dafe2e211d73756fff0a100e86374467aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d046a675d1bbc2602011d5a0e25dc38384873efa69062d8a88e1209bd7eb572a`

```dockerfile
```

-	Layers:
	-	`sha256:37c34ad2d7a4d59603a61f1401aacc0f8677fdb7e13cc48d5a433a57f9f840b2`  
		Last Modified: Thu, 06 Nov 2025 00:25:37 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73685a968bd94489f4f1c7a8ba58877528cadf4c29988e783c7e112ccb51a6a`  
		Last Modified: Thu, 06 Nov 2025 00:25:38 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
