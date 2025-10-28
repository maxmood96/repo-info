## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:a9d7474e07c96c8d4e7d295f83c372745295999a5610380685cc05b93c288457
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
$ docker pull golang@sha256:b92bb7ea43099d4b6af4934ce36c0e289e1cbaa96150f73f6a6935fb1d12c5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95691296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718cccd10d60dca82a17eca313b2daa6e0ec82b5fd123faa2ad2974e43915efd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056775ed30e157929b6fe27ade95e188a73807481226a7a6b74d86c856a73517`  
		Last Modified: Mon, 27 Oct 2025 21:07:48 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed0125ec0f9fecb5ad10be0dd03e9fbc038a3da639715455b9acfe33ee37f3`  
		Last Modified: Mon, 27 Oct 2025 21:07:41 GMT  
		Size: 91.6 MB (91597540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5a010e9c813112f1bf4da36546f26fcbc91d4595f192ceb72be2310013770c`  
		Last Modified: Mon, 27 Oct 2025 21:07:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e3f0df43a878441a7a105ee52206b866ed48211dbf3d671042b4fc3db7ee5885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 KB (220750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c212cb66001c3236b578ef5ad464a5f7e6989a36b30cdd3f34ecdf9c761b205`

```dockerfile
```

-	Layers:
	-	`sha256:4bb3bbd8fe1852f7c890d1867c5a6eb15b9bb372823a85eec318c8e3b714b4be`  
		Last Modified: Mon, 27 Oct 2025 23:23:52 GMT  
		Size: 195.6 KB (195612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9df0700b79e0b1b0efe1bdd5a9e7e2d0048fe1b6594b9ed11a6b71c7ff607ec`  
		Last Modified: Mon, 27 Oct 2025 23:23:53 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:da60dd3a150db05afcce9aa4697c68fb606cc2336cc83d69ef576171c4d51119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91968387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b405f22ead71d5081ba06d8b2caabe3c605f12f28143fb16cca288648dffae7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a5895c5be3d094227142c6313656e862982364299140d940171ae7b962b00`  
		Last Modified: Mon, 27 Oct 2025 21:06:50 GMT  
		Size: 292.3 KB (292296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481a45f1b7e81712b6a51b64a28320f5cdc697d0b9d49668a102223a0815a361`  
		Last Modified: Mon, 27 Oct 2025 21:06:57 GMT  
		Size: 88.2 MB (88171853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a1de63425d5efdc299c8bdf9b9e49510c44ddd08f1a2eb510bf98c312fa541`  
		Last Modified: Mon, 27 Oct 2025 21:06:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6b7308e44f2d0cde7349a0cc3c86743311c85b7145d4b19747392b16e5dde1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4b809a54ed88a48394d2880ed5a55b6b1d1c6f0973929b982b210276f66d9`

```dockerfile
```

-	Layers:
	-	`sha256:dc527f10b36bad4dfb405cbef02739c4b9587518db46376e38d1fc05505afaa7`  
		Last Modified: Mon, 27 Oct 2025 23:23:56 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:61f63126536e76d321e14d58b42b0c40f084f6db2f5393d09f082bbe44250c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91432230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba3f4f8ae45c200b551e79ed4c9667861ec6134e6f5f4104217875d745de329`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862709020bb25de16f068e3444f117a1e34f06999128d74ac94800bdc411589c`  
		Last Modified: Mon, 27 Oct 2025 21:11:19 GMT  
		Size: 291.2 KB (291199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e78bce73be399b5f32cb65e0bc936590deb899ee136e761115443ad3660df`  
		Last Modified: Mon, 27 Oct 2025 21:11:33 GMT  
		Size: 87.9 MB (87919319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4af01b92c74e9c181ab2e063fd265becc04271471dce2c8e9af114ecc38204`  
		Last Modified: Mon, 27 Oct 2025 21:11:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:cfa7238a08c3eeb7873c1266c4632efd872af0266dc280622fa9044ebdfe0f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4861f3e4633f6f7fde6d5f1d9ac03fd206eeebefb1066e57f6809f8cc48a4053`

```dockerfile
```

-	Layers:
	-	`sha256:7efd2a805470823f653cd8b9ebe3fe480b39a6cde43fc1cb893501071934da0c`  
		Last Modified: Mon, 27 Oct 2025 23:23:59 GMT  
		Size: 195.6 KB (195632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b27b25bd59e6ab6f600e6f2286204a74a12f649b73c1258544d932b7caa035`  
		Last Modified: Mon, 27 Oct 2025 23:24:00 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5a2e6b4fcbe5f13b5ba47de14fcbfe85f92a9bea9311520c7397bc0f3183095e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91287953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bba30baa9335ed1923c2ad017c6eeb0014182e129ee08d9d55bb629f1b0c7f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64e325008abdca915403e85a7ac4957ec433b29d95e89387c083adf03a49701`  
		Last Modified: Mon, 27 Oct 2025 21:07:48 GMT  
		Size: 294.1 KB (294094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75eb2c973c6fbfd8ad3a7e393b43c7170aa83e9a02eff9c12f176ce891587b5`  
		Last Modified: Mon, 27 Oct 2025 21:07:46 GMT  
		Size: 86.9 MB (86855633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7996aa146467159e2ba5b42425a2780eafd67723058a79c69c5e24b4cfa778c6`  
		Last Modified: Mon, 27 Oct 2025 21:07:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e8401a99470b2bb2dde5b1a043ef3935514b42fb1561aab3674e534cfd923e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 KB (220966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f37b9816abfc83313bd85ff0377f0e9c970feb594a00f05a7feb30c5aec653e`

```dockerfile
```

-	Layers:
	-	`sha256:d0a9a65e2a1e4857acb29ea00fd00e46c460133f325b02dbe279eca3ff32e784`  
		Last Modified: Mon, 27 Oct 2025 23:24:04 GMT  
		Size: 195.7 KB (195668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeaa691b2382062fa43e1d67d6a3716893892abd1c9762b06dae32b7de15398e`  
		Last Modified: Mon, 27 Oct 2025 23:24:04 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:e10db6a18652bc949470b2551c80ed06647e700663ebf8fec3a3c86b509b04c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93656642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c4f573793ad716bc8797d3600f0d84d53a5c4e21db710f4861f875f36ba731`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558a6d044b355c3fdc9f1fac4679f645d2768d85d721529353dc108965bd39d`  
		Last Modified: Mon, 27 Oct 2025 21:09:02 GMT  
		Size: 291.6 KB (291632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306627769a351c52d3a3779e00eff7152c4e91ea12a59e21b051f7345636c1ed`  
		Last Modified: Mon, 27 Oct 2025 21:08:46 GMT  
		Size: 89.7 MB (89745922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2748b7acbe18db75aa89cabe935725f6781529f76cb13977d6298a53c625137`  
		Last Modified: Mon, 27 Oct 2025 21:09:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b15b38221b2f46e7c4d7893d96878fcb341c862a3c033c8afc53b2b939a33f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abed9ee27a427390b33bc1a5ec30b8a559249b2f383b56368aca9ac559c116d`

```dockerfile
```

-	Layers:
	-	`sha256:e88434705ac35bd709e59dd235c4ef1c317ac67c4062a81bee77688572c9481c`  
		Last Modified: Mon, 27 Oct 2025 23:24:08 GMT  
		Size: 195.6 KB (195571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e360cd369447f543566ba92982507aed28562f810d5b0640f73b530f51a7ac`  
		Last Modified: Mon, 27 Oct 2025 23:24:08 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:7b9ed7f5f0a4072ea25985b16e5d7377ae809fef7b658abfdef9178919f27621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92261241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ee5c8a2b379ca5c480384565936a49d973ba191df99a17585681f1b466b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34403a3833161e7317f5f43c031b3114df383a82ea83c5851edc4d5c8b921a`  
		Last Modified: Thu, 09 Oct 2025 04:12:57 GMT  
		Size: 294.6 KB (294579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f672a68eba01ff6a61528f0b4d6424e083bf2d654ca12da312b3edc3a8b90`  
		Last Modified: Mon, 27 Oct 2025 21:08:47 GMT  
		Size: 88.2 MB (88234264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e340feac7725bc768b72bd6e30db2c8afc76890888829277f2017285942433`  
		Last Modified: Mon, 27 Oct 2025 21:16:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:eaf42619a8117d139d9c3af754d19cbef99d11d4a35933bd6d10a87ff55253f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727c4c211f5bea3c18092ab3a94255462e1ae67cc0d3095f86fa9bc1b7d23b49`

```dockerfile
```

-	Layers:
	-	`sha256:38ed660e094d5afeb71f496579e5990ae262f4f8a1cc718d2197f41e646eb79a`  
		Last Modified: Mon, 27 Oct 2025 23:24:12 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6fb79a475c1d8f0856e63e50b74f753f5a54c7b1c90f67ad1d585dde164987`  
		Last Modified: Mon, 27 Oct 2025 23:24:13 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:6df8198b726173668518996ba7de728093557c8240b3c180d8b58d06dd1653de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92476088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc701c996d535d01ae865712c4d4a60fc9c357986b4036296ebea7be2b45134c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 20 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
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
	-	`sha256:3ba33301841d9f0f671dfe6e1858a3107b8e894cdb9a7921f01148f354845cef`  
		Last Modified: Fri, 24 Oct 2025 22:19:23 GMT  
		Size: 88.7 MB (88669180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacee968acd7e58570f6597e878306b4768254f158661396f1b090181aa47651`  
		Last Modified: Fri, 24 Oct 2025 22:19:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9da2e934cba0ee62230d2318935a9159845c8f7f54c1217ad6b9b2028e9ad386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b507ecce409d0a3cc4630223078c2486260dc34b3d20d158c0fbb3c260be12`

```dockerfile
```

-	Layers:
	-	`sha256:098413abd245af098ae198ff914918a3b87dbe9f2857f4d512d006c3a6e1c1d6`  
		Last Modified: Fri, 24 Oct 2025 23:23:26 GMT  
		Size: 193.7 KB (193707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b91082c610947ba78a9c0f9a7dd5c9255a8f7b119076d08977b8f73fd705ccaa`  
		Last Modified: Fri, 24 Oct 2025 23:23:27 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:f357cb98bf52feb08eceb1de23b76e7ff31f07d44d866cb45a3a0add8ff8d3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93756521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f2072767e37c0be7c47b2c040653d58063408701215674a6402e8def4e06c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2de0d30ada31da192f5016a4897bdd65bd1ab1a8a13dcbc1a8bf1e887eba8f`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 292.2 KB (292158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a092d1611329304bb10b51ed24c5eb7129e31e22cce2e99b258f719f86a22d0f`  
		Last Modified: Mon, 27 Oct 2025 21:08:13 GMT  
		Size: 89.8 MB (89814961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029925df7cf63041c688de8677a93d46623f316ffee74193c14561d224d509e1`  
		Last Modified: Mon, 27 Oct 2025 21:14:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7061e151c5e9e61a2c5fe04fe610bc0b1ef30e9bc58f36417d3f5d09283ab802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768db7483b0095e8198481ddc11bdbe818b413bd565b1107ce3709bd0ceee1f3`

```dockerfile
```

-	Layers:
	-	`sha256:d2398254ab742b84db2e9e85ef1d41f447d993c4ffa71fbd41775a3d5e308bf3`  
		Last Modified: Mon, 27 Oct 2025 23:24:16 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420f19071b4eb69da1236951e9646e9252a831c4b59226f14da1bca1319b5c40`  
		Last Modified: Mon, 27 Oct 2025 23:24:17 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
