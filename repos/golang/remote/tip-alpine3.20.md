## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:585e620bd2ac633c317038474ba7f993c033a12659937b0b9352599291f6b8de
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
$ docker pull golang@sha256:891df708b8c9f86ffe229c30a562e7fd822b83046543b62d576c698a4634d748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129998524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d9ead6468afde306a8c82a1109d533f117b52cf3c235e949bc5ca1ed395d46`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcf337fc660fbe3e93b47a3a2202159c50685f1087d997afcf540fe93c0d1f5`  
		Last Modified: Mon, 14 Apr 2025 21:51:26 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013504ab5187d636f1901fcb4a6eeb2b2ad7ca1cea03792606973678944bf0e4`  
		Last Modified: Mon, 14 Apr 2025 21:51:15 GMT  
		Size: 126.1 MB (126077078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d8438827cd3a7f57b441ee964f028744ffa5f792eaf4c495f571b63f585d02`  
		Last Modified: Mon, 14 Apr 2025 21:51:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3e237f809334856241633d5e69688959140213b6138d78642d458f47ae941178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0dc5a9757d6af9e7f93148e3f3f0273bf660e77275f5e69da2b9b426317dfd`

```dockerfile
```

-	Layers:
	-	`sha256:731151e37db72f1ad3876e53ac08b1a865f83b1bb6aaf7a497931e521e5a73e0`  
		Last Modified: Mon, 14 Apr 2025 21:51:26 GMT  
		Size: 205.4 KB (205443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c1db4e5ffc9f3374eef4abef12c8cb6857aadbb030a172494238e29a2c44a4`  
		Last Modified: Mon, 14 Apr 2025 21:51:25 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:4a19b9b05b3c36450a44c10d233c03b7cee53cf75bf21e5d6e361276bbefc289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125910479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1ef4867b5dc62d372f179d244eb906a4186bdc6d0d91e414a62027f55e0eae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
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
	-	`sha256:84a7bf435709d1c27794da4aa58bbf1c4a90e82ff2338f06023036bd847c51bc`  
		Last Modified: Mon, 21 Apr 2025 22:36:52 GMT  
		Size: 122.2 MB (122241957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d98676a1b77c2a167ad95c1cbd1590c5f811a487b9595186ea12fb098c934`  
		Last Modified: Mon, 21 Apr 2025 22:40:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ac994b03c86e27d3e03437329b0d8892476246f0501676dadb9e41eb073e6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063dc954634e76d813b0cce506b4b938fb638253c8d4ec3d34f51827084b0896`

```dockerfile
```

-	Layers:
	-	`sha256:fe62bfe035e13539b40b4917bce7fc97781fb429e6c302616722fe7ca2e3b276`  
		Last Modified: Mon, 21 Apr 2025 22:40:18 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:316bdaad52b5b34346ba36d199bde238cbbfbeab859b314e1a31fcadf5347641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124498959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510edc06c3e757772522f4766a34c94b4c5bffbdd45efbf9ede8faf0a53a1e0a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
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
	-	`sha256:e131e20eff5d97e9796f801f5335249fcb3b27557a67cdb1b0533cbc32974fff`  
		Last Modified: Mon, 14 Apr 2025 21:52:15 GMT  
		Size: 121.1 MB (121108078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab49c067a9001b43adad2f541fc00fa95940abdb3b8c61f39adcfe2723c1da46`  
		Last Modified: Mon, 14 Apr 2025 22:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:41830c7813956b2743a1f85fa04e71cac21318030f2f24a6ef286e4eeefa055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9afecfaadb59d43a8cb13250bc9764807d484b50f0221bd4afb31b2e7becfdf`

```dockerfile
```

-	Layers:
	-	`sha256:3d7eeaec8fbbbfb614c7b23a9031a4239b7083c3d5e40afb2a6987daae66d330`  
		Last Modified: Mon, 14 Apr 2025 22:02:22 GMT  
		Size: 205.4 KB (205423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafd73cc858fad58d42fc0a5e7f6876df3102117444acbdd017df280db7508fd`  
		Last Modified: Mon, 14 Apr 2025 22:02:22 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f6e1dc9688652eab48714a284dd48ffe17c949c63b77ea1e6f61ae5330f53214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123158490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95563f756238c84cbccb1a9fa46cf0554ec60520807fc23441718bba12a70778`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d91181a4474d3822cc4cabd1e8df2eed7942133a31b6fe7528c1a3639a00d`  
		Last Modified: Mon, 14 Apr 2025 21:56:34 GMT  
		Size: 297.5 KB (297478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b206f4f1851ae209ce8b8172ce5c71a21bf857b5a5fc8341f94dabec27aaed`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 118.8 MB (118769688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0d6d300f1e9976f03d461d713d90790eaf1daf412d178bb8e02af44dd409f2`  
		Last Modified: Mon, 14 Apr 2025 21:56:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:72b52e87c1ed738bb23c71126a813af27431ba2fb8e84f0b78299ebecf2298f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 KB (230123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434bd9bcfbbc982314f3e515dabebbbf41dbb938822e8a8ce8bca0eae7d73178`

```dockerfile
```

-	Layers:
	-	`sha256:77db73cff93113cd76890be51018d38f90d8a4a3c97dbc1b5956f149a0355380`  
		Last Modified: Mon, 14 Apr 2025 21:56:34 GMT  
		Size: 205.5 KB (205475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7decd7fdc204abb6a40a2982645948269ced6319b92b160cd2bba804c8e06`  
		Last Modified: Mon, 14 Apr 2025 21:56:34 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:2f0f86c5de3766058996f77e0483ede868ae3359cebdea59f1bcf4443d7305e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128810440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea3522ecd544c7b54251ea93d8ce6ccefc43ef8c261c520a85db02e29ea5f5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da19f81f95234be2f436440204e905609ce287f59a8f5bf2cd302f3da51b8c13`  
		Last Modified: Mon, 21 Apr 2025 22:37:49 GMT  
		Size: 295.1 KB (295137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22385500e9d61ec2b239f5d3bd81241409c720a3ebb2a4cf2d458346f64bcc50`  
		Last Modified: Mon, 21 Apr 2025 22:37:44 GMT  
		Size: 125.0 MB (125043477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72177e65800fe60930d540caa24cf09db08868e358e6b00d6aeaf76223acb6bd`  
		Last Modified: Mon, 21 Apr 2025 22:37:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8301cb5c0cfc6611c7338b124e85e52696c0e172b59fc6b5b839b45f43867bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c5445586a18dac89bb926c568c242c76601e39c29039c01a1c52652670382d`

```dockerfile
```

-	Layers:
	-	`sha256:f8ef6bd4e11dcd4015b0cb0a7d99be48896226940139fbadff9d6627421dc5c5`  
		Last Modified: Mon, 21 Apr 2025 22:37:49 GMT  
		Size: 205.4 KB (205388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1112779d67d9225cb6d9c7322a7d483b17486fc0e10d7fc4b027985ec9a204b`  
		Last Modified: Mon, 21 Apr 2025 22:37:48 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:c2fec1172d5808067ae2d8d10f81ed49debf4aa516633461f2e29a2f4e142a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124781470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef5f1bc99feef8ae34321adb16a94ffbc444f421788dcff787b11501d8d2c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5950c2617b2e37b28d36382b32bdc610566f7587eaecf172653230b9278424e`  
		Last Modified: Mon, 14 Apr 2025 21:58:56 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394c4e947a61e9f0edca853e080387bc94a62b435ba7141bd2b21c9acb3149`  
		Last Modified: Mon, 14 Apr 2025 21:52:05 GMT  
		Size: 120.9 MB (120907733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2b6b72cb89849fa7530fb004aa41903e89c24dd1a5b93ed15cb90750be4a88`  
		Last Modified: Mon, 14 Apr 2025 21:58:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d39bdbf69926aa92d374eeddd53ebb9b8c60e139f94c38b93f193ab414eb29d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217ed520fc225c97d75f9c1d7ae9726718d4bdc2ec9a7540244b8cd674a9aefa`

```dockerfile
```

-	Layers:
	-	`sha256:20d4d2d8fcc8d7cfffda411c13ff74754d285c27a82e4fef25d373f7ac815af6`  
		Last Modified: Mon, 14 Apr 2025 21:58:55 GMT  
		Size: 203.6 KB (203554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a56e533b8c897d40c7d617274154a629652bca1b2c609d6a6e96f9e97c33dfd`  
		Last Modified: Mon, 14 Apr 2025 21:58:55 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:78542556ba1eb7def870f0c2d9356e456c4f9372dcc4670b121ad87b384cd290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124930339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6f1c931a0827f478438d3211488de0918c51518bc2d08fc44c95d5aa8a364`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
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
	-	`sha256:9d0cc7d671cb98f96a9b881e518de5f5b9784e511412b2c2087bc879cb5253c9`  
		Last Modified: Mon, 14 Apr 2025 22:30:40 GMT  
		Size: 121.3 MB (121261504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c73dde468093f431a10b0a96d7b44454e602b057282bb0de66225c30b5cbb`  
		Last Modified: Mon, 14 Apr 2025 23:08:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d12f413a53d77b38acbcd6d14c785f9c9261d124e1a9a115e65b9e0770d05da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf24f2537559a993d70673a514a517b0ee99b033dea47266270521286e8af953`

```dockerfile
```

-	Layers:
	-	`sha256:6536780a5630a0229a6e6c6b12b28bd48f86c6a607b7f2c1346fc9275885afd4`  
		Last Modified: Mon, 14 Apr 2025 23:08:22 GMT  
		Size: 203.6 KB (203550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ea70e72345b24ae3b722efe989b2bbfecbaa65f4dcecc466ab63a44241a7e5`  
		Last Modified: Mon, 14 Apr 2025 23:08:22 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:658609e74a80078a933beaacad211df37b4d45e869fadd3d50336d1fb338d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127090340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0b0a34e467af8ec16fff15c95e2d0e610dd664d7380b36f7bd2a2a697e6dfc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e7fca1d9a730d1f433c30e90db2ee0f57358064bb42fafd714109fc27562`  
		Last Modified: Mon, 14 Apr 2025 21:59:00 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3413729307d44114afade63be5a02a91d2719dffc8bdec785d42f725815b7f`  
		Last Modified: Mon, 14 Apr 2025 21:52:34 GMT  
		Size: 123.3 MB (123330348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51881c292f94de132cb92d225cefd0a0109de0238dd6dd6ff432cd19f16acba`  
		Last Modified: Mon, 14 Apr 2025 21:58:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:845510ec60a7411b72cafca7de0bb9f584e9631c90b8bb62303446cff910721a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8483d09168a4df3109dde0ed0a98486479fdbd6faba7e5e31bf6b95174a313c`

```dockerfile
```

-	Layers:
	-	`sha256:866f825167cce95467a5a9b6576e3697c0a1828601626ed76bf80d37b396bb52`  
		Last Modified: Mon, 14 Apr 2025 21:59:00 GMT  
		Size: 203.5 KB (203492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ea668a3594eeb6b2de75152b6b7e7c03576a437eaf7a6c7a5271c1bed49152`  
		Last Modified: Mon, 14 Apr 2025 21:58:59 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json
