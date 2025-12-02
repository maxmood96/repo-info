## `golang:tip-20251128-alpine`

```console
$ docker pull golang@sha256:f56701a102f9484929e787f56fced7bbe162c1f7980c0a0e65baa0909418e8c5
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

### `golang:tip-20251128-alpine` - linux; amd64

```console
$ docker pull golang@sha256:5c0ed663d7df9c8a44f2e3f672b62e18d38556a2074d2e22295d329d49eedcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98207004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c8d116803a7119ecb851792bd772efad53ae2d20d9c409cc1dd06b6f92d57e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 18:09:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 18:11:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 18:11:48 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 18:11:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:11:48 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 18:11:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 18:11:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab416500544f9ea40122dc1fff269747b8e3a8d007a38a8ebd7eb8587580f9c0`  
		Last Modified: Tue, 02 Dec 2025 18:12:14 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bddb7d3a70ce4416859bc043870fe267e8c2d84ef67b4798e1d7d1c031b815`  
		Last Modified: Tue, 02 Dec 2025 18:12:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:13c80e72e8fd26d4fa276efe2ed9eb2442c6a9c3310ab5450d080046ee4622e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5772d8306a12dc47d8244a68370ddac4611c2dd3b908d7e6bc03edd27465236`

```dockerfile
```

-	Layers:
	-	`sha256:6a67ab278a91956a5e0cdfa65dde2904ad382d47ac4cb83bef1ab5acc56b67ea`  
		Last Modified: Tue, 02 Dec 2025 18:24:25 GMT  
		Size: 195.6 KB (195614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36d03ff01c767a3f8c31a8d89a09871ff27558e4c07df1bec07c933b5725e82`  
		Last Modified: Tue, 02 Dec 2025 18:24:26 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:99fca1706483126d8a635aa9ffaf4f33977d7d824abd650470968fbfa6ab04b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94275005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c8ce658e0ff62935b844a04d1ee99f5adfd6de4bb2f0fd39da6da25fedbdb2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:53:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:56:30 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:30 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:30 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf7fead58209debc1524bf08a1ea6051657698777dc56a31711fe22ca6d91fb`  
		Last Modified: Tue, 02 Dec 2025 17:57:08 GMT  
		Size: 292.3 KB (292310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cef798cb03bb0097c86699403eb8a58ab2cf9b985080b34f19c3c37355503d`  
		Last Modified: Mon, 01 Dec 2025 23:59:35 GMT  
		Size: 90.5 MB (90478457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14500601914ad23f6fe79bd559d6ee5bb1e19969641cb8c5ab08507f61b8dd1e`  
		Last Modified: Tue, 02 Dec 2025 17:57:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c9518129520556017ea70927b7a0a668be5d3144e22ef86e56e99e140fd0cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14192ea6237ab15e7024e1da309bd8a34a86df1a3c76fac58858bddf6d043903`

```dockerfile
```

-	Layers:
	-	`sha256:0a02f3651bc16aab038f11074dcaf607dd41077858fb6f2c6c5fd23a561ecf6b`  
		Last Modified: Tue, 02 Dec 2025 18:14:28 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:dfc6fbe353cd6b8711ba9a61b3e4e29f6d81144969f3ef9236001035a9e2c7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93711274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a156a70a5cacaec56500900176f54af37e9a1089c6b1fb58eee749199293bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:48:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:56:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:11 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c503d8216e3d83c88f2e6fa55a973a50afa1ea035ad31e9d6a22606d88f7ea`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 291.2 KB (291216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf7fc9fa7de36e22f2be3a595e0c244e27314b9b9ac9ccee4fd2d2ad912c5d`  
		Last Modified: Tue, 02 Dec 2025 17:56:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1b52b3e7665fb59b0f6e92b7622d06f14e9c4b7092aa08589ea3e9946eb7a39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ee5585673c82262af7f946eaef123c8c7434269b4fcb190ce93e9b7965b048`

```dockerfile
```

-	Layers:
	-	`sha256:4c070b1601aa0e28af90d48e0a14072dc969fd0cf44627792afae0277969b967`  
		Last Modified: Tue, 02 Dec 2025 18:14:31 GMT  
		Size: 195.6 KB (195634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83178d15640283cebdd9d01d0c263770f70a71cb2d615e30dd14a70ecf0fb885`  
		Last Modified: Tue, 02 Dec 2025 18:14:32 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e08a2b385972059cc346746d30bf1069144bf60c46e3661a7c6bb63ad186b694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93643754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8304355b94c1ab26d37386ad92e1cb5227bc9fd7dc12910f3b6f8a83964a9173`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:53:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:55:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:55:18 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:55:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:55:18 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:55:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:55:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e00a27c8e708706f890d4b379ca37629fcd60c05830622dd099a838dc434db`  
		Last Modified: Tue, 02 Dec 2025 17:55:49 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0f9024daedf6c3c064b979656e63c1f1acd57febe4298c34005175a7b6888f`  
		Last Modified: Tue, 02 Dec 2025 17:55:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:eeb941fdcf4dac488e72c817cc5d358d72d17069897566ad83fe475cd7c81ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b6f269932624a7ebc1bae56d335d01f985e1855e13fa5eca8a60fc3ea1d16b`

```dockerfile
```

-	Layers:
	-	`sha256:c4984bd77aad83ac8da1a8c0bb306fc3820233a1c4eac270041da16e5ed453f0`  
		Last Modified: Tue, 02 Dec 2025 18:14:36 GMT  
		Size: 195.7 KB (195670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47cba4914b1c3c9671dd8e13fff9cae2a774222f33fb841d3e8c32b02adb3fd3`  
		Last Modified: Tue, 02 Dec 2025 18:14:36 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; 386

```console
$ docker pull golang@sha256:23b5b9c3d325ad6b6bb871738a271ccafc7580cfc9043e32e9c9aefad02b215c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95939130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2443b7785f11c40596f96b4e43f021d7b63f5b4d41f2bd057dc7376b50e34f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:56:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:17 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:17 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d26f109d271775642bb52c5ca8e4127de7fe26da9efa068f074533d442cb797`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 291.6 KB (291636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585612384cfda56a02c40d31a01e155dc86b78ddfea575efa77be976c4356502`  
		Last Modified: Tue, 02 Dec 2025 17:56:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:af0cad05c9bcd7f18e45f09066fbfb7a78bb4bf1d5ad34df882868296325a176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109a78456b49b23563df00d42e4d42d4f9f7f7b6f00a86f3b9c9e7395a8d74ec`

```dockerfile
```

-	Layers:
	-	`sha256:3d554ca2fa1ad6bfde231edd5678aabaf91a5b63670cab2870514eab41e29881`  
		Last Modified: Tue, 02 Dec 2025 18:14:40 GMT  
		Size: 195.6 KB (195573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d38706b36a993ec570e4fab6a6f9cf22a437563695c206752814d91dac2b17`  
		Last Modified: Tue, 02 Dec 2025 18:14:41 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:3963ec7a2cc1ef636453c1536afe8d475f88f30d8765a0855a79b5de0b71e8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94768123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5789c206b86a926be6bd672755f4435159f88185b99916475b7c1c61e5d28fcc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 02:50:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:50:37 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 02:56:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 02:56:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ee4242807d5eec61fa095a5c2f00f155044d9c099f2f96b9280a66eec7ef6`  
		Last Modified: Tue, 02 Dec 2025 02:52:27 GMT  
		Size: 90.7 MB (90741131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1afc40953a3f1b3a1cf15b303e23f4baaaf1bfb85e5c11a0c9a6d0b1c64a2b2`  
		Last Modified: Tue, 02 Dec 2025 02:57:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5e1f21e76b4f6056ab3350b517d091f4d090b6b7539b7d28ec4809abe291c133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99264b1f7e1ed1bc6d8c125ac33ddd3455698c771debee3a70bd3c8d86bba78c`

```dockerfile
```

-	Layers:
	-	`sha256:e3ed3abb8cdf391a5d6aae3f28d8a1686c7a183b2d5779d29fe987a9cbe502ec`  
		Last Modified: Tue, 02 Dec 2025 18:14:44 GMT  
		Size: 193.7 KB (193713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a87690369f98f2290af2de743f66fd5bbf6b1dd11c66f12f5d8ed537be129d`  
		Last Modified: Tue, 02 Dec 2025 18:14:44 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:26b9e86757950db8f26479248a9ff1f956ae448b0d1e5b04b47ccd7573a5b826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95186001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f84607262deff6c366c64dc0136b5ba95740535eec7269f5efdcbd714f743`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 14:37:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 14:37:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 14:37:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 14:37:11 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 15:20:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 15:20:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3dee934585ab74409616bca59b39f30d113b18941a71d91f5e16fd83b3d954`  
		Last Modified: Tue, 02 Dec 2025 14:44:57 GMT  
		Size: 91.4 MB (91379080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dd23dc43dafa13d64b101a38c843311541512b1757e83f49bcb3b64768f928`  
		Last Modified: Tue, 02 Dec 2025 15:22:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:aad92cf1d030f293164fae3a72ce27cb0ee61b176c79caadfefbb766e2c703a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 KB (218067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc9b948db5e74da2f3e9092d6a7e1fcc146836052ba9f26abbeaaa8a9fe17ea`

```dockerfile
```

-	Layers:
	-	`sha256:6f181b3511fe00fb132a0b663e8c66f85eea75ac2755adaa73a78082ef644306`  
		Last Modified: Tue, 02 Dec 2025 18:14:48 GMT  
		Size: 193.7 KB (193709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f53daa0b035a7b961494d9b4c13ae017596b460aae3ed96998813220831daa`  
		Last Modified: Tue, 02 Dec 2025 18:14:48 GMT  
		Size: 24.4 KB (24358 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; s390x

```console
$ docker pull golang@sha256:dcf9b97023214dc240f2b75aa2ff2aa7d7ab56c9c9818d22256106edbac68556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97227828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d32ba0e900584e67b3e438224618b0a66a53dd3f4eab9a29d0d1c1c065d223`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:24:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:24:38 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:24:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94177cc1b10be488b5d187dad00f1ccc030bc5cd416e55c943d85498ded2fbfe`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 292.1 KB (292150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d587a6ce9332cd64ade4d6449590e6112812b54bfc350eb8b57100babd31c208`  
		Last Modified: Tue, 02 Dec 2025 00:25:52 GMT  
		Size: 93.3 MB (93286276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08440b358baed72456badec2929b9cfc484572f9545f484bfe295627a36acbb3`  
		Last Modified: Tue, 02 Dec 2025 00:25:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:71e6947e4208905d69fa1e1c1648f9cb51ba8321621070ff86b1283c8ab7bdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998b61123ef0f12d4319c5812a72421280d6babfd5e5ef39bd0a10800d8bb910`

```dockerfile
```

-	Layers:
	-	`sha256:1f5af1f0fff021cfc680c31e0dd2d829084b5d13f3d030f12e4923af7e96130d`  
		Last Modified: Tue, 02 Dec 2025 18:14:51 GMT  
		Size: 193.7 KB (193663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85cd4f8e025dfe860c82a8cc978d9560137dd51a2e2f2b58d77b483b3f26312c`  
		Last Modified: Tue, 02 Dec 2025 18:14:52 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
