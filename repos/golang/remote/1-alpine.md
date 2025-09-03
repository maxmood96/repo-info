## `golang:1-alpine`

```console
$ docker pull golang@sha256:7fe17a60f87e85c7996c52baae5e49b193ea2b42009c8dedc07ff2de42e384dc
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:546671046d6f9f786c24b83111ba1801b736ee4b01b23db33e4f3eb41d4f8883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64127895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02244f13a4e20c6fa0c9b550f226683e8b63ecbc77e08a831072daf220b8501`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 18:13:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e451c10b31532d8616ff155adb8383bcfe95b7388ad69363af6512986430f9`  
		Last Modified: Wed, 03 Sep 2025 18:49:01 GMT  
		Size: 282.4 KB (282439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330457f0054be4c07fbaeac90483ac4f534113ccd944fe16beb9e079a3ab3a36`  
		Last Modified: Wed, 03 Sep 2025 18:49:05 GMT  
		Size: 60.0 MB (60045609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47af78ce4e7644116937dd73c4624dd335cedafdcfbb998d89e8c4d7c652854`  
		Last Modified: Wed, 03 Sep 2025 18:49:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4b1935e3f7c6b914a97623733ead7a05b254c7cc9ddf75d01f201c1fb4d91e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 KB (219019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e7621f97f77f8481f4ae38ebdd5921ad3a463836ec9803d3c9e1251add3480`

```dockerfile
```

-	Layers:
	-	`sha256:f40134f1d0462d9aae2e7e71afb594c2adb40cd54881627e3620dc3e842a5a50`  
		Last Modified: Wed, 03 Sep 2025 19:05:02 GMT  
		Size: 192.9 KB (192949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392fc9a355f1728f4c8a2bb32797ae9b005b10d7849541c21beff6a9ffe6244`  
		Last Modified: Wed, 03 Sep 2025 19:05:03 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:e2147e0562cdcae48de0162a5510c1e66953364ab76906e1cc1a2624999d0a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62762593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc1db0634e43d3981a7d89e1150ced35b675d0b2d603b17d0e2dedd1d99967e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 18:13:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a44638bfcc9a284518c23ffdd9987c08149ae934bfdc646c64661f53945d956`  
		Last Modified: Wed, 03 Sep 2025 18:48:34 GMT  
		Size: 59.0 MB (58978196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4631275be0b0e97c3cbcc9d86f045fb292508dc13ce4dce1e2653b9ba1d4bfb`  
		Last Modified: Wed, 03 Sep 2025 18:48:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1c8992ce002b0780413165eff7efb815b1ac2564621035f00a43801b10140d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce59abeeb09d6ff19235fefbe71b37212a780318e0b1cd0d80da58737bab213`

```dockerfile
```

-	Layers:
	-	`sha256:35a54aebe895a4be3e4e38de9a824e73458f9a05dfa76095c48d22d6ef37a085`  
		Last Modified: Wed, 03 Sep 2025 19:05:07 GMT  
		Size: 26.0 KB (25987 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:c7c5efde8826a9f5d6fa4158158f6bc65c409cfa241bb6accf9b81e88b9c80c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62479857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d88f0635ff94575255286d346f088e232f25bf5b34f9c6c02f4baf4dfbcd2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 18:13:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec999c8e928607a0bc4da54080226a6c247c744815a64f6c10bf38b015958ebf`  
		Last Modified: Wed, 03 Sep 2025 19:08:36 GMT  
		Size: 59.0 MB (58978176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588ecf6b5dcc843c1c6a16f9c6243ed7412f88950d57d90fd50cd05e0a125b21`  
		Last Modified: Wed, 03 Sep 2025 18:50:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7d6adc32baf79e23e76f98bfb4496556e3691a763e2bd6c30f115a001e420c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 KB (219206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f16d7d2fe5d3bd3c37b10ad40326bf687e18756b7f2ecd04e266efb2e6a031`

```dockerfile
```

-	Layers:
	-	`sha256:93817bc51f547c53b96985c385ff45b6dd2d3fd8cc67e64f4eeef7f35f8f3caf`  
		Last Modified: Wed, 03 Sep 2025 19:05:11 GMT  
		Size: 193.0 KB (193003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29b094ea2c51e433ec6c5f468c4ba84c59f485c91f56f20e51bee16e1b08c5d`  
		Last Modified: Wed, 03 Sep 2025 19:05:12 GMT  
		Size: 26.2 KB (26203 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:690d8c2d3af65501c70fc270cf886c6621f86e58fbe670c54bcc1f9cc2e8cb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61971093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16364065902cbe8d833c4e234ee59ca8b5e5ea02492530f07a1ae7be03711819`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 18:13:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21357df949f743a56d3417cb15486b8a5579e1b74b558f43b89f72158c8010f`  
		Last Modified: Tue, 02 Sep 2025 17:28:59 GMT  
		Size: 284.7 KB (284705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4681030a890db37290ab2fddf45adb75dbd1fbf983ba1b16efefb7221b97b1ec`  
		Last Modified: Wed, 03 Sep 2025 18:48:35 GMT  
		Size: 57.6 MB (57555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1263033b96d9290f4969661ad0abb50c064aa016a442c57ef7309a1372f7ce`  
		Last Modified: Wed, 03 Sep 2025 18:55:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b289f9d224ae812b8b854588b6f6ef4c74e9ecc00f6740305d7b9cf2d477d4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaa5b7475a4e84e7f04a7243493f5b63522ed68974fddf10687091cd9f0bbbb`

```dockerfile
```

-	Layers:
	-	`sha256:ec90af24c14206c5a727be661e766614991544b735c12df189c614ffa076b31f`  
		Last Modified: Wed, 03 Sep 2025 19:05:18 GMT  
		Size: 193.1 KB (193053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5831707ac048a5f5ea99ee1d4b44851ccb77a492e627a0cf3ea09d0f00b7220`  
		Last Modified: Wed, 03 Sep 2025 19:05:19 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:8603b4172a3a73b18e6581e30a384e64d55dc512acd42e7d3518e8cc0f05f8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62662141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8176f929bc53b44b733dfcb2959f74179f1c6c636fa33a136c3785effe7fa294`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 18:13:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f21ed875acf7c5f504751888fa66d4bd9f358fb5bc77f8037acda5b193aa602`  
		Last Modified: Wed, 03 Sep 2025 19:04:10 GMT  
		Size: 282.9 KB (282929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8134730600d4cfc74c5293aacb74478de1de4810632b08ac46dafe23f69bbce`  
		Last Modified: Wed, 03 Sep 2025 19:04:05 GMT  
		Size: 58.8 MB (58764049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30a3702792336a02334e1ba89de5b19916e199cd5648837b56943913dbc3b66`  
		Last Modified: Wed, 03 Sep 2025 19:04:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b3c0c3e0755a74a038bebe9158bb00e611d9809780a324131c932ebf626892d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e8a5fc7a4011be1ea7f00d568e5f06cf936fc4ed8bb96dea79b16c14f5032e`

```dockerfile
```

-	Layers:
	-	`sha256:81a6ebd30bf7a1472f3525b5a21e9a0f3b3b250a41b6a288b4f55d2506049caa`  
		Last Modified: Wed, 03 Sep 2025 19:05:23 GMT  
		Size: 192.9 KB (192890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ae859c6e427af8e3f4e802de34152edef4d75faabff0bed3d290cc5b54fdfc`  
		Last Modified: Wed, 03 Sep 2025 19:05:24 GMT  
		Size: 26.0 KB (26013 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:fe4c73520db67dc4717edff6fed0366b41e30ffa78f73659a22491a7dda31a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62048554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eef75352116bd972311aed7215de781b2b32f4129c87b93d2a4045358088c3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 18:13:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093a8784e85737b54c7bd288e58eb1c4d919cf932185be9835fe0acd194ad05`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295eaa21ceb778d7859c40f41ccdf7cdeffaaa99a56ac388f747e3eb72308f3`  
		Last Modified: Wed, 03 Sep 2025 18:50:02 GMT  
		Size: 58.0 MB (58036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01c481c7763c179c2e7a07ee1c506a1b64587a0dd8c90777578db6698e870bb`  
		Last Modified: Wed, 03 Sep 2025 18:51:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c6c89241e7df50f90dae8f2a92b8e7b93529599177c93c423c5e60cba222b1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d255263ab634c0e84fc114ac2c9319c442601dbc675ab0a2ff13dd6b4ed994`

```dockerfile
```

-	Layers:
	-	`sha256:1e53469f38c9c1a5ebfa8564293d79c8c6d4b013f657a65bf2a4edb8d8ffd832`  
		Last Modified: Wed, 03 Sep 2025 19:05:28 GMT  
		Size: 191.1 KB (191070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecdd65c87e95eafce7bb8d69fef67bf8d608837300626b2ae9af31373492cbba`  
		Last Modified: Wed, 03 Sep 2025 19:05:29 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:263c144be810750e13a4f62e077566cde359c4e842a637fe2d4acbc5cd9dadb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62365784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87d3825b8f08880b370897f8eb24287fc9cd63ccae0748fb29b521d24be151a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8818a250444a855ca5b23afc25325ec1add801f7bb83153c967335fb20cce8c`  
		Last Modified: Sun, 17 Aug 2025 10:47:36 GMT  
		Size: 58.6 MB (58570045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa73a00a8f5fcc1c6a012f631aad24947f80e562087eaca0a51207300fd3461`  
		Last Modified: Sun, 17 Aug 2025 10:47:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f68cdc4641428992dcefe0f1cad00466a8ac8e1cffda5415ad3b08d4899f5cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ab71e56790dd4f49fbca94ee576c16d28c7c471f2900a161fc8daae5c360d`

```dockerfile
```

-	Layers:
	-	`sha256:53255fc251dd550cd68d5dd0fb5bca76e0aa7c19e60cb00084fa14283bcfab7f`  
		Last Modified: Sun, 17 Aug 2025 11:22:33 GMT  
		Size: 191.1 KB (191066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97cfe30457d396b46f67c7834bff742583368d2b74eb9af9de34623add00eff7`  
		Last Modified: Sun, 17 Aug 2025 11:22:34 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:75253a0b527eb969cc146e0b053d5d8673addd9e2b40f79177f62bb4276911aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63304399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc33bbddb04368f22498f49eca690c10bc4d36f079dfbb06d20534659ed463`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:89728d5505e76d00f7cc71fa49c201a61287905cbe59a17bf424ca8b447de170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 KB (217064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995137f0573e262f1b2e9d6bc19a757e5a85fefc905193368a5c51f1c990f068`

```dockerfile
```

-	Layers:
	-	`sha256:a2f42721e14a391dba32d9e0fa089aac843d0867277d0bb2eac46d874995252c`  
		Last Modified: Wed, 13 Aug 2025 23:22:53 GMT  
		Size: 191.0 KB (190998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4ae0bd5537eb786087da085dc077b4a0a68221b23d29a3fed7e3afe4654a2c`  
		Last Modified: Wed, 13 Aug 2025 23:22:54 GMT  
		Size: 26.1 KB (26066 bytes)  
		MIME: application/vnd.in-toto+json
