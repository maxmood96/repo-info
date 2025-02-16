## `golang:alpine3.21`

```console
$ docker pull golang@sha256:2d40d4fc278dad38be0777d5e2a88a2c6dee51b0b29c97a764fc6c6a11ca893c
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

### `golang:alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:32ece9b4650da07c5e92744894d2fb9e857729466eeb9e38c99f7ddec83803ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82742776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8e4dc60ac807159f7d92b7f9f36b36e8f1b9ffe80fe8ad5321f7ed997c06c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c153488beade6babe34cb14b1432e9eca39ed9bf4ef46b731cc0a10913316035`  
		Last Modified: Fri, 14 Feb 2025 21:01:58 GMT  
		Size: 294.9 KB (294886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a60326dddc23e8774b39171d6496c16678bd44e52909e9a94763d62f3cbf89`  
		Last Modified: Wed, 12 Feb 2025 10:29:37 GMT  
		Size: 78.8 MB (78805485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195c646559109bee91f2dc5bb1eee64f85e926c5223dc95ccf20668f05bf7f14`  
		Last Modified: Fri, 14 Feb 2025 21:01:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:691a841010138b9b902d628a4cc261f24460d6088d8219309d6101369f16f55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 KB (245853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6264ec5341643f0edbf0c081e280d267d6fb9456264b75d6f985bd79b8f4be6`

```dockerfile
```

-	Layers:
	-	`sha256:9309e0b4d0574c05558747b519e9419d5aea92c6d797dcca8a9c2ea885d87b06`  
		Last Modified: Fri, 14 Feb 2025 21:22:24 GMT  
		Size: 219.8 KB (219784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b39c5bcfad330e6627f392edf6a2461cf8f8f8a97124f77790004bdecf26e03`  
		Last Modified: Fri, 14 Feb 2025 21:22:24 GMT  
		Size: 26.1 KB (26069 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:80444272c7f7e37193d2eade8083e47d42db7308a7a6a4e352bb4be4c4e52124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80629753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064e02f5cada2d3e6ada8628459ce242394912ccc523475586e32694887486b8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfbc5ed5374505d1f87434271b64decfa3768ba4e2d1e2b2ea97c9bc2282605`  
		Last Modified: Wed, 12 Feb 2025 18:46:34 GMT  
		Size: 77.0 MB (76968613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f64237f003b7523365bc31c4cdd5e7f6a0a7ae3aecadb77ea7aadd32e6651c`  
		Last Modified: Sat, 15 Feb 2025 00:22:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:92a2d87c21296779e106fcc626b05e8e8f1b6b17e9868f1a64e59a7cc84772b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5692b2811cbee84232023f3e0020d19e208d5a8be5fc35a6d5f6e63d2360acf`

```dockerfile
```

-	Layers:
	-	`sha256:607f2a5c2f05674d56ded3467267fb35095540e580eb5f72005e14a74ad0234f`  
		Last Modified: Sat, 15 Feb 2025 00:22:33 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:edfb9b5553854417d3d60e28d0e7392224d1437a99f0e9925b49f9dc81193f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80361929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e0c6cf2653dc4624e55878ee1e1e273b6e3814e457ee3c4758995417fa1bec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff7ce8adbb73c193102166498a2962195641bfa6bbc14e5dfa44f02e4d7d0f`  
		Last Modified: Wed, 12 Feb 2025 19:33:49 GMT  
		Size: 77.0 MB (76968450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301b31cee9f485f6c65cee405f319ec9cf6fbddaa252ae570b98a54eb4065b0a`  
		Last Modified: Sat, 15 Feb 2025 00:31:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0f98d3384d592e3b424dcda1599e380080692be895111cdb5fbe890a2a93829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (246018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88368dc2f053e06da0d8116b31fc0222ebe9882bf909b36a36be61fe2b1ff925`

```dockerfile
```

-	Layers:
	-	`sha256:5aa9f812b8eea357837b2c76d2b2470f8fb0fb973949ec811ce6bd99cb333f8a`  
		Last Modified: Sat, 15 Feb 2025 00:22:34 GMT  
		Size: 219.8 KB (219816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f633b4f4455acae3394fe952f6bf547d1c4e4cf7f3e4861733f681b771b346`  
		Last Modified: Sat, 15 Feb 2025 00:22:34 GMT  
		Size: 26.2 KB (26202 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9f4cd29d2351d0cb0c674f83e19fd9a06d2ee4ad053a6c12df48607a4e7eb911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79351251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f5bd625c1b89e695817c6a5b207a24563c30dcaa6b4c183c5fce51245ffe0d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa1d43e92f86dc074668d0ee29a76fd40e91e4c4142a8f0580170417c1a1e6`  
		Last Modified: Sat, 15 Feb 2025 00:23:39 GMT  
		Size: 297.8 KB (297842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18364ce0d2587c74fc30d8602f743c52178d9e6408c64d9091baffbff467af7`  
		Last Modified: Wed, 12 Feb 2025 09:53:52 GMT  
		Size: 75.1 MB (75060222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d476c939a0568149dd1f92e1efdc4f4c562a475772453124720a8e1fcb9f660`  
		Last Modified: Sat, 15 Feb 2025 00:24:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:be267f24964249f8509808f628fc3756856bdf06371c382a28c3fd5cba7e2f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 KB (246140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576ae7b2afa470c8a131f52ac6e7269691bdb2632fea53ad9aaa9bb22398af64`

```dockerfile
```

-	Layers:
	-	`sha256:6b9d4c54c500378a82d3d3666a7018d8ca1addd4ed77b39397115279f643f4e4`  
		Last Modified: Sat, 15 Feb 2025 00:22:36 GMT  
		Size: 219.9 KB (219888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:693fe451130035d916c84cc8b7467a99e3015e44436fee5e4885019318063c29`  
		Last Modified: Sat, 15 Feb 2025 00:22:36 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:a88aef3ac8a2c2fd547f65eba6e8220aace8eabba5d93c00c9f76bdfba578c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80489457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261d6342f47c871cce11544fb658e1393ac00ca03f5b4937f781eb681b30fdc3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed412e2cf7bfa23dba6be7c4a29c1dc4abc8343818dfc63524e83dbea008a00d`  
		Last Modified: Fri, 14 Feb 2025 21:31:53 GMT  
		Size: 295.6 KB (295598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366fc1b7517b38e35749547747afd275840849b03e59ce7bdb829acdcf634998`  
		Last Modified: Wed, 12 Feb 2025 20:00:58 GMT  
		Size: 76.7 MB (76730079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4aa629c8436a4dbff7a7c9eb93afacca252b85727274f6e0db12e2309d1240`  
		Last Modified: Fri, 14 Feb 2025 21:31:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1dd13f22f201f83669043a552b6f73813350b9359a627c67e851fd63fa62898f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 KB (245717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf79fa85e0c55e5692ddc6da9f25169c528ab552ab79bd03a4813e08ca3c560f`

```dockerfile
```

-	Layers:
	-	`sha256:2906e681776af55ca2dbd80c857b1dbfa09fff5b939b7aaca192de6ed3d85b73`  
		Last Modified: Fri, 14 Feb 2025 21:22:28 GMT  
		Size: 219.7 KB (219703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d384ce21ff7be34a6633754589c67100b2b31ac551af6ae0ec200a88b65d6fb`  
		Last Modified: Fri, 14 Feb 2025 21:22:28 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:11487e26fecf2e2c1fbb2c63f452ae772f29ae8b7478bd18a4e06054c8ddee19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79243876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346819d3f607994961f49613d584add6b3971701817eecfd157a06e6d449c481`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542036b0f90df8875e93add192346f3bcc8edd586aa34c11a6af80938cb06173`  
		Last Modified: Sat, 15 Feb 2025 00:31:41 GMT  
		Size: 298.3 KB (298267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b7c4c3ab33b16dd1aa80a96c66161c50757bc73ad50fd5e3235ed3f8700038`  
		Last Modified: Wed, 12 Feb 2025 19:33:55 GMT  
		Size: 75.4 MB (75371105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536e0ea57783e69f07d237c673f135e13e76dc59e8fb59bcfff21523ca85e973`  
		Last Modified: Sat, 15 Feb 2025 00:31:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6b2857d8deea715cf075d047ffd59dd3c3c7e2b20c21dcbcd4056b0627d15edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 KB (244069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa99f1e5e3fbcffbb6a56126e5269ca2e7b25ba0e37df5869fc3592f193d08f`

```dockerfile
```

-	Layers:
	-	`sha256:918ed2e1d99a420d2776099c356109b400da339ffd9b11cededca0ddaa187ec2`  
		Last Modified: Sat, 15 Feb 2025 00:22:39 GMT  
		Size: 217.9 KB (217927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a37c6d9ee29e11265d46d12afefff72efd2207f3bd5455d9b556c48741ca7bdb`  
		Last Modified: Sat, 15 Feb 2025 00:22:40 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:e97abe9220963470157acde5b6a59a18fcb98127b25d993455bb9173d9b303f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79791722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7bd7e7efa8acb00126defda3b2121e2c9358d70893aee6e64c0c4fb0938b0a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffa708fdc17b8cf349d7f1289d946270c4966bf9c0a48f32861d451e8e049cc`  
		Last Modified: Wed, 12 Feb 2025 19:32:37 GMT  
		Size: 76.1 MB (76144779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279924519f597eba704f586e0e4d2061c381a64ac752cc3e107fb73506c6dd5b`  
		Last Modified: Sun, 16 Feb 2025 09:31:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ae9fc2582ae5d2dde4fa4410ff71595363dc03164bfff7b6644af5277cf6b259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 KB (244065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e5247a2d1b923f5d36cb67e8eae3dde0753d38edef1b3e3280147ce5ae5563`

```dockerfile
```

-	Layers:
	-	`sha256:4cc73afc8b4ee7c9ff5c50bd8cafadc3a85370db0d7041569a0ac8e4f90e5fb9`  
		Last Modified: Sun, 16 Feb 2025 09:22:26 GMT  
		Size: 217.9 KB (217923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dfabe40b80e091d1cb5feb1366dc275f2d9d764a8772edf999c1cbb22f11ec3`  
		Last Modified: Sun, 16 Feb 2025 09:22:27 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:5e9609a75f129fd63e9659f8302042b161851949c0170b10451516084ac285c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81382801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf19a4ecdabd05cc380d03425620729d73191e005ea5703670ec94bbfb4594c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 11 Feb 2025 19:31:16 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45367ec7901486a744e83b8e8c40908894d960175ae2dea51903497a09542717`  
		Last Modified: Sat, 15 Feb 2025 00:31:43 GMT  
		Size: 296.2 KB (296178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5930b6893bd720b83184453384f2d98bb6ef640665d0b46f232b2c1eed78c3e4`  
		Last Modified: Wed, 12 Feb 2025 19:26:33 GMT  
		Size: 77.6 MB (77618898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c93453d26398372a5addc7873dfb134d4973d16e1d540d8e4bfa2f1a028990a`  
		Last Modified: Sat, 15 Feb 2025 00:31:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c4175569f7770559c993542a6b4c85ee7c956502c546dc58e4831f7b97db411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 KB (243903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe695882d6f61478ea68e1c51d8bb8e6e3ff3812f788ae3f18b7febe4c63034`

```dockerfile
```

-	Layers:
	-	`sha256:27410bd9156e1de45f4f90dc0135274923957be0ef6f9be634b6b414346d1902`  
		Last Modified: Sat, 15 Feb 2025 00:22:42 GMT  
		Size: 217.8 KB (217833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6a32cfc4a9f42dc79dc2799f0247be36b96c41d11584b464228d0315d2d9ff`  
		Last Modified: Sat, 15 Feb 2025 00:22:43 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
