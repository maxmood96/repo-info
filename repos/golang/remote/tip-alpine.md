## `golang:tip-alpine`

```console
$ docker pull golang@sha256:a868f3b9ad14ac0b86fc141feeb3e9829e8b4e5e0663f35e983d97aae6588d0a
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
$ docker pull golang@sha256:81890fb0c0400635fb4e8aa3a9de9a4f97d5969b0bb4eef33afe5251df7b21cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129994316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1620616e92f790e11e3e66ecd8ad234eb31f632b4d9eac704a30dc22a6be923f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894232ea060610266e9959d52005206a0c756978c9789a75e362de4cbdcf9da6`  
		Last Modified: Mon, 31 Mar 2025 17:36:40 GMT  
		Size: 294.9 KB (294902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdcf0ac50c31370559153f24cee269e765f93f7d9caa55e2923550ee66d79`  
		Last Modified: Mon, 31 Mar 2025 17:35:08 GMT  
		Size: 126.1 MB (126057009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83915061899d96d1826479c98e4291287ed9148f94b2e1122d92aad5de7518db`  
		Last Modified: Mon, 31 Mar 2025 17:36:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bb0941e5a0c9f707d2a637363d9ffde3e417e585d5dc01924ce505e90696e371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd32635e47e5fcf31a8b77929140b2bdbea75ac6450ee54a4003fdf39eb921c`

```dockerfile
```

-	Layers:
	-	`sha256:af3de090928463d150686673c7c1ce6d1f4c8d04a39d2f9985cbe48bb3d46d45`  
		Last Modified: Mon, 31 Mar 2025 17:36:40 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0940534f728a064b61a2e695819672674dec3fe1f61e5849159b03e19bc36888`  
		Last Modified: Mon, 31 Mar 2025 17:36:40 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:bfefd1da5bb212398c54093ee560bdbd02a52798d56091a44ad2560d4c3366c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124993101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8787813d595ebc3395d7b7ec9f61c11bed988fe2b79a2b3002060d99a81ffa23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:e2f25f8480ec104bb905a90dd4c3c957e03605868c08a66605d9b85e02dc6d17`  
		Last Modified: Mon, 31 Mar 2025 17:34:04 GMT  
		Size: 121.3 MB (121331960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfac4b84c512727b42ac9555be11b13dfff82d37834cbf6349358b4213930fd1`  
		Last Modified: Mon, 31 Mar 2025 17:34:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:94366737459843ca9c60a80b3053d0490cffda08ccecc6e0131117d59e9cf21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac5a367570036cb93751c12237811cd4cf04a1452e836af3853868254f4b0c9`

```dockerfile
```

-	Layers:
	-	`sha256:83feec730fc7177ade283e53c491a4837bc70d667457c07b9695473699d6fefa`  
		Last Modified: Mon, 31 Mar 2025 17:34:00 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:0c6232d561d7ebd21e39f51b855e3587fc75a46978ba20b0cbbea729cab3eab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124383978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baabe4dc939f9e9a5fcc497400d1acf852fca2e9076f2faf4d0386252e193c7b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:5df465922d4d37689f205f8db79322885e1b2a4fcb76bc9411e873e87dc4d228`  
		Last Modified: Mon, 31 Mar 2025 19:49:55 GMT  
		Size: 121.0 MB (120990498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea30c2a93a584670b81ff3a9a841db50560ccd5ed413efb29d55c070e2b6ef14`  
		Last Modified: Mon, 31 Mar 2025 19:56:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3f1a2bcc48e95ff22023394a8ed66b8bf3ece96038e3e92f8db6ca611905a10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e14e5a2b6e2bc46e148df21d3dcd1d617f20e88aee2af0a4fab4608e209c194`

```dockerfile
```

-	Layers:
	-	`sha256:1b934dd55c1d1dbb7699b43162f9d2099bdcd8f8d7be247ce306aa3f2bc357cb`  
		Last Modified: Mon, 31 Mar 2025 19:56:34 GMT  
		Size: 211.7 KB (211707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd4efbe3de52aea9eb369b39b479867c5ad2865fd7173bdd6e63b26e3e8a690`  
		Last Modified: Mon, 31 Mar 2025 19:56:34 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:49ce68ea293cc26274c99e3a7c0ac258707830bc3b647be716c6d09bb1d15508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122895411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116dddb8f2696e0e54fce19a376a27b0998b09d595c2a24924d50d9240a0721`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:15331666df650886c34693df6448a24027e3a0aedd81057f599d0c56087566f5`  
		Last Modified: Mon, 31 Mar 2025 17:54:53 GMT  
		Size: 118.6 MB (118604354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44243d47f02acef0dd5e5f215d38466d9d0be70b4d935ba4cc2d9943eff007cc`  
		Last Modified: Mon, 31 Mar 2025 17:59:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:01b4377af9939328be5af6a16bd7f9829b97123ced85df9096937b6169f09a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338095ca2948d5f30e3836868f73699e4eb0434952e36df6a438abd6d361f148`

```dockerfile
```

-	Layers:
	-	`sha256:dd8a03d81d0d94a43eceb2ef137054d67fe6a391ffc525e49015c7ebdf6f95a9`  
		Last Modified: Mon, 31 Mar 2025 17:59:30 GMT  
		Size: 211.8 KB (211767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b73370c71e65e3da04e07ce301cd353989eb226a9052f418309c8c721ca70400`  
		Last Modified: Mon, 31 Mar 2025 17:59:35 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:233b7b0f2f2d809d854c289624b17575650cee51f474e91c8ac62fc855942ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127906011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4195956c2f60eb4c1aff7164e9de88298fd93d9d447918a2eaa29352c4ff3af4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cbdde9c318882cfe45672dc5dcad0c9e7bf63868ccdce627ef914da7501314`  
		Last Modified: Mon, 31 Mar 2025 17:37:01 GMT  
		Size: 295.6 KB (295593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20357d85d18b3e3e63dc269591697947f7bf020ba7021f1f8a7b1b769a804fe`  
		Last Modified: Mon, 31 Mar 2025 17:36:49 GMT  
		Size: 124.1 MB (124146637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f864c89fc6ee45cd60dd5b46afd673ae613cf1a9256e0e155782bb1a5d9133`  
		Last Modified: Mon, 31 Mar 2025 17:37:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:65fcee543bde04904bb390bed0901170ad8205a5bc7130a7e9df288980222ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693392c8390371212d98f3c3f0b948b0e7a037415bb159ac3d5a1d84701cd36`

```dockerfile
```

-	Layers:
	-	`sha256:bcb9785670a024bd0d8300dfceeb21381308a51721bb12b25908795faac4ed8c`  
		Last Modified: Mon, 31 Mar 2025 17:37:01 GMT  
		Size: 211.6 KB (211646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f5658285cd9f482223b86ea96249b193e5dd677f120fbf6c62aadb091dcebd`  
		Last Modified: Mon, 31 Mar 2025 17:37:01 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:793dfeab7d252f8ebbf4b1f6d55b85b52c20cab2caabe74f45940bbba6463b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124778066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ad41ac96e45ed67b00f1da889fa85f3898960a21de41b1a85f3cf866024c4b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:22730901dc3a920565010f112cf1fbaf34e7ad303fd15179e51589258f9c3f8c`  
		Last Modified: Mon, 31 Mar 2025 19:23:49 GMT  
		Size: 120.9 MB (120905289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfe1f7afe231e36258d7455379e43a2c6d9bf92df5d889aeb908faf5d782b1`  
		Last Modified: Mon, 31 Mar 2025 19:27:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ffe60d872328bca82da1afa3142347bc8fa751c12c95a38f5e968471bcbd43ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae3848aa0b2edd4f2cdce6cddd24f292dd582a19206741266927348f996eedc`

```dockerfile
```

-	Layers:
	-	`sha256:d8b48f14f2e322f763220df62100fc7f67a78bfda0949802738f71a59889d842`  
		Last Modified: Mon, 31 Mar 2025 19:27:14 GMT  
		Size: 209.8 KB (209834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0c3dbe59547754078ec5e601f64b531b796b25e8c636a1da2ccaffe8ff5278`  
		Last Modified: Mon, 31 Mar 2025 19:27:14 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:272b84788965a9c41085bc5bae1c279c9517b0aefafd40510ad69dd706320edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124871188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a71d9ab04bc4b90ec4cdefe821928efe90551ca31f276155527755c8692380`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:b3dbd81f507685434e2982d239e7e190f14c1b29624821d3f5baf22e4f468fad`  
		Last Modified: Mon, 31 Mar 2025 18:55:03 GMT  
		Size: 121.2 MB (121224244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49fc52b0180f4caaaef804b4b357705a8408e606dde073eff2737cf2718df4c`  
		Last Modified: Mon, 31 Mar 2025 18:54:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3c0487a62c8ee11e26dbedb0579d9b828fdb913a977d1963839201c1e9d9d5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a206774bc46531e93fad6ab83486880b9780c6111dd76e854b115222e896b7`

```dockerfile
```

-	Layers:
	-	`sha256:bc25da03eb6bb504028899ba438ffa3456a5055fff5f3373c0dc4ea03b8912c8`  
		Last Modified: Mon, 31 Mar 2025 18:54:46 GMT  
		Size: 209.8 KB (209830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86dcb9ceb45c41fd19e286487df24a7ef1de1787f1aedb97b6f898f11e0bb0f`  
		Last Modified: Mon, 31 Mar 2025 18:54:46 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:78c3a50904c875d27b03485b7c75a26dc49372bbe1d3a338a4ccb9b06d4f2d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127100547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a95274d6fb03eb29716a245615f4bc5c2490b224223508f15a0fd2d9474d61e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:ab9fd359663b603237a3ae91c837b8d5c159e2e6258d720d7dd1b12433408ceb`  
		Last Modified: Mon, 31 Mar 2025 19:12:01 GMT  
		Size: 123.3 MB (123336639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cddb3b8178fd772ff4c1906cd42c8bbd22994cf8d2663f5fa17c05bb5fff9`  
		Last Modified: Mon, 31 Mar 2025 19:15:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9bb4f1ba896ab375a10d9d8d1045faaa96e5dea21a2c2066b23ff6fd6e6871f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d9aed334860585f79ceae0736bf8844c6377d94123ae48f4444c139f31bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:064c81b56be8ba8d99d22b9a2b80cb0b53f99b3693c47f4192ada79b665a7258`  
		Last Modified: Mon, 31 Mar 2025 19:15:02 GMT  
		Size: 209.8 KB (209760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f56a955dbb91b40c14cd3a4757b16a46da7b537d1e6b0d8681b80e087afcf516`  
		Last Modified: Mon, 31 Mar 2025 19:15:02 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json
