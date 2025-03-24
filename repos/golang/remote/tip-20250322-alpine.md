## `golang:tip-20250322-alpine`

```console
$ docker pull golang@sha256:e3cc68fd655c5bb106fd274847e6746dcc98f2c74e790d00452e1584eef9a16f
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

### `golang:tip-20250322-alpine` - linux; amd64

```console
$ docker pull golang@sha256:d44ad65f19718c42e50579091d18c2529ff508157eec93c3452f85608e17ea80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129959335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cfd5317d83d88962878cea408b80fac8bd899faa14c2d394bea119ebad4a53`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d0dc95cb0fe7c9c90b562aa05dc994f0d59d98417860cde66c37e6258eee7e`  
		Last Modified: Mon, 24 Mar 2025 21:23:41 GMT  
		Size: 294.9 KB (294900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cbe769fc954b1a5756fdf48e31713555a112012d07425d7d4a076ea9376a7`  
		Last Modified: Mon, 24 Mar 2025 21:23:19 GMT  
		Size: 126.0 MB (126022030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce9ff13cd4740638802d4d1169f5040958fddc007cca309e3a12319ec3f7ad3`  
		Last Modified: Mon, 24 Mar 2025 21:23:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5a98f1eb07135669c7221eec5a9ee10d08b728e8b3b6eca339aa5715b3975912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8e81379dfc1423887801fd3035f4a1317690952d0ca895c1090dc612cef71d`

```dockerfile
```

-	Layers:
	-	`sha256:ff127a01ff2d4d160c4680d07cbd9dc649423e1bc1fcb9e1f8665b7d1b657e6f`  
		Last Modified: Mon, 24 Mar 2025 21:23:41 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abba071126126a37df6b6bb3b45ba66fc7aa1aadcf6d7d3f9d22eebb97bf9b3e`  
		Last Modified: Mon, 24 Mar 2025 21:23:41 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8b2861109327d7ea5c800d8184db03dc6d2fcd683c0f195f9bdf24a264de72cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124942643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9051e245e67c2e892d6a13bcbe59ffeddab2fbfb66b01465bd80241cd3d6dfbb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e6a0579c5ff3ee75a0b9bbce7a3f1ed648ca9daffbf53e165b1b1a72b4c26b`  
		Last Modified: Mon, 24 Mar 2025 21:23:09 GMT  
		Size: 121.3 MB (121281502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c97de39e8aa9437e6468362bb4e1222ac9d16a8dc6b4628b3a1d20d017036b`  
		Last Modified: Mon, 24 Mar 2025 21:23:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6515223f96625804a9087cd887d59ea033f04d2b2775febb05e209aa7f9f1bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffafc04fde3c9c471c6cd1e006f13861ac4661e5f5ddf8a65e9df9e9ff7f979`

```dockerfile
```

-	Layers:
	-	`sha256:c530ebeb264453ddb1c5c2fc98106469a2bbcf156c7a605844872651db5cbea9`  
		Last Modified: Mon, 24 Mar 2025 21:23:06 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:89010adcd335ac66a389f0bba11e4f7e712aff1ee9417a90270bda707374bfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124338812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056270f94325b40ebdf30b0b3c593e916e8105a2aa8e5d615cd90c773e7d63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353e9c70d02c05f5d0756f45338b0d2910b536c139fce40d68a3d97077441d9`  
		Last Modified: Mon, 24 Mar 2025 21:24:23 GMT  
		Size: 120.9 MB (120945332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc892795c7aacc182e4c1e42b394129d10f2223e4e9c056fac649fbce3d7350`  
		Last Modified: Mon, 24 Mar 2025 21:32:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3622540eb0225b8465623740f794d2ab952b2a8a2af3a535bcecfc0afc150f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29b39992762eadc4ca8a4c12ef8167b804d275ef7710263d1c9e18e21c85649`

```dockerfile
```

-	Layers:
	-	`sha256:9c7c0fa5b99a71901cc2266ec2b17d88360657e6b379e2af8c19db1c91c56320`  
		Last Modified: Mon, 24 Mar 2025 21:32:23 GMT  
		Size: 211.7 KB (211707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f714240dec54cd9343196cb98cc80c99d618b823a55ba276d0fef595c60b69b7`  
		Last Modified: Mon, 24 Mar 2025 21:32:23 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:167312c2e5e7eb0308ac15132fe50a807ad372198effd0a8cef927dc1398d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b9b437787e60197f089e77e6266282a17fe1030c5aac0f655434679aaebc04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa27b15393e951766b04748acddefa2554a614c3407abc8145f05a37f7e1559`  
		Last Modified: Mon, 24 Mar 2025 21:24:41 GMT  
		Size: 118.6 MB (118559237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f26d52fabe148ec3160e6c592033b142a6b7255b263c571b2021775a7aed31`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1d43e125fd4b5666812c5545602e85084686674f42c1307d25ae84982b1504f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ebba95114e46f7a97b10d36d10a3b73ae3efb472b97d88767ed9115423b933`

```dockerfile
```

-	Layers:
	-	`sha256:c29dc98daee38ce5405a782ae24a4f8237548ab38d09a3f3080528ab8188ecc4`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 211.8 KB (211767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:103a3bf3f2352434f0c23ad42aa5c2d36b38b8af5b55bdfd0ff0efa578a4db75`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; 386

```console
$ docker pull golang@sha256:dd69aee57d3374259cc722a2f6a15e7be79ddbf02cbc473f81d5be155ed6da9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127871693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5844a74e8b43aaa60190f3094f4cf34f0aec509507e39b800088f778651e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3c9ec89ef444dbf79cd05121a2769286ac33fe84b96dd3e0b42c10e8351ac`  
		Last Modified: Mon, 24 Mar 2025 21:23:35 GMT  
		Size: 295.6 KB (295593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76390dce495fb7dc13ff79afd09a2f809cad266d649bc9c2cf3aae32aea2ff71`  
		Last Modified: Mon, 24 Mar 2025 21:23:39 GMT  
		Size: 124.1 MB (124112320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573ca698a0125b8ea59f2bc46bef3a72d78eebcad4a9ce141be705a9886b45ec`  
		Last Modified: Mon, 24 Mar 2025 21:23:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cd0875ca3d4a92e002c182f749d4f21b1ab267caf98a40a3ebfbcb4c46a3ed1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ceffaf28a3985974d91958edbf12e8bf711fe706701ad804fc58f9bf31b4d`

```dockerfile
```

-	Layers:
	-	`sha256:d4b9ff1e33aa91039e82600d9ea54d396863208608232b0974b80fd925e180bb`  
		Last Modified: Mon, 24 Mar 2025 21:23:35 GMT  
		Size: 211.6 KB (211646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2f423fb0265aaa5c61bc2bae9ee2003c95fea121d8b2e23cc2d889078dc73d`  
		Last Modified: Mon, 24 Mar 2025 21:23:35 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:7366bbcb4c63640ff2d13a26314156c90e6f11f4529c1ed2855b726094a0cf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124711021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7565f38f4562495a9946263434b9b39762c9f0320e1d399fa09049d2feb75f3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1867a2d294df0d3b21b808b4672bced3956fb4c495003b07361f0a8e9cb5d1`  
		Last Modified: Mon, 24 Mar 2025 21:44:58 GMT  
		Size: 120.8 MB (120838244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667493f5231a468f1753c7e55bca5327862116a7648b2441c81a4043c39d95b0`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9942f127dde7af13afe0eaee9c24f13c1a9d67518877b2958b1363b01673c93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1ce273ede04cd89b626faf027a1dc4289f4feb564d097412f5af32f21e49b9`

```dockerfile
```

-	Layers:
	-	`sha256:8e42f111016bcacdae35ed303033b360dbd46700481d8d5072ffec6c470e56ed`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 209.8 KB (209834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2599d80ca242ebb0338221279a41b9976db38e5983af0b9679e04fd49455e62a`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:dee7fc2c98246fd62e46d66d23083e58d9d2863009010e0a0d3067175fa12dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124869785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d341ee80e1418f16991dfffa14503d8a2b42c1b8dfd55863d7fcbef707e86d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d1dcd6a0865fdc41b8f9b0f05194766b10c2f89e1bc97978e63dd59f41eaa6`  
		Last Modified: Mon, 24 Mar 2025 22:01:06 GMT  
		Size: 121.2 MB (121222842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1966868d7486f0a095934ef947778379a3c3c78d32040994f5dc608b39b94daa`  
		Last Modified: Mon, 24 Mar 2025 22:00:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4e5f2901293f32a664d56b1616d64caf33156c633bd037d8d3a85118ffe31b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 KB (234235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2b0e87615e3b4401661d669920c28fc3b8e64b07b8f0d4219bc72fc682b257`

```dockerfile
```

-	Layers:
	-	`sha256:83833b169cfbbeb510b86907bb469aa2360dac967b3a175186543606491e769e`  
		Last Modified: Mon, 24 Mar 2025 22:00:49 GMT  
		Size: 209.8 KB (209830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63c4017c2723e9f24bfbe1dcdfd9936b2f45331f2e1584c42f827494700a0c4`  
		Last Modified: Mon, 24 Mar 2025 22:00:49 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250322-alpine` - linux; s390x

```console
$ docker pull golang@sha256:6a13cf04d26ecf19ae3e7ee067699fe03cb3b09c6bec29605e09fec2f5193862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127046814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2a50a840ff89fb7534c18ecb9051d3f7e0bdfcb88d0a412192081693d7fbf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f92bbf60c027242fd3e59fa4d4252eab4d7c2b21b8d05ba9b89f6a7dbd625f3`  
		Last Modified: Mon, 24 Mar 2025 21:23:38 GMT  
		Size: 123.3 MB (123282906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0872e5cde81c0529bbb4d23dceab86cc8562024d982496c88b49dcd8da19c3`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250322-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0807a1f16b4a5c57cee5f73ca5cdb3ac04878dfd16c67eabf965ea069544dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1700ac29157a924cec8de2be5edd68305506d09922b8a369e49963d880f1259d`

```dockerfile
```

-	Layers:
	-	`sha256:f1480246da87e99bdd8ec206487d961585a1833d1cd5817d5d6c72a69c605a66`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 209.8 KB (209760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25341040731dcf6afaf290909d60fb4637e9d34ce38f65d81222d87c1c1e51c5`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
