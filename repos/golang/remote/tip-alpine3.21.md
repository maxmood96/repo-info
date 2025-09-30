## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:497093d0c7f6dc9db601e25da6bf5d3ecb00667233a99594a2233e4558b310f6
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:94cee07176702d99e6023d0715fd7301f7602bfca6d8c3b4c74c800e8e4931ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87781681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48778449a72e75173ce2860aecb47df58a876f8b940b27a54940c1bd87b075c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f7a70b927973cce331a310498ef387c7e702a0356d4afc0b890f8c333678b0`  
		Last Modified: Mon, 29 Sep 2025 17:59:01 GMT  
		Size: 282.4 KB (282423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd392ccd6779e7a888cee1ecce65db01995a1886c75ae75a375deb44486fd071`  
		Last Modified: Mon, 29 Sep 2025 20:26:43 GMT  
		Size: 83.9 MB (83861530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2628684b547922bc611d35941a12603a4127504ba57d969520bc4cc8761b1e1a`  
		Last Modified: Mon, 29 Sep 2025 17:59:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b70c8b02b27b771da540f7d10b2ca242169fad3485486a36344ea9a9e7f1c6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491620f286463fbfd6391eb841cc9c7fb99e7015ebf9ecc240bb45a091b47755`

```dockerfile
```

-	Layers:
	-	`sha256:437e756e1229fe6c19507ec2e74ce56ee5f920f7a0449365123c762f68e6c710`  
		Last Modified: Mon, 29 Sep 2025 20:24:16 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f6f9ea03c115edb68835331101ccfbc7d71654049a9920f51afa8c65ff9bb8`  
		Last Modified: Mon, 29 Sep 2025 20:24:17 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:d67be95a0f7833b84b8f123bd54852b7dd32320dc2a7a8812376a8baaf7f642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84781639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0106dc5b44d9aa57a45fb479a325adf799c71cf9fb54b12687738c770d7fb5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9d786f18824d226ce6669ca79620f5447a2c3d91977043c4fe45022bdb5214`  
		Last Modified: Mon, 29 Sep 2025 18:01:03 GMT  
		Size: 283.3 KB (283283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d2bafb7c748b20043b1cea03995c53d72f0418aa848e1ea104b1890116ea7`  
		Last Modified: Mon, 29 Sep 2025 18:01:11 GMT  
		Size: 81.1 MB (81134385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e2669b8c7f5d8d5c20507090cbc994a336c252e4702989cc6bec98ca043eb`  
		Last Modified: Mon, 29 Sep 2025 18:01:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:216608ad64eb84f98795108fdcebd13186810dc92b1ad2c2f5dab7dedffb58d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5740978a3b5aef7a3ca6a17712769c4f845d6edcb033f4fe63fa8b67e2bb7e75`

```dockerfile
```

-	Layers:
	-	`sha256:eb7a9c8c961991a6303f21136eda79cd6fa715a97a5f99a05e04afaf2dab2023`  
		Last Modified: Mon, 29 Sep 2025 20:24:20 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:1729bfeb8891d1149e39f99fa12b1fc3da89838af7515113a8d039c85cb7c606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84273333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd8695585f881beef2080d428c93d0361e11aadca2824fdc1bba3105e04d3b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980e96c943cff30a1ea4a0d6e57166b9277c5004b05284cb7f946dc9107fe4e1`  
		Last Modified: Mon, 29 Sep 2025 18:04:20 GMT  
		Size: 282.5 KB (282467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea36933200b5f141ab18c26e141eacf675fe2778fc8f3cca0727236a934dcf`  
		Last Modified: Mon, 29 Sep 2025 18:04:27 GMT  
		Size: 80.9 MB (80893837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ed5b858ad967dafad344eef5bf03cc1f33c62e27a203047e780db04869130b`  
		Last Modified: Mon, 29 Sep 2025 18:04:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:84a9b166ed2fe7e3589167a0b1989182357eb49a6471156394811295458e9b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd3c5657c070d974b3967de1a81b518842afc253a0a81cc854e475f9bf268c`

```dockerfile
```

-	Layers:
	-	`sha256:be630317c10824232b8385810ab4c8708fc3138dfacefa2fcf3fafa3f90632e5`  
		Last Modified: Mon, 29 Sep 2025 20:24:23 GMT  
		Size: 190.1 KB (190126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dee089ae211d3a6961892b03c12c80b910de7aeafe4682f462014bc64a1e40b`  
		Last Modified: Mon, 29 Sep 2025 20:24:24 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d3b97f2399c9aac01a8532b442ee9a75a1d9faebe898423110eeb85e0c681a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84086547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60207300ce9875a8870386e26bce1e66828a3532784c7102ed348309a3f53534`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6434b1b33ff698779ee6d2701883e92ad890d82d6965dae1f0eb99b4588b9c75`  
		Last Modified: Mon, 29 Sep 2025 18:02:13 GMT  
		Size: 284.7 KB (284680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94a779ece8baaa3a2b9ccff68843c683bfb8ad46a4cbd1f1c29fcc7f5e6802e`  
		Last Modified: Mon, 29 Sep 2025 18:02:35 GMT  
		Size: 79.8 MB (79814772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7799853a7b51a035aad88a8620e026a91be08f21ce09e9baf1576b79c312cc7`  
		Last Modified: Mon, 29 Sep 2025 18:02:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:66a6376b5fe0babc34a9d01d47c520e1206f791eaf34e112deef6c8807b37cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f832f7dc0357860626fa2ebf79141f80f2e1a95f107335ff8c0169f9e037086b`

```dockerfile
```

-	Layers:
	-	`sha256:f460c2df71e70e22902905e981387739ba446ad34daa851e82e301690d85b54c`  
		Last Modified: Mon, 29 Sep 2025 20:24:27 GMT  
		Size: 190.2 KB (190152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da63b69f71c83c97200be16ce171ef7fd25530ae97bf876268de5480ef70859`  
		Last Modified: Mon, 29 Sep 2025 20:24:28 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:6a0d39e92e07030aa0a592831ff64adbe89196002e16d330e2c8fc88e8156920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86274452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f7c7d918ea93761930bfbf7d71b936331fa1ce03491774dbea8afa8187141d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998e3ea182d69aa0da08e89ccd1bc193a3669a747d886e751ac2c91dc21a9748`  
		Last Modified: Mon, 29 Sep 2025 17:58:28 GMT  
		Size: 282.9 KB (282881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe29e58b8c06a986ae5ca92831db1a0d8e315d4140a28e6305b3b9513f262ee`  
		Last Modified: Mon, 29 Sep 2025 22:06:46 GMT  
		Size: 82.5 MB (82530689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f978a03139e0fb0440efa25ccaa4fe6d2b3cca2be674b4739e2ff46dfc5abba`  
		Last Modified: Mon, 29 Sep 2025 17:58:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d924c3ee239343ef3fe3ec1533ccad1553e7673ebe4ff0380628229906e1158f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287ed5a4667a07eaf0fb782def2f88c6c74a17f246755fd77859be65727a27f`

```dockerfile
```

-	Layers:
	-	`sha256:3a9886822e652fe79937c2341e86f0e48f606a9ec2a1e3dd063d2caec4cc2482`  
		Last Modified: Mon, 29 Sep 2025 20:24:31 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95db0c592edeb5db5917e72e1eb27e595948f3bdecce818f5fe138572d182dec`  
		Last Modified: Mon, 29 Sep 2025 20:24:32 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:4ed8035be4a4b95e02070f0b1177fcb3f5fbe99eca37ae0e5362fdabd774af93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85061964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd35f9f926a2f289c0039138780797bce3c4bc13e3efe8d6fcde320003afc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4f87ea37b18b6aa0437373912738d64af4d802d362ee5a870ff483bf726a87`  
		Last Modified: Mon, 29 Sep 2025 18:34:21 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4682e6be6673e7aa33301c5b30874cd778044246d060f0fbf3c29475651b8b`  
		Last Modified: Mon, 29 Sep 2025 18:07:23 GMT  
		Size: 81.2 MB (81207592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cace535c24bac6184aa5bdf1fb5ea33d14b1398dc78612189c14ae920c14c7`  
		Last Modified: Mon, 29 Sep 2025 18:34:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c6f63a4a4e741e2bd961a251e9f8666a14ac6dfd85ebac6f7e7c1b6172069615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcab2753bd497adf782686c4554de4f0e6f515d11abdbc973272d232585d35e`

```dockerfile
```

-	Layers:
	-	`sha256:edb90e2fecea3fac3122bd070e47eac21054e9af54790776beefd6ca84a4b46d`  
		Last Modified: Mon, 29 Sep 2025 20:24:35 GMT  
		Size: 188.2 KB (188205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faafd866fa9d8561032f7ef858c6f1271dab8e5557e1dddae3ccb7fb1f5fc39e`  
		Last Modified: Mon, 29 Sep 2025 20:24:36 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:d3755864e5544859c9a32d9260cf324a9c679ad4f290d26b90f2f9814c309fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85155386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c97dc48251632aabb382b43dd808fed1558a6b546b7e1bb3d52d529c0b5b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1abfcbaa70a0168de1aea7c77a550816bb9fc5ed593a95bf38e36239223dcc`  
		Last Modified: Mon, 29 Sep 2025 19:43:19 GMT  
		Size: 81.5 MB (81523388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ea531c536977c044114a90369bb2e48fe3397e46bd0e80d113dee4a68602e2`  
		Last Modified: Mon, 29 Sep 2025 20:54:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e4c24763a10f9c50806a18bc9e59ff4ccf922b0135e502eb5820ceb68ec25f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2319e5708dfcfee6fa84b1ae58496fd2f1518e74c8c4f45545c438821fd11b22`

```dockerfile
```

-	Layers:
	-	`sha256:829000d63c2cf2627ef5705e3444be49f93712e682e8bb89b8d2b24d9047b29a`  
		Last Modified: Mon, 29 Sep 2025 23:23:35 GMT  
		Size: 188.2 KB (188201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe239307ea94f67b2ef2458e9af4bf05d4335e2620f719e1f3e92174c7120cf`  
		Last Modified: Mon, 29 Sep 2025 23:23:36 GMT  
		Size: 24.6 KB (24553 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:708c7d1b372c3a37a755c9d5411eca64ce04416725fdf1c4bf14346dbd344804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86183690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a860e6a90403918a07430d6a6526efe2a451366f8aa4441a82406661f4d558ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b403b9db0d1935e14098117e3188eb33a1eb2a0127388863b40f42ddd800c0`  
		Last Modified: Mon, 29 Sep 2025 18:34:16 GMT  
		Size: 283.4 KB (283430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ed6e6981e4c029c9853a9bbba242bc2c9b41f236141c1f10c1334ce58549f0`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 82.4 MB (82438002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54d272fe065523d329f889d667a672ba678a5d4bc05aeede6f78aea761d0fe`  
		Last Modified: Mon, 29 Sep 2025 18:34:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:94c43e6a1ab799c03b1a29999651c0fd9c457b220df16d13e299a506f873fdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 KB (212676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a354e9ccb543de089432d4f2ac5d485c48e45d088fee02cf3056c6fcf514755`

```dockerfile
```

-	Layers:
	-	`sha256:77bc5e9e1767ff29e36f2f5b508689d4b24ab9aee9057819a2bf998ba16ca544`  
		Last Modified: Mon, 29 Sep 2025 20:24:39 GMT  
		Size: 188.2 KB (188169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:165a7a0e6ebcd150a409e24f1b548583377658546a0f4c92fb53b2ac1c915d80`  
		Last Modified: Mon, 29 Sep 2025 20:24:40 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json
