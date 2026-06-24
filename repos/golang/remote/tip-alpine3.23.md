## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:bc46908c7b117c7c2b2fbb76bb9bea2086f5447dfd9f9465e641aed652873729
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

### `golang:tip-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:669731a3a93a594e38b886ff4f6d07a863ffc1893c1da54d61d2f4dcffd1bc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106649013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd4b9af70ae28f98a2faf30fb335a5f96f7bc06d793f9d9834a74090021359e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:40:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:42:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:42:56 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:42:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:42:56 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:42:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:42:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadad8861700614d8b71977a862d0de37dbd8f23553feb1bd4138cbbe9e83750`  
		Last Modified: Mon, 22 Jun 2026 22:43:14 GMT  
		Size: 245.0 KB (245045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ced9bfc2a0ce47376a0e89056fba2dbdc199ef992671e729f2b29cd85c5af1`  
		Last Modified: Mon, 22 Jun 2026 22:43:09 GMT  
		Size: 102.6 MB (102559388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d513ef2d3ff63ca6f2e3abbcd339d6ead5cc9d755649bb2a0f8e0c16b1f9b2`  
		Last Modified: Mon, 22 Jun 2026 22:43:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:990a346e16950558e33623b8ddd829e25c613f53d288b0d69b5955d3109b37f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 KB (200595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7c9187ceefc6f72f8a22a4a75ebd491f3c3bd38ee5388cba05fa8faa77764`

```dockerfile
```

-	Layers:
	-	`sha256:2d5a7ff1bd1b97cde1390ee01464749a7b701210d4c5a9d3bf91dd10476d36ea`  
		Last Modified: Mon, 22 Jun 2026 22:43:14 GMT  
		Size: 176.1 KB (176126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df6763ccd06483c092912b30dca92f5ec1d918c3c2e56ccdf55fbe9d44501de`  
		Last Modified: Mon, 22 Jun 2026 22:43:14 GMT  
		Size: 24.5 KB (24469 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:8dd03d22cfb06332b488b054a2efcf932cca49717fe70b056b7987d7b5858f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102385469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15f9dccb8bc9a3d603a02ae5e8880834973f04799137eeb807edd49e3bbc570`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:40:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:43:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:43:37 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:43:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:43:37 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:43:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:43:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089d8b8bd967c9269b2c882609438797cd573373af903d88dc18c7f69fe2f493`  
		Last Modified: Mon, 22 Jun 2026 22:43:52 GMT  
		Size: 246.1 KB (246140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099298a9b55f99c5c1c21a12818fb4e2eaf7834dca329c07e51b1c2bab857622`  
		Last Modified: Mon, 22 Jun 2026 22:42:13 GMT  
		Size: 98.6 MB (98586575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e39152bd2da2db85bc063f4d0cfd38193c316645831403017c0368a11ecf08`  
		Last Modified: Mon, 22 Jun 2026 22:43:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:2c10d80a110f8be2601bccfc0974305a9e49326bbe6644090c4f1aa2029f7111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6988439a6fe4b12600cb459c26afaa9b157f95276805ee8575493275ad4a3fb8`

```dockerfile
```

-	Layers:
	-	`sha256:61bc01d3805dd2bc7b9a7d8fdf57603cbd25260da3aa624b08851f692a8842fc`  
		Last Modified: Mon, 22 Jun 2026 22:43:52 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:5a4155fffade1aab1c3e5a9ca0f422bdde563f517ea236e5f786a819149399e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8b4576d4947a4228aed301b58c5dacb902d91a0d8c1c53f4a6008e9f6c7c41`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:43:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:46:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:46:57 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:46:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:46:57 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:47:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:47:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4bee520e40f1a80314e77b516d4d93961c3780be089a59cb169435e976b8a1`  
		Last Modified: Mon, 22 Jun 2026 22:47:16 GMT  
		Size: 245.1 KB (245133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6c0ac1bf1a1f35e41966874d41949d2c8d30b471f4a54f05d28249cc12bc`  
		Last Modified: Mon, 22 Jun 2026 22:45:14 GMT  
		Size: 98.3 MB (98276162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a503b28d6df8856975573170009f6fcdcf775774fbf1c8f87a98e1de34400a`  
		Last Modified: Mon, 22 Jun 2026 22:47:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:8b2d8e0e5e3e08d6e8697cd02b6f5ee53efb3b36779bc3aded2d2e1b5f41936d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 KB (200057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780710cdf196e1554d2db521f9b840d81628b6afbb631a87ea03d90a5829649`

```dockerfile
```

-	Layers:
	-	`sha256:2857894b45232bb5ab8e5f627fa641b8114a433a336e59278264a753f7d4bc4e`  
		Last Modified: Mon, 22 Jun 2026 22:47:16 GMT  
		Size: 175.5 KB (175480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:698010e6d75a6d7e201aeab5c388607cdf038d12ba612718b42377bac4db5768`  
		Last Modified: Mon, 22 Jun 2026 22:47:15 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1958620377dd974c4690bcdb0d5a8f92197babcb8e6851baf4582ca3726f6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101388949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fda1992366fff183b00c95d71c925247d5116531a90132d01fbd735ec1d60cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:41:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:43:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:43:02 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:43:02 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:43:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:43:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89bdb5ab26c34c992e64a3f580ead8519848d4f6b493fd29308a7b725e5df9`  
		Last Modified: Mon, 22 Jun 2026 22:43:20 GMT  
		Size: 247.5 KB (247488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a4f06fe9b49ab2b0e448e3bb545bf0083fe0a192a188b8354bf30a5042489`  
		Last Modified: Mon, 22 Jun 2026 22:43:15 GMT  
		Size: 97.0 MB (96959444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5813c10a40ba22220c1c0b14d05cca1a737f395c5bd201fdb21b3a607aae824f`  
		Last Modified: Mon, 22 Jun 2026 22:43:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:8c38633a203abb82ebdd15dd66820afdb0ec9ff05d312586298d9291aea23ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 KB (200109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e4c71a46e99aff41c771a0f0beee2d19c7dbc991f8701581536f1a0217f77c`

```dockerfile
```

-	Layers:
	-	`sha256:06f53dcad8a7677cf062f9fcd2f1806b769b47734447df0f254f3e3e2be6a3fa`  
		Last Modified: Mon, 22 Jun 2026 22:43:20 GMT  
		Size: 175.5 KB (175508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f1ee8b78859c2e3b76f3c0d2d5c269472261806ba6bd71c83338d21b141b02`  
		Last Modified: Mon, 22 Jun 2026 22:43:20 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:fd301536ebca1a3c3c9806fe9b91b78546b532ea72172aa044fe9de6fcdfb329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569ec407db78160adc43711de667da23dffb5cc95396c7283786cacf464aafbc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:41:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:40:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:40:40 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:40:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:40:40 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:43:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:43:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae52e7380d5e969378192f66b19b302861109159ac9a587e64315cd77ece44a`  
		Last Modified: Mon, 22 Jun 2026 22:43:53 GMT  
		Size: 245.6 KB (245574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675e2fd1600788af1a6ae5db185dc20a1f52bf11f13c9afd16f6795c307c09a`  
		Last Modified: Mon, 22 Jun 2026 22:41:13 GMT  
		Size: 100.3 MB (100338995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0342bfa40e9b213206f5dfb3b3cfc3c8f4bcb1020968e1f489bf0c624c9ae927`  
		Last Modified: Mon, 22 Jun 2026 22:43:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:43168d0fc2a2ad79f3da22243b36d79e9c7b01be43405c62740a841ad2180a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 KB (200531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3349b6e95a89d1744dcba9ef3b8676baaece23f86e9b6e58bfb00e56b3bdcd9`

```dockerfile
```

-	Layers:
	-	`sha256:bb7028849a71231d15bbe7c129ac3635c6f42901e865699e7779841f3eb6dbb3`  
		Last Modified: Mon, 22 Jun 2026 22:43:53 GMT  
		Size: 176.1 KB (176095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016efb61cee86bdc6c4894506b9f41c1afa1be901199a7fda0eac28a911dbb89`  
		Last Modified: Mon, 22 Jun 2026 22:43:53 GMT  
		Size: 24.4 KB (24436 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:a85da9cf4fdd88b8b1d607465a3c47eb9aa1301297791acb40f23bc9365194f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103005647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730cf54540f749024aa4f2c59f00405e9ae38fad273ac4f9944ab8a8829970f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:49:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:08 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:46:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:46:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2afe4ddf70535a87895dd2928115f13eed6bd80bb630863f6b224ede37a652`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 247.9 KB (247906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec7882ea306fbaa9d198836e0980a8d1968fa6de95f144db148dc1345d3f57`  
		Last Modified: Mon, 22 Jun 2026 22:42:20 GMT  
		Size: 98.9 MB (98945286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f023a858ef379021d02d26336614b92ad249541cbf5b4b9f6ddef93b975f2e`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:266373c70d5fcfe37e94bae9cac51c159559cfdd39d6a53b736bcffe3e6c7f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 KB (200024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a27244d349e4e8ba637301c01c3efff0b587c4b9afc333ac8c7dca607b7322`

```dockerfile
```

-	Layers:
	-	`sha256:1e58ee632fa4b0e80f121c9687d33c10e3d6dd3f5bd16eec05e3749f0789a62d`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 175.5 KB (175513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7587f1b8b4e6f5044fef8c9a3ab77c20061156089a4640edd2aa740435ddf4f`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:3bc04b4997db83c906a9177ef76df66297fb6e7f5a7307e0dd090caa80284652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103713727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f13c8d27ea012056a9d9cfc8c903adcf4cd5dba0a9d13f9f7001727a45b4ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 23 Jun 2026 14:05:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Jun 2026 10:07:31 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 10:07:31 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 10:07:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 10:07:31 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 10:53:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 10:53:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1b6a4c21a78dbb25159d2e273a4550eac3caff5f0f9a74168efac89740c36`  
		Last Modified: Tue, 23 Jun 2026 14:06:21 GMT  
		Size: 245.5 KB (245467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5865baa224ce2c671d269d1c0dd162b2508142e741adc2f2a4904ebd20774719`  
		Last Modified: Wed, 24 Jun 2026 10:11:02 GMT  
		Size: 99.9 MB (99894861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0dc7b20ce9ff633a473fb1bec8a0326d554a467878da2c0a6489d4b03bfe27`  
		Last Modified: Wed, 24 Jun 2026 10:54:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:33489d6c4a3eaa456933d99f7784d14cdaa83da0bb935e378695f45d1aadcb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 KB (200020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bba74304947d0b83ee2ac163b91360344408b16dd10d141e33bd0b37ba75265`

```dockerfile
```

-	Layers:
	-	`sha256:20d76afd0fc30953c56c259eb844d73a7ba295352e00bbbef15a18e15eb0630d`  
		Last Modified: Wed, 24 Jun 2026 10:54:37 GMT  
		Size: 175.5 KB (175509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50dc1ee45e987507f304bda5081b517d811dd9a3b4ed8426f1914dbe3fda08d3`  
		Last Modified: Wed, 24 Jun 2026 10:54:37 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:c86544ae130462a7b1200da9efa2714a08e30a5b2e333dfa55ab1ec314b13a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104963352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d230476f54569bb9361ad66751a362e8b250bacf08a7ab57fae42bbad39b8bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:15:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:44:12 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:44:12 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:44:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:44:12 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:44:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:44:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a4c1c12951d87a35e79662deb5da49084be2cf265098c2a5ec87540765d246`  
		Last Modified: Mon, 22 Jun 2026 20:16:21 GMT  
		Size: 246.1 KB (246132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf953c950bf774a1558a2610c27217993faad44f113fb37ad0ee60aef8db0d`  
		Last Modified: Mon, 22 Jun 2026 22:44:49 GMT  
		Size: 101.0 MB (101009813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63574d8c4f2fb3d41034cf94ab23e9a3dccaf34320fae86624af6fa2a6060faa`  
		Last Modified: Mon, 22 Jun 2026 22:44:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:6922959a3e8084d561d8637a2340c512995a5a88e77b06364257ae36464bdc4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 KB (200518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e4839798ed75287e93ee8b6ee79d4e536447558dca8892679d826a0d0bd3bc`

```dockerfile
```

-	Layers:
	-	`sha256:530b8e82521d63b1678994b320391524b3d7bf09f44538c62976af435d4cace9`  
		Last Modified: Mon, 22 Jun 2026 22:44:47 GMT  
		Size: 176.2 KB (176223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c0b0b79fe895ce8543b23236d25df513f3986ce358c30c813a31a06bca8c3b`  
		Last Modified: Mon, 22 Jun 2026 22:44:47 GMT  
		Size: 24.3 KB (24295 bytes)  
		MIME: application/vnd.in-toto+json
