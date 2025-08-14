## `golang:1-alpine3.22`

```console
$ docker pull golang@sha256:244baa35bcfaf9a5b3444519df6d42554a1f92dc33820bd98f0662df270d8a6a
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

### `golang:1-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:68fc16b7551a4cf71251f343a47ff766ec4fa7c02fbdeb4c5ed2a14c2c23ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64128130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20132bb448d9b0a8ecbe754579b8fb657d8d471368d0e94f2455741f775ca5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9168a8d358bf9c23869fdb0be8e1271e50047e54d79c3728ac1a8666a40b1141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 KB (219019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085d79e7e001e9aec70bbc1a4f0a52fed73ea60b9bf770f3a4de7ea72fb5d3a`

```dockerfile
```

-	Layers:
	-	`sha256:186a136a1806a499518c3feff01c5dc9eaad98c0404b6cebaae14a7e492007be`  
		Last Modified: Wed, 13 Aug 2025 20:22:45 GMT  
		Size: 192.9 KB (192949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45dd80db29d718e3efa1d356b97dc5994955bd844f2ba0edf20cd3805da46dc0`  
		Last Modified: Wed, 13 Aug 2025 20:22:46 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:b60549a6346077ef98a5ddb3c3e3839319798ff7a9f72a7b4704f80dabc5df13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62761231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035d7f90816323c84722454166d904d031aeeb763d1d26a8d403774dc26b24b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e2d0a9099afb33db14727fe8c4a421f7167e579b03d506144987f21f96694c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145ea74a8e79b47b76153f71d743ff9e906d00ec1596ddb9f3772614c8fd332`

```dockerfile
```

-	Layers:
	-	`sha256:9d8e0b4fb2c1b716e5fefd10916cd218cdf7660cccb0c1b389cea696d64ec6b8`  
		Last Modified: Wed, 13 Aug 2025 20:22:50 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:46d6ba16f6c8f1a4eebb20a87cc8f1e2a8383efaea2eafa2b9d4fdbf9aa594eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62478594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54da9831f15836e1651b5c214ceab484f061f9211a347e24f539bfdd4de1c571`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0e64e4c8cff7c8d337a4e29811e760b0326e89b217e082c49a46e973fb807450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 KB (219206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12919b97486602ce5a58a1f4a1e550b1b87fd70a8e0f907b9d3d367b6a535e2`

```dockerfile
```

-	Layers:
	-	`sha256:d7380cf814b20670d9af395385ce6f955920028b435d002a940f47870101c7b7`  
		Last Modified: Thu, 14 Aug 2025 05:22:31 GMT  
		Size: 193.0 KB (193003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a1e059fb173a855f097bea135c1b3bf2be4616f256e22971a3b6e74a192ac8`  
		Last Modified: Thu, 14 Aug 2025 05:22:32 GMT  
		Size: 26.2 KB (26203 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a8d0fd810f0074ba0d7b1245501e9b1fb017922504c8e5ede3334fb876688029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61971192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea50bc9f564d64a9ab6b2607175693719455aa7c729c73a4f31393250c26a76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:23ac621d30934737c8f3a1ca03e42835eb31d34559b0d66c09c4331d467ea1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2bf2246acb050fde288efefdeb59cd7ccba7c515de74885883b25a1398e101`

```dockerfile
```

-	Layers:
	-	`sha256:eef09eccb7dba7818186ce4c83aff3af9c885f9158b09d8622fc023264c02c70`  
		Last Modified: Wed, 13 Aug 2025 23:22:40 GMT  
		Size: 193.1 KB (193053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b32e29aa95553b2cc2653e68c8a8c8ec3972561ee5393949e9aa1b727883fd`  
		Last Modified: Wed, 13 Aug 2025 23:22:41 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:5dffbd69b37b8e9fc35d94817e94bc7bf4fd047147e3c5353d357bd3492992bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62661186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a935350bce2c99e529ac2e734f7414e2e1e45cf5c769e97ac0e5f4540298ee8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ec508b759fa4860a008e7405fdfcd668657172db3932b410b5494cdefe2c7`  
		Last Modified: Wed, 13 Aug 2025 18:04:40 GMT  
		Size: 282.9 KB (282925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c63a4b9dc1f72141c9a2ae757dabf818be084da59430ae2f1f1200a26ac66c`  
		Last Modified: Wed, 13 Aug 2025 18:08:47 GMT  
		Size: 58.8 MB (58763097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ae8d33fef4c943b8b5ff9ac6c4cfc4d2d2af52460b575426e184376823b82d`  
		Last Modified: Wed, 13 Aug 2025 18:04:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:836c17e50f70ae6b703624d633bbb20a86fe456d2913c498d0d3c3de780e6a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1325456830a2c39289ff35fa3506858dd4f49f703c294b9e5d97fcd0e582267`

```dockerfile
```

-	Layers:
	-	`sha256:d8bc6a9d794efd323e3be7e6538db5b51236df8e0f2d449332cc0849942b8422`  
		Last Modified: Wed, 13 Aug 2025 20:22:59 GMT  
		Size: 192.9 KB (192890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b2e9b310f2a2233b2539177023b55bdbc7caacd58329a8a30479152e6e8bc6`  
		Last Modified: Wed, 13 Aug 2025 20:23:00 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:ffbca091258e5353bfdde5ff5d0aafe7de6018e520d46e8ad95cd3c89125cfc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62047482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acb110a69c8282096005b80c19cc9f9bb40ed1ead59d96d1aa456421af742ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:52f774277c15e91f23da40a47a6d12c26b58e931f0c7a78446ae609639068cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1339783e3488eb83df9b21a73c7115ac835d091c9681618d0acc23f58f46f606`

```dockerfile
```

-	Layers:
	-	`sha256:49bf97d307b5ac751050f0d39d332b4072081ad20a82d4a2bcf0712260a5931d`  
		Last Modified: Wed, 13 Aug 2025 23:22:47 GMT  
		Size: 191.1 KB (191070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d811647e066ea2a917257b39ec91a809526d7f33a2c436b391043ab4230477a3`  
		Last Modified: Wed, 13 Aug 2025 23:22:47 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:c9bbc8fd7a472ba0aef33e686fd81dfad11873726df375b22ae63c5f9a490155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80125276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1315703bab08aede085768301b45edf2fcc95888969608c5ae0a5422e29a65`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Aug 2025 19:37:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Aug 2025 19:37:08 GMT
ENV GOLANG_VERSION=1.24.6
# Wed, 06 Aug 2025 19:37:08 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Aug 2025 19:37:08 GMT
ENV GOPATH=/go
# Wed, 06 Aug 2025 19:37:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 19:37:08 GMT
COPY /target/ / # buildkit
# Wed, 06 Aug 2025 19:37:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Aug 2025 19:37:08 GMT
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
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86162f2242a5c468f422dd32feaa1e42dc715729f0e4964938f9980b50fb72c`  
		Last Modified: Wed, 06 Aug 2025 20:35:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:636361335b35d1e54accbb5cc1a7b63f2c8022e42e39aaa57463cd1028d835e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 KB (233505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025f016a7838699dc19770c5497a9a27bd8e90f98fc2a044a2c156db9bf3a8da`

```dockerfile
```

-	Layers:
	-	`sha256:ce96c8724b10f13133c38455740754ca764d8b34b9d1169230f37bd77d86a0ee`  
		Last Modified: Wed, 06 Aug 2025 21:48:46 GMT  
		Size: 207.4 KB (207364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9e7efc9108b3e661d1200f48fdb5a9aa71e3004f4ec508d546f02b0ac17b5a`  
		Last Modified: Wed, 06 Aug 2025 21:48:47 GMT  
		Size: 26.1 KB (26141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; s390x

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

### `golang:1-alpine3.22` - unknown; unknown

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
