## `golang:tip-20251102-alpine`

```console
$ docker pull golang@sha256:bfb431ba02a05e251da227f6bc5c27a3684e063630cac74320bf972f1ac726ec
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

### `golang:tip-20251102-alpine` - linux; amd64

```console
$ docker pull golang@sha256:97052836df0a4e9d5845e8f94e30e54e4781b2351aa65707463800e9a752ce75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95720442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2be445158b7cbfd3a14ac6ffa59bb815b8ff7344e33cddf50c79d2477d26842`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:06:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:37 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:37 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e2f79a7b2e9596723fde694a84745ed4eaa97da0ea3e1ba5933c9ef14c47a`  
		Last Modified: Mon, 03 Nov 2025 18:07:59 GMT  
		Size: 291.2 KB (291164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702f95a181291c0837938aaba83ff4f41afa7e8e6da99dfb7bdd907309ced277`  
		Last Modified: Mon, 03 Nov 2025 18:07:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:647ba2bcfe4206ac003bdb07ef10a98c8d4c76adad411f648729b2e1dd542acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f94bbcd7f6cb45cba6eb3f6d677a9c7db68656c2518ae32280d86c79e78c7`

```dockerfile
```

-	Layers:
	-	`sha256:d8489cdce3973b0d2b779b377cf1c6eafc61c4e18cd10b1e44c3a176b2e71d9f`  
		Last Modified: Mon, 03 Nov 2025 21:23:55 GMT  
		Size: 195.6 KB (195612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28bcf21769012de9691a5631aa8b3eb5ff428920353c051da0b8c331dcb466d`  
		Last Modified: Mon, 03 Nov 2025 21:23:56 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8c868579ded67665adc319b150264810f621de26f9ecd1af1b0d0b4a0f3031ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91861166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eb2da5a89b33e5a0be9ee3084cfcd9bfedec757877d5d52ad55f214d4dd1b3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:05:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:35 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:35 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:07:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:07:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a8b493de58517c8d69b75e78ff52b00bffbc9a2feecfde3c1d5192ca304b8e`  
		Last Modified: Mon, 03 Nov 2025 18:07:58 GMT  
		Size: 292.3 KB (292336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518140b1232c759e1bbff002fa828b3b3a5b3d09a55146300b06356a080e134`  
		Last Modified: Mon, 03 Nov 2025 18:08:08 GMT  
		Size: 88.1 MB (88064592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebaf2179be82eaf8c3c625d65bd6e435da428ec035fe436d110d4a6c95a10b5`  
		Last Modified: Mon, 03 Nov 2025 18:07:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f74bdd8688038b8539f491f941f7b212b3556679f67ab8ae7d5bb12808638978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f461838921b0176e65fc427a0779f6d8dc966dff73d31cefc3f3a9e2475f998`

```dockerfile
```

-	Layers:
	-	`sha256:25baec31065cc81c9d3ae246450bd0e2d8eda3305c8b8e5ed902a135eb178302`  
		Last Modified: Mon, 03 Nov 2025 21:23:59 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:78bf9c26def68352996e3f14019fb06da35bae40fe7a5cbe2aaeb03adf62f86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91319600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70e20cd6c96019d66ddb16de57cb073b5387e93e213afb25bdf6e0ed312e2e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:07:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:10:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:10:15 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:10:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:10:15 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:10:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:10:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7dbb2154ec5add08c5b7917a6d946a262308e5b56b37266cb350c472b1ac61`  
		Last Modified: Mon, 03 Nov 2025 18:10:37 GMT  
		Size: 291.2 KB (291208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b1e5d69a9f2d1b07f79370dbb0f50d46789c7a7bb999fb6cfa88ccef68265`  
		Last Modified: Mon, 03 Nov 2025 18:10:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f2f01a0dd18956a981c336a1029015d4eaefa64758916bf08e5813e6cb6b1f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86e053eab3c8b355752930b33259875c25d8f12828c233be97dd8e9cf15c33f`

```dockerfile
```

-	Layers:
	-	`sha256:652aa8f51710183008948dc06482a90ea7d6fe1e3e6c6f44887bdf53dfcc57ce`  
		Last Modified: Mon, 03 Nov 2025 21:24:02 GMT  
		Size: 195.6 KB (195632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acdc343c83356d194cff5e1458e5dd36ae708c53c445c0d143300368eaf83fe`  
		Last Modified: Mon, 03 Nov 2025 21:24:03 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:86c9bef53ca75dcf5db61ed1aad9c6a7f64b1319f05c9ba6fa88360fede00b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91310905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d9d8b5f39b34e91995f792daaceb7bf4af519af65a8e8bbf21cea501cb1b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:54 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:54 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:07:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:07:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02204155711f1d9e6e57c7b879cd9792de1ed7ee9c31150d31c447ee231b309`  
		Last Modified: Mon, 03 Nov 2025 18:08:15 GMT  
		Size: 294.1 KB (294107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619e35e8381c26327bcb6096fec1ca7649cac7a28a7d8b769b87e025a96b5512`  
		Last Modified: Mon, 03 Nov 2025 18:08:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:73ff0206e3d3884121b89cd4040dbd3c1988188cf201ab1d8853a812ea6f86da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906d71aadacf03fcbd5981ebe92db162f094f6fe278f831a63be9602f165ac6`

```dockerfile
```

-	Layers:
	-	`sha256:688cf91febfa0937bf1f3f37fe413cd56042cdc74163606c56bd363ff0bf1edf`  
		Last Modified: Mon, 03 Nov 2025 21:24:07 GMT  
		Size: 195.7 KB (195668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5886b15b66b470cdbe83be67adb748a09b458c18253aedf2c16d0eb8e5d5768`  
		Last Modified: Mon, 03 Nov 2025 21:24:08 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; 386

```console
$ docker pull golang@sha256:b86f4b143b28a746e30869683974dcce47b70f23b21356ab769b4358e0202af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93523743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fb88b1ee32d24f39ee785a9b5b5fa59e905c630742680e451260193635722b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:06:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:09:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:09:09 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:09:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:09:09 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:09:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:09:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c867c802136d98a33cbac425931e3cfa4f0f2f566d838e4013003615a6ecca`  
		Last Modified: Mon, 03 Nov 2025 18:09:31 GMT  
		Size: 291.6 KB (291627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dced42faa7a8ae4fa1460b93ee6fe255b6b0a23d20644774aeb6962173e515`  
		Last Modified: Mon, 03 Nov 2025 18:09:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:259db583a7a8b0b60f62188774f9037b41dc7a7cfd74a784ac96b97a077db733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546790370cadceb999ef55360b47cb678f2bf6b04f5b80487ad13b054d001a6d`

```dockerfile
```

-	Layers:
	-	`sha256:9c132e4839ba7eec51d8a25a3accac92b53e31af9f6e685c6452770a3dd4bde5`  
		Last Modified: Mon, 03 Nov 2025 21:24:11 GMT  
		Size: 195.6 KB (195571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cdef90ea562416102bb365305a69a6b7dbed1abeda2b311f5cf81fc73c162c`  
		Last Modified: Mon, 03 Nov 2025 21:24:13 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:619559d9d05b61b1074e88c7b9818afeab0773432e7559b9f4a6fa717b6bdecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92318849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54e5299bb7dc661508ae18ba12d640099b68c0810883852d616f1743717caa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:17:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:18:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:18:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c8bd62217b855f213063830cb5c2b3ccc4717b8ba91afea33b4f12c5e23dcc`  
		Last Modified: Mon, 03 Nov 2025 18:18:26 GMT  
		Size: 294.6 KB (294587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceec0e4d5de5dea09954f1a27c8249b0a35d8d279f74fc99310146c6bcff3247`  
		Last Modified: Mon, 03 Nov 2025 18:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5e422a00218ad0300e0077ae8a9d02fe4b9d4e9e6e0a2d54423da21788d7666c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d13db5983ff61d337fd1ce5fe9b3a0cd2eb6dd1c98643ed5bb3da9d161e15e8`

```dockerfile
```

-	Layers:
	-	`sha256:8a22fdceca6f60767d9481436523319cd8c85c865d9dfa4a640eedce44284a3d`  
		Last Modified: Mon, 03 Nov 2025 21:24:17 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450e5b1146238443d34f0fb0f1f32b8d6b1136cb01ff856bc1ece19d220d90f7`  
		Last Modified: Mon, 03 Nov 2025 21:24:17 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:8aa91784989093b0769adc0d6ebaedfc552abbc40240199053f39e0b9ca7d166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92603327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8028cbd3d0c27838a7b86746dabbfb030aa63a2dffa25b0e5433a29161c33649`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 21:01:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 19:28:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 19:28:57 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 20:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 20:10:31 GMT
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
	-	`sha256:568766c8d70cce8f34aaf3713ad1c1267acad6ccddf02bbbe3d428a4c87f11f0`  
		Last Modified: Mon, 03 Nov 2025 19:36:15 GMT  
		Size: 88.8 MB (88796418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3236c2890d28de5a1f8962dcb6d7f862419dd8e282b861a7ba427e2dbb8ede7c`  
		Last Modified: Mon, 03 Nov 2025 20:11:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:55dd17edda325de76a9d1ae239ceacbfd94c86ace999bdcca04123c53beced95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49928298dea6620117dc2803bd653f216c12113a58c63ad85177d1885051ec8d`

```dockerfile
```

-	Layers:
	-	`sha256:a5bdf00f40ab6cfb051bf3ae39d1654972fec35e5648d84b02d762055ba97903`  
		Last Modified: Mon, 03 Nov 2025 21:24:21 GMT  
		Size: 193.7 KB (193707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f74ff09450842c19cdb49f8d159bcfd368b22643ad8d81711621f2e4e41d2e6`  
		Last Modified: Mon, 03 Nov 2025 21:24:22 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-alpine` - linux; s390x

```console
$ docker pull golang@sha256:30d590eb687066f3ad8b5cc178b9fb2d8cc416cebe85a0833b4d576a9ce8e194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93777947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d9affe333b124be142042b43da5b7348619b24d4aa89283e7dc9af3b2ebe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:14:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:14:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:14:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce53ff9bf2eef5053eb507e6c4a528322e0535fda9d363fa7b72a5259d021f2b`  
		Last Modified: Mon, 03 Nov 2025 18:14:51 GMT  
		Size: 292.2 KB (292156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c84c0a2b8c3becb9b5fae9dc0218be8d82025dbb521618694049793d9e42c`  
		Last Modified: Mon, 03 Nov 2025 18:14:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:202e3ef9cd89dfc8707e5752ab26ad19a50c3ce714902eb14ee9b34590345fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc6e2e493a89154220c943f8ec55a07ecb73fdca1535d2c8368b79bb34adb10`

```dockerfile
```

-	Layers:
	-	`sha256:6cb359cd76d7270fa66502d3a6819d51bbbacc42fadc323fc0b142c532b2e89f`  
		Last Modified: Mon, 03 Nov 2025 21:24:25 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7156d40b41f6831b029dc47511e8664baaae883af4b8c02370706a3a13b713c`  
		Last Modified: Mon, 03 Nov 2025 21:24:26 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
