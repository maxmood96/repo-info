## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:a8836ec73ab2f18e7f9abe18cdf2580b9575226e7dabeec3fc5230f8788aa9c4
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
$ docker pull golang@sha256:4707c052e5bd90c1c6ae16d1825e3ea5076ec1b06de30e34596b1e6f6b9916cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73268522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60a31a97fdb2c7eac5f46e5ab4cdd6e79fb96e960b520f9574a34fa163fa785`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb7f89ddd560368de98a53e7fbc004ef3d4bb2ea7e6efbb80992a6f907eed1`  
		Last Modified: Tue, 02 Jul 2024 22:06:14 GMT  
		Size: 292.4 KB (292425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2f51ff3dde07bfa1ce35b5597b2d97295e64a461d98e696feda7b25a6dc5f`  
		Last Modified: Tue, 02 Jul 2024 22:06:15 GMT  
		Size: 69.4 MB (69352095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935834aa092a42930b12249d2899dcc59baac0616accbcd97e672ba7b26c469a`  
		Last Modified: Tue, 02 Jul 2024 22:06:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ebc3f95ee30eb7221a365fe7cd1cba35bb5ebca9829924f52c3e771b951443b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9615b2a8feba15bf11e6723041e2f5951e12e7b541332c1230bb741b02a9fde9`

```dockerfile
```

-	Layers:
	-	`sha256:a3b74842a65fc8fc74e7fcd2724977a9508cfa5827dc7e6d59edc78c7ff0325a`  
		Last Modified: Tue, 02 Jul 2024 22:06:14 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:829dcd7dacea2b9b23ae3400614e337d27b79dc717903c2889439bb7473fc224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71377761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6faccbd48fd120a9755943e1b196b050ead2cd3feb183ccea05ece383cbfb1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c99d4340891f1a8f3f40ad250e01514665cc907d7c944d5670a1a3da9161563`  
		Last Modified: Tue, 02 Jul 2024 22:22:22 GMT  
		Size: 293.6 KB (293613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a528a178c88ba9b89a4047689ee438ae3a530ce2004fe5bcf7bd618341780f`  
		Last Modified: Tue, 02 Jul 2024 22:22:24 GMT  
		Size: 67.7 MB (67716837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030dbceba6f02b465600112929efc00d2a23451cd022b70b051b0cb2d6bf1611`  
		Last Modified: Tue, 02 Jul 2024 22:22:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ec253c7046875f65552bd2a533a3fdda3c83dff428fc8a074998b1f8ff31dd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342886c15034202ab25338c9fbe02d37e252cea7e45480f0d08a9f1c0d88a3f0`

```dockerfile
```

-	Layers:
	-	`sha256:2aa6b486a070741b43ef3c8e69273103154bfb3c1b79d8c2de9f63a7a0d2da0f`  
		Last Modified: Tue, 02 Jul 2024 22:22:22 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:524255606d746af71c63ea153a61d28f13a04a0031be0c5aab0427286744f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71104372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505d47b3e7ceb07d1fc3a5244200b122f08795161e218bc69ae34abc120f0102`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1dc8ae002023cf0a7266e02dc08ad7072c292c31e81a16d773ffc91b6aa297`  
		Last Modified: Wed, 03 Jul 2024 02:24:41 GMT  
		Size: 292.5 KB (292467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1377363fadc0bb3eb9a3cd846c096d02c646b0f4af9bef4893106284c049e37`  
		Last Modified: Wed, 03 Jul 2024 02:23:25 GMT  
		Size: 67.7 MB (67716891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af347af85856efbdab23806d3a2fda0de737dcb81504aa880293b165c8bdb38`  
		Last Modified: Wed, 03 Jul 2024 02:24:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e460ff65df76135625b5126cd9e2a631b83a40ff47535012d255e05356570802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594788eff578191b0f88e00a079e7b0fcef3acfd269e5efc3ce31430c63a9b69`

```dockerfile
```

-	Layers:
	-	`sha256:73e41a65fc8ffbbdb9411b732ff1a0e1989cc0323fb825744ab5680e3bc8ab0c`  
		Last Modified: Wed, 03 Jul 2024 02:24:41 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d6d72990ed8400b547c91e25b14d97712f4eb9d0c899ed8aed05feed668d1f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70656649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96a5189625045a52a0b26f2513c7deaf5d23da92b522eca0ee8f9a5a37d7a3b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763d8310d87528dad44d0fd3ad17e81221c0c207c455a029f9a94de450eebb7b`  
		Last Modified: Wed, 03 Jul 2024 01:42:57 GMT  
		Size: 295.5 KB (295464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad54470edeaca3376e9010d6ee8ae76847ce9900d3bfcdf32fc98cfd6fc2fa26`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 66.3 MB (66272226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b1003f5882a5d5a535645e21145ae456e8c0f232071a98b6a80e6e671ef8ee`  
		Last Modified: Wed, 03 Jul 2024 01:42:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e2b397f26936052b9fa1137a4b06b1ff3867452f763ff85c520727645a692993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24238f1a737c25f49d97454133bcef310049ffb34a12c39cd0f84cbe3ab5544c`

```dockerfile
```

-	Layers:
	-	`sha256:645d1ebe4c9575794f076f88ed260f4a6722293cdf5998321bdbc7a523a281ff`  
		Last Modified: Wed, 03 Jul 2024 01:42:57 GMT  
		Size: 26.0 KB (25972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:7fcb463c2b3e2e2860ed5119b7ddb1677eb8249ef597b7be29164ca9d4f717eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71103867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b074aac9a5e9bb66a540e4e58452297e0d3202723bc0a839a50a84be64c802b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6245d43f1d67e6b89e6f5685ef00c1c58fb4c3f39df0f253ccc26cf13864d8a`  
		Last Modified: Tue, 02 Jul 2024 22:06:17 GMT  
		Size: 292.9 KB (292884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b75921c461b2ae6d1ff16df768b5e8ff34e9b73cf9704174903aa4e8c76f79`  
		Last Modified: Tue, 02 Jul 2024 22:06:19 GMT  
		Size: 67.3 MB (67341356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63babd30530b5fa597a6429cd4de7e6add7159163b3bebf14263797e5c62f21f`  
		Last Modified: Tue, 02 Jul 2024 22:06:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b9cce3e56afbf25738f8b0eed8c290c71da1643632b322ddd9f0d2103c63a5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe42da2fff361d1392c2f9eb221de2106e988cdadd70e073f2149379ab9afa9`

```dockerfile
```

-	Layers:
	-	`sha256:f790078c638662471a35182b9bc18d20c09c17fedf9eae1ba677c757b2e61df4`  
		Last Modified: Tue, 02 Jul 2024 22:06:17 GMT  
		Size: 25.6 KB (25570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:fcbeaf889d8d8229be5c51ba0bfe137385a78abfb6b0f9f229706210ee3a237f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70308555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a29aada7a6be788bd72a0a489b6d821bff868da73eaaabdfb666941e45cd8f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477fe0e563a78bfc8789f98753a872bab84abaf1026e276ac6665d797175815b`  
		Last Modified: Fri, 21 Jun 2024 01:47:42 GMT  
		Size: 295.9 KB (295884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfed35a1567d183c45c7e8a04b11d626d4dd085224a9a1f3f9e560e2bdf63a8`  
		Last Modified: Fri, 21 Jun 2024 01:47:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:4de5e3afbb442d3e2b1e139f91e4951163d89f41c2fe2d19735a56612d8ce0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9991b45b67a17b7e5f34e7fe3bcb9e03841d8c3b7ace8e096c7d0ec7c96bee0d`

```dockerfile
```

-	Layers:
	-	`sha256:061089abef69390fa54a2ed336488df48fc4ee7155d1db2bf06f9d96e8a7cdc6`  
		Last Modified: Fri, 21 Jun 2024 01:47:41 GMT  
		Size: 25.7 KB (25689 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:27229884e3bf2952597bdeb77b6e1be3116a63273e851126ae47ff14a68f0262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70567475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bc84d930a346ea8949c7348c5b7b2b1e4af662cc8daeb0609f4d2e0f5dcc95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fabd91b6a1a591759f176be6e8c4ddf7d6c5b79c5fffe72fa34ed233e62f93`  
		Last Modified: Wed, 03 Jul 2024 01:24:08 GMT  
		Size: 293.2 KB (293186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39589efb4f4523cf902577d9136ea8d30bac98adf4bfb817724f0f6dbfa86c`  
		Last Modified: Wed, 03 Jul 2024 01:24:18 GMT  
		Size: 66.9 MB (66903096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fd487051268d12d3ee5ad597726cedd9dee83912d9ab8ecb8b6669ade27ff2`  
		Last Modified: Wed, 03 Jul 2024 01:24:08 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f503a8c23c6c3b15bd1320cbe5dca475d14b23ca8ecbec74113eddef4697c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3094dc0a4648f63dc2ac54e8ae6207d53b3b7666165078c27b994272c1d4d4d`

```dockerfile
```

-	Layers:
	-	`sha256:c1d4d571be3d01288d5e9e90831874025bc0f46da288c332b46998209cf984df`  
		Last Modified: Wed, 03 Jul 2024 01:24:08 GMT  
		Size: 25.7 KB (25690 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:a8d78b603053adf3573b93a3bc0c3accb7a7f6237d41a6470107be4a17ba7ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72166996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599959bd786df3e5f7bcbb8be90e38ba59d3721524aa604e62ec345f1a0c2ba4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6075f580ff9155257f851e1279c2fef823c1d43c42d2bf92f41b459ec8db60`  
		Last Modified: Wed, 03 Jul 2024 01:09:31 GMT  
		Size: 293.4 KB (293409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6f6007c9329045de5e9eb34e33d4910d207bf4c542c6d21724a0ac4001d3c`  
		Last Modified: Wed, 03 Jul 2024 01:09:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a45b0d6afef570994fde79725e70960dbf5a7c93e554fc10d3a803e0e217f219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96665eaea0c708295004fb7ae7ea25ddb05f34cce44dc9a86394dc2f380396c`

```dockerfile
```

-	Layers:
	-	`sha256:4f033662b72b3e7b40666538cd6eaa6d15e61cf2e82105279168d523ae1f7bf8`  
		Last Modified: Wed, 03 Jul 2024 01:09:31 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json
