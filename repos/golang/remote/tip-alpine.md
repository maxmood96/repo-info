## `golang:tip-alpine`

```console
$ docker pull golang@sha256:fa8ad725ebc82572730de2fbc59a18280f9bcd209f1357009af2b95404a1dcab
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
$ docker pull golang@sha256:9f08be9b0d6bff9137135a153fd7f776a86d8acc4e221f394904903ee5fb614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129994319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f55c790807982b2eb64368fe52611a423cd12ef3f6fb8f2d3122585447a108`
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
	-	`sha256:b32ff0e06d18808f30b299a4230f9a930c7f7fb1c7b45efd94037dc3c796d434`  
		Last Modified: Tue, 01 Apr 2025 17:13:22 GMT  
		Size: 294.9 KB (294905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdcf0ac50c31370559153f24cee269e765f93f7d9caa55e2923550ee66d79`  
		Last Modified: Mon, 31 Mar 2025 17:35:08 GMT  
		Size: 126.1 MB (126057009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e9050593618bd71ec8cefb37f40431c7acc534627bf8d78eef71cc4c111747`  
		Last Modified: Tue, 01 Apr 2025 17:13:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7b0fc7aa16db953c18c3cc24b320a78745f566a47bcbf79d43eac8ba5d863326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569372354dc07a4563deee6010b2b7cf3290190b9483fdefa1d1ed45345fa803`

```dockerfile
```

-	Layers:
	-	`sha256:960824684eda2b17d830d18e60e350fbc3b574c3149c7a949b905f1acc04eed7`  
		Last Modified: Tue, 01 Apr 2025 17:13:22 GMT  
		Size: 211.8 KB (211799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f3a27fb6e66bf4198e455cea20d0e882b38a18b6dc191126b1ed1d9aa5de9c`  
		Last Modified: Tue, 01 Apr 2025 17:13:22 GMT  
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
$ docker pull golang@sha256:65367b914a68a8c22d03117a5e8e6cd015127cd82491c26e36609dbb75f21d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae9060af2be1da76778fb1ec3e8a04954f3195010eff3536b49cf40f7039249`

```dockerfile
```

-	Layers:
	-	`sha256:ce0dd2880086db53320ac70b1707362d8056c049029146fb432b0b1ccaffc939`  
		Last Modified: Tue, 01 Apr 2025 17:12:36 GMT  
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
$ docker pull golang@sha256:87ca016cb68dba020b8572f10bea59c127f57da9741362da347c3cb7f3e3e31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127906014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bd6b2ad8ced5729f17de7c96c59280e9a8d63eca7623a0ba410624a415a08f`
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
	-	`sha256:0c7d3547ba4b686cd954248bd43555c96c0707935b321ab2625bdbf17073d715`  
		Last Modified: Tue, 01 Apr 2025 17:14:03 GMT  
		Size: 295.6 KB (295596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20357d85d18b3e3e63dc269591697947f7bf020ba7021f1f8a7b1b769a804fe`  
		Last Modified: Mon, 31 Mar 2025 17:36:49 GMT  
		Size: 124.1 MB (124146637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716e950b77c72959538c048d803cc014b526a498a7db1e63416c1e7164623619`  
		Last Modified: Tue, 01 Apr 2025 17:14:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:18ac13b0d2bc09f5b6d7f659481421b7695976379776225c09e948f928e531c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 KB (236833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfbbaa3b60d0b8cb236e5d69af176e7816bf2cdd25f33b5cb53e2a2867a5fab`

```dockerfile
```

-	Layers:
	-	`sha256:9546e9252967afe2e9a143519eaca956ef1566a4bdf6e8afb679494a50b3d1bc`  
		Last Modified: Tue, 01 Apr 2025 17:14:04 GMT  
		Size: 211.7 KB (211734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a2c62b1dd886fb997690077c1eaa692095c3c71e084bda739988d50d1b13e7`  
		Last Modified: Tue, 01 Apr 2025 17:14:04 GMT  
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
$ docker pull golang@sha256:f9f0c6422fa96b652c5fb0a3c1835b5d703bb7c834ba75bc7c8e749c753e49f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51609b876e45b65898eae3342473572875798784277ff70b48da15b2caad3878`

```dockerfile
```

-	Layers:
	-	`sha256:6b1adedafd68c57e1619a3197a7c46f27d8f66f736a2af936cef462376ee725a`  
		Last Modified: Tue, 01 Apr 2025 17:20:23 GMT  
		Size: 209.9 KB (209922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503fd3d9a4337cd123b3353174381e177a1f8ca04f8b7d08a171133a66249bd0`  
		Last Modified: Tue, 01 Apr 2025 17:20:23 GMT  
		Size: 25.2 KB (25199 bytes)  
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
$ docker pull golang@sha256:46122a911512e82e6c96b373534a47e4bceb0228472c542b618f6f29ef1bfa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3dcef8a4989955f962f7eaac56a8103143de3e5d30a15f8d321ed1bdc348f3`

```dockerfile
```

-	Layers:
	-	`sha256:fdb35cdc9930fc51f3e5be1add8c4f93361994c34bc7f5152b260d2911f2b85d`  
		Last Modified: Tue, 01 Apr 2025 17:19:05 GMT  
		Size: 209.8 KB (209848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b080c2a366785d20d086178304ced196b24c36ec47d6b837922ae0d702be34de`  
		Last Modified: Tue, 01 Apr 2025 17:19:05 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
