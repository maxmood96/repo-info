## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:d25555723265ba450d22e783aadf73b2ccedcd8720669e26d5e31efe59fb75e8
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
$ docker pull golang@sha256:e01986bb47f5e2fc9a156759463a64956673e581038d7a175049c26a65abc2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98096711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cffd3c668a53ee94925bc32afb56771ccba7a547ef5aa1cbc3e8aee2bcdd41`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 22:02:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 22:01:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:01:32 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:01:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:01:32 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:04:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:04:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42125aca78ea9f37cc6092fe2bd626aac109969357536381c6297959b6cccf18`  
		Last Modified: Tue, 07 Apr 2026 22:04:42 GMT  
		Size: 291.3 KB (291265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8966583daebf02f7188b966cc8cfaaff27cf5fc1ff9b30af37d939f77e22335f`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 94.0 MB (94000413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc07da7faa004260e0267797f21a106eb538f1eaa2d0a341f5d27c0c3a4f2ed`  
		Last Modified: Tue, 07 Apr 2026 22:04:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:fbdc10e64d6f70c15da874e636e4ea7cbf47b145b6c5c8648405ed8b3fcd5d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ef976256ebba95ccb0e08f904dfe098524abae184f55dd1a96131e82764e1a`

```dockerfile
```

-	Layers:
	-	`sha256:dd093fb616026ce3aa1ee63e1d9ba198247e1b7c9a4a5a95232d63c215c2ac9e`  
		Last Modified: Tue, 07 Apr 2026 22:04:42 GMT  
		Size: 195.0 KB (194984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0439ec43265a792b038367ff9a83fa064e608b5c097a24691b19c19ac5adacad`  
		Last Modified: Tue, 07 Apr 2026 22:04:42 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:a4bf5b18c572f87cd8888156ffe011081e09ba5f6b7cce642c0318329e335471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94213705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f325b4b6d741f92275d63ec5c975fa65a7e4ce6dd658170d1b17c870f0fabd4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:58:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 22:01:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:01:32 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:01:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:01:32 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:01:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:01:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb1d662fef31d487b74e63a4890f32f9a8bd0a1c83c62427a4268ede49df3f`  
		Last Modified: Tue, 07 Apr 2026 22:01:48 GMT  
		Size: 292.3 KB (292308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393680f702bf36f995f3d05ba855c679536e58106a81ae55184686e8496850ed`  
		Last Modified: Mon, 06 Apr 2026 18:41:39 GMT  
		Size: 90.4 MB (90416194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b954fd239aebd6d163b2049c7478b317d756d88f8e41995d58c822d61fe0537a`  
		Last Modified: Tue, 07 Apr 2026 22:01:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:90edaef84f06f8225c6efb977ee65c08fc69790e76e97265eefba4b70a0e3bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1925cbdd58a872838bf6772ed5145e64d0b05ce75ac21a125c18b982fee236bc`

```dockerfile
```

-	Layers:
	-	`sha256:cb09c3bb8ebf330964503e31ac09c1d1b4589fe0d84e445b2f0ca899eb3dbfc0`  
		Last Modified: Tue, 07 Apr 2026 22:01:48 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:b9a153a2c83f498adb9ca6b2083625f90b2608b6d5586017f2302abfa3648d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93651701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d3b2b985fa02393d0057cf2f66e2acddb6d783094ab419c6934cfe30bc026`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 22:00:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 22:03:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:03:46 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:03:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:03:46 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:03:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:03:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b56ee23b89b73c693ec68db581b9e500e4a4d2129fc75701a1e43c2f01dd8e`  
		Last Modified: Tue, 07 Apr 2026 22:04:04 GMT  
		Size: 291.2 KB (291206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866705b29d2f18b79748f9fadfbe79c21fa37d231a94fa79b6aae3edf75ac398`  
		Last Modified: Mon, 06 Apr 2026 18:42:37 GMT  
		Size: 90.1 MB (90136708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5bae92df6cbe09d662cb2ec94c44c07b554646564d38930e20c97459441689`  
		Last Modified: Tue, 07 Apr 2026 22:04:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:1fd007e95625f24036b4b71c7933b1cd4ec3a452f5aa54847423cbca4b6d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a9afbe5ae2251e8fe156a4535951b87d71a67807462c8c8ba6340e88a22017`

```dockerfile
```

-	Layers:
	-	`sha256:c425998ab036fce235039a7e318b0d211733c34d487dad1f58c7ebd2f8fb8303`  
		Last Modified: Tue, 07 Apr 2026 22:04:04 GMT  
		Size: 195.0 KB (194988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f239cbe3576aeef39c35fa68823fd8f356af0e3656eb8688f4237b736dc568`  
		Last Modified: Tue, 07 Apr 2026 22:04:04 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2e463442089a74974397ec455f80adbdb038ef90c10910e1ee3a853fea614f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93518737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d5d8d6ffb1ce3e656ab39f23c23b4adfd76b647acf565fbc2b6b6d72850674`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 22:05:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:59:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:59:45 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:59:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:59:45 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:06:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:06:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29a17622c4066b010cd43bb047f34e820261015ce63f3f4354aade162e84d`  
		Last Modified: Tue, 07 Apr 2026 22:07:06 GMT  
		Size: 294.1 KB (294106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffa2ba5933aea1f1c364c6a791a91c9e49057e35639f30985503d0547a7466`  
		Last Modified: Mon, 06 Apr 2026 18:41:04 GMT  
		Size: 89.1 MB (89084955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170fea2434a0b1e7f33cedb18e1a77fc6075e61a4408a61449da94420e06ef78`  
		Last Modified: Tue, 07 Apr 2026 22:07:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e6abf75be8b31b998cbf091657436973fbf2837d072c8b6d8976ae26152b9a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61450726964cfd9d4e7e5c29f50c11ab1d6f1b4b2ef9d7e0ce2f28f431b1cb83`

```dockerfile
```

-	Layers:
	-	`sha256:0b8b00f758105cb9dcc3101feb9358ddc74eb841fa688acdfa29441aa36c91ad`  
		Last Modified: Tue, 07 Apr 2026 22:07:06 GMT  
		Size: 195.0 KB (195016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9079d222dd6df9024c25b40c54f77b320321da27190e8e2d7633e3d4b6db6b87`  
		Last Modified: Tue, 07 Apr 2026 22:07:06 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:3ee87e4d804b733cb8cbbe81a6a266108a12c96139bb9cc0229c33f8448a6949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95754281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe901cff071d479f4ac4acb25e0814ad7867afee4b3fb3d046628898d507e2b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 22:01:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 22:01:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:01:08 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:01:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:01:08 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:03:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:03:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6947c08e1a72686f30cd3c26243b5e9bc89e02081e83231491006d3513a13b4`  
		Last Modified: Tue, 07 Apr 2026 22:03:55 GMT  
		Size: 291.6 KB (291623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b82e2680f4d14426f015346712b6e5f30c486655039ad7e1ec71d21151434`  
		Last Modified: Mon, 06 Apr 2026 18:41:48 GMT  
		Size: 91.8 MB (91841768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1de4e6408614d0487318d9f188eefe99aa2baf32e906b401c528545554f1f1`  
		Last Modified: Tue, 07 Apr 2026 22:03:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:594078dcff64a1be9bf75abe0a49e3346f03aad5109360ca7ba23f81139b2603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d964e49bbb48ce1dde303c321610ee4c29a4bef52b99cf6cd58b74d0cee66527`

```dockerfile
```

-	Layers:
	-	`sha256:1d80df6da11b87ba7b92611240f008e395b8101a813f7905597644e5ae39e360`  
		Last Modified: Tue, 07 Apr 2026 22:03:55 GMT  
		Size: 195.0 KB (194953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e6905918b3230f7c33a1c6736896b1052f6148710b4440807431e7158a8fb5`  
		Last Modified: Tue, 07 Apr 2026 22:03:55 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:241eec8eb654d46e429809e5a15f51c4d0d09f50f151e106cb991f5168c38957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94831827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404471c8a24c845668240c9a3430d2ec12fe351908b115d90a7426207c67b205`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:28:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Apr 2026 02:35:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Apr 2026 02:35:44 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2026 02:35:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 02:35:44 GMT
COPY /target/ / # buildkit
# Wed, 08 Apr 2026 02:40:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Apr 2026 02:40:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e1ebafd39830591510ded21f3f10c22801e3e344d366979450ab6f748be747`  
		Last Modified: Tue, 07 Apr 2026 21:29:10 GMT  
		Size: 294.6 KB (294576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc368d4f4523089f91977c543e8d1f1e4d28e3b0d524ab4ee1d1ce21debe4d`  
		Last Modified: Mon, 06 Apr 2026 18:58:20 GMT  
		Size: 90.8 MB (90802796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ac0134efeddc2d9741ed2e1ac02b7cf19fc7b72a4a1e3adf67eb229b4a30a8`  
		Last Modified: Wed, 08 Apr 2026 02:40:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:43e207ba0327c5cdcfa63c1a8f59957ac18a5ad9b7253751dc6834c91a82316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eefdb0b72b3d171004b39d90f63a90e14b13de695c64ae1c3262d79ccc2e53`

```dockerfile
```

-	Layers:
	-	`sha256:2f1447013370ebcb8f74b4924d7f00abd986eda320a67199119d8838dbcfceca`  
		Last Modified: Wed, 08 Apr 2026 02:40:40 GMT  
		Size: 193.1 KB (193071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166a960a5a907c9c2ec5e4d621ca865cdf35ca6f6eea89813d7d22f197979d29`  
		Last Modified: Wed, 08 Apr 2026 02:40:40 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:c955abdb6e76cb8fddba272c204f50209c338a139527142b529171de2e48cd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94978187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a909ba6f3875fa167aec26a4f3ebf070408bd3031cabbb18c58570aae6520848`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 09:33:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 00:07:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 00:07:49 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 00:07:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 00:07:49 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 01:34:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 01:34:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffd6ced4c894ab06d11bb63b601a98fc1d0536c2ff8bedffe653c521058ea`  
		Last Modified: Tue, 24 Mar 2026 09:34:58 GMT  
		Size: 291.5 KB (291515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54965d042f5518ecbbacb568db6d4c79f2db392d6bb595ff62396d66c4a52e68`  
		Last Modified: Tue, 07 Apr 2026 00:14:41 GMT  
		Size: 91.2 MB (91169092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afab4a7a7c3a6581c8131dae4bd5edeac041294eda66d1f29c5fdc471b6360a`  
		Last Modified: Tue, 07 Apr 2026 01:35:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:42378a4874167b34827c59acb392215c7423830fe2bb8ffa5229aadd2982c173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea321dc07109c2cb670ef43f5a1bb278e2c6882a7f3b19e61299e543715c108e`

```dockerfile
```

-	Layers:
	-	`sha256:2fe17c057c79c0d4a23cb2c695cd758503ca42448c6866257f025608a29479e4`  
		Last Modified: Tue, 07 Apr 2026 01:35:50 GMT  
		Size: 193.1 KB (193067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6da8b370c5748495e5e7d66d8112345e5b45703d5c5f3fb50e8107e8248803`  
		Last Modified: Tue, 07 Apr 2026 01:35:50 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:8241b5747e7876ede628fbecb70e9d88b6a28c6882b047c0d057f2bfc8744d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97125609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8bce46d9ab388fb6304a85fc9ea9f75996316edbf3b66617d392e316fadb06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 22:02:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:02:54 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:02:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:02:54 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:03:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:03:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1809a5164db0e7b2de9fa4d6919edf47a69e899062c24486fd5d318f2bbcbb3`  
		Last Modified: Tue, 07 Apr 2026 21:15:30 GMT  
		Size: 292.1 KB (292149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7bb14b36d862c74817ebfb57b26695332f89670a6fc97f1c869402d1de33e`  
		Last Modified: Mon, 06 Apr 2026 20:04:12 GMT  
		Size: 93.2 MB (93182867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64d1b431ba8524d2fa6b7b9687153dba52b222e126585cd8ba1233f9abeb910`  
		Last Modified: Tue, 07 Apr 2026 22:03:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6f53005b3fc3d3c27df0ba866c0e4a937bc5202717c0a74ba773fe7a33c84841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d425b44d53e05a447b63e96101d5d0a7726e653665c00f7f1e707be19e22f2`

```dockerfile
```

-	Layers:
	-	`sha256:0b7777e060887880c7d6f8afa1e7bb4d5054ae8d714760756d0f468b4b2c5971`  
		Last Modified: Tue, 07 Apr 2026 22:03:43 GMT  
		Size: 193.0 KB (193033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3531059e9f7f0c3974f41a47f6ad87bd28945b1682a5b8ceb13c77c45ed99c2`  
		Last Modified: Tue, 07 Apr 2026 22:03:43 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
